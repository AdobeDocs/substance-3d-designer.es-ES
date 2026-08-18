---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Utilice el nodo Detección de bordes para detectar bordes en texturas para crear contornos y efectos de máscara basados en bordes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Detección de bordes
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# Detección de bordes

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

## Detección de bordes

**En:** *Filtros/Efectos*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Detecta el contraste en imágenes en blanco y negro y, a continuación, crea una máscara en blanco y negro que resalta el contraste.

Útil en muchos casos donde se necesita algún tipo de máscara para los bordes. Tenga en cuenta que funciona mejor con entradas de alto contraste; si es necesario, ajusta el contraste antes de pasar algo a este nodo.

## Parámetros

* **Ancho del borde**: *1.0 - 16.0* Anchura de las áreas detectadas alrededor de los bordes.
* **Redondez de borde**: *0.0 - 16.0* Redondea, desenfoca y suaviza la máscara generada.
* **Invertir**: *Falso/Verdadero*\
  Invierte el resultado.
* **Tolerancia**: *0.0 - 1.0* Factor de umbral de tolerancia para dónde deben aparecer los bordes.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/edge-detect-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
