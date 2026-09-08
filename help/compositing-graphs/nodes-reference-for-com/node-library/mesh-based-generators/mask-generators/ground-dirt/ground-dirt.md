---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: Utilice el nodo Dirt de tierra para generar máscaras de acumulación de dirt basadas en la posición y orientación de la malla en relación con el suelo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt de tierra
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 6%

---


# Dirt de tierra

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el dirt acumulado desde cero, lo contrario de [De abajo arriba](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md) o [Dust](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md). No tiene anulación de mapa personalizada.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Posición</b> <i>Entrada en escala de grises</i> | Mapa de posición hecho un bake en el que basar el efecto. ¡Obligatorio! |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel</b> <i>0.0 - 1.0</i> | Define el nivel de apariencia total del dirt. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. |
| <b>Height de Dirt</b> <i>0.0 - 1.0</i> | Define el height (proporcionalmente) en el que debe aparecer el dirt. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/ground-dirt-ex.gif" />
        </td>
    </tr>
</table>
