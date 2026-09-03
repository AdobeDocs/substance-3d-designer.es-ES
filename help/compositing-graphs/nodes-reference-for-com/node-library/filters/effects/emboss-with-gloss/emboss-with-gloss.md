---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: Utilice el nodo Relieve con brillo para crear efectos en relieve con mapas de brillo para añadir profundidad y brillo a las texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Relieve Con Brillo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---


# Relieve Con Brillo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss-01.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza un efecto de relieve con brillo añadido (reflejo de specular) en una entrada de color y height. Básicamente, añade una iluminación falsa y hecha un bake a una imagen en función de la información del height. Resulta útil para algunos estilos de texturizado que requieren luz hecha un bake en las texturas.

Para obtener una versión con más opciones, consulte [Uber Relieve](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md). También está la versión atómica más simple de [Relieve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Color</b> <i>Entrada de color</i> |  |
| <b>Height</b> <i>Entrada en escala de grises</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Color de resaltado</b> <i>(Valor de color)</i> | Color del resaltado del specular. |
| <b>Color de sombra</b> <i>(Valor de color)</i> | Color utilizado en áreas sombreadas/sin iluminación. |
| <b>Brillo</b> <i>0.0 - 0.5</i> | Tamaño de resaltado de brillo. |
| <b>Intensidad</b> <i>0.0 - 10.0</i> | Intensidad del resaltado. |
| <b>Ángulo claro</b> <i>0.0 - 1.0</i> | Ángulo de incidencia de la luz (fingida). |
