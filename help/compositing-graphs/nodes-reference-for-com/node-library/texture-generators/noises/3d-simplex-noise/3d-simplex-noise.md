---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ""
description: Utilice el nodo Ruido simple 3D para generar patrones de ruido simple 3D para crear texturas volumétricas suaves y de aspecto natural.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido simple en 3D
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%
---

# Ruido simple en 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-simplex-noise.resources/3d-simplex-noise.png){width="128px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera un ruido de procedimiento cuando se conecta un mapa de posición al horno en la ranura de entrada. Está diseñado para su uso únicamente con el motor de GPU.\
Similar a [Ruido 3D Perlin](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), pero más rápido y sencillo, para los casos en los que el rendimiento y la velocidad importan.

Este ruido se puede probar con [Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) como entrada en lugar de un mapa con bake real (como se muestra en la imagen de ejemplo siguiente).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>0.0 - 64.0</i> | Establezca la escala global del efecto. |
| <b>Tamaño</b> <i>0.0 - 2.0</i> | Realice escalas no uniformes en los ejes X, Y y Z por separado. |

## Ejemplos

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="3d-simplex-noise.resources/3d-simplex.gif" class="modal-image" alt="Ruido simple en 3D - Ejemplo 1" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>
