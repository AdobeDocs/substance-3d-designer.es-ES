---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: Utilice el nodo Dirt de tierra para generar máscaras de acumulación de dirt basadas en la posición y orientación de la malla en relación con el suelo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt de tierra
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Dirt de tierra

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

## Dirt de tierra

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el dirt acumulado desde cero, lo contrario de [De abajo arriba](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md) o [Dust](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md). No tiene anulación de mapa personalizada.

## Entradas

* **Posición**: *Entrada en escala de grises*\
  Mapa de posición al horno en el que basar el efecto. ¡Obligatorio!
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

## Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define el nivel de apariencia total del dirt.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Height de Dirt**: *0.0 - 1.0* Configura el height (proporcionalmente) en el que debe aparecer el dirt.

## Imágenes de ejemplo

![](../../../../../../assets/ground-dirt-ex.gif)

</td>
</tr>
</table>
