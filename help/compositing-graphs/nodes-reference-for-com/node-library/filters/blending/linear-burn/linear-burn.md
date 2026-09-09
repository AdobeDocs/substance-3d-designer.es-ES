---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/linear-burn.html"
breadcrumb-title: ''
description: Utilice el nodo Subexponer lineal para fusionar texturas mediante el modo de subexposición lineal para crear efectos de sombreado y contraste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Linear Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Subexposición lineal
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---


# Subexposición lineal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](linear-burn.resources/linear-burn.png){width="128px"}

<b>En:</b> Filtros > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza una mezcla de Linear Burn. La fórmula matemática es Primer plano + Fondo - 1.

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
