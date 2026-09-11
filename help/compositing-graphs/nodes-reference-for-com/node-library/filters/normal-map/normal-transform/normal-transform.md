---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación normal para aplicar transformaciones a los mapas normales conservando correctamente las direcciones vectoriales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Transformación normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

De forma similar al nodo de Transformación 2D atómica, esto permite la transformación de los mapas normales sin romper el espacio-tangente, en su lugar se recalcula sobre la marcha, lo que resulta en mapas normales siempre correctos.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Matrix2x2</b> <i>(Matriz de transformación):</i> | Gire o escale la entrada. |
| <b>Desplazamiento</b> <i>-0.5 - 0.5</i> | Mueve o traduce el resultado. Cuando el control Transformación está presente, el resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambiar entre diferentes Formatos de mapa de normales (invierte el canal verde) |
