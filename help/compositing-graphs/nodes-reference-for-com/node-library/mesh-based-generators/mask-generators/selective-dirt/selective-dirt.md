---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: Utilice el nodo Dirt selectivo para generar máscaras de acumulación de dirt selectivas basadas en la geometría de malla para lograr un intemperismo realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt selectivo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# Dirt selectivo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## Dirt selectivo

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) representa un simple efecto de dirt en bordes convexos.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Máscara de variación**: *Entrada en escala de grises*\
  Mapa de variación opcional, se puede activar a través de parámetros.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define el nivel total del efecto y lo revela gradualmente.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Variación**: *0.0 - 1.0* Define la cantidad de variación/suciedad que se mezclará en el efecto.
* **Omitir máscara de variación**: *Falso/Verdadero* Permite reemplazar la variación con una ranura de entrada personalizada.

## Imágenes de ejemplo

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>
