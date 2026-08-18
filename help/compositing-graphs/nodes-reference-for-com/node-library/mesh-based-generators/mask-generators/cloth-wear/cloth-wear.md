---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Desgaste de tela para generar máscaras de desgaste en superficies de tela en función de la curvatura de la malla y las áreas de contacto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de tela
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# Desgaste de tela

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cloth-wear.png){width="128px"}

## Desgaste de tela

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

La máscara representa los bordes rasgados sobre los materiales de tela. Utiliza un detalle de tela Heightmap que determina la mayor parte del look; sin un mapa adecuado, el efecto parece muy básico.

## Parámetros

### Entradas

* **Height de tela**: *Entrada en escala de grises*\
  Height solo para el patrón de tela. Este no es el height de su objeto (horneado), sino más bien un patrón de detalle de azulejos.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Curvatura**: *Entrada en escala de grises*\
  Curvatura horneada/generada para determinar bordes elevados.

### Parámetros

* **Cantidad de bordes definidos**: *0.0 - 1.0*
* **Suavizado de desgaste**: *0.0 - 5.0* Determina lo difuminados o suaves que están los bordes desgastados.

## Imágenes de ejemplo

![](../../../../../../assets/cloth-wear-ex.gif)

</td>
</tr>
</table>
