---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-format-specifications.html"
breadcrumb-title: ''
description: Obtenga información sobre las especificaciones de formato de rutas y la estructura de datos que utilizan los nodos de rutas y splines.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Format Specifications
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Especificaciones de formato de trazados
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---


# Especificaciones de formato de trazados

Esta página describe el formato de trazados y proporciona instrucciones para manipular los datos en ese formato mediante las funciones incluidas en las herramientas de trazados.

## Especificaciones de formato

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

En esta sección se explica cómo se codifica un documento <b>Paths</b> (o imagen):

Un documento de trazados es una lista de trazados, cada uno de los cuales describe una lista de segmentos codificados en una textura de color de punto flotante de <b>32 bits</b>.

La textura se divide en partes &quot;superior&quot; (*$pos.y &lt; 0.5*) e &quot;inferior&quot; (*$pos.y > 0.5*).

Cualquier dato de un píxel en la parte &#39;superior&#39; está semánticamente estrechamente relacionado con el píxel coincidente en la parte &#39;inferior&#39; y viceversa.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Rutas Datos codificados por polígono](../../../../../../assets/PathsPolygon_Data.jpg "Rutas Datos codificados por polígono")

</td>
</tr>
</table>

>[!NOTE]
>
> Los datos de rutas requieren una precisión de 32 bits y el uso de una profundidad de bits inferior producirá resultados incorrectos.
> 
> Por lo tanto, asegúrese de establecer el parámetro &quot;Formato de salida&quot; de los nodos que generan datos de trazados en &quot;Alta precisión HDR (32F)&quot;.

Permita que `*uv\_pos*` sea una dirección 2D (como *$pos*) de un píxel de la parte &#39;superior&#39;.

En el resto de este documento:

* <b>top[uv\_pos].XYZW</b> hará referencia a los 4 elementos flotantes almacenados en el píxel de la parte superior.\
  top[uv\_pos] == muestra\_color(rutas, uv\_pos)
* <b>bottom[uv\_pos].XYZW</b> hará referencia a los 4 elementos flotantes almacenados en el píxel coincidente de la parte inferior.\
  bottom[uv\_pos] == muestra\_color(rutas, uv\_pos + Float2(0, 0.5))

top[uv\_pos] y bottom[uv\_pos] juntos forman una unidad semántica U[uv\_pos] del documento, compuesta por 8 flotantes.

### Encabezado del documento

Cada documento de Paths comienza con un encabezado de documento. Es la primera unidad semántica U[(0,0)]:

+++Superior
<b>X</b>

El número de rutas (debe ser un entero positivo en [0; 16777216]).

Si algunos trazados están vacíos, todavía cuentan aquí. Por lo tanto, puede pensarlo como un &quot;número de encabezados de trazados que se deben decodificar&quot;.

<b>YZ</b>

El tamaño de píxel de este documento (es decir, exactamente `Float2(1,1) / $size`).

Esto es útil cuando se leen las rutas de acceso desde un [procesador de píxeles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) o un [mapa de píxeles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md), por ejemplo, cuyo tamaño de salida es diferente.

<b>W</b>

1/16 = 0,0625 (indicador de encabezado)

+++

+++Inferior
<b>XY</b>

La dirección del último vértice definido en este documento. Esto resulta útil para anexar nuevos datos.

Por lo tanto, puede ser realmente cualquier dirección mayor (en orden de escaneado) que la dirección del último vértice. Debe estar en el intervalo &rbrack;0, 1[×]0, .5&lbrack;

<b>ZW</b>

No utilizado, debe ser Float2(0, 1)

+++

### Encabezados de ruta

El encabezado del documento va seguido inmediatamente de los encabezados de número de rutas = top[(0,0)].X, uno por unidad semántica.\
E.g. si hay 3 rutas en el documento, se almacenarán en U[(0,1)\*pixel\_size], U[(0,2)\*pixel\_size] y U[(0,3)\*pixel\_size] (con pixel\_size = top[(0,0)].YZ).

