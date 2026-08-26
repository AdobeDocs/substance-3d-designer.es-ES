---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/modify-color-palette.html"
breadcrumb-title: ''
description: Utilice el nodo Modificar paleta de colores para ajustar y transformar paletas de colores extraídas de texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Modify Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modificar paleta de colores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---


# Modificar paleta de colores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Cuantificar color](../../../../../../assets/ModifyColorPalette.png "Icono Cuantificar color"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Modifica los colores de una paleta ordenada y los aplica a una imagen mediante un mapa de ID.

Los colores se pueden seleccionar haciendo coincidir los índices del mapa de ID con los índices de colores de la paleta.

Por ejemplo, el color #2 de la paleta se aplicará a todos los píxeles del mapa de ID con un valor de ID de 2.

Este nodo se puede utilizar en combinación con los siguientes nodos: [Cuantificar color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Crear paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Aplicar paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Ver paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Conectores de salida

</td>
<td style="border: 0;" valign="top">

### Parámetros

</td>
</tr>
</table>

## Conectores de entrada

|  |  |
| --- | --- |
| <b>ID</b> *Escala de grises* PRINCIPAL | Mapa de ID de entrada utilizado para seleccionar colores, con el fin de modificarlos y distribuirlos en la salida.   Un mapa de ID es una imagen en la que los píxeles que forman parte de un todo (por ejemplo, una forma) tienen el mismo valor de identificación único. En este caso, el valor es un entero.   Se puede generar una asignación de ID usando un nodo [Quantize Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md). |
| <b>Paleta</b> *Color* | Una lista ordenada de colores de RGB codificados como una fila de píxeles. La paleta puede contener un máximo de 256 colores. Esta es la paleta que modifica el nodo.   Las paletas se pueden producir con los nodos [Quantize Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) o [Create Color Palette](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md). |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Color* | El resultado de asignar los colores de la paleta modificada a los índices del mapa de ID. |
| <b>Paleta</b> *Color* | La paleta actualizada con las modificaciones de color especificadas aplicadas.   La paleta se puede aplicar a otra imagen con el nodo [Apply Color Palette](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md) o visualizarse con el nodo [View Color Palette](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md). |

## Parámetros

|  |  |
| --- | --- |
| <b>Modo de selección de color</b> *Entero* | Método de selección del color de destino en la paleta que se debe modificar:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Índice de color:</b> Índice del color de destino</li> <li data-preserve-html="true"><b>Espacio de imagen:</b> Posición en el mapa de ID donde se debe muestrear el índice. Cuando se selecciona este modo, un gizmo de posición está disponible en la vista 2D para facilitar la selección</li> </ul> |
| <b>Posición de color</b> *Float2* *Disponible cuando &#39;Modo de selección de color&#39; está establecido en &#39;Espacio de imagen&#39;* | Posición en el mapa de ID donde se debe muestrear el índice.   Utilice el gizmo de la vista 2D para seleccionar fácilmente una ubicación en la imagen.   Sugerencia: Puede mostrar la imagen cuantificada de la que se extrae el mapa de ID y, a continuación, seleccionar el nodo Modificar paleta de colores para mostrar el gizmo. Esto hace que la selección de un color para modificarlo sea más intuitiva. |
| <b>Índice de color</b> *Entero* *Disponible cuando &#39;Modo de selección de color&#39; está establecido en &#39;Índice de color&#39;* | Índice del color de destino.   Los colores de la paleta se ordenan de izquierda a derecha y el índice del primer color es 0. |
| <b>Difusión de selección de color</b> *Flotador* | Controla hasta dónde llega la selección a los colores vecinos.   Los colores se organizan en un *cubo* cuyo ancho, height y profundidad son un degradado en el que cada componente de un color aumenta de 0 a 1 (p. ej. rojo, verde y azul en RGB).   Este parámetro ajusta la distancia alrededor del color seleccionado en el cubo donde otros colores también se pueden modificar, donde 1 es la anchura total del cubo. |
| <b>Contraste de selección de color</b> *Flotador* | Controla el degradado de difuminación de la selección sobre los colores vecinos.   Los colores se organizan en un *cubo* cuya anchura, height y profundidad son un degradado en el que un componente de un color aumenta de 0 a 1 (p. ej. rojo, verde y azul en RGB).   Este parámetro ajusta el difuminado de la selección sobre otros colores del cubo alrededor del color seleccionado, donde 0 es un degradado suave desde el color seleccionado hasta el más lejano y 1 es un límite desde completamente incluido hasta no incluido. |
| <b>Espacio de color de distancia</b> *Entero* | Los colores se organizan en un *cubo* cuya anchura, height y profundidad son un degradado en el que un componente de un color aumenta de 0 a 1 (p. ej. rojo, verde y azul en RGB).   Este parámetro le permite seleccionar el espacio de color utilizado para distribuir colores en el cubo, lo que cambia los colores contiguos.   Puede seleccionar el espacio de color que se ajuste a su caso de uso:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Laboratorio (color):</b> Un espacio de color perceptual estandarizado, que distribuye los colores de tal manera que los colores que &#39;parecen&#39; cercanos están realmente cerca en el cubo. Esto es adecuado para imágenes que pueden visualizarse en pantallas.</li> <li data-preserve-html="true"><b>RGB (Datos):</b> El color se divide en rojo, verde y azul y se distribuye directamente a lo largo de esos ejes, sin tener en cuenta la percepción humana. Esto es adecuado para imágenes que contienen datos sin procesar, como mapas normales.</li> </ul> |
| <b>Modo</b> *Entero* | Método de modificación del color de destino:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Anular color:</b> reemplaza el color por otro</li> <li data-preserve-html="true"><b>HSL:</b> ajusta el color con los desplazamientos de tono, saturación y luminosidad</li> </ul> |
| <b>Opacidad</b> *Flotador* | Controla la interpolación entre los colores original y modificado, donde 1 significa que el color modificado reemplaza por completo al color original. |
| <b>Anular color</b> *Float3* *Disponible cuando &#39;Mode&#39; está establecido en &#39;Override color&#39;* | Especifica el color que debe sustituir al color original. |
| <b>HSL</b> *Float3* *Disponible cuando &#39;Mode&#39; está establecido en &#39;HSL&#39;* | Controla los desplazamientos de tono, saturación y luminosidad aplicados al color original. |

## Ejemplos

![Modificar paleta de colores: Ejemplo 1](../../../../../../assets/modify_color_palette_example_1.png "Modificar la paleta de colores: Ejemplo 1"){zoomable="yes"}

![Modificar paleta de colores: Ejemplo 2](../../../../../../assets/modify_color_palette_example_3.png "Modificar la paleta de colores: Ejemplo 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_before.jpg" alt="modify_color_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_after.jpg" alt="modify_color_example_2_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>
