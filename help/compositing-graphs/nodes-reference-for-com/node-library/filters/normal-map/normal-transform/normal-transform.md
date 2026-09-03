---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformar normal para aplicar transformaciones a los mapas de normales conservando correctamente las direcciones vectoriales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Transformo normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-transform.resources/normal-transform-01.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

De forma similar al nodo 2D del Transformo atómico, esto permite la transformación de Normalmaps sin romper el espacio-tangente, en su lugar se vuelve a calcular sobre la marcha, lo que resulta en normalmaps siempre correctos.

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
