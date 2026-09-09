---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión normal para fusionar mapas de normales y crear transiciones suaves entre detalles de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# Fusión normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-blend.resources/normal-blend.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

La Fusión normal le permite fusionar dos mapas normales con una máscara opcional, al tiempo que se asegura de que todos los valores permanecen normalizados. No difiere mucho de un [nodo de Fusión atómica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), pero ha agregado cálculos internos para los mapas normales.

La Fusión normal no está pensada para combinar (superponer) los mapas normales, donde el mapa superior añade detalles al mapa inferior. Para ello, usa [Combinación normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md) en su lugar.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>NormalFG</b> <i>Entrada de color</i> | Mapa normal frontal/superior. |
| <b>NormalBG</b> <i>Entrada de color</i> | Fondo/Mapa normal inferior. |
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Usar máscara&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Usar máscara</b> <i>Falso/Verdadero</i> | Activa o desactiva el uso del mapa de máscara. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-blend.resources/normalblend-ex.gif" /><br><i>(el formato .gif introduce el tramado en el ejemplo, los resultados en la aplicación son suaves)</i>
        </td>
    </tr>
</table>
