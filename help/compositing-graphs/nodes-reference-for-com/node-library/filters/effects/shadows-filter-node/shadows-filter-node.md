---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo de filtro Sombras para generar efectos de sombra a partir de las texturas de entrada para añadir profundidad y realismo a los materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombras (nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# Sombras (nodo de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shadows-filter-node.resources/shadows-1.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una versión sin formato y solo en escala de grises del nodo [Shape Drop Shadow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md). Solo toma una forma binaria en blanco y negro como entrada y devuelve únicamente la sombra.

Puede ser útil si está justo después de la sombra y no desea trabajar con un nodo más completo, por ejemplo, al crear su propio material o iluminación hecha un bake.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Distancia de sombra</b> <i>0.0 - 1.0</i> | Controla a qué distancia debe caer la sombra. |
| <b>Ángulo claro</b> <i>0.0 - 1.0</i> | Controla el ángulo de incidencia de la luz. |
| <b>Suavizado de bordes</b> <i>0.0 - 1.0</i> | Determina lo suaves o duros que son los bordes de las sombras. |
| <b>Ejemplos</b> <i>1 - 16</i> | Define la calidad del ajuste Suavizado de bordes. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shadows-filter-node.resources/shadow-ex.png" />
        </td>
    </tr>
</table>
