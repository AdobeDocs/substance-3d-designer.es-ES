---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: Utilice el nodo Dirt de borde para generar máscaras de acumulación de dirt en los bordes de malla para crear efectos de intemperismo de borde realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt Edge
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# Dirt Edge

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-dirt.png){width="128px"}

## Dirt Edge

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa un efecto de dirt que se acumula alrededor de los bordes, basándose únicamente en un mapa de curvatura.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para la colocación de efectos. ¡Obligatorio!
* **Máscara de variación**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo, solo se utiliza cuando está activado el parámetro override.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define la cantidad de dirt.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Variación**: *0.0 - 1.0* Se mezcla en la cantidad de enmascaramiento/separación a gran escala que debe ocurrir.
* **Omitir máscara de variación**: *Falso/Verdadero*

## Imágenes de ejemplo

![](../../../../../../assets/edge-dirt-ex.gif)

</td>
</tr>
</table>
