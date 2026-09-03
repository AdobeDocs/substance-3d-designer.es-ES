---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Utilice el nodo Cancelación de AO para eliminar la oclusión ambiental de los materiales escaneados para el procesamiento de texturas limpias.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cancelación de AO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# Cancelación de AO

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ao-cancellation.resources/ao-cancellation-01.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo intenta eliminar cualquier información de iluminación de Oclusión ambiental del mapa de Albedo (Color base), basándose en una entrada de mapa de AO independiente. Se puede utilizar para garantizar que la información de tu Albedo sea correcta para la PBR y que, en su mayoría, carezca de información de iluminación (fuerte).

Nodo útil para cuando se tiene un mapa de AO hecho un bake de una malla escaneada o, alternativamente, incluso un mapa de AO generado a partir de información de Height o normal.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cancelación de AO</b> <i>0.0 - 1.0</i> | Intensidad con la que se elimina la información de iluminación. |
| <b>Saturación de AO</b> <i>0.0 - 1.0</i> | Compensación de (des)saturación para las áreas en las que se elimina la iluminación. Se puede utilizar para devolver cualquier pérdida de color en áreas más oscuras. |
