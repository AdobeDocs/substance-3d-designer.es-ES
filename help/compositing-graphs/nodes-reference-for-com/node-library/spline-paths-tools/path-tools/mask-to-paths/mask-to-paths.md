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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# Máscara a trazados

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](mask-to-paths.resources/mask-to-paths-01.png "Icono de nodo")

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

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Escala de grises</i> | Patrón de entrada que se debe convertir en una lista de trazados. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Color</i> | Una previsualización compuesta en la parte superior de la máscara para ayudar a visualizar los efectos de los parámetros. |
| <b>Rutas</b> <i>Color</i> | Lista de trazados codificados en una imagen en color. cada ruta describe una lista de segmentos codificados.<br>El resultado se puede procesar usando otro nodo de procesamiento de rutas o enviarlo a un nodo de [Rutas a spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para procesarlo más como splines. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Máscara suave</b> <i>Flotador</i> | Aplique suavizado a la máscara de entrada.<br>Útil cuando el patrón de entrada tiene bordes muy afilados, lo que suele causar artefactos. |
| <b>Valor de umbral de máscara</b> <i>Flotador</i> | Valor de escala de grises de <b>Mask</b> que se usará para separar el exterior (valores &lt; valor de umbral de máscara) y el interior (valores > valor de umbral de máscara) de la forma. |
| <b>Ruta de acceso decimal</b> <i>Flotador</i> | Controla implícitamente la cantidad de segmentos que se generarán.<br>Una gran cantidad de diezmación hará que las formas redondeadas sean algo poligonales, mientras que ninguna diezmación generará casi un segmento por píxel.<br>Una cantidad razonable coincidirá mejor con la forma de las líneas rectas y curvas sin crear muchos puntos intermedios para las líneas rectas. |
| <b>Cerrar rutas abiertas</b> <i>Booleano</i> | Cree un segmento entre los vértices inicial y final de los trazados abiertos.<br>Deshabilitar esto puede corregir líneas no deseadas que atraviesan su patrón de una manera inesperada, sin embargo, las rutas no se pueden cerrar más. |
| <b>Umbral de vértice</b> <i>Flotador</i> | Cada vértice codificado en trazados puede contener un indicador que indique si es duro (es decir, una esquina) o suave.<br>Este parámetro te permite marcar más o menos esquinas de acuerdo con el ángulo entre sus segmentos adyacentes.<br><i>Nota:</i> Este indicador de &#39;esquina&#39; no es compatible actualmente con ningún nodo existente, pero está disponible para usarse en un nodo [Path Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). También puede visualizar las esquinas con el nodo [Rutas de vista previa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md). |
| <b>Modo de inicio de ruta</b> <i>Entero</i> | El método para seleccionar qué vértice debe ser el inicio de cada trazado generado alrededor de las formas de la máscara.<br>Esto tiene un impacto significativo al convertir los <b>trazados en splines</b> generados mediante el nodo dedicado, ya que varios nodos spline utilizan el inicio y el final de las splines.<br>*- Vértice más agudo:* El vértice que forma el ángulo más bajo con sus vértices anterior y siguiente <br>*- Vértice en el extremo de una dirección especificada:* El último vértice en una dirección dada <br>*- Vértice más cercano a una posición especificada<br>* Vértice más alejado position<br>* Función de inicio personalizada:* Utilice una función personalizada para seleccionar el vértice que debe utilizarse como inicio de cada ruta |
| <b>Dirección de inicio</b> <i>Flotador</i> | El ángulo que describe la dirección utilizada para seleccionar el vértice de inicio. Para cada trazado, se selecciona el último vértice en esta dirección.<br>El valor es un *número de vueltas* que se usa para girar un vector de dirección X-izquierda. Esto significa que 0 establece un vector de dirección de (-1, 0) y 0,25 (90 grados) establece un vector de dirección de (0, 1).<br><i>Nota:</i> Este parámetro está disponible cuando <b>Modo de inicio de trazado</b> está establecido en &#39;Vértice en el extremo de una dirección especificada&#39; |
| <b>Posición de destino de inicio</b> <i>Float2</i> | Posición en la imagen utilizada para seleccionar el vértice de inicio.<br>Para cada ruta de acceso, se selecciona el vértice más cercano o más alejado de esta posición, de acuerdo con el <b>modo de inicio de ruta de acceso</b> seleccionado.<br><i>Nota:</i> Este parámetro está disponible cuando <b>modo de inicio de ruta de acceso</b> está establecido en &quot;vértice más cercano a una posición especificada&quot; o &quot;vértice más alejado de una posición especificada&quot; |
| <b>Función de inicio</b> <i>Flotador</i> | Función utilizada para seleccionar el vértice de inicio. Devuelve un valor de tipo Float.<br>Para cada vértice, se ejecuta la función y se selecciona el vértice para el que la función devuelve el *resultado más alto*.<br>Variables disponibles:<br>*-* vertex.cornerness(Flotante)*:* La puntuación del vértice como candidato para ser un vértice <br>*-* vertex.pos(Flotante2)*:* La posición del vértice en el espacio de imagen<br><i>Nota:</i> Este parámetro está disponible cuando el modo de inicio de ruta está establecido en &#39;Vértice más cercano a una posición especificada&#39; o &#39;Función de inicio personalizada&#39; |
| <b>Modo de pedido</b> <i>Entero</i> | El método para ordenar los trazados generados.<br>El cuadro delimitador *de los trazados de posición o tamaño* (Cuadro B) se puede usar como criterio para ordenar los trazados.<br>Esto tiene un impacto significativo al convertir los <b>trazados en splines</b> generados mediante el nodo dedicado, ya que varios nodos spline utilizan el orden de las splines.<br>*- Heredado (rápido):* El método utilizado en la versión anterior de este nodo, que ofrece un rendimiento significativamente mejor <br>*- Por la posición del centro de Box en la dirección:* Los trazados se ordenan según la posición de este nodo el centro de su caja, desde el primero hasta el último a lo largo de la dirección especificada <br>*- Por caja de caja de caja de caja de bolsa posición superior izquierda a lo largo de la dirección:* Los trazados se ordenan según la posición de la esquina superior izquierda de su caja de caja, desde el primero hasta el último a lo largo de la dirección especificada <br>*- Por tamaño de caja - De mayor a menor:* Los trazados se ordenan según el tamaño de su caja de bolsa, de mayor a menor <br>*- Por tamaño de caja - De menor a mayor:* trazados de menor a mayor <br>*: función de ordenación personalizada:* Usar una función personalizada para ordenar rutas |
| <b>Dirección del pedido</b> <i>Flotador</i> | Ángulo que describe la dirección utilizada para ordenar los trazados de primero a último en esa dirección.<br>El valor es un *número de vueltas* que se usa para girar un vector de dirección X-izquierda. Esto significa que 0 establece un vector de dirección de (-1, 0) y 0,25 (90 grados) establece un vector de dirección de (0, 1). |
| <b>Función de ordenación</b> <i>Flotador</i> | Función utilizada para ordenar los trazados. Devuelve un valor de tipo Float.<br>Las rutas de acceso se ordenan en *orden ascendente* según el valor de esta función. En otras palabras, el resultado de la función para cada ruta de acceso es la *clave de ordenación* utilizada para ordenar las rutas de acceso.<br>Variables disponibles:<br>* box.center (Flotante2): La posición del center<br>* box.topleft del cuadro de ruta (Flotante2): Posición del cuadro de ruta de acceso de la esquina superior izquierda<br>* bbox.size (Flotante2): El tamaño del cuadro Trayectoria (X: anchura, Y: height) |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/mask-to-paths-02.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/mask-to-paths-03.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/mask-to-paths-04.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/mask-to-paths-05.jpg" alt="MaskToPaths-Variant1-After">
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

![Ejemplo de nodo 2](mask-to-paths.resources/mask-to-paths-06.gif "Ejemplo de nodo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](mask-to-paths.resources/mask-to-paths-07.gif "Ejemplo de nodo 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 3: Modos de inicio](mask-to-paths.resources/mask-to-paths-08.gif "Ejemplo de nodo 3: Modos de inicio"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 3: Modos de ordenación](mask-to-paths.resources/mask-to-paths-09.gif "Ejemplo de nodo 3: Modos de pedido"){zoomable="yes"}

</td>
</tr>
</table>
