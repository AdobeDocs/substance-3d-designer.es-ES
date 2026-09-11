---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Edge Wear de metal para generar máscaras de desgaste en bordes metálicos en función de la curvatura y posición de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de metal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---


# Edge Wear de metal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-edge-wear.resources/metal-edge-wear.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa el desgaste de los bordes en un objeto metálico, con arañazos y astillas que aparecen en bordes elevados convexos, potencialmente enmascarados por áreas oscuras hechas un bake de AO.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. |
| <b>Oclusión ambiental</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. |
| <b>Entrada de Suciedad</b> <i>Entrada en escala de grises</i> |  |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |
| <b>Normal del Espacio Mundial</b> <i>Entrada de color</i> |  |
| <b>Posición</b> <i>Entrada de color</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel de desgaste</b> <i>0.0 - 1.0</i> | Define la cantidad total de desgaste, revela gradualmente. |
| <b>Contraste de desgaste</b> <i>0.0 - 1.0</i> | Define el contraste del resultado final. |
| <b>Smoothness de bordes</b> <i>0.0 - 16.0</i> | Define el smoothness del difuminado desde las aristas desde la curvatura. |
| <b>Cantidad de Suciedades</b> <i>0.0 - 1.0</i> | Define la cantidad de suciedad que se fusionará entre los bordes. |
| <b>Escala de Suciedad</b> <i>1 - 16</i> | Define la escala de la Suciedad. |
| <b>Enmascaramiento de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Define la cantidad de efecto que tiene el AO en el efecto final, es decir, las áreas oscuras se enmascaran. |
| <b>Peso de curvatura</b> <i>0.0 - 1.0</i> | Define la cantidad de efecto que tienen las aristas convexas de la curvatura en el efecto final. |
| <b>Usar Suciedad personalizada</b> <i>Falso/Verdadero</i> | Habilita una ranura de entrada de mapa de Suciedad personalizada. |
| <b>Usar triplanar</b> <i>Falso/Verdadero</i> | Habilite la proyección [Tri Plana](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) para ocultar las costuras. |
| <b>Contraste de fusión triplanar</b> <i>0.0 - 1.0</i> | Define el contraste de fusión para la proyección triplanar. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="metal-edge-wear.resources/metal-edge-wear-ex.gif" />
        </td>
    </tr>
</table>
