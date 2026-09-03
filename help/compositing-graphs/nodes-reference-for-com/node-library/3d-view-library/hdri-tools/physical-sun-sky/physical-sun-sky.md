---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: Utilice el nodo Físico de SunSky para generar entornos de iluminación de sol y cielo físicamente precisos para una previsualización realista del material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CieloSolFísico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# Sol/Cielo físico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](physical-sun-sky.resources/physical-sun-sky-01.png){width="200px"}

<b>En:</b> Vista 3D > Herramientas HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Implementación física de Sol y Cielo basada en el modelo de claraboya Hosek-Wikie. Proporciona una base excelente para un HDRI artificial.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Posición Sun</b> | intervalo = [0,1]x[0,1] (ángulos de longitud-latitud) |
| <b>Turbidez</b> <i>1.0 - 10.0</i> | La turbidez varía de 1 a 10 |
| <b>Albedo</b> <i>0.0 - 1.0</i> | El albedo va de 0 a 1. |
| <b>Color de tierra</b> <i>(Valor de color)</i> | Color del plano de tierra. |
| <b>Exposición (VE)</b> <i>-1.0 - 4.0</i> | Valor de exposición del resultado. |
| <b>Tamaño del sol</b> <i>0.0 - 4.0</i> | Escala del Sol, cualquier valor diferente a 1 no es físicamente correcto. ¡El valor tiene efectos sutiles! |
| <b>Intensidad del sol</b> <i>0.0 - 1.0</i> | Intensidad del disco solar. El disco Sun es bastante pequeño, por lo que el efecto no se ve inmediatamente. |
| <b>Intensidad del cielo</b> <i>0.0 - 1.0</i> | Intensidad del cielo. También afecta la llamarada del sol en el cielo, no el disco en sí. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="physical-sun-sky.resources/physical-sun-sky-02.gif" />
        </td>
    </tr>
</table>
