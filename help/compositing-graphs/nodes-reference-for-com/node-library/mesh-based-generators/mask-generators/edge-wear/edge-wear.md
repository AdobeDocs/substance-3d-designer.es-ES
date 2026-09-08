---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Edge Wear para generar máscaras de desgaste en los bordes de malla para crear daños realistas en los bordes y efectos de intemperismo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 7%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Este nodo representa el desgaste en los bordes del objeto. Tiene algunos parámetros, pero no es el más fácil de usar: te recomendamos que juegues y te hagas una idea de las cosas. El nodo es bastante poderoso, aunque no se puede hacer ninguna máscara de anulación personalizada.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel</b> <i>0.0 - 1.0</i> | Define la extensión total del efecto. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. |
| <b>Umbral</b> <i>0.0 - 1.0</i> | De forma similar a Nivel, establece la extensión total del efecto. |
| <b>Ancho de bordes</b> <i>0.0 - 1.0</i> | Define la plenitud del efecto de resaltado. Reduce para hacerlos más ligeros. |
| <b>Desorden</b> <i>0.0 - 1.0</i> | Define la cantidad de ruido que se debe fusionar para romper el smoothness. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-wear-ex.gif" />
        </td>
    </tr>
</table>
