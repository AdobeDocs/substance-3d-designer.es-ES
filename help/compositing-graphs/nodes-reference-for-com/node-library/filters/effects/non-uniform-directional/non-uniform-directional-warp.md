---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: Utilice el nodo Non Uniform Directional Warp para aplicar una deformación direccional no uniforme y crear efectos de distorsión variados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Non Uniform Directional Warp
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

## Dir. no uniforme Deformar (escala de grises)

**En:** *Filtros/Efectos*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Deformación de dirección no uniforme es una versión avanzada de [Deformación de dirección](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) que permite que la intensidad y la dirección de la deformación se controlen mediante una entrada de imagen. Permite mucho más control y puede crear una distorsión de imagen muy útil e interesante, en el mismo vano que [Desenfoque de Pendiente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

Se diferencia de [Deformación multidireccional](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) en que permite el control sobre el ángulo a través de una entrada de mapa personalizada, mientras que Deformación multidireccional solo permite que la dirección se controle a través de parámetros. Esto significa que puede crear efectos finales y curvos avanzados que de lo contrario no serían posibles.

## Parámetros

### Entradas

* **Entrada**: *Entrada en escala de grises*\
  Mapa base al que se aplicará la deformación.
* **Entrada de intensidad**: *Entrada en escala de grises*\
  El mapa de máscara obligatorio que controla la intensidad del efecto de deformación debe ser de escala de grises.
* **Entrada de ángulo de deformación**: *Entrada en escala de grises*\
  El mapa de máscara obligatorio que controla el ángulo del efecto de deformación debe ser de escala de grises.

### Parámetros

* **Intensidad**: *0.0 - 20.0*\
  Define la intensidad del efecto de deformación y la distancia que se deben expulsar los píxeles.
* **Ángulo de deformación**: *0.0 - 1.0*\
  Define el ángulo o la dirección en la que se aplica el efecto Deformar.
* **Multiplicador de entrada de ángulo de deformación**: *0.0 - 1.0*\
  Define el efecto del mapa de entrada de ángulo de deformación. El mapa de entrada de ángulo de deformación se utilizará para interpolar de 0 al valor de este parámetro.
* **Modo de seguimiento**: *Mín., Máx., Promedio*\
  Define cómo se mezclan los rastros.
* **Longitud del rastro**: *0.0 - 1.0*\
  Establece la longitud de los rastros.
* **Fundido de seguimiento**: *0.0 - 1.0*\
  Establece cuánto debe desaparecer cada pista
* **Curva de seguimiento**: *-1.0 - 1.0* Solo tiene efecto si el fundido de seguimiento no es 0. Define cómo se comporta el efecto de atenuación.

## Imágenes de ejemplo

</td>
</tr>
</table>
