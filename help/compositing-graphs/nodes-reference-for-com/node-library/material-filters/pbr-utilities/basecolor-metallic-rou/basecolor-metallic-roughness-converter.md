---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: Utilice el nodo Convertidor de rugosidad metálica BaseColor para realizar conversiones entre distintos formatos de material PBR y flujos de trabajo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Convertidor de rugosidad Metálico BaseColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Convertidor BaseColor / Metálico / Rugosidad

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-convert.png){width="128px"}

## Convertidor BaseColor / Metálico / Rugosidad

**En:** *Utilidades de filtros de materiales/PBR*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo convierte los mapas Basecolor, Metálico y de Rugosidad a diferentes salidas de modelo PBR, como el modelo Specular/Brillo. Algunos de los destinos de salida incluidos son motores de procesamiento conocidos, como Vray, Corona, Redshift, Renderman y Arnold.

Esto es útil si tienes gráficos o materiales que se hacen con un modelo de PBR, mientras que tu objetivo requiere un modelo diferente.

## Parámetros

* **Usar entrada SpecularLevel**: *False/True* Expone una ranura de entrada adicional a la entrada SpecularLevel. Esto también se tiene en cuenta durante la conversión.
* ***Destino**: *PBR Diffuse/Specular/Gloss, Vray (GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4 (AiStandard), Arnold 4 (AlSurface), RenderMan (PxrSurface)**Define el modelo de destino de conversión.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
