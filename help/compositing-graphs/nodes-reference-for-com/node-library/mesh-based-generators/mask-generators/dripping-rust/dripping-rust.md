---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Utilice el nodo Óxido de goteo para generar patrones de goteo de óxido basados en la geometría de malla y la dirección de la gravedad.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Óxido goteo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# Óxido goteo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa los copos de óxido y las motas, con las fugas que corren hacia abajo.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa hecho un bake o generado para ayudar con la colocación del óxido. |
| <b>Oclusión ambiental</b> <i>Entrada en escala de grises</i> | Mapa hecho un bake o generado para ayudar con la colocación del óxido. |
| <b>Posición</b> <i>Entrada en escala de grises</i> | Mapa hecho un bake o generado para direcciones de goteo. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Difusión de Óxido</b> <i>0.0 - 1.0</i> | Control principal de la cantidad de óxido. |
| <b>Contraste de Óxido</b> <i>0.0 - 1.0</i> | Define la cantidad de óxido en las motas generadas (no afecta a los goteos). |
| <b>Smoothness de propagación</b> <i>0.0 - 1.0</i> | Cantidad de efecto de desenfoque/mancha que se aplica a las motas de óxido. |
| <b>Intensidad de goteo</b> <i>0.0 - 1.0</i> | Establece la fuerza y la longitud de los goteos de los manchas. |
| <b>Smoothness de goteos</b> <i>0.0 - 1.0</i> | Cantidad de desenfoque y suavizado que se aplica a los goteos. |
| <b>Cantidad de muestras de goteo</b> <i>0 - 32</i> | Define el nivel de calidad (pasos) para el efecto de goteos. Tiene un ligero efecto en la velocidad. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/dripping-rust-ex3.gif" />
        </td>
    </tr>
</table>
