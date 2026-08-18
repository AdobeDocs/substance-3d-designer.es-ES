---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación vectorial para transformar texturas entre dos entradas mediante campos vectoriales para transiciones suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación vectorial
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# Transformación vectorial

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

## Transformación vectorial (escala de grises)

**En:** *Filtros/Efectos*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Distorsiona una imagen de entrada por un mapa vectorial. El efecto es similar al de la distorsión UV con un mapa normal o el uso de un &quot;mapa de flujo&quot; en los sombreadores de videojuegos. Los píxeles de entrada se mueven por los vectores definidos en los valores Rojo y Verde del mapa vectorial.

Este nodo en sí no es el más difícil de usar, pero la creación de un mapa de vectores adecuado se hace cargo. Le recomendamos que trabaje con las profundidades de bits más altas para garantizar la precisión al realizar la transformación.

La transformación vectorial es muy similar a [Deformación vectorial](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md): la principal diferencia es que este nodo de transformación no &quot;repite&quot; ni &quot;segmenta&quot; el resultado cuando se coloca fuera de los límites del lienzo. En su lugar, se sujeta y repite los bordes.

## Parámetros

### Entradas

* **Entrada**: *Entrada en color/escala de grises* Entrada de origen que debe ser el destino de la deformación.
* **Campo vectorial**: *Entrada de color* El mapa de vectores utilizado para controlar la deformación.

### Parámetros

* **Importe**: *0.0 - 1.0* Define la intensidad del efecto de deformación y funciona como un multiplicador para el mapa de vectores.

## Imágenes de ejemplo

</td>
</tr>
</table>
