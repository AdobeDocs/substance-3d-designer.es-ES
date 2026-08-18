---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-notch.html"
breadcrumb-title: ''
description: Utilice el nodo Muesca de borde para generar patrones de muesca en los bordes de malla para crear daños de borde y efectos de sangría realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Notch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Muesca de borde
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Muesca de borde

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-notch.png){width="128px"}

## Muesca de borde

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa una máscara simple para bordes elevados, dividida por un ruido de alta frecuencia. Consulte [Dirt de bordes](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md) o [Daños de bordes](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md) para obtener más opciones.

## Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para resaltar bordes. ¡Obligatorio!
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

## Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define el nivel del efecto Muesca de borde.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.

## Imágenes de ejemplo

![](../../../../../../assets/edge-notch-ex.gif)

</td>
</tr>
</table>
