---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Utilice el nodo Resplandor para añadir efectos de resplandor a las texturas para crear apariencias de materiales luminosos y emisores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Resplandor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# Resplandor

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

## Resplandor

**En:** *Filtros/Efectos*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza un efecto del tipo &quot;Resplandor externo&quot;, como se ve en otros programas conocidos de edición de imágenes. Básicamente, añade un contorno de degradado atenuado alrededor de la entrada.

Tenga en cuenta que esto no está destinado a funcionar para imágenes con canales Alpha, como cabría esperar. Incluso la versión en color solo espera máscaras binarias, negras y blancas como entrada; solo permite utilizar un resplandor de color. Si busca una versión que funcione en imágenes con transparencia, consulte [Resplandor de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utilice &quot;Resplandor&quot; para las entradas de color o &quot;Escala de grises&quot; para las entradas de escala de grises.

## Parámetros

* **Cantidad de brillo**: *0.0 - 1.0* Opacidad global para el efecto de resplandor.
* **Borrar cantidad**: *0.0 - 1.0* Umbral para cortar el efecto de resplandor. Útil para áreas semitransparentes.
* **Tamaño de resplandor**: *0.0 - 20.0* Controla hasta dónde llega el efecto de brillo.
* **Color de brillo**: *(Valor de color) (Solo versión de color)*Establece el color del efecto de resplandor.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/glow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
