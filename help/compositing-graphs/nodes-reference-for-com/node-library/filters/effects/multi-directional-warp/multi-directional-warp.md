---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: Utilice el nodo Deformación direccional múltiple para aplicar efectos de deformación en varias direcciones para crear patrones de distorsión complejos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deformación multidireccional
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 3%

---


# Deformación multidireccional

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-directional-warp.resources/multi-directional-warp-01.png)![](multi-directional-warp.resources/multi-directional-warp-02.png)

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Multi-Deformación direccional aplica [Deformación direccional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) varias veces en direcciones opuestas mientras la textura desplazada permanece en su lugar. Se diferencia de la Deformación direccional estándar en que puede empujar en múltiples direcciones, mientras que la versión atómica solo permite una. De esta manera se resuelve el problema clásico donde la Deformación direccional siempre parece empujar la imagen demasiado lejos en una sola dirección, en lugar de trabajar a lo largo de múltiples direcciones o ejes en lugar de una sola dirección.

Se diferencia principalmente de [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) en que es ligeramente más limitado: la dirección de la deformación sólo se controla mediante parámetros y no se puede establecer mediante un mapa de entrada. La ventaja es que es ligeramente más fácil de usar y puede ser más preciso dependiendo de su caso de uso.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada de color/escala de grises</i> | Mapa base al que se aplicará la deformación. Puede ser en color o en escala de grises. |
| <b>Entrada de intensidad</b> <i>Entrada en escala de grises</i> | El mapa de máscara obligatorio que controla la intensidad del efecto de deformación debe ser de escala de grises. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 20.0</i> | Define la intensidad del efecto de deformación y la distancia que se deben expulsar los píxeles. |
| <b>Ángulo de deformación</b> <i>0.0 - 1.0</i> | Define el ángulo o la dirección en la que se aplica el efecto Deformar. |
| <b>Modo</b> <i>Promedio, Máx., Mín., Cadena</i> | Define el modo de Fusión para pasadas consecutivas. Solo tiene efecto si Directions es 2 o 4! |
| <b>Direcciones</b> <i>1, 2, 4</i> | Define el número de ejes que funciona la deformación. 1 significa que se mueve en la dirección del Ángulo, y el opuesto de esa dirección, 2 significa el eje del ángulo, más el eje perpendicular, 4 significa los ejes anteriores, más 45 inclemencias de grados. |
