---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Utilice el nodo Sobel de curvatura para detectar bordes de curvatura mediante los operadores Sobel para crear máscaras basadas en bordes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel de curvatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# Sobel de curvatura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza una conversión de curvatura de un solo paso simple y estricta para introducir [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). El mapa resultante tiene matices blancos para áreas convexas y negros para cóncavas. La curvatura siempre produce líneas más gruesas y transiciones nítidas.

Este nodo es útil para resaltar u oscurecer rápidamente determinados bordes. Es ligeramente diferente de [Curvature](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), ya que produce resultados de mejor calidad, pero sigue siendo nítido y duro.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 1.0</i> | Intensidad del efecto, ajusta el contraste. |
| <b>Tipo normal</b> <i>DirectX, OpenGL</i> |  |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/curv-sobel-ex.png" />
        </td>
    </tr>
</table>
