---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/create-color-palette-16.html"
breadcrumb-title: ''
description: Utilice el nodo Crear paleta de colores para extraer una paleta de 16 colores de texturas para efectos estilizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Create Color Palette (16)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crear paleta de colores (16)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# Crear paleta de colores (16)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Cuantificar color](create-color-palette-16.resources/CreateColorPalette16.png "Icono Cuantificar color"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Crea una lista ordenada de colores y la emite como una paleta, con un máximo de 16 colores.

El nodo puede anexar nuevos colores a una paleta existente, utilizando el conjunto de entradas &quot;Paleta&quot;.

Este nodo se puede utilizar en combinación con los siguientes nodos: [Cuantificar color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Aplicar paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Modificar paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Ver paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Paleta</b> <i>Color</i> PRINCIPAL | Una lista ordenada de colores de RGB codificados como una fila de píxeles. La paleta puede contener un máximo de 256 colores.   Esta entrada es opcional. Si se utiliza, los colores configurados por el nodo se anexan a esta paleta.   La paleta se puede visualizar con el nodo [View Color Palette](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md). |
| <b>Cantidad de color de paleta</b> <i>Entero</i> | Cantidad de colores almacenados en la paleta.   Si ese número no coincide con la cantidad real de colores en la entrada de imagen de la &#39;Paleta&#39;, la visualización puede estar incompleta o tener más espacios en blanco de los absolutamente necesarios. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Paleta</b> <i>Color</i> | La paleta actualizada con los colores especificados anexados. |
| <b>Cantidad de color de paleta</b> <i>Entero</i> | Cantidad actualizada de colores almacenados en la paleta, con la cantidad especificada de colores añadidos. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad de color</b> *Entero* | Cantidad de colores que se deben añadir a la paleta. |
| <b>Color #</b> *Float3* *Tantos parámetros disponibles como el valor &#39;Cantidad de color&#39;* | Un color que debe añadirse a la paleta.   Los colores se añaden a la paleta en el mismo orden que esta lista numerada. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Crear paleta de colores: Ejemplo 1](create-color-palette-16.resources/create_color_palette_example_1.png "Crear paleta de colores: Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Crear paleta de colores: Ejemplo 2](create-color-palette-16.resources/create_color_palette_example_2.png "Crear paleta de colores: Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

![Crear paleta de colores: Ejemplo 3](create-color-palette-16.resources/create_color_palette_example_3.png "Crear paleta de colores: Ejemplo 3"){zoomable="yes"}
