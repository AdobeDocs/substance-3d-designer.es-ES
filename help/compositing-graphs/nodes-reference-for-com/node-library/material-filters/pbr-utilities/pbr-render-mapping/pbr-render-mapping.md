---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: Utilice el nodo Asignación de Renderizaciones PBR para convertir salidas de material a diferentes formatos de asignación de Renderizaciones PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Asignación de renderizaciones PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# Asignación de renderizaciones PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render-mapping.resources/pbr-render-mapping-01.png)![](pbr-render-mapping.resources/pbr-render-mapping-02.png)

<b>En:</b> Filtros de material > Utilidades de PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este es un nodo de extensión para el [nodo Renderización PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), que te permite asignar una textura independiente a la forma de una [Renderización PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) anterior. Su objetivo principal es permitirte reasignar cada canal independiente de tu [Renderización PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), de vuelta a la forma, para crear desgloses compuestos de canales de mapa, como en los ejemplos a continuación. Puede crear su propio método compuesto y máscaras utilizando los nodos de asignación de Renderizaciones PBR como componente.

Existe una versión en color y en escala de grises para los dos tipos de datos: utilice color para mapas difusos, utilice escala de grises para mapas de rugosidad, de metal y otros mapas en escala de grises.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Textura</b> <i>Entrada en color/escala de grises</i> | Textura para asignar a una forma. |
| <b>UV</b> <i>Entrada de color</i> | Entrada de datos UV obligatoria desde un [nodo Renderización PBR.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Color de fondo</b> <i>(Valor de color)</i> | Defina un valor de color sólido para utilizarlo en el fondo. |

## Ejemplos

El ejemplo es una composición de cuatro nodos de asignación de Renderizaciones PBR diferentes, que usan una selección de histograma [en un degradado lineal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md) como máscaras.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md)[

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render-mapping.resources/pbr-render-mapping-03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render-mapping.resources/pbr-render-mapping-04.png" />
        </td>
    </tr>
</table>
