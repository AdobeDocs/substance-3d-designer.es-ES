---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: Utilice el nodo Height a unidades de mundo normales para convertir mapas de height a mapas normales utilizando la escala de unidades de mundo para obtener detalles precisos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height a Unidades Mundiales Normales
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# Height a Unidades Mundiales Normales

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-to-normal-world-units.resources/normal-hq.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de conversión de Height a normal avanzado que utiliza unidades del mundo real durante la conversión.

Útil para cuando conozca las dimensiones de Heightmap de origen y desee realizar la conversión más precisa, como cuando se trabaja con material digitalizado.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Tamaño de superficie (cm)</b> <i>0.0 - 1000.0</i> | Dimension de la entrada Heightmap. |
| <b>Profundidad de Height (cm)</b> <i>0.0 - 100.0</i> | Profundidad máxima de los detalles del mapa de altura. |
| <b>Formato normal</b> <i>OpenGL, DirectX</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Muestreo</b> <i>Estándar, Sobel</i> | Cambia entre dos modos de muestreo para determinar la precisión. |
