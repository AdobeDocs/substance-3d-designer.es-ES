---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: Utilice el nodo Deformación multidireccional para aplicar efectos de deformación en varias direcciones para crear patrones de distorsión complejos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deformación multidireccional
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---


# Deformación multidireccional

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-directional-warp-color.png)![](../../../../../../assets/multi-directional-warp-grayscalepng.png)

## Deformación multidireccional (escala de grises)

**En:** *Filtros/Efectos*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Deformación multidireccional aplica [Deformación direccional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) varias veces en direcciones opuestas mientras la textura desplazada permanece en su lugar. Se diferencia del estándar Deformación direccional en que puede empujar en varias direcciones, mientras que la versión atómica solo permite una. De este modo, se soluciona el problema clásico de deformación direccional, que siempre parece alejar demasiado la imagen en una sola dirección; en su lugar, funciona en varias direcciones o ejes en lugar de en una sola dirección.

Se diferencia principalmente de [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) en que es ligeramente más limitado: la dirección de la deformación sólo se controla mediante parámetros y no se puede establecer mediante un mapa de entrada. La ventaja es que es ligeramente más fácil de usar y puede ser más preciso dependiendo de su caso de uso.

## Parámetros

### Entradas

* **Entrada**: *Entrada de escala de grises/color*\
  Mapa base al que se aplicará la deformación. Puede ser en color o en escala de grises.
* **Entrada de intensidad**: *Entrada en escala de grises*\
  El mapa de máscara obligatorio que controla la intensidad del efecto de deformación debe ser de escala de grises.

### Parámetros

* **Intensidad**: *0.0 - 20.0*\
  Define la intensidad del efecto de deformación y la distancia que se deben expulsar los píxeles.
* **Ángulo de deformación**: *0.0 - 1.0*\
  Define el ángulo o la dirección en la que se aplica el efecto Deformar.
* **Modo**: *Promedio, Máx., Mín., Cadena*\
  Define el modo de fusión para pasadas consecutivas. Solo tiene efecto si Directions es 2 o 4!
* **Direcciones**: *1, 2, 4* Define el número de ejes que funciona la deformación. 1 significa que se mueve en la dirección del Ángulo, y el opuesto de esa dirección, 2 significa el eje del ángulo, más el eje perpendicular, 4 significa los ejes anteriores, más 45 inclemencias de grados.

## Imágenes de ejemplo

</td>
</tr>
</table>
