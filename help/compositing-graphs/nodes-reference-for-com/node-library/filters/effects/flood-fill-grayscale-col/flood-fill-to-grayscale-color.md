---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Utilice el nodo Flood Fill a color de escala de grises para rellenar regiones conectadas con colores de escala de grises para crear motivos monocromos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill a GrayscaleColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Flood Fill a escala de grises/color

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-grayscale-color.resources/floodfill-to-grayscale.png){width="128px"}

![](flood-fill-to-grayscale-color.resources/floodfill-to-color.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Utiliza datos del Flood Fill para generar muestras de valores de escala de grises o de color. A diferencia de [Flood Fill a escala de grises aleatoria](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), estos dos nodos permiten un mayor control para establecer la variación y los tonos exactos, con un mapa de entrada adicional adicional para determinar el valor base que se debe aleatorizar según la celda.

Es un sistema potente para dar a cada célula un valor o color único, pero aún así retener el control y basarlo en una entrada predeterminada.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Entrada de color</i> |  |
| <b>Entrada de color/escala de grises</b> <i>Entrada de color/escala de grises</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ajuste de luminancia/color</b> <i>-1.0 - 1.0</i> | Defina el sesgo o el valor base del nodo. Cuando se utiliza una entrada de escala de grises o de color, se utiliza para cambiar ese valor inicial como punto de partida. |
| <b>Aleatorio de luminancia/color</b> <i>-1.0 - 1.0</i> | Establezca la cantidad de variación. |
