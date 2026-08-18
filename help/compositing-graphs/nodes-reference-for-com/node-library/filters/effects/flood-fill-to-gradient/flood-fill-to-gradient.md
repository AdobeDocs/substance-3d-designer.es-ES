---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: Utilice el nodo Flood Fill a degradado para rellenar regiones con valores de degradado para crear transiciones de color suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill a degradado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# Flood Fill a degradado

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-gradient.png){width="128px"}

## Flood Fill a degradado

**En:** *Filtros/Efectos*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Transforma una base de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) en degradados (orientados aleatoriamente). Muy útil para crear un mapa de altura en el que los azulejos se inclinan y se inclinan aleatoriamente.

## Parámetros

### Entradas

* **Flood Fill**: *Entrada de color* Datos de Flood Fill base.
* **Entrada de ángulo**: *Entrada en escala de grises*\
  Mapa opcional para determinar el ángulo por celda con un mapa externo.
* **Entrada de Pendiente**: *Entrada de escala de grises* Mapa opcional para determinar la intensidad de pendiente del degradado por celda.

### *Parámetros*

* **Ángulo**: *0.0 - 1.0* Establece un ángulo/dirección uniforme y global para todos los mosaicos.
* **Variación de ángulo**: *0.0 - 1.0* Aleatoriza el ángulo de cada mosaico individualmente. ¡Este es el parámetro más útil y poderoso!
* **Multiplicar por tamaño de cuadro delimitador**: *0.0 - 1.0* Ajusta todo el efecto lineal según el tamaño del cuadro delimitador individual del azulejo. Esto significa que los azulejos más pequeños terminarán siendo más oscuros que los más grandes.
* **Multiplicador de entrada de imagen angular**: *0.0 - 1.0* Establecer la influencia del mapa de entrada de ángulo opcional en las direcciones de degradado generadas
* **Multiplicador de entrada de imagen de Pendiente**: *0.0 - 1.0*\
  Definir la influencia del mapa de entrada de Pendiente opcional en la intensidad de pendiente de degradado generada.
* **Multiplicar por intensidad de Pendiente**: *0.0 - 1.0*
* **Color de Pendiente plana**: *(Valor de escala de grises)*Permite ajustar el valor sólido de las pendientes planas.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodgradient-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/floodgradient-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
