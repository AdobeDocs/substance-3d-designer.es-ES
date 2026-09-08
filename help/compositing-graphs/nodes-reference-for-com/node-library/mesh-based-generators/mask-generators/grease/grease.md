---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Utilice el nodo Grasa para generar máscaras de acumulación de grasa basadas en la geometría de malla y las áreas de contacto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grasa
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 5%

---


# Grasa

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara está diseñada específicamente para las caras de los personajes y otras áreas específicas. Genera un tipo de máscara de grasa de piel en áreas de bajo thickness.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Thickness</b> <i>Entrada en escala de grises</i> | Mapa de Thickness al horno en el que se basa todo el efecto. ¡Obligatorio! |
| <b>Ruido</b> <i>Entrada en escala de grises</i> | Mapa de ruido opcional para anular la suciedad de grasa. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel</b> <i>0.0 - 1.0</i> | Define la cantidad total de efecto que debe aparecer. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. |
| <b>Umbral de Thickness</b> <i>0.0 - 1.0</i> | Establece un thickness mínimo en el que debe aparecer el efecto. Igual de importante que Level; retoca esto para que se ajuste a tu mapa de Thickness. |
| <b>Anular ruido</b> <i>Falso/Verdadero</i> | Ajuste para anular el mapa interno de suciedades de grasa con una ranura de entrada personalizada. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/grease-ex.gif" />
        </td>
    </tr>
</table>
