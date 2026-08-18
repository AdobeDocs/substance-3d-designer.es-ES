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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Height Normal Blender

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

## Height Normal Blender

**En:** *Filtros/Mapa Normal*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo de acceso directo que fusiona un mapa de altura en escala de grises en un mapa normal. La entrada de Height se convierte a un mapa normal internamente y, a continuación, se fusiona correctamente con la entrada normal.

Esta es una forma más rápida de fusionar detalles que hacerlo manualmente con nodos separados, pero es posible que le falte control y perfeccionamiento para ciertas necesidades.

## Parámetros

### Entradas

* **Height**: *Entrada en escala de grises*\
  Mapa de altura en escala de grises con el que fusionarse.
* **Normal**: *Entrada de color*\
  Base Normalmap para fusionar.

### Parámetros

* **Intensidad normal**: *0.0 - 16.0* Intensidad de la conversión normal de la entrada de Height.
* **Formato normal**: *DirectX, OpenGL*\
  Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
