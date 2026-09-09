---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: Utilice el nodo HQ de desenfoque para aplicar efectos de desenfoque de alta calidad a las texturas para crear resultados de desenfoque suaves y de aspecto profesional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desenfocar alta calidad
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# Desenfocar alta calidad

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](blur-hq.resources/blur-hq-1.png){width="128px"}

![](blur-hq.resources/blur-hq-grayscale.png){width="128px"}

<b>En:</b> Filtros > Desenfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza un desenfoque gaussiano de alta calidad en el resultado. Mucho mejor que [el desenfoque estándar de la caja atómica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [.](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utilice &quot;Desenfocar HQ&quot; para las entradas de color o &quot;Desenfocar HQ en escala de grises&quot; para las entradas de escala de grises.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 16.0</i> | Intensidad (radio) del desenfoque. Cuanto más alto sea este valor, mayor será el desenfoque. |
| <b>Calidad</b> <i>0 - 1</i> | Aumenta la cantidad de muestreo interno para obtener una calidad aún mayor, a una velocidad de cálculo reducida. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="blur-hq.resources/hqblur-example.gif" />
        </td>
    </tr>
</table>
