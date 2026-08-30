---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación cuádruple para aplicar transformaciones cuadrilaterales a las texturas para la corrección y deformación de la perspectiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación cuádruple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---


# Transformación cuádruple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](quad-transform.resources/quad-transform-grayscale.png){width="128px"}

![](quad-transform.resources/quad-transform.png){width="128px"}

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de transformación especial que permite la transformación de una forma cuádruple a través de la interacción con sus puntos de vértice. Permite transformaciones muy específicas de forma práctica.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>p00</b> | Punto superior izquierdo. |
| <b>p01</b> | Punto inferior izquierdo |
| <b>p10</b> | Punto superior derecho. |
| <b>p11</b> | Punto inferior derecho. |
| <b>Sacrificio</b> <i>Solo frontal, Solo posterior, Delantero sobre trasero, Reverso sobre frontal</i> | Establecer el sacrificio/ocultación de la forma cuando los puntos se cruzan entre sí. |
| <b>Habilitar Mosaico</b> <i>Falso/Verdadero</i> |  |
| <b>Color de fondo</b> <i>(valor de escala de grises)</i> | Color de fondo sólido si el mosaico está desactivado. |
| <b>Muestreo</b> <i>Bilineal, Más Cercana</i> | Definir la calidad de muestreo. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="quad-transform.resources/quad-example.gif" />
        </td>
    </tr>
</table>
