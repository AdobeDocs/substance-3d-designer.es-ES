---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
breadcrumb-title: ''
description: Utilice el nodo Blanqueamiento solar para generar máscaras basadas en la exposición solar y crear efectos descoloridos y blanqueados por el sol realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Sun Bleach
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blanqueador solar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Blanqueador solar

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/sun-bleach.png){width="128px"}

## Blanqueador solar

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara es similar a [Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md), pero también es compatible con el AO, lo que da lugar a una máscara que representa un blanqueamiento suave y un desvanecimiento en la parte superior de un efecto.

## Entradas

* **Espacio normal**: *Entrada de color*
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

## Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define la cantidad total de blanqueamiento y desplaza el efecto hacia abajo.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Oclusión**: *0.0 - 1.0* Establece la influencia del AO en el resultado final.

## Imágenes de ejemplo

![](../../../../../../assets/sun-bleach-ex.gif)

</td>
</tr>
</table>
