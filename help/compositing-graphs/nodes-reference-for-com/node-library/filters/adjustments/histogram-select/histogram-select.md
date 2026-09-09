---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-select.html"
breadcrumb-title: ''
description: Utilice el nodo Selección de histograma para seleccionar y extraer rangos específicos de histogramas de texturas para ajustes específicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selección de histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---


# Selección de histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-select.resources/histogram-select.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

De forma similar a [Análisis de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), este efecto establece una posición de valor de escala de grises, con un rango alrededor del cual se desvanece. El contraste se puede ajustar para que el rango sea más nítido.

[Haz clic aquí para ver un vídeo de la Academia de Substance sobre la selección de histograma.](https://youtu.be/p9wcmJBFyGA?t=535)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Posición</b> <i>0.0 - 1.0</i> | Establece la posición central en la que se produce la selección del intervalo. |
| <b>Intervalo</b> <i>0.0 - 1.0</i> | Establece la anchura del intervalo de selección. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste/atenuación del resultado. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-select.resources/histoselect-ex.gif" />
        </td>
    </tr>
</table>
