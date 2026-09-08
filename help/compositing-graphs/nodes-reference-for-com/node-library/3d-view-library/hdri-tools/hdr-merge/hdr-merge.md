---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: Utilice el nodo Combinación HDR para combinar varias imágenes HDR en un único panorama para crear mapas de entorno compuestos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinación HDR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# Combinación HDR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hdr-merge.png){width="200px"}

<b>En:</b> Vista 3D > Herramientas HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Combina varias exposiciones fotográficas para crear una imagen de Alto rango dinámico. La primera entrada es la imagen más subexpuesta.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-16</b> <i>Entrada de color</i> | Introduce imágenes. La cantidad disponible depende del parámetro. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Entradas</b> <i>2 - 16</i> | Define la cantidad de entradas disponibles. |
| <b>Delta de exposición (VE)</b> <i>0.0 - 4.0</i> | Define la diferencia de exposición que se debe interpretar entre imágenes. |
| <b>Punto blanco</b> <i>0.0 - 13.0</i> | Definir punto blanco para realizar algún ajuste en el resultado final. |
