---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Utilice el nodo Selección de borde para generar máscaras y seleccionar bordes de malla para crear efectos de desgaste y desgaste basados en bordes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selección de borde
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---


# Selección de borde

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara es la mejor forma de seleccionar cualquier tipo de borde en función de la curvatura. Convexo, cóncavo en cualquier nivel o contraste se puede aislar, proporcionando un excelente método abreviado para evitar hacer esto manualmente a través de un [nodo de niveles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para resaltar bordes. ¡Obligatorio! |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel</b> <i>0.0 - 1.0</i> | Define la cantidad total de resaltado de bordes tanto para Convexo como para Cóncavo. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resaltado para Convexo y Cóncavo. |
| <b>Convexo</b> |  |
| <b>Ancho de bordes convexos</b> <i>0.0 - 1.0</i> | Define la anchura del realzado para aristas convexas. Tenga en cuenta que un suavizado en aumento puede provocar bordes más finos. |
| <b>Suavizado convexo</b> <i>0.0 - 1.0</i> | Defina la suavidad de la transición para aristas convexas. |
| <b>Intensidad convexa</b> <i>0.0 - 1.0</i> | Define la intensidad máxima del realzado de bordes para aristas convexas. Establézcalo en 0 para que no se resalte. |
| <b>Cóncavo</b> |  |
| <b>Ancho de bordes cóncavos</b> <i>0.0 - 1.0</i> | Defina la anchura del resaltado para los bordes cóncavos. Tenga en cuenta que un suavizado en aumento puede provocar bordes más finos. |
| <b>Suavizado cóncavo</b> <i>0.0 - 1.0</i> | Defina la suavidad de la transición para los bordes cóncavos. |
| <b>Intensidad cóncava</b> <i>0.0 - 1.0</i> | Establezca la intensidad máxima del resaltado de bordes para bordes cóncavos. Establézcalo en 0 para que no se resalte. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-select-ex.gif" />
        </td>
    </tr>
</table>
