---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz para generar máscaras basadas en las condiciones de iluminación de la malla y crear variaciones de material realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# Luz

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara es un poco diferente de otros generadores: se limita a hacer una iluminación falsa, basada en el World Space Normalmap, que devuelve una máscara de &quot;mapa de luz&quot; en blanco y negro.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ángulo horizontal</b> <i>0.0 - 1.0</i> | Define el ángulo horizontal de la luz falsa. |
| <b>Ángulo vertical</b> <i>0.0 - 1.0</i> | Define el ángulo vertical de la luz falsa. |
| <b>Resaltar Brillo</b> <i>0.0 - 0.999</i> | Establece el pliego de atenuación del área resaltada. |
| <b>Nivel de resaltado</b> <i>0.0 - 1.0</i> | Define el nivel de brillo del área resaltada. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/light-ex.gif" />
        </td>
    </tr>
</table>
