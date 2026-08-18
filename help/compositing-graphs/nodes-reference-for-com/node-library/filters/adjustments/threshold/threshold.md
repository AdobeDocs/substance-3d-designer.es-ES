---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: Utilice el nodo Umbral para convertir texturas en escala de grises a blanco y negro, según un valor de umbral para crear máscaras.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Umbral
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# Umbral

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## Umbral

**En:** *Filtros/Ajustes*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Devuelve blanco si se cumplen los *criterios de comparación* establecidos en el parámetro **Mode** para el valor de píxel de entrada en relación con el valor **Threshold**.\
Similar a [Análisis de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), pero con contraste siempre en el nivel máximo. Sirve como una forma más precisa y rápida de obtener resultados similares a la exploración por histograma.

### Parámetros

* **Umbral**: *0.0 - 1.0*\
  Valor de luminancia con el que se compara el valor del píxel de entrada.
* **Modo**:\
  Criterio según el cual se debe comparar el valor de píxel de entrada con el valor **Umbral**:
  * *Mayor*
  * *Mayor o igual que*
  * *Inferior*
  * *Inferior o igual*

## Imágenes de ejemplo

</td>
</tr>
</table>
