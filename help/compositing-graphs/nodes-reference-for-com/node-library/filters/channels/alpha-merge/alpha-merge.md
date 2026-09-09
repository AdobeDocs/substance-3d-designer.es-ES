---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/channels/alpha-merge.html"
breadcrumb-title: ''
description: Utilice el nodo Combinación de Alpha para combinar texturas de RGB con canales alfa para crear texturas RGBA.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Channels > Alpha Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinación de Alpha
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---


# Combinación de Alpha

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](alpha-merge.resources/rgb-a-merge.png)

<b>En:</b> Filtros > Canales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Agrega un canal alfa a una entrada sin canal alfa. No debe confundirse con [Combinación RGBA](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md), este nodo es mucho más sencillo y solo agrega alfa.

Nodo simple pero práctico para cuando solo quieres enmascarar algo, o cuando tu resultado requiere un alfa.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>RGB</b> <i>Entrada de color</i> | Imagen en color sin alfa |
| <b>A</b> <i>Entrada en escala de grises</i> | Imagen en escala de grises que se utilizará como alfa del resultado. |
