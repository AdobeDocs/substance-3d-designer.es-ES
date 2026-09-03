---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: Utilice el nodo Noise Upscale 1 para aumentar la escala de las texturas mediante algoritmos basados en ruido para conservar los detalles al aumentar la resolución de la textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Noise Upscale 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---


# Noise Upscale 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-1.resources/noise-upscale-1-01.png){width="128px"}

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza un procedimiento de ruido de entrada y lo escala a doble resolución, manteniendo el detalle pero sin introducir demasiadas baldosas. Utiliza un tipo de máscara &quot;X&quot; y se fusiona con contraste similar a la entrada original (el modo de fusión interno es Copiar).

Este nodo está destinado principalmente a optimizar gráficos lentos que utilizan ruidos grandes y pesados. Permite utilizar resoluciones más altas sin introducir demasiado tiempo de cálculo adicional.

Consulta [Noise Upscale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md) y [Noise Upscale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) para obtener diferentes variaciones de este proceso.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Desplazamiento1X</b> <i>0.0 - 1.0</i> | Desliza las partes superior e inferior sobre el eje X. |
| <b>Desplazamiento1Y</b> <i>0.0 - 1.0</i> | Desliza las partes superior e inferior sobre el eje Y. |
| <b>Desplazamiento2X</b> <i>0.0 - 1.0</i> | Desliza las partes izquierda y derecha sobre el eje X. |
| <b>Desplazamiento2Y</b> <i>0.0 - 1.0</i> | Desliza las partes izquierda y derecha sobre el eje Y. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-1.resources/noise-upscale-1-02.png" />
        </td>
    </tr>
</table>
