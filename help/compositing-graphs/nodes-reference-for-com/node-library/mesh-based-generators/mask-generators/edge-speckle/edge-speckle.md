---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Utilice el nodo Edge Speckle para generar patrones de desgaste moteado en bordes de malla para crear efectos de daño de borde realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 6%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-speckle.resources/edge-speckle.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa los bordes con una pequeña mota añadida para dividirlos. Consulte también [Dirt Edge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para resaltar bordes. ¡Obligatorio! |
| <b>Máscara de variación</b> <i>Entrada en escala de grises</i> | Ranura de máscara opcional utilizada para enmascarar los efectos del nodo. Activar con &quot;Anular máscara de variación&quot;. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel</b> <i>0.0 - 1.0</i> | Define la cantidad total de resaltado de bordes. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. |
| <b>Selección de bordes</b> <i>0.0 - 1.0</i> | Define la influencia de las aristas convexas. |
| <b>Variación</b> <i>0.0 - 1.0</i> | Define hasta qué punto la máscara de variación rompe el efecto. |
| <b>Omitir máscara de variación</b> <i>Falso/Verdadero</i> | Anula la máscara integrada con una ranura de entrada personalizada. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-speckle.resources/edge-speckle-ex.gif" />
        </td>
    </tr>
</table>
