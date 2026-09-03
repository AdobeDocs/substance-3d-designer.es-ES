---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-15-1.html"
breadcrumb-title: ''
description: Consulte las notas de la versión 15.1 de Substance 3D Designer para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versión 15.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---


# Versión 15.1

Substance Designer 15.1 ofrece una ventana de creación de gráficos completamente renovada con acceso directo a muestras, nodos de ruido mejorados para mayores posibilidades creativas, categorías organizadas en el menú de nodos y mucho más.

*Fecha de publicación: 11 de diciembre de 2025*

![Banner de Designer 15.1](version-15-1.resources/version-15-1-01.png)

## Mejora de la creación de gráficos

En esta versión, la [ventana de creación de gráficos](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) se ha <b>rediseñado completamente</b> para mejorar la experiencia inicial del usuario en Substance 3D Designer. El objetivo principal de esta actualización es agilizar el proceso de selección de plantillas, lo que permite a los usuarios identificar de forma eficaz la plantilla más adecuada para sus necesidades.

Las miniaturas ofrecen al instante <b>referencias visuales</b> para los tipos de materiales previstos, mientras que las sugerencias detalladas proporcionan toda la información pertinente. Para mejorar la organización, las plantillas ahora se clasifican en <b>categorías</b> específicas, como materiales, filtros y procesamiento de digitalizaciones.

Aunque la interfaz principal se ha actualizado, los usuarios siguen teniendo acceso a vistas anteriores, incluidas las opciones de lista, paquetes y directorios.

[Más información](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)

![rediseñar nueva ventana de gráfico](version-15-1.resources/version-15-1-02.png){zoomable="yes"}

## Muestras incrustadas

Con el lanzamiento de nuestra ventana de creación de gráficos rediseñada, hemos agregado una variedad de [<b>materiales de muestra</b>](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) directamente dentro del software. Esta mejora responde a su solicitud de un mejor acceso a los recursos de aprendizaje.

![Nueva ventana de creación de gráficos para las muestras](version-15-1.resources/version-15-1-03.png){zoomable="yes"}

Para satisfacer esta necesidad hemos incluido muestras de materiales tales como telas (incluyendo cuero y satén), madera, metal, plástico, cerámica y más. Estos ejemplos están pensados para ayudarle a iniciar sus proyectos con facilidad y familiarizarse con los principales nodos de la familia disponibles en Substance 3D Designer

Cada gráfico está <b>anotado</b>, cuidadosamente organizado y contiene un número mínimo de nodos para que sea lo más fácil de entender posible.

Puede acceder a las muestras en la categoría &quot;Muestras de material&quot; al crear un nuevo gráfico de Substance, o directamente desde la pantalla de inicio mediante el cómodo botón &quot;Ir a muestras&quot;.

Junto con estos materiales fundamentales, también proporcionamos <b>ejemplos avanzados</b> para demostrar cómo usar las funciones de <b>FX-map y procesador de píxeles</b> de manera más eficaz.

[Más información](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)

![muestra de madera en substance designer](version-15-1.resources/version-15-1-04.png){zoomable="yes"}

## Nuevos ruidos

Los ruidos desempeñan un papel crucial en la mayoría de los gráficos, por lo que nos hemos centrado en varias mejoras clave de esta versión para mejorar su funcionalidad y facilidad de uso.

Con esta actualización, hemos introducido <b>una mejor compatibilidad con escenarios que no son de mosaico</b>, lo que garantiza que los patrones de ruido se comporten del modo esperado sin el mosaico obligatorio. Anteriormente, los nodos de ruido se forzaban a colocar en mosaico o producían resultados incorrectos cuando el mosaico estaba desactivado.

La mayoría de los ruidos ahora incluyen <b>nuevos parámetros</b>, lo que proporciona a los usuarios un mayor control creativo. Estas opciones adicionales permiten a los autores de gráficos ajustar con precisión el aspecto y el comportamiento del ruido en sus flujos de trabajo.

Por último, bitdepth <b> ya no está bloqueado de forma rígida a 16 bits</b>. Ahora puede anular la configuración de profundidad de bits en instancias de nodo individuales, lo que le permite lograr un mayor detalle y rango dinámico cuando sea necesario, u optimizar los gráficos para el rendimiento.

