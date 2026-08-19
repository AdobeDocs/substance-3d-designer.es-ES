---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Utilice el nodo Grasa para generar máscaras de acumulación de grasa basadas en la geometría de malla y las áreas de contacto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grasa
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# Grasa

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## Grasa

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara está diseñada específicamente para las caras de los personajes y otras áreas específicas. Genera un tipo de máscara de grasa de piel en áreas de bajo thickness.

## Parámetros

### Entradas

* **Thickness**: *Entrada en escala de grises*\
  Mapa de Thickness al horno en el que se basa todo el efecto. ¡Obligatorio!
* **Ruido**: *Entrada en escala de grises*\
  Mapa de ruido opcional para anular la suciedad de grasa.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define la cantidad total de efecto que debe aparecer.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Umbral de Thickness**: *0.0 - 1.0* Establece un thickness mínimo para que el efecto aparezca. Igual de importante que Level; retoca esto para que se ajuste a tu mapa de Thickness.
* **Anular ruido**: *Falso/Verdadero* Establecer para invalidar el mapa interno de suciedades de grasa con ranura de entrada personalizada.

## Imágenes de ejemplo

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>
