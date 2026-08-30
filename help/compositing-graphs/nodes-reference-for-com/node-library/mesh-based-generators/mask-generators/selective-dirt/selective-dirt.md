---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: Utilice el nodo Dirt selectivo para generar máscaras de acumulación de dirt selectivas basadas en la geometría de malla para lograr un intemperismo realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt selectivo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 8%

---


# Dirt selectivo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](selective-dirt.resources/selective-dirt.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) representa un simple efecto de dirt en bordes convexos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. |
| <b>Máscara de variación</b> <i>Entrada en escala de grises</i> | Mapa de variación opcional, se puede activar a través de parámetros. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel</b> <i>0.0 - 1.0</i> | Define el nivel total del efecto y lo revela gradualmente. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. |
| <b>Variación</b> <i>0.0 - 1.0</i> | Define la cantidad de variación/suciedad que se fusionará en el efecto. |
| <b>Omitir máscara de variación</b> <i>Falso/Verdadero</i> | Permite anular la variación con una ranura de entrada personalizada. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="selective-dirt.resources/selective-dirt-ex.gif" />
        </td>
    </tr>
</table>
