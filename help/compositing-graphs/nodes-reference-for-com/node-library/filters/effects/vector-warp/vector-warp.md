---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: Utilice el nodo Deformación vectorial para deformar texturas mediante campos vectoriales para crear efectos de distorsión fluida y orgánica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deformación vectorial
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# Deformación vectorial

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-warp.resources/vector-warp-01.png){width="128px"}

![](vector-warp.resources/vector-warp-02.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

La deformación vectorial es un efecto de distorsión avanzado, similar a [Deformar](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) y [Deformación direccional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md), con la principal diferencia de que se basa en un mapa de bits vectorial (de color) en lugar de un mapa de escala de grises. Esto significa que es más potente y versátil que sus primos nodo atómico.

El mapa vectorial es similar a un mapa normal, pero no es necesario normalizarlo y solo se utilizan los canales R y verde (X e Y). Los canales azules y Alpha pueden dejarse en negro si lo desea. La construcción de un buen Mapa de Vectores puede ser el mayor desafío en el uso de este nodo; puede [convertir mapas en escala de grises a Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) o construir el mapa combinando canales con [Combinación RGBA.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) Como alternativa, también se puede usar algo como [&quot;Flow Map&quot;](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting).

Este nodo puede ser útil cuando se desea realizar distorsiones muy específicas con direcciones variables, donde los nodos de deformación estándar no lo cortan.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada de color</i> | Mapa para distorsionar. |
| <b>Mapa de vectores</b> <i>Entrada de color</i> | Mapa del controlador de distorsión. Se utilizan los canales de color rojo y azul. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 1.0</i> | Multiplicador de intensidad para el mapa vectorial. |
| <b>Formato de vector</b> <i>DirectX, OpenGL</i> | Cambia el canal Verde entre la interpretación Arriba y Abajo. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="vector-warp.resources/vector-warp-03.png" />
        </td>
    </tr>
</table>
