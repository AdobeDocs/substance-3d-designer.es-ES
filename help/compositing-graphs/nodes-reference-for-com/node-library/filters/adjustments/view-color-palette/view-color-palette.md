---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: Utilice el nodo Ver paleta de colores para visualizar los datos de la paleta de colores extraídos de texturas para su análisis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ver paleta de colores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---


# Ver paleta de colores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Cuantificar color](view-color-palette.resources/ViewColorPalette.png "Icono Cuantificar color"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Empaqueta una paleta de colores en un cuadrado o rectángulo para visualizarla más fácilmente en la vista de gráficos o la vista 2D.\
El empaquetado tiene por objeto dejar el menor número posible de espacios vacíos.

</td>
</tr>
</table>

Se mantiene el orden de los colores en la paleta, con los colores que fluyen de izquierda a derecha y de arriba abajo de forma similar al ajuste de texto.

Este nodo se puede utilizar para visualizar las paletas producidas por los siguientes nodos: [Cuantificar color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Crear paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Modificar paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Paleta</b> <i>Color</i> PRINCIPAL | Una lista ordenada de colores de RGB codificados como una fila de píxeles. La paleta puede contener un máximo de 256 colores.   Esta es la paleta que el nodo empaqueta y procesa. |
| <b>Cantidad de color de paleta</b> <i>Entero</i> | Cantidad de colores almacenados en la paleta.   Si ese número no coincide con la cantidad real de colores en la entrada de imagen de la &#39;Paleta&#39;, la visualización puede estar incompleta o tener más espacios en blanco de los absolutamente necesarios. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Color</i> | La visualización de la paleta empaquetada. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ver paleta de colores: Ejemplo 1](view-color-palette.resources/view_color_palette_example_1.png "Ver paleta de colores: Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ver paleta de colores: Ejemplo 2](view-color-palette.resources/view_color_palette_example_2.png "Ver paleta de colores: Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ver paleta de colores: Ejemplo 3](view-color-palette.resources/view_color_palette_example_3.png "Ver paleta de colores: Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ver paleta de colores: Ejemplo 4](view-color-palette.resources/view_color_palette_example_4.png "Ver paleta de colores: Ejemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
