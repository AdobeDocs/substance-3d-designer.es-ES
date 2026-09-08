---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Desgaste de cuero para generar máscaras de desgaste en superficies de cuero basadas en la curvatura de la malla y los puntos de contacto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de cuero
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 5%

---


# Desgaste de cuero

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el desgaste con un patrón de cuero, con más desgaste en los bordes basados en la curvatura. Es similar a [Edge Wear de fibra de vidrio](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) en cuanto a funcionalidad y tiene en su mayoría los mismos parámetros.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para la colocación de los bordes. ¡Obligatorio! |
| <b>Oclusión de ambiente</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para ocluir ciertas áreas. Recomendado, pero no obligatorio. |
| <b>Entrada de Suciedad</b> <i>Entrada en escala de grises</i> | Ranura de entrada de mapa de Suciedades opcional que se puede activar mediante el parámetro &quot;Usar Suciedad personalizada&quot;. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel de desgaste</b> <i>0.0 - 1.0</i> | Define el nivel de desgaste global, revelándose gradualmente. |
| <b>Contraste de desgaste</b> <i>0.0 - 1.0</i> | Define el contraste del efecto. |
| <b>Cantidad de Suciedades</b> <i>0.0 - 1.0</i> | Define la cantidad de suciedad (motivo de piel predeterminado) que se fusionará entre los bordes. |
| <b>Enmascaramiento de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Define la medida en que el AO oculta los efectos de desgaste. |
| <b>Peso de curvatura</b> <i>0.0 - 1.0</i> | Define hasta qué punto los bordes de la curvatura afectan al resultado final. Incluso si se establece en 0, todavía necesita un mapa de curvatura. |
| <b>Usar Suciedad personalizada</b> <i>Falso/Verdadero</i> | Permite anular el motivo de cuero predeterminado incorporado. Utilice en su lugar una ranura de entrada personalizada. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/leather-wear-ex.gif" />
        </td>
    </tr>
</table>
