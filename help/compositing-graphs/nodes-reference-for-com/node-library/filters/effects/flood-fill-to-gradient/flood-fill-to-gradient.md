---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: Utilice el nodo Flood Fill a degradado para rellenar regiones con valores de degradado para crear transiciones de color suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill a degradado
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# Flood Fill a degradado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-gradient.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Transforma una base de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) en degradados (orientados aleatoriamente). Muy útil para crear un mapa de altura en el que los azulejos se inclinan y se inclinan aleatoriamente.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Entrada de color</i> | Datos de Flood Fill base. |
| <b>Entrada de ángulo</b> <i>Entrada en escala de grises</i> | Mapa opcional para determinar el ángulo por celda con un mapa externo. |
| <b>Entrada de Pendiente</b> <i>Entrada en escala de grises</i> | Mapa opcional para determinar la intensidad de pendiente del degradado por celda. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ángulo</b> <i>0.0 - 1.0</i> | Establece un ángulo/dirección uniforme y global para todos los mosaicos. |
| <b>Variación de ángulo</b> <i>0.0 - 1.0</i> | Aleatoriza el ángulo de cada azulejo individualmente. ¡Este es el parámetro más útil y poderoso! |
| <b>Multiplicar por tamaño de cuadro delimitador</b> <i>0.0 - 1.0</i> | Ajusta todo el efecto lineal en función del tamaño del cuadro delimitador individual del azulejo. Esto significa que los azulejos más pequeños terminarán siendo más oscuros que los más grandes. |
| <b>Multiplicador de entrada de imagen angular</b> <i>0.0 - 1.0</i> | Definir la influencia del mapa de entrada de ángulo opcional en las direcciones de degradado generadas |
| <b>Multiplicador de entrada de imagen de Pendiente</b> <i>0.0 - 1.0</i> | Definir la influencia del mapa de entrada de Pendiente opcional en la intensidad de pendiente de degradado generada. |
| <b>Multiplicar por intensidad de Pendiente</b> <i>0.0 - 1.0</i> |  |
| <b>Color de Pendiente plana</b> <i>(valor de escala de grises)</i> | Permite ajustar el valor sólido de las pendientes planas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/floodgradient-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/floodgradient-ex1.png" />
        </td>
    </tr>
</table>
