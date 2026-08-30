---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
breadcrumb-title: ''
description: Utilice el nodo Sobel normal para generar mapas de normales a partir de mapas de altura mediante la detección de aristas Sobel para los detalles de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# Sobel normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-sobel.resources/normal-hq.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Convierte una entrada Heightmap en una salida Normalmap. Este nodo es una versión un poco más avanzada del [nodo atómico normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) y utiliza muestreo Sobel en lugar del método de muestreo estándar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 3.0</i> | Intensidad de las normales convertidas. |
| <b>Formato normal</b> <i>OpenGL, DirectX</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
