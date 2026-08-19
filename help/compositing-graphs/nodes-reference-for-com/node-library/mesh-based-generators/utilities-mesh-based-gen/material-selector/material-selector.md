---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Utilice el nodo Selector de material para seleccionar materiales en función de los datos de malla para crear efectos de textura de varios materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selector de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# Selector de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## Selector de material

**En:** *Generadores basados en malla**/Utilities*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Convierte un mapa de ID a todo color en una máscara binaria, en blanco y negro. Permite mezclar y combinar diferentes colores en una máscara.

Esto es útil si no quieres usar [Fusión de varios materiales](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) y prefieres usar la máscara manualmente o, alternativamente, si quieres usar manualmente esas mismas máscaras en otras ubicaciones.

## Parámetros

* **Materiales**: 1 - 16\
  Define el número de materiales para los que está activada la combinación.
* **Habilitar material #1-16**: False/True\
  Cambia la fusión y combinación de colores en la máscara de salida final. Se puede activar para todos los colores que desee combinar.
* **Material #1-16**: (Valor de color)\
  Selector de color para el color de los materiales que se convertirá a blanco y negro.
* **Parámetros del selector de color**\
  Modifica la fusión y conversión del color a blanco y negro.
  * **Rugosidad**: 0,01 - 1,0\
    Cuánto mezclar con los colores vecinos.
  * **Relleno**: 0,0 - 1,0\
    Nitidez de la transición, como Contraste.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
