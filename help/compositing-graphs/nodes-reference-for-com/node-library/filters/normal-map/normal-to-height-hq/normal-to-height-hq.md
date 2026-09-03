---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Utilice el nodo HQ Normal a Height para convertir mapas de normales en mapas de altura de alta calidad para la extracción de detalles de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal Al Height HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# Normal Al Height HQ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq-01.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de conversión inversa que intenta volver a convertir un mapa normal de espacio tangente en un mapa de altura. Este es el nodo más avanzado; [Normal al Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) tiene menos opciones y utiliza cálculos diferentes.

Útil para cuando sólo tiene un origen Normalmap, pero aún desea realizar operaciones combinándolo con un mapa de altura. Tenga en cuenta que esto nunca podrá proporcionar un resultado 100% correcto, ya que la información se pierde por la naturaleza del proceso cuando el Height se convierte a Normal. Nunca puede reemplazar un mapa de altura correctamente generado!

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Equilibrio de Relieve</b> <i>0.0 - 1.0</i> | Fusiones entre el sesgo de baja y alta frecuencia. |
| <b>Intensidad de Height</b> <i>0.0 - 1.0</i> | Intensidad o multiplicador para el mapa de altura, funciona un poco como la opacidad global. |
| <b>Normalizar Height</b> <i>Falso/Verdadero</i> | Ajusta automáticamente el rango de mapa de altura para utilizar contraste completo, como un [nivel automático](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md). |
| <b>Calidad</b> <i>Normal, Alta</i> | Cambia entre velocidad o calidad. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal-to-height-hq-02.png" />
        </td>
    </tr>
</table>
