---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/liquid.html"
breadcrumb-title: ''
description: Utilice el nodo Líquido para generar patrones de líquidos y fluidos para crear agua, aceite y otros efectos en la superficie de fluidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Liquid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Líquido
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5a6c28b9acabf15714a1fd8bb4e7593192555fa2
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---


# Líquido

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](liquid.resources/liquid.png){width="128px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Esta es una variante simple de [Gaussian Noise](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), que [deforma](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) consigo misma para crear un efecto similar al de un líquido.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>1 - 128</i> | Establece la escala global del efecto. |
| <b>Desorden</b> <i>0.0 - 1.0</i> | Desplaza la fase del ruido para introducir una pequeña variación |
| <b>Intensidad de deformación</b> <i>0.0 - 1.0</i> | Define la intensidad del efecto de deformación. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="liquid.resources/liquid-ex.gif" />
        </td>
    </tr>
</table>
