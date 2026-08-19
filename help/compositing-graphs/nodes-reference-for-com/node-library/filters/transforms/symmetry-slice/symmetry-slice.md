---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Utilice el nodo Sector de simetría para dividir texturas a lo largo de los ejes de simetría para crear patrones y efectos reflejados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sector de simetría
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# Sector de simetría

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## Sector de simetría

**En:** *Filtros/Transformaciones*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo de operación de simetría/reflejo complejo. Permite una gran variedad de operaciones geométricas con control total, pero requiere cierta experimentación.

En comparación con [Mirror](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) y [Symmetry](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md), este nodo tiene muchas más opciones.

## Parámetros

* **Modo de simetría**: *0 - 6* Elegir geometría de simetría/línea espejo. Las opciones son Horizontal, Vertical, Diagonal izquierda-derecha, Diagonal derecha-izquierda, Invertir vertical, Esquina y Esquina diagonal.
* **Modo de transferencia**: *0 - 6\
  Modo de fusión. Las opciones son:*
* **Fusionar**: *0.0 - 1.0* Vuelve a mezclar la imagen original con el resultado.
* **Voltear lado**: *False/True* Voltea el origen, lo que significa que se invierte el lado de origen de la operación. La simetría de izquierda a derecha, por ejemplo, se convierte en derecha a izquierda.
* **Voltear lado2**: *Falso/Verdadero* Solo se usa cuando el modo de simetría es 5 o 6. Voltear origen de esquina.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
