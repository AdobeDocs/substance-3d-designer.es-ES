---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# Convertidor BaseColor / Metálico / Rugosidad

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-convert.png){width="128px"}

<b>En:</b> Filtros de material > Utilidades de PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo convierte los mapas Basecolor, Metálico y de Rugosidad a diferentes salidas de modelo PBR, como el modelo Specular/Brillo. Algunos de los destinos de salida incluidos son motores de procesamiento conocidos, como Vray, Corona, Redshift, Renderman y Arnold.

Esto es útil si tienes gráficos o materiales que se hacen con un modelo de PBR, mientras que tu objetivo requiere un modelo diferente.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Usar entrada SpecularLevel</b> <i>Falso/Verdadero</i> | Expone una ranura de entrada adicional a la entrada SpecularLevel. Esto también se tiene en cuenta durante la conversión. |
| <b>Destino</b> <i>PBR Difuso/Specular/Gloss, Vray (GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4 (AiStandard), Arnold 4 (AlSurface), RenderMan (PxrSurface)</i> | Establece el modelo de destino de conversión. |
