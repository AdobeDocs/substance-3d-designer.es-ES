---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Utilice el nodo Resplandor de forma para añadir efectos de resplandor a formas y texturas para crear efectos visuales luminosos y atmosféricos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Resplandor de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Resplandor de forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## Resplandor de forma (escala de grises)

**En:** *Filtros/Efectos*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Crea un resplandor suave alrededor de una máscara de entrada (para la versión de escala de grises) o una forma con un canal alfa (para la versión de color). En comparación con [Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md), esto funciona de una forma más similar a otro software de edición de imágenes 2D, ya que es un efecto más completo con más controles.

## Parámetros

* **Modo**: *Suave, Preciso* Cambia entre dos modos de precisión.
* **Ancho**: *-1.0 - 1.0* Controla hasta dónde llega el brillo.
* **Difusión**: *0.0 - 1.0* Límite / umbral para el efecto de desenfoque, hace que el resplandor parezca sólido cerca de la forma.
* **Opacidad**: *0.0 - 1.0*\
  Opacidad de fusión para el efecto resplandor.
* **(Sombra) Color**: *(Valor de color)*Matiz de color que se aplica al resplandor.
* **Color de máscara**: *(Valor de color) *(Solo versión de escala de grises)**Color sólido que se va a utilizar para la salida de transparencia asignada.
* **La Entrada Está Premultiplicada**: *False/True *(Solo versión de color)**Si la entrada debe asumirse como premultiplicada.
* **Salida de premultiplicación**: *Falso/Verdadero* Especifica si el resultado debe premultiplicarse.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
