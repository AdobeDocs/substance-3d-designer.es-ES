---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación cuádruple para aplicar transformaciones cuadrilaterales a las texturas para la corrección y deformación de la perspectiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación cuádruple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---


# Transformación cuádruple

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/quad-transform-grayscale.png){width="128px"}

![](../../../../../../assets/quad-transform.png){width="128px"}

## Transformación cuádruple (escala de grises)

**En:** *Filtros/Transformaciones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo de transformación especial que permite la transformación de una forma cuádruple a través de la interacción con sus puntos de vértice. Permite transformaciones muy específicas de forma práctica.

## Parámetros

* **p00**: Punto superior izquierdo.
* **p01**: Punto inferior izquierdo
* **p10**: Punto superior derecho.
* **p1**: Punto inferior derecho.
* **Sacrificio**: *Solo frente, Solo espalda, Delante sobre atrás, Reverso sobre frente* Establece el sacrificio/ocultamiento de la forma cuando los puntos se crucen entre sí.
* **Habilitar Mosaico**: *Falso/Verdadero*
* **Color de fondo**: *(Valor de escala de grises)*Color de fondo sólido si el mosaico está desactivado.
* **Muestreo**: *Bilineal, Más cercana* Establece la calidad del muestreo.

## Imágenes de ejemplo

![](../../../../../../assets/quad-example.gif)

</td>
</tr>
</table>
