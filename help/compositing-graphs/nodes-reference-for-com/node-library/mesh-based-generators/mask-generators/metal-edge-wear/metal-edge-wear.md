---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Edge Wear de metal para generar máscaras de desgaste en bordes metálicos en función de la curvatura y posición de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de metal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Edge Wear de metal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-edge-wear.png){width="128px"}

## Edge Wear de metal

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el desgaste de los bordes en un objeto de metal, con arañazos y astillas que aparecen en bordes elevados convexos, potencialmente enmascarados por áreas oscuras de AO horneadas.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Entrada de Suciedad**: *Entrada en escala de grises*
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Normal del Espacio Mundial**: *Entrada de color*
* **Posición**: *Entrada de color*

### Parámetros

* **Nivel de desgaste**: *0.0 - 1.0* Define la cantidad total de desgaste, y se revela gradualmente.
* **Contraste de desgaste**: *0.0 - 1.0* Establece el contraste del resultado final.
* **Smoothness de bordes**: *0.0 - 16.0* Establece el smoothness de la difuminación desde los bordes de la Curvatura.
* **Cantidad de Suciedades**: *0.0 - 1.0* Define la cantidad de suciedad que se debe fusionar entre los bordes.
* **Escala de Suciedad**: *1 - 16* Establece la escala de la Suciedad.
* **Enmascaramiento de Oclusión ambiental**: *0.0 - 1.0* Define la cantidad de efecto que tiene el AO en el efecto final, enmascarando las áreas oscuras.
* **Peso de curvatura**: *0.0 - 1.0* Define la cantidad de efecto que tienen los bordes convexos de la curvatura en el efecto final.
* **Usar Suciedad personalizada**: *Falso/Verdadero* Habilita una ranura de entrada de mapa de Suciedad personalizado.
* **Usar triplanar**: *False/True* Habilita la proyección [Tri Planar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) para ocultar las costuras.
* **Contraste de fusión triplanar**: *0.0 - 1.0* Define el contraste de fusión para la proyección triplanar.

## Imágenes de ejemplo

![](../../../../../../assets/metal-edge-wear-ex.gif)

</td>
</tr>
</table>
