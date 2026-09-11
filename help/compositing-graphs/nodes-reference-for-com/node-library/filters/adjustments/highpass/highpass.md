---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/highpass.html"
breadcrumb-title: ''
description: Utilice el nodo Paso alto para extraer detalles de alta frecuencia de las texturas para crear efectos de enfoque y mejora de detalles.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paso alto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# Paso alto

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](highpass.resources/high-pass-greyscale.png){width="128px"}

![](highpass.resources/high-pass.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza un filtro de paso alto, disponible en color y en una versión en escala de grises. Similar a la acción Photoshop con el mismo nombre.\
Resulta útil para eliminar las grandes diferencias de luminancia en las imágenes, como cuando se limpian las texturas para embaldosado.

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utilice &quot;Paso alto&quot; para entradas de color y &quot;Escala de grises de paso alto&quot; para entradas de escala de grises.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Radio</b> <i>0.0 - 64.0</i> | Radio del filtro: un radio pequeño elimina pequeñas diferencias, un radio más grande elimina grandes áreas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="highpass.resources/highpass-example.png" />
        </td>
    </tr>
</table>
