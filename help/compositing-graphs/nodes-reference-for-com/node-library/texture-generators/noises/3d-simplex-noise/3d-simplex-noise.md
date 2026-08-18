---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: Utilice el nodo Ruido simple 3D para generar patrones de ruido simple 3D para crear texturas volumétricas suaves y de aspecto natural.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido simple en 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Ruido simple en 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## Ruido simple en 3D

**En:** *Generadores De Texturas**/Ruidos*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera un ruido de procedimiento cuando se conecta un mapa de posición al horno en la ranura de entrada. Está diseñado para su uso únicamente con el motor de GPU.\
Similar a [Ruido 3D Perlin](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), pero más rápido y sencillo, para los casos en los que el rendimiento y la velocidad importan.

Este ruido se puede probar con [Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) como entrada en lugar de un mapa con bake real (como se muestra en la imagen de ejemplo siguiente).

## Parámetros

* **Escala**: *0.0 - 64.0*\
  Establezca la escala global del efecto.
* **Tamaño**: *0.0 - 2.0* Realice escalas no uniformes en los ejes X, Y y Z por separado.

## Imágenes de ejemplo

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>
