---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: Utilice el nodo Umbral para convertir las texturas de escala de grises a blanco y negro en función de un valor de umbral para crear máscaras.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Umbral
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 5%

---


# Umbral

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](threshold.resources/threshold-2.png){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Devuelve blanco si se cumplen los *criterios de comparación* establecidos en el parámetro **Mode** para el valor de píxel de entrada en relación con el valor **Threshold**.\
Similar a [Análisis de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), pero con contraste siempre en el nivel máximo. Sirve como una forma más precisa y rápida de obtener resultados similares a la exploración por histograma.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Umbral</b> <i>0.0 - 1.0</i> | Valor de luminancia con el que se compara el valor del píxel de entrada. |
| <b>Modo</b> | Criterio según el cual se debe comparar el valor de píxel de entrada con el valor **Umbral**:<br><br>- *Mayor*<br>- *Mayor o igual*<br>- *Inferior*<br>- *Inferior o igual* |
