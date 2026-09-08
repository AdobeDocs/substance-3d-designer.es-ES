---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: Utilice el nodo Desenfoque anisotrópico para aplicar efectos de desenfoque direccional para crear efectos de desenfoque de movimiento y de desenfoque.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desenfoque anisotrópico
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# Desenfoque anisotrópico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

<b>En:</b> Filtros > Desenfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza un [desenfoque direccional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md) de alta calidad, con algunas configuraciones para personalizar la apariencia. También conocido como &quot;desenfoque de movimiento&quot;.

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utiliza &quot;Desenfoque anisotrópico&quot; para las entradas de color o &quot;Desenfoque anisotrópico en escala de grises&quot; para las entradas de escala de grises.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 16.0</i> | Intensidad (radio) del desenfoque. Cuanto más alto sea este valor, mayor será el desenfoque. |
| <b>Anisotropía</b> <i>0.0 - 1.0</i> | Direccionalidad del desenfoque. Establecer esto en 0.0 es lo mismo que realizar un desenfoque normal. |
| <b>Ángulo</b> <i>0.0 - 1.0</i> | Define el ángulo de la dirección del desenfoque. |
| <b>Calidad</b> <i>0 - 1</i> | Cambia entre un [desenfoque de cuadro](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) y un desenfoque de HQ internamente. Intercambia velocidad por calidad. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/aniso-blur-example.gif" />
        </td>
    </tr>
</table>
