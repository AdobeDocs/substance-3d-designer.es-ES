---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-damages.html"
breadcrumb-title: ''
description: Utilice el nodo Daños en los bordes para generar máscaras de daños en los bordes de la malla para crear efectos realistas de desgaste y rotura de los bordes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Damages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Daños en los bordes
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# Daños en los bordes

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-damages.png){width="128px"}

## Daños en los bordes

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el daño causado a los bordes elevados y convexos en función de la curvatura y el AO horneado.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para la colocación de efectos. ¡Obligatorio!
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para la colocación de efectos. ¡Obligatorio!
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Cantidad de daño de borde que se aplica.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Intensidad de daños**: *0.0 - 1.0* Cambia entre un aspecto desportillado y uniforme y un aspecto caótico, arañado y muy dañado.

## Imágenes de ejemplo

![](../../../../../../assets/edge-damages-ex.gif)

</td>
</tr>
</table>
