---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/luminosity-blend-node.html"
breadcrumb-title: ''
description: Utilice el nodo Mezcla de luminosidad para fusionar texturas basadas en valores de luminosidad para crear efectos compuestos basados en el brillo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Luminosity (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luminosidad (nodo de Fusión)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6507710c6005db383ba88ce9e5c6ad9c34d87c9f
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# Luminosidad (nodo de Fusión)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<b>En:</b> Filtros > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza un modo de fusión Luminosidad, que conserva el tono y la crominancia del fondo, al tiempo que adopta la luminancia del primer plano.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Primer plano</b> <i>Entrada de color</i> |  |
| <b>Fondo</b> <i>Entrada de color</i> |  |
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo. |
| <b>Fusión alfa</b> <i>Falso/Verdadero</i> | Alterna la fusión de los canales alfa Primer plano y Fondo. Si se establece en False, se omite el canal alfa del primer plano. |
