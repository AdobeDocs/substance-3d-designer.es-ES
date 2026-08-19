---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Edge Wear para generar máscaras de desgaste en los bordes de malla para crear daños realistas en los bordes y efectos de intemperismo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## Edge Wear

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Este nodo representa el desgaste en los bordes del objeto. Tiene algunos parámetros, pero no es el más fácil de usar: te recomendamos que juegues y te hagas una idea de las cosas. El nodo es bastante poderoso, aunque no se puede hacer ninguna máscara de anulación personalizada.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define la extensión total del efecto.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Umbral**: *0.0 - 1.0* De forma similar a Nivel, establece la extensión total del efecto.
* **Ancho de bordes**: *0.0 - 1.0* Establece la totalidad del efecto de resaltado. Reduce para hacerlos más ligeros.
* **Trastorno**: *0.0 - 1.0*\
  Define la cantidad de ruido que se debe fusionar para romper el smoothness.

## Imágenes de ejemplo

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>
