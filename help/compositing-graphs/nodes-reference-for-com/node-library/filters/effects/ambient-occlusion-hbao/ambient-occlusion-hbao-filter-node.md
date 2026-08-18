---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo de filtro HBAO de Oclusión ambiental para generar mapas de oclusión ambiental mediante algoritmos basados en horizonte para un sombreado realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oclusión ambiental (HBAO) (nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Oclusión ambiental (HBAO) (nodo de filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## Oclusión ambiental (HBAO)

**En:** *Filtros/Efectos*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Toma un mapa de altura como entrada y genera un mapa de Oclusión ambiente a partir de él. Utiliza la Oclusión Ambiental Basada en Horizonte, un algoritmo originalmente destinado a la generación de AO en tiempo real de espacio de pantalla. Muy útil para crear mapas de procedimientos AO a partir de mapas de altura de procedimientos.

Para obtener una versión alternativa más avanzada pero más lenta del AO, consulte [Oclusión ambiental (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

## Parámetros

* **Usar unidades del mundo**: *Falso/Verdadero* Cambia el uso de las unidades de espacio en el mundo o en la pantalla. Activa parámetros adicionales que permiten un control más preciso.
* **Profundidad de Height**: *0.0 - 1.0* Sólo se usa cuando World Units está establecido en False. Controla la escala global.
* **Tamaño de superficie**: **0.0 - 1000.0** Solo se usa cuando World Units está establecido en True. Controla la escala global.
* **Escala de Height (cm)**: *0.0 - 1000.0* Solo se usa cuando World Units está establecido en True. Controla la escala global.
* **Radio**: *0.0 - 1.0* Controla la propagación del AO.
* **Calidad**: *4 muestras, 8 muestras, 16 muestras*\
  Establece el nivel de calidad determinando la cantidad de muestras utilizadas para el cálculo.
* **Optimización de GPU**: *Falso/Verdadero* Habilita la optimización interna de la GPU y acelera el procesamiento.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
