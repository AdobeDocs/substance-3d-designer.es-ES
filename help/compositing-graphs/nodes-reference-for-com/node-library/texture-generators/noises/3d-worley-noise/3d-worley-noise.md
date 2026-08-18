---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Utilice el nodo Ruido de trabajo 3D para generar ruido de trabajo basado en la posición 3D para crear efectos de textura volumétrica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido Worley 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Ruido Worley 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

## Ruido Worley 3D

**En:** *Generadores De Texturas**/Ruidos*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Uno de los ruidos más versátiles y avanzados de la biblioteca, genera un ruido Worley en el espacio 3D, basado en un mapa de posición de entrada. Tiene muchas opciones que lo hacen mucho más potente que los ruidos basados en [Celdas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) o [Distancia](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md) estándar.

## Parámetros

* **Escala**: *1 - 64*\
  Establezca la escala global del efecto.
* **Tamaño**: *0.0 - 1.0* Realice escalas no uniformes en los ejes X, Y y Z por separado.
* **Modo**: *Euclidean, Manhattan, Chebyshev, Minkowski\
  Cambie la métrica de distancia. Permite algunos tipos de ruido muy diferentes.*
* **Número de Minkowski**: *0.0 - 20.0* Solo con la métrica de distancia de Minkowski. Fusiona diferentes tipos de métricas.
* **Estilo**: *F1, F2, F2-F1, Borde, Color aleatorio* Establecer la combinación de métricas matemática. Permite muchas más combinaciones.
* **Ancho de borde**: *0.0 - 1.0* Cuando la matemática de combinación de bordes está activa, controla el ancho del borde.
* **Redondez**: *0.0 - 1.0* Solo disponible con los modos F1, F2 y F2-F1. Establece la posición intermedia del nivel.
* **Invertir**: *Falso/Verdadero*\
  Invierte el resultado.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/3d-worley-ex04.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/3d-worley-ex03.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/3d-worley-ex02.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/3d-worley-ex01.png" width="256px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |

</td>
</tr>
</table>
