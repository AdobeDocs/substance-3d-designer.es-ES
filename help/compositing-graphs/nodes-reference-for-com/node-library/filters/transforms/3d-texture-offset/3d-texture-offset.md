---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/3d-texture-offset.html"
breadcrumb-title: ''
description: Utilice el nodo Desplazamiento de Textura 3D para desplazar texturas en el espacio 3D y crear efectos de paralaje y variaciones de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > 3D Texture Offset
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desplazamiento de textura 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Desplazamiento de textura 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3dtextureoffsetgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3dtextureoffsetcolor.png){width="200px"}

</td>
</tr>
</table>

<b>En:</b> Filtro > Transformación

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo **Desplazamiento de Textura 3D** aplica una *transformación de desplazamiento* en los ejes **X**, **Y** y **Z** en un objeto descrito por la *textura 3D* conectada a la **Entrada**.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Escala de grises/Color</i> | La <i>textura 3D</i> que describe un objeto 3D.<br>El objeto se describe normalmente en un <i>cubo de unidades</i>. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Desplazamiento</b> <i>Float3</i> | Cantidad de desplazamiento en <i>espacio de entorno</i> aplicado en el objeto descrito por la <i>textura 3D</i> conectada a <b>Input</b>. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3dtextureoffset-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3dtextureoffset-node.png" />
        </td>
    </tr>
</table>
