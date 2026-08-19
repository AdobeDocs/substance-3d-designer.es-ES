---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Usa el nodo Cancelación de AO para eliminar la oclusión ambiental de los materiales escaneados para el procesamiento de texturas limpias.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cancelación de AO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# Cancelación de AO

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## Cancelación de AO

**En:** *Procesamiento De Escaneo/Filtros De Materiales*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo intenta eliminar cualquier información de iluminación de Oclusión ambiental del mapa de Albedo (color base), basándose en una entrada de mapa de AO independiente. Se puede utilizar para garantizar que la información de tu Albedo sea correcta para la PBR y que, en su mayoría, carezca de información de iluminación (fuerte).

Un nodo útil para cuando se tiene un mapa de AO horneado de una malla escaneada o, alternativamente, incluso un mapa de AO generado a partir de información de Height o Normal.

## Parámetros

* **Cancelación de AO**: *0.0 - 1.0* Intensidad con la que se quita la información de iluminación.
* **Saturación de AO**: *0.0 - 1.0*(Dessaturación) compensación para áreas donde se elimina la iluminación. Se puede utilizar para devolver cualquier pérdida de color en áreas más oscuras.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
