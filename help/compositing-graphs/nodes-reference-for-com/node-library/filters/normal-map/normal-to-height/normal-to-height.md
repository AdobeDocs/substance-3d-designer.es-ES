---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Utilice el nodo Normal a Height para convertir mapas de normales en mapas de altura para extraer información de profundidad de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal al Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# Normal al Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height.resources/normal-to-height.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de conversión inversa que intenta volver a convertir un mapa normal de espacio tangente en un mapa de altura. Esta es la versión un poco más simple; [Normal a Height HQ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) tiene más opciones.

Útil para cuando sólo tiene un origen Normalmap, pero aún desea realizar operaciones combinándolo con un mapa de altura. Tenga en cuenta que esto nunca podrá proporcionar un resultado 100% correcto, ya que la información se pierde por la naturaleza del proceso cuando el Height se convierte a Normal. Si ajusta la configuración en consecuencia, esta versión que no es HQ realiza un trabajo decente de conversión de detalles simples.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Equilibrio de Relieve</b> <i>0.0 - 1.0</i> | Ajuste la medida en que las distintas frecuencias influyen en el resultado final. Esto depende en gran medida del mapa de entrada y requiere un poco de ajuste. |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Opacidad global</b> <i>0.0 - 1.0</i> | Ajusta la opacidad global del efecto. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height.resources/normal2heightex.png" />
        </td>
    </tr>
</table>
