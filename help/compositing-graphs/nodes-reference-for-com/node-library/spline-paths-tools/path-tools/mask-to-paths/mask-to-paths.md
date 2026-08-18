---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: Utilice el nodo Máscara a trazados para convertir texturas de máscara en datos de trazado para la generación de trazados de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Máscara a trazados
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# Máscara a trazados

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/mask-to-paths-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de trazado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Convierte un patrón de entrada de escala de grises <b>Mask</b> en una lista de segmentos de ruta codificados en la salida <b>Paths</b>.

Los controles sobre la posición inicial de los trazados generados, así como su orden en la lista, están disponibles.

Los trazados generados se pueden procesar posteriormente mediante nodos dedicados, por ejemplo, [Transformación 2D de trazado](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), [Deformación de trazados](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md), o se pueden convertir en splines mediante el nodo [Ruta a spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para asignar o dispersión formas a lo largo de ellos.

</td>
</tr>
</table>

>[!NOTE]
>
> El método utilizado para codificar trazados se explica en la página [Especificaciones de formato de trazados](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md).

## Conectores de entrada

<b>Máscara</b> *Escala de grises*\
Patrón de entrada que se debe convertir en una lista de trazados.

## Conectores de salida

<b>Vista previa</b> *Color* Vista previa compuesta en la parte superior de la máscara para ayudar a visualizar los efectos de los parámetros.

<b>Rutas</b> *Color*\
Lista de trazados codificados en una imagen en color. cada ruta describe una lista de segmentos codificados.\
El resultado se puede procesar usando otro nodo de procesamiento de rutas o enviarlo a un nodo [Rutas a spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para procesarlo más como splines.

## Parámetros

<b>Máscara suave</b> *Flotante*\
Aplique suavizado a la máscara de entrada.\
Útil cuando el patrón de entrada tiene bordes muy afilados, lo que normalmente provoca artefactos.

<b>Valor de umbral de máscara</b> *Float* Valor de escala de grises de <b>Mask</b> que se usará para separar el exterior (valores &lt; Valor de umbral de máscara) y el interior (valores > Valor de umbral de máscara) de la forma.

<b>Ruta de acceso decimal</b> *Float* Controla implícitamente la cantidad de segmentos que se generarán.\
Una gran cantidad de diezmación hará que las formas redondeadas sean algo poligonales, mientras que ninguna diezmación generará casi un segmento por píxel.\
Una cantidad razonable coincidirá mejor con la forma de las líneas rectas y curvas sin crear muchos puntos intermedios para las líneas rectas.

<b>Cerrar trazados abiertos</b> *Boolean* Crear un segmento entre los vértices inicial y final de los trazados abiertos.\
Desactivar esto puede corregir las líneas no deseadas que atraviesan el patrón de forma inesperada; sin embargo, es posible que las rutas ya no estén cerradas.

<b>Umbral de vértice</b> *Flotante*\
Cada vértice codificado en trazados puede contener un indicador que indique si es duro (es decir, una esquina) o suave.\
Este parámetro le permite marcar más o menos vértices según el ángulo entre sus segmentos adyacentes.\
*Nota:* Este indicador &#39;corner&#39; no es compatible actualmente con ningún nodo existente, pero está disponible para usarse en un nodo [Path Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). También puede visualizar las esquinas con el nodo [Rutas de vista previa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md).

<b>Modo de inicio de ruta</b> *Entero* Método para seleccionar qué vértice debe ser el inicio de cada trazado generado alrededor de las formas de la máscara.\
Esto tiene un impacto significativo al convertir los <b>trazados a splines</b> generados mediante el nodo dedicado, ya que varios nodos spline utilizan el inicio y el final de las splines.\
*- Vértice más agudo:* El vértice que forma el ángulo más bajo con sus vértices anterior y siguiente\
*: vértice en el extremo de una dirección especificada:* El último vértice en una dirección dada\
*- Vértice más cercano a una posición especificada
* Vértice más alejado de una posición especificada
* Función de inicio personalizada:* Utilice una función personalizada para seleccionar el vértice que debe utilizarse como inicio de cada ruta

<b>Dirección de inicio</b> *Flotador*&#x200B;Ángulo que describe la dirección utilizada para seleccionar el vértice de inicio. Para cada trazado, se selecciona el último vértice en esta dirección.\
El valor es un *número de vueltas* que se usa para girar un vector de dirección X-izquierda. Esto significa que 0 establece un vector de dirección de (-1, 0) y 0,25 (90 grados) establece un vector de dirección de (0, 1).\
*Nota:* Este parámetro está disponible cuando <b>Modo de inicio de ruta</b> está establecido en &quot;Vértice en el extremo de una dirección especificada&quot;

<b>Posición de destino de inicio</b> *Float2* Posición en la imagen utilizada para seleccionar el vértice de inicio.\
Para cada ruta, se selecciona el vértice más cercano o más alejado de esta posición, según el <b>modo de inicio de ruta</b> seleccionado.\
*Nota:* Este parámetro está disponible cuando <b>Modo de inicio de ruta</b> está establecido en &quot;Vértice más cercano a una posición especificada&quot; o &quot;Vértice más alejado de una posición especificada&quot;

<b>Función de inicio</b> *Float* Función utilizada para seleccionar el vértice de inicio. Devuelve un valor de tipo Float.\
Para cada vértice, se ejecuta la función y se selecciona el vértice para el que la función devuelve el *resultado más alto*.\
Variables disponibles:\
*-* vertex.cornerness(Float)*:* La puntuación del vértice como candidato para ser una esquina\
*-* vertex.pos(Float2)*:* Posición del vértice en el espacio de imagen\
*Nota:* Este parámetro está disponible cuando el modo de inicio de ruta está establecido en &quot;Vértice más cercano a una posición especificada&quot; o &quot;Función de inicio personalizada&quot;

<b>Modo de pedido</b> *Integer* Método para ordenar los trazados generados.\
La posición o el tamaño del cuadro delimitador *de los trazados* (cuadro B) se puede usar como criterio para ordenar los trazados.\
Esto tiene un impacto significativo al convertir las <b>rutas de acceso a splines</b> generadas mediante el nodo dedicado, ya que varios nodos spline utilizan el orden de las splines.\
*- Heredado (rápido):* El método utilizado en la versión anterior de este nodo, que ofrece un rendimiento significativamente mejor\
*- Por ubicación central del cuadro en la dirección:* Los trazados se ordenan de acuerdo con la posición del centro de su cuadro, del primero al último en la dirección especificada\
*- Por cuadro de diálogo Cuadro de diálogo Posición superior izquierda a lo largo de la dirección:* Los trazados se ordenan según la posición de la esquina superior izquierda de su cuadro de diálogo, de primero a último a lo largo de la dirección especificada\
*- Por tamaño de bandeja - De mayor a menor:* rutas están ordenadas según el tamaño de su bandeja, de mayor a menor\
*- Por tamaño de bandeja - De menor a mayor:* Las rutas se ordenan según el tamaño de su bandeja, de menor a mayor\
*- Función de ordenación personalizada:* Utilice una función personalizada para ordenar rutas

<b>Dirección de orden</b> *Float*&#x200B;Ángulo que describe la dirección utilizada para ordenar los trazados de primero a último en esa dirección.\
El valor es un *número de vueltas* que se usa para girar un vector de dirección X-izquierda. Esto significa que 0 establece un vector de dirección de (-1, 0) y 0,25 (90 grados) establece un vector de dirección de (0, 1).

<b>Función de ordenación</b> *Float* Función utilizada para ordenar los trazados. Devuelve un valor de tipo Float.\
Las rutas de acceso se ordenan en *orden ascendente* según el valor de esta función. En otras palabras, el resultado de la función para cada ruta es la *clave de ordenación* utilizada para ordenar las rutas.\
Variables disponibles:
* bbox.center (Float2): La posición del centro del Path Bbox
* bbox.topleft (Float2): posición de la esquina superior izquierda del cuadro Trazado
* bbox.size (Float2): tamaño del cuadro Trazado (X: anchura, Y: height)

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/MaskToPaths-Demo2.gif "Ejemplo de nodo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](../../../../../../assets/MaskToPaths-Demo1.gif "Ejemplo de nodo 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 3: Modos de inicio](../../../../../../assets/MaskToPaths-Demo3.gif "Ejemplo de nodo 3: Modos de inicio"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 3: Modos de ordenación](../../../../../../assets/MaskToPaths-Demo4.gif "Ejemplo de nodo 3: Modos de pedido"){zoomable="yes"}

</td>
</tr>
</table>
