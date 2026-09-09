---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-range.html"
breadcrumb-title: ''
description: Utilice el nodo Rango de histograma para reasignar valores de textura basados en rangos de histograma para la corrección y los ajustes de color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rango de histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# Rango de histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-range.resources/histogram-range-1.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Reducir o mover el rango de una entrada de escala de grises. Se puede usar para reasignar transiciones, de forma similar a [Luminosidad de contraste](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md), pero con diferentes controles que podrían tener más sentido en algunas situaciones.\
Consulte también [Análisis de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) para ver otra forma más útil de reasignar el rango.

[Haga clic aquí para ver un vídeo de la Academia de Substance sobre el Rango de histograma.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=517s)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intervalo</b> <i>0.0 - 1.0</i> | Cuánto hay que reducir el rango desde. Esto es similar a mover los reguladores de los niveles mínimo y máximo hacia dentro. |
| <b>Posición</b> <i>0.0 - 1.0</i> | Desplazamiento para la reducción del rango, estableciendo un punto medio diferente para la reducción del rango. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-range.resources/histogram-range.gif" />
        </td>
    </tr>
</table>
