---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Utilice el nodo Reemplazar rango de color para reemplazar los colores de un rango especificado por colores nuevos para la corrección de color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Reemplazar rango de color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# Reemplazar rango de color

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](replace-color-range.resources/replace-color-range-01.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Reemplaza Color de origen por Color de destino, con controles adicionales. Por ejemplo, se puede utilizar para cambiar el color de partes de un mapa de ID de material (hacer un bake).

Para obtener una versión más avanzada, vea [Coincidencia de color.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Color de origen</b> <i>(Valor de color)</i> | Color que reemplazar. |
| <b>Color de destino</b> <i>(Valor de color)</i> | Color con el que reemplazar. |
| <b>Intervalo de origen</b> <i>0.0 - 1.0</i> | Rango o tolerancia del origen seleccionado. Se puede aumentar para que los colores contiguos también cambien de tono. |
| <b>Umbral</b> <i>0.0 - 1.0</i> | Difuminación/contraste para el rango. Establezca bajo para reemplazar solo el color de origen, o más alto para reemplazar también los colores que se fusionan en origen. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="replace-color-range.resources/replace-color-range-02.png" />
        </td>
    </tr>
</table>
