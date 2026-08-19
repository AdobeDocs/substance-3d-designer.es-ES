---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Utilice el nodo Normal a Height para convertir las asignaciones normales en asignaciones de height para extraer información de profundidad de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal al Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Normal al Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

## Normal al Height

**En:** *Filtros/Mapa Normal*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo de conversión inversa que intenta volver a convertir un mapa normal de espacio tangente en un mapa de altura. Esta es la versión un poco más simple; [Normal a Height HQ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) tiene más opciones.

Útil para cuando sólo tiene un origen Normalmap, pero aún desea realizar operaciones combinándolo con un mapa de altura. Tenga en cuenta que esto nunca podrá proporcionar un resultado 100% correcto, ya que la información se pierde por la naturaleza del proceso cuando el Height se convierte a Normal. Si ajusta la configuración en consecuencia, esta versión que no es HQ realiza un trabajo decente de conversión de detalles simples.

## Parámetros

* **Equilibrio de Relieve**: *0.0 - 1.0* Ajusta hasta qué punto las diferentes frecuencias influyen en el resultado final. Esto depende en gran medida del mapa de entrada y requiere un poco de ajuste.
* **Formato normal**: *DirectX, OpenGL*\
  Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).
* **Opacidad global**: *0.0 - 1.0* Ajusta la opacidad global del efecto.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2heightex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
