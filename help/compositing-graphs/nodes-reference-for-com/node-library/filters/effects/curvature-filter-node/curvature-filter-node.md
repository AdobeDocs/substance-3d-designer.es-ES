---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo Filtro de curvatura para generar mapas de curvatura a partir de mapas de altura para detectar superficies convexas y cóncavas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura (nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Curvatura (nodo de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza una conversión de curvatura de un solo paso simple y estricta para introducir [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). El mapa resultante tiene matices blancos para áreas convexas y negros para cóncavas. La curvatura siempre producirá líneas delgadas como píxeles y transiciones nítidas.

Este nodo es útil para realzar u oscurecer rápidamente determinados bordes. Está limitado en comparación con [Curvature Smooth](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (que produce resultados de mayor calidad) y [Curvature Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (que tiene más opciones).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 10.0</i> | Intensidad del efecto. Aumenta el contraste del resultado. |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/curvature-ex.png" />
        </td>
    </tr>
</table>