Consulta la lista completa de ruidos actualizados en las [notas de la versión](#release-notes) que aparecen a continuación.

Ejemplos:   [Celdas 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) [Nubes 2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md) [Arañazos direccionales](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-scratches/directional-scratches.md) [Ruido de humedad 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

![ruido de desorden direccional](version-15-1.resources/version-15-1-05.gif){zoomable="yes"}

## Jerarquía en el menú de nodos

Para abordar el desafío de localizar nodos específicos dentro de la extensa biblioteca, hemos introducido categorías en el menú Nodo.

El gran número de nodos disponibles puede dificultar la búsqueda rápida del deseado. Para agilizar este proceso, se ha implementado un nuevo atributo [<b>Group</b>](../../compositing-graphs/graph-parameters/graph-parameters.md) en el nivel de gráfico. Cuando se define este atributo, se utiliza para organizar y ordenar los resultados de búsqueda.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![búsqueda de nodos con categoría 1](version-15-1.resources/version-15-1-06.png){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![búsqueda de nodos con categoría 2](version-15-1.resources/version-15-1-07.png){zoomable="yes"}

</td>
</tr>
</table>

## Salida predeterminada

Cuando un nodo tiene varias [salidas](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), no es posible mostrarlas todas simultáneamente en la vista 2D o como miniatura del nodo. La pauta predominante en estos casos es utilizar la primera clavija conectada o, si ninguna está conectada, la primera salida de forma predeterminada.

Sin embargo, es posible que este enfoque no siempre produzca resultados óptimos. Por ejemplo, en algunos nodos Spline, el primer pin conectado a menudo representa datos de coordenadas de spline, lo que no es adecuado para la previsualización.

Para solucionar este problema, se ha introducido un atributo de salida predeterminado. Esta función permite al autor del gráfico <b>especificar qué salida debe mostrarse de forma predeterminada</b>, lo que mejora la intuición del uso del nodo y facilita una comprensión más clara del gráfico creado.

Juegue con la siguiente imagen para ver la diferencia antes y después de la definición de salida predeterminada.

[Más información](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

<table>
  <tr>
    <td>
      <img src="version-15-1.resources/version-15-1-08.png" alt="defaultouput2">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="version-15-1.resources/version-15-1-09.png" alt="Con la salida predeterminada, las miniaturas siempre son relevantes.">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

## Nodo &#39;Is defined&#39;

Al trabajar con gráficos de funciones, puede ser necesario determinar si existe una [variable](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) en el gráfico.

Por ejemplo, detectar la ausencia de una variable permite proporcionar un valor de reserva, lo que garantiza que la función se comporte como se espera sin que sea necesario establecer explícitamente cada entrada. Por eso hemos agregado el nodo [&#39;Is defined&#39;](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md).

[Más información](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)

![Se ha definido el nodo](version-15-1.resources/version-15-1-10.png){zoomable="yes"}

## Notas de la versión

### 15.1.0

*(Lanzado el 11 de diciembre de 2025)*

### Añadido

* [NewGraph] Repaso de la nueva ventana gráfica
* [NewGraph] Agregar muestras de materiales y muestras avanzadas
* [NewGraph] Añada un nuevo atributo de gráfico para los datos de plantilla (categoría y subtítulo)
* [NewGraph] Opción Quitar formato de salida
* [Contenido] Añadir funciones hash
* [Contenido] Añadir tonemappers a functions.sbs
* [Contenido] Ruido anisotrópico v2: agregar formato de salida predeterminado, agregar desorden
* [Content] Aplicación de mayúsculas y minúsculas de oración a etiquetas de nodo y parámetros
* [Contenido] Puntos BnW 1 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] BnW spots 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] BnW spots 3 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Celdas 1,2,3,4 v2: añadir formato de salida predeterminado, sin soporte de mosaico, opciones de desorden
* [Contenido] Nubes 1 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Nubes 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Nubes 3 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Color para enmascarar v2
* [Contenido] Ruido direccional 1 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Ruido direccional 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Ruido direccional 3 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Ruido direccional 4 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Arañazos direccionales v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 1 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 3 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 4 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 5 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Degradado de Dirt v2: añadir formato de salida predeterminado, nuevas opciones de desorden
* [Content] Base de Suma fractal v2: agregar formato de salida predeterminado, desorden, sin compatibilidad con mosaicos
* [Contenido] Suma fractal 1,2,3,4 v2: agregar formato de salida predeterminado
* [Contenido] Ruido gaussiano v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Manchas gaussianas 1 y 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Fibras sucias 1,2,3 v2: añadir formato de salida predeterminado, sin soporte de mosaico, opciones de desorden
* [Contenido] Ruido de humedad v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Nuevo nodo &quot;Ruido de humedad 2&quot;
* [Contenido] Ruidos: actualizar para agregar el formato de salida predeterminado
* [Contenido] Ruido de Perlin v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Asignador de formas: agregar modo de filtro
* [Contenido] Mapeador UV: agregar modo de filtrado
* [Contenido] Forma de onda 1 v2: usar formato de salida predeterminado + nuevas opciones
* [Contenido] Ruido blanco v2: usar formato de salida predeterminado, agregar opciones de distribución
* [Bakeres] Muestra solo las UV de la malla seleccionada
* [Bakers] Añada una opción para seleccionar el método de coincidencia de geometría por nombre
* [Bakeres] Seleccione el Baker más cercano cuando se elimine un baker
* [Panaderos] UDIM: definir una lista de azulejos UV para hornear
* [Panaderos] Actualice bake sdk a 3.15.4.
* [Vista 3D/SceneBrowser] Evite seleccionar un elemento UsdPrimitive al hacer clic con el botón derecho en él
* [ColorManagement] Compatibilidad con ACES 2.0
* [Gráfica de composición] Permite definir un nodo de salida como &quot;Salida predeterminada&quot;
* [Cooker] Quitar advertencia en entradas no conectadas de instancias de función††
* [Funciones] Añadir operador isDefined
* [Graph] Agrupe los elementos por atributo &#39;group&#39; en el menú de nodos
* [Graph] Mejora la representación de miniaturas

### Correcciones

* [Vista 3D] La textura de escala de grises L16 se muestra con un matiz rojo cuando se conecta al entorno o a baseColor
* [Vista 3D] Al cambiar el enlace de material de una escena sin material, se crea un nuevo material &quot;predeterminado&quot;
* [Vista 3D] Las normales calculadas no son correctas para mallas de OBJ específicas
* [Vista 3D] El entorno personalizado de SBSSCN no está visible al cargar en Pathtracer
* [Vista 3D] Errores en la consola al girar un entorno desactivado
* El Specular level [Vista 3D] no se aplica correctamente
* [Vista 3D] El Specular edge color no funciona cuando se utiliza el rasterizador Eclair
* [Vista 3D] El material añadido por el usuario no se aplica en escenas predeterminadas
* [Vista 3D] [Panaderos] El color del material es demasiado oscuro una vez se ha anulado o al utilizar un panadero de &quot;Color&quot;
* [Vista 3D]&#x200B;[Bakeres] No hay color de material en FBX archivo
* [Bakeres] Los colores de material de los archivos FBX no se detectan correctamente
* [Baker] La opción &#39;recompute\_tangents&#39; siempre es &#39;false&#39; en las exportaciones de ajustes preestablecidos de JSON
* [Bakers] CLI: Bloqueo al ejecutar el mismo panadero de forma consecutiva a través del archivo JSON
* [Bakeres] La actualización del parámetro &#39;color-generator&#39; no funciona para &#39;Escala de grises&#39;
* [Contenido] Enmascarar trazados: Error en las proporciones no cuadradas
* [Contenido] Procesador de Renderizaciones PBR/iconos: Lóbulo de specular incorrecto
* [Contenido] Trazados a spline: Establezca el &#39;Tamaño de salida&#39; en &#39;Relativo al principal&#39; de forma predeterminada
* [Contenido] Lista de puntos: Los puntos no están en el orden correcto cuando la textura de los datos no es cuadrada
* [Contenido] Asignador de splines: Error de línea de 1px en casos aleatorios
* [Contenido] Asignador de splines: UV estirados en algunos casos cuando el thickness es 0
* [Graph] Bloqueo al eliminar la salida de un subgráfico de función
* [Graph] El tipo de color del nodo de entrada se puede cambiar en paquetes de solo lectura
* [Graph] La entrada principal se puede cambiar en paquetes de solo lectura
* [Propiedades] El color del widget de previsualización de color no coincide con el estado del botón sRGB
* [Scene] No se puede cargar un archivo OBJ de más de 2 GB
* [UI] Los estados de acoplamiento de la consola y el administrador de dependencias no se restauran después de reiniciar

### ERRORES CONOCIDOS

* [Bakers] Se bloquea al realizar el procesamiento con algunos controladores NVIDIA específicos
* [Vista 3D] OpenGL: es posible que algunas escenas importadas no se procesen
* [Vista 3D] Buscatrazos: rendimiento lento al actualizar texturas con teselación/desplazamiento activado
* [Vista 3D] Algunas propiedades de material de color no se administran correctamente cuando se anulan
* [Vista 3D] Las escenas con animaciones simples no se admiten correctamente
* [Vista 3D] Aún no se admiten mallas con varios UDims
* [Vista 3D] Las mallas con múltiples UV no son compatibles y pueden provocar una representación de material no válida
* [Vista 3D] El trazador de trazados no es compatible con tarjetas gráficas AMD