Si hay más trazados de los que puede contener una línea de píxeles, los encabezados de trazado restantes se escriben en la siguiente línea o líneas, en orden de escaneado.\
Se permite tener encabezados de ruta de acceso null (`top[...].XYZW = Float4(0,0,0,0)`); dicho trazado podría seguir siendo un único trazado vacío.

El encabezado de ruta de acceso de la ruta de acceso N se definirá en la dirección `path\_addr` y se definirá como:

+++Superior
<b>X</b>

Número de vértices de este trazado. Debe estar en el intervalo [0, 1677216].

Si los vértices inicial y final de un trazado cerrado están en la misma posición, todavía cuentan para 2 vértices.\
Una ruta con 0 vértices es una ruta válida de todos modos.

<b>Y</b>

Indicador *Is\_closed*: 1 si el trazado está cerrado (por ejemplo, un círculo), 0 en caso contrario (por ejemplo, una línea recta).

<b>Z</b>

El índice de la ruta *N.* Debe coincidir absolutamente con *path\_addr* (consulte la nota siguiente).

<b>W</b>

El indicador de encabezado: 1/16 = 0,0625.

+++

+++Inferior
<b>XY</b>

Dirección de vértice inicial (o primera).

<b>ZW</b>

Dirección de fin (o último) vértice.

+++

>[!NOTE]
>
> Puede calcular `path\_addr` desde N mediante la función `Utils/pixel\_index\_to\_position` en rutas\_tools.sbs: `path\_addr = pixel\_index\_to\_position(N+1)`

### Información de vértices

Los vértices se pueden encontrar en cualquier parte de la imagen después de los encabezados (encabezados de documento o de ruta). Los vértices pueden ser de varios &quot;tipos&quot; (Inicio, Medio o Fin) y se vinculan explícitamente entre sí mediante 2 punteros de dirección (&quot;vínculos&quot;).

Los vértices <b>Inicio</b> y <b>Fin</b> son especiales en este sentido: Para permitir la representación de trazados cerrados o de una red arbitraria de trazados enlazados entre sí, uno de los enlaces se utiliza realmente para formar una lista circular enlazada hacia delante de todos los demás vértices de Inicio o Fin que representan el mismo vértice. Tales vértices que coinciden entre sí se llaman &quot;hermanos&quot;. [Ilustración bienvenida]

Formalmente, cada vértice de la dirección `*vert\_addr*` se define así:

+++Superior
<b>XY</b>

La posición del vértice. Las coordenadas pueden ser cualquier valor flotante que no sea NaN o ±inf. No existe la noción de mosaico en este nivel (puede ser manejado o no por la implementación de cada filtro), por lo que se supone que los trazados deben ser definidos en el plano euclidiano.

<b>Z</b>

El índice de trazado de vértice. Un vértice solo puede pertenecer a un trazado. (Como se mencionó anteriormente, los vértices inicial y final pueden tener hermanos). El índice de ruta se puede utilizar para recuperar el encabezado de ruta (consulte Encabezados de ruta de sección más arriba), por lo que debe estar sincronizado.

<b>W</b>

Tipo de vértice. Se divide entre el signo del valor y su valor absoluto:

En la parte de signo, un valor de 0 significaría que no hay ningún vértice aquí en realidad (todos los demás componentes deben ser 0 también). Un valor negativo significa que el vértice está marcado como una &quot;esquina&quot;; uno positivo que el vértice es &quot;liso&quot;. El vértice de vértice frente a vértice suave es un atributo puro y aislado y no tiene ningún impacto ni significado en el resto de la codificación de Trazados.

En la parte de valor absoluto, el tipo de píxel (Inicio, Medio o Fin) y otro indicador (trivial\_link) están codificados:

* *0,125*: Vértice del extremo (el último vértice de la forma; enlaces siempre no triviales, ver a continuación)

