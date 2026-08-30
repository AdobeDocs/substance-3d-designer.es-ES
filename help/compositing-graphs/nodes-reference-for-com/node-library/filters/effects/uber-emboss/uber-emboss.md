---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Utilice el nodo Relieve de Uber para crear efectos de relieve avanzados con controles de profundidad, ángulo e iluminación personalizables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Relieve de Uber
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# Relieve de Uber

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](uber-emboss.resources/uber-emboss.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Versión avanzada con muchas características de [Relieve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Realiza un elaborado efecto de iluminación falso en 2D basado en un mapa de altura.

Resulta útil a la hora de crear iluminación integrada para determinados estilos de texturizado cuando se necesita mucho control.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Color</b> <i>Entrada de color</i> | Imagen base para modificar. |
| <b>Height</b> <i>Entrada en escala de grises</i> | Se utiliza el mapa de altura como controlador del efecto. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Color de ambiente</b> <i>(Valor de color)</i> | Color utilizado en áreas sombreadas. |
| <b>Color de Difuso</b> <i>(Valor de color)</i> | Color utilizado en áreas iluminadas. |
| <b>Color de Specular</b> <i>(Valor de color)</i> | Color utilizado para los reflejos del specular |
| <b>Intensidad de luz</b> <i>0.0 - 1.0</i> | Intensidad de la luz (fingida). |
| <b>Ángulo claro</b> <i>0.0 - 1.0</i> | Ángulo de incidencia de la luz (falsificada) |
| <b>Intensidad del Specular</b> <i>0.0 - 1.0</i> | Intensidad de los reflejos del specular. |
| <b>Brillo de Specular</b> <i>0.0 - 1.0</i> | Tamaño del resaltado del specular. |
| <b>Rugosidad de Difuso</b> <i>0.0 - 1.0</i> | Rugosidad utilizada para calcular la iluminación difusa. |
| <b>Opacidad de sombras</b> <i>0.0 - 1.0</i> | Opacidad de fusión de las áreas sombreadas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="uber-emboss.resources/uberemboss-ex.png" />
        </td>
    </tr>
</table>
