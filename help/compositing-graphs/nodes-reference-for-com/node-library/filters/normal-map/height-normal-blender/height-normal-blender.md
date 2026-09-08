---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Utilice el nodo Mezclador normal de Height para fusionar mapas normales y de height para combinar información de detalle de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height Normal Blender
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Height Normal Blender

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de acceso directo que fusiona un mapa de altura en escala de grises en un mapa normal. La entrada de Height se convierte a un mapa normal internamente y, a continuación, se fusiona correctamente con la entrada normal.

Esta es una forma más rápida de fusionar detalles que hacerlo manualmente con nodos separados, pero es posible que le falte control y perfeccionamiento para ciertas necesidades.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height</b> <i>Entrada en escala de grises</i> | Mapa de altura en escala de grises con el que fusionarse. |
| <b>Normal</b> <i>Entrada de color</i> | Base Normalmap para fusionar. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad normal</b> <i>0.0 - 16.0</i> | Intensidad de la conversión normal de la entrada de Height. |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
