---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo Filtro de clonación para duplicar y desplazar regiones de textura para crear patrones y efectos de mosaico perfectos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clonar (Nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Clonar (Nodo de filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

## Clonar

**En:** *Filtros/Transformaciones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Clona la imagen de entrada una vez en una ubicación especificada. Puede funcionar como una cruda herramienta de &quot;tampón de clonar&quot;.

Requiere un poco de cuidado para obtener los resultados esperados:

* Lo ideal es que la imagen de entrada tenga un canal alfa (como una pegatina), ya que la fusión es solo una copia recta.
* La máscara se establece de forma predeterminada en negro, por lo que, para ver los resultados, debe conectarse al menos un valor de escala de grises blanca uniforme.
* El desplazamiento se recortará fuera de la imagen fácilmente, por lo que debe utilizar valores pequeños.

## Parámetros

### Entradas

* **Origen**: *Entrada de color*\
  Imagen para clonar. Importante: lo ideal es que la imagen tenga un canal alfa.
* **Máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo. El valor predeterminado es negro.

### Parámetros

* **Desplazamiento**: *-*\
  Mueve o traduce el resultado. Positivo es Izquierda y Arriba, Negativo es Derecha y Abajo. Use valores pequeños, 1.0 y superior lo mueve fuera de la imagen.
* **Máscara de desenfoque**: *0,0 - 10,0\
  Aplicar un filtro de desenfoque a la máscara para suavizar los bordes.*

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/clone-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
