---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ""
description: Utilice el nodo Desenfocar para aplicar efectos de desenfoque a las texturas para suavizar los detalles y crear efectos de enfoque suave.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desenfocar
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 6%
---

# Desenfocar

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Icono de nodo de desenfoque](blur.resources/blur-9.png)

**En:** nodos atómicos

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo de desenfoque realiza una operación de desenfoque de cuadro: calcular el promedio de los valores de píxeles en una distancia establecida, lo que da como resultado un aspecto borroso y nítido. Proporciona la operación de desenfoque más simple, rápida y básica disponible en [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html).

Aunque el desenfoque funciona bien para operaciones rápidas y sencillas, como suavizar ligeramente algunos bordes, en cualquier escenario más exigente, [Desenfocar HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) es una mejor opción, ya que compensa el rendimiento por la calidad.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="blur.resources/blur-tooltip.gif" alt="información sobre herramientas de desenfoque" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

## Parámetros

* **Intensidad**: 0-unlimited\
  Define la intensidad o la distancia del desenfoque. El número no está limitado, pero con valores altos toda la imagen se convierte en un color promedio.

En el ejemplo siguiente se muestra el desenfoque de este nodo a la izquierda, frente a [Desenfocar HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) a la derecha, cuando se usan valores altos (50 en este caso). Con valores de 1-2 aproximadamente, la diferencia no es apreciable.

| Desenfoque (atómico) | Desenfocar alta calidad |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-example.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-hq.png"/></div> |