* *0,25*: Vértice inicial (el primer vértice de la forma; enlaces siempre no triviales, ver a continuación)

* *0,5*: Vértice medio con vínculos no triviales

* *1*: Vértice medio con vínculos triviales

&quot;Vínculos triviales&quot; se refiere al hecho de que los vértices anterior y siguiente (en la lista de vértices del trazado actual) se almacenan en el píxel a la izquierda (vert\_addr-(0,pixel\_size)) y a la derecha (vert\_addr+(0,pixel\_size) respectivamente, mientras que &quot;vínculos no triviales&quot; significa que al menos uno de estos se almacena en otro lugar.

+++

+++Inferior
Independientemente de la &quot;trivialidad&quot; de los vínculos, los valores de confianza de los vínculos se almacenan en la parte inferior:

<b>XY</b>

La dirección del vértice anterior de esta ruta. Para los vértices de inicio, esto señala al siguiente vértice del mismo nivel.\
si |top[vert\_addr].W| = 1, then bottom[vert\_addr].XY = vert\_addr - (0,pixel\_size)

<b>ZW</b>

La dirección del siguiente vértice de esta ruta. Para los vértices finales, esto apunta al siguiente vértice del mismo nivel.\
si |top[vert\_addr].W| = 1, then bottom[vert\_addr].ZW = vert\_addr + (0,pixel\_size)

+++

## Leer y escribir información de trazados

Si desea crear sus propios nodos de procesamiento de trazados, dispone de varias herramientas.

Los conceptos básicos los proporcionan los nodos [Paths Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) y [Paths Vertex Processor Simple](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md), que básicamente se pueden usar del mismo modo que un [procesador de píxeles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md).

Si necesita características más allá de lo que ofrecen los nodos del procesador de vértices de rutas (más texturas de entrada, o más vértices anteriores o siguientes), copiar la implementación de este gráfico podría ser un buen punto de partida (suponiendo que reemplace el nodo <b>Get(&quot;%perVertex&quot;)</b> por su procesamiento personalizado).

Pero en caso de que quieras hacer algo más extraterrestre que aplicar una función por vértice, aquí hay una explicación detallada de las herramientas que puedes usar. Estas suelen ser pequeñas funciones auxiliares que se pueden encontrar en el mismo paquete que los otros nodos de rutas (*rutas\_tools.sbs)*. (Estas funciones no se exponen en el [<b>menú Biblioteca</b>](../../../../../../interface/the-library/the-library.md) y <b>Nodo</b>.)

### Funciones de &#39;Lectura&#39;

En la carpeta `Read`, puede encontrar varias de estas, útiles para recopilar información sobre las rutas:

Algunos pueden proporcionarle información sobre un píxel determinado. Todos toman como entrada el valor Float4 muestreado en la parte \*top\*. Si se fijan en su implementación, son súper simples. Su objetivo es transmitir más significado que los nodos atómicos:

+++is_header
Compruebe que el valor de muestra actual sea un encabezado de ruta o un encabezado de documento.

+++

+++path_is_closed
Compruebe el indicador Is\_Closed (.Y) en un encabezado de ruta. Se \*supone que ya ha comprobado que es una ruta\* con `is\_header` y que `current\_pixel\_is\_document\_header` devolvió false.

+++

+++is_vertex
Compruebe que el valor muestreado actual es un vértice, es decir, no un encabezado ni un píxel vacío.

+++

+++is_start_vertex
Compruebe si un valor \*top-part sampled\* es un vértice de inicio (no es necesario comprobar `is\_vertex` primero).

+++

+++is_mid_vertex
Compruebe si un valor \*top-part sampled\* es un vértice que no es un vértice de inicio ni de fin (no es necesario comprobar `is\_vertex` primero).

+++

+++is_end_vertex
Compruebe si un valor \*top-part sampled\* es un vértice Fin (no es necesario comprobar `is\_vertex` primero).

+++

+++is_segment_start
Mano corta para `is\_start\_vertex || is\_mid\_vertex`. Es más útil para el procesamiento basado en [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md), para procesar cada segmento como máximo una vez.

+++

+++is_corner
Marque la marca de esquina del vértice (no es necesario comprobar `is\_vertex` primero: si la respuesta es verdadera, usted está en un vértice seguro). Por favor recuerde que esta bandera no está soportada aún por nodos oficiales.

+++

+++has_trivial_links
Si se trata de un vértice, indica si se puede deducir fácilmente la posición de los vértices anterior y siguiente sin muestrear la parte inferior. (Nota: Un elemento que no sea un vértice siempre devolverá false.)

Probablemente no desee usar esto directamente, sino más bien usar una de las funciones `sample\_next\*` o `sample\_prev\*`, que se encargan de ello por usted.

+++

+++sample_next, sample_prev
Dado el valor muestreado de la parte superior `*sampled*` y su posición `*sampled\_position*`, devuelve el valor muestreado de la parte superior del vértice siguiente (respectivamente anterior) y establece una variable Float2 `*next\_sampled\_pos*` en la posición (en la parte superior) de este vecino (es decir, &lt;valor devuelto> = SampleColor(next\_sampled\_pos, image0). `*input0PixSize*` debe ser igual al tamaño de píxel del trazado (top[(0,0)].YZ).

Si el píxel actual (`*sampled*`) es un vértice <b>Start</b>, *sample\_prev* devolverá el siguiente elemento relacionado de este vértice; del mismo modo, si es un vértice <b>End</b>, *sample\_next* devolverá el siguiente hermano de este vértice (es decir, tal vez no sea lo que desee). Consulte `*sample\_next\_advanced*` y `*sample\_prev\_advanced*` a continuación para resolver este problema.

Tenga en cuenta que para simplificar, se supone que <b>la información de rutas se almacena en input0!</b> Además, a diferencia de lo que indica el documento de la función, no es necesario declarar previamente `*next\_sampled\_pos*`. `*[out]next\_sampled\_pos*` es un parámetro ficticio para recordarle que este segundo &quot;valor devuelto&quot; existe.

Puede comprobar `*paths\_trace*` [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md), en el parámetro Iterations del tercer nodo iterate, para obtener un ejemplo de cómo usarlo.

![Caso de uso mínimo de sample_next](../../../../../../assets/paths-spec_fxmap-sample-next_02.png "Caso de uso mínimo de sample_next")



![Caso de uso de sample_next en rutas de previsualización (path_trace)](../../../../../../assets/paths-spec_fxmap-sample-next_01.png "Caso de uso de sample_next en rutas de previsualización (path_trace)")



+++

+++sample_next_advanced, sample_prev_advanced
Esto está destinado a trabajar en caminos cerrados. En el caso de los trazados abiertos, el vértice Inicio o Fin no tiene un elemento relacionado y, en este caso, ambas funciones devuelven el mismo elemento y sólo el vecino. En los vértices inicial o final con más de un elemento relacionado (rutas conectadas en red), se devolvería el vértice vecino del siguiente elemento relacionado de la lista vinculada.

+++

### Funciones de &#39;escritura&#39;

En la carpeta `Write`, encontrará pequeños ayudantes que crean un Float4 listo para ser escrito <b> por un [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)</b>.

De hecho, [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) multiplica RGB por Alpha antes de dibujar, por lo que los valores reales no se premultiplican para compensar eso. Si desea utilizar estas funciones, por ejemplo, en un [procesador de píxeles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), le recomendamos que vuelva a aplicar la premultiplicación o que escriba una versión personalizada (más optimizada para su caso de uso y más fácil de usar).

+++document_header
Genera la parte superior del encabezado del documento, declarando el número de rutas de acceso proporcionadas.

+++

+++document_last_vertex_spec
Crea la parte \*bottom\* del encabezado del documento, que especifica la última dirección de vértice (consulte A.1.).

+++

+++path_header
Crea la parte superior de un encabezado de ruta de acceso, según el número de vértices de la ruta de acceso `*nbVertices*`, el indicador `*isClosed*` y `*pathIndex*`.

+++

+++start_vertex, mid_vertex y end_vertex
Crea la parte superior de un vértice, estableciendo la posición, el texto y otras opciones en consecuencia.

Acerca de *mid\_vertex* y el parámetro *hasTrivialLinks*: Lo ideal sería establecer el valor adecuado, pero si por cualquier razón no se puede saber si los vínculos serán triviales o no, se puede establecer con seguridad en false (a costa de un procesamiento más lento de la ruta generada).

+++

No hay ningún generador de partes inferiores para encabezados de ruta ni vértices: ambos codifican dos vínculos a la parte superior, por lo que esta función sería esencialmente un constructor Vector Float4 de dos Float2. No olvide dividir XYZ por W si está escribiendo con [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) (dado que W es la Y de una dirección, nunca debe ser null).

Encontrará un ejemplo pertinente de cómo usar estas funciones en el paquete <b>*paths\_polygon.sbs* </b>que aloja el nodo [Paths Polygon](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md).

### Métodos para procesar rutas

Es probable que utilice un procesador de píxeles o un Fx-Map para implementar su procesamiento personalizado, cada uno de los cuales tiene sus fortalezas y debilidades:

+++FX-Map
La solución basada en [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) suele ser la preferida cuando se realizan operaciones de alto nivel que requieren un conocimiento global de toda la ruta (o rutas) o una acumulativa (por ejemplo, reempaquetar los vértices después de la diezmación o teselación). También es la forma más sencilla de abordarlo, por lo que si está realizando un procesamiento personalizado por primera vez, puede que desee utilizar un mapa de efectos, a pesar de que *puede* ser más lento.

En primer lugar, debe estar familiarizado con Fx-Map. Si no es así, consulte la [documentación específica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md).

Le recomendamos que examine la implementación de [Rutas de vista previa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) en <b>*rutas\_trace.sbs*</b> y [Rutas polígono](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md) en <b>*rutas\_polygon.sbs*</b> para tener una idea sobre cómo leer y escribir (respectivamente) una ruta usando un mapa de efectos.

+++

+++Procesador de píxeles
La solución [Pixel Processor](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) encajará si solo necesitas información &quot;local&quot;. Aquí queremos decir &quot;local&quot; no espacialmente (la distancia entre el elemento) sino topológicamente (vértices unidos). Así es como se implementa el procesador de vértices. El procesador de píxeles suele ser más rápido que el Fx-Map para este tipo de operación, ya que la función de cada píxel se evalúa en paralelo, mientras que solo se accede a una cantidad limitada de datos. Sin embargo, el esfuerzo de implementación podría ser mucho más importante, ya que solo puede modificar el píxel actual.

No entraremos en detalles, ya que hay mucho que decir dependiendo de su caso de uso específico, pero lo primero que hay que hacer es comprobar dónde se encuentra:

¿Está en la parte superior ($pos.y &lt; 0.5) o inferior ($pos.y > 0.5)? Recomendamos que recuerde que en una variable dedicada (p.ej. `*isTop*`) y que crea un objeto Float2 de tipo `*vert.addr*`, ese valor es `*$pos*` para la parte superior y `$pos - (0,0.5)` para la parte inferior.

¿Qué hay en *vert.addr*? Muéstrelo y compruebe si hay algo (W != 0) entonces, si lo hay, qué exactamente. ¿Un encabezado (W = 0,0625) (comprobar con `*Read/is\_header*`) o un vértice (comprobar con `Read/is\_vertex`)? Y si es un encabezado, ¿es el encabezado del documento o un encabezado de ruta? (Puede usar `*Read/current\_pixel\_is\_document\_header*` para comprobarlo). Utilice una o varias de las funciones auxiliares para que coincidan con lo que le resulte interesante.

+++
