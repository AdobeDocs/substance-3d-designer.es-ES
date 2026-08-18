---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Utilice el nodo Selección de borde para generar máscaras y seleccionar bordes de malla para crear efectos de desgaste y desgaste basados en bordes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selección de borde
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Selección de borde

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## Selección de borde

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara es la mejor forma de seleccionar cualquier tipo de borde en función de la curvatura. Convexo, cóncavo en cualquier nivel o contraste se puede aislar, lo que proporciona un excelente método abreviado para evitar hacerlo manualmente a través de un [nodo de niveles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para resaltar bordes. ¡Obligatorio!
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define la cantidad total de resaltado de bordes tanto para Convexo como para Cóncavo.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resaltado para Convexo y Cóncavo.
* **Convexo**
  * **Ancho de bordes convexos**: *0.0 - 1.0* Establece el ancho del resaltado para bordes convexos. Tenga en cuenta que un suavizado en aumento puede provocar bordes más finos.
  * **Suavizado convexo**: *0.0 - 1.0* Establezca la suavidad de la transición para los bordes convexos.
  * **Intensidad convexa**: *0.0 - 1.0* Establece la intensidad máxima del resaltado de bordes para bordes convexos. Establézcalo en 0 para que no se resalte.
* **Cóncavo**
  * **Ancho de bordes cóncavos**: *0.0 - 1.0* Establecer la anchura del resaltado para bordes cóncavos. Tenga en cuenta que un suavizado en aumento puede provocar bordes más finos.
  * **Suavizado cóncavo**: *0.0 - 1.0* Establezca la suavidad de la transición para los bordes cóncavos.
  * **Intensidad cóncava**: *0.0 - 1.0* Establezca la intensidad máxima del resaltado de bordes para bordes cóncavos. Establézcalo en 0 para que no se resalte.

## Imágenes de ejemplo

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>
