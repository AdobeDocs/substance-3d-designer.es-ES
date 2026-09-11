---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: Utilice el nodo Flood Fill a tamaño de cuadro para rellenar regiones con valores de tamaño de cuadro delimitador para los efectos de escala procedimienta.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill a tamaño de cuadro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---


# Flood Fill a tamaño de cuadro

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-bbox-size.resources/floodfill-to-bbox-size.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera un mapa en escala de grises a partir de una base [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md), con valores vinculados al tamaño individual de cada mosaico.

Los valores son relativos al tamaño total del lienzo (un azulejo blanco completo significaría que estira todo el lienzo), por lo que el contraste suele ser bajo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Salida</b> <i>max(X, Y), X, Y</i> | Define en qué métrica se basa el valor: ancho, largo o ambos. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-bbox-size.resources/floodbbox-ex1.png" />
        </td>
    </tr>
</table>
