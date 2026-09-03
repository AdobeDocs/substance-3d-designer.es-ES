---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Utilice el nodo Detección de bordes para detectar bordes en texturas para crear contornos y efectos de máscara basados en bordes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Detección de bordes
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# Detección de bordes

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-detect.resources/edge-detect-01.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Detecta el contraste en imágenes en blanco y negro y, a continuación, crea una máscara en blanco y negro que resalta el contraste.

Útil en muchos casos donde se necesita algún tipo de máscara para los bordes. Tenga en cuenta que funciona mejor con entradas de alto contraste; si es necesario, ajusta el contraste antes de pasar algo a este nodo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ancho del borde</b> <i>1.0 - 16.0</i> | Ancho de las áreas detectadas alrededor de los bordes. |
| <b>Redondez de borde</b> <i>0.0 - 16.0</i> | Redondea, desenfoca y suaviza la máscara generada. |
| <b>Invertir</b> <i>Falso/Verdadero</i> | Invierte el resultado. |
| <b>Tolerancia</b> <i>0.0 - 1.0</i> | Factor de umbral de tolerancia para el lugar en el que deben aparecer los bordes. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-detect.resources/edge-detect-02.png" />
        </td>
    </tr>
</table>
