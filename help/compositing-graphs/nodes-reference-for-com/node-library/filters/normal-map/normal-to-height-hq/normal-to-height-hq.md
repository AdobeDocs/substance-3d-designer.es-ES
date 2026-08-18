---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Utilice el nodo HQ Normal a Height para convertir mapas normales en mapas de height de alta calidad para la extracción de detalles de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal Al Height HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# Normal Al Height HQ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height-hq.png){width="128px"}

## Normal Al Height HQ

**En:** *Filtros/Mapa Normal*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo de conversión inversa que intenta volver a convertir un mapa normal de espacio tangente en un mapa de altura. Este es el nodo más avanzado; [Normal al Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) tiene menos opciones y utiliza cálculos diferentes.

Útil para cuando sólo tiene un origen Normalmap, pero aún desea realizar operaciones combinándolo con un mapa de altura. Tenga en cuenta que esto nunca podrá proporcionar un resultado 100% correcto, ya que la información se pierde por la naturaleza del proceso cuando el Height se convierte a Normal. Nunca puede reemplazar un mapa de altura correctamente generado!

## Parámetros

* **Formato normal**: *DirectX, OpenGL*\
  Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).
* **Equilibrio de Relieve**: *0.0 - 1.0* Mezcla entre el sesgo de frecuencia baja y alta.
* **Intensidad de Height**: *0.0 - 1.0* Intensidad o multiplicador para el mapa de altura, funciona un poco como la opacidad global.
* **Normalizar Height**: *Falso/Verdadero* Ajusta automáticamente el rango de mapa de altura para usar contraste completo, como un [nivel automático](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md).
* **Calidad**: *Normal, Alta* Cambia entre velocidad y calidad.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2height-hq-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
