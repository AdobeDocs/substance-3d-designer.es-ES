---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz para generar máscaras basadas en las condiciones de iluminación de la malla para crear variaciones de materiales realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# Luz

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

## Luz

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara es un poco diferente de otros generadores: se limita a hacer una iluminación falsa, basada en el World Space Normalmap, que devuelve una máscara de &quot;mapa de luz&quot; en blanco y negro.

## Parámetros

* **Ángulo horizontal**: *0.0 - 1.0* Establece el ángulo horizontal de la luz falsa.
* **Ángulo vertical**: *0.0 - 1.0* Establece el ángulo vertical de la luz falsa.
* **Resaltar brillo**: *0.0 - 0.999* Establece la extensión de difuminación del área resaltada.
* **Nivel de resaltado**: *0.0 - 1.0* Establece el nivel de brillo del área resaltada.

## Imágenes de ejemplo

![](../../../../../../assets/light-ex.gif)

</td>
</tr>
</table>
