---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Utilice el nodo Hald CLUT para aplicar tablas de consulta de color utilizando el formato Hald CLUT para la gradación y corrección de color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hald-clut.resources/hald-clut.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aplica una LUT a la imagen de entrada. La LUT debe estar en formato Hald con resolución 4096\*4096. Vea <http://www.quelsolaar.com/technology/clut.html> para obtener más información.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>entrada</b> <i>Entrada de color</i> | Imagen en la que se aplica la LUT. |
| <b>lut</b> <i>Entrada de color</i> | Ranura de entrada Lut. Debe ser 4096x4096. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad LUT del Alpha</b> <i>Falso/Verdadero</i> | Define si el efecto LUT está ponderado por el canal alfa. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="hald-clut.resources/content-hald-clut.jpg" />
        </td>
    </tr>
</table>
