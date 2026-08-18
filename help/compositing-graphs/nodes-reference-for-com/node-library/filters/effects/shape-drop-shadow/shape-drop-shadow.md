---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Utilice el nodo Sombra paralela de formas para agregar efectos de sombra paralela a formas para crear profundidad y dimensión en texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombra paralela de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Sombra paralela de forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

## Sombra paralela de forma (escala de grises)

**En:** *Filtros/Efectos*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza el conocido efecto &quot;Sombra paralela&quot; de otro software de procesamiento de imágenes 2D, sobre una máscara de entrada en blanco y negro (para la versión de escala de grises) o una imagen con transparencia (para la versión de color).

Difiere del efecto [Sombras](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) en que devuelve imágenes con transparencia total aplicada, lo que hace que el efecto sea más completo y similar al que esperarías de otro software.

## Parámetros

* **Ángulo**: *0.0 - 1.0*&#x200B;Ángulo de incidencia de la luz (falsa).
* **Distancia**: *-0.5 - 0.5* Distancia entre la sombra y/o la forma.
* **Tamaño**: *0.0 - 1.0* Controla el desenfoque/difuminado de la sombra.
* **Difusión**: *0.0 - 1.0* Límite/umbral para el efecto de desenfoque, hace que la sombra se extienda aún más.
* **Opacidad**: *0.0 - 1.0*\
  Opacidad de fusión para el efecto de sombra.
* **(Sombra) Color**: *(Valor de color)*Matiz de color que se aplicará a la sombra.
* **Color de máscara**: *(Valor de color) *(Solo versión de escala de grises)**Color sólido que se va a utilizar para la salida de transparencia asignada.
* **La Entrada Está Premultiplicada**: *False/True *(Solo versión de color)**Si la entrada debe asumirse como premultiplicada.
* **Salida de premultiplicación**: *Falso/Verdadero* Especifica si el resultado debe premultiplicarse.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/dropshadowex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
