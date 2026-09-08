---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: Utilice el nodo de fusión Subexposición de color para oscurecer las texturas aumentando el contraste para crear efectos de sombras y subexposición.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Subexposición de color
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---


# Subexposición de color

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-burn.png){width="128px"}

<b>En:</b> Filtros > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza una fusión de Subexponer color entre Primer plano y Fondo. Matemáticamente la fórmula es 1 - (1-Fondo) / Primer plano.

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
