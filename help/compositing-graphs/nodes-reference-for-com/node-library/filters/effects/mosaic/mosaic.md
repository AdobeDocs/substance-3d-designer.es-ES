---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: Utilice el nodo Mosaico para crear efectos de mosaico dividiendo texturas en bloques y motivos pixelados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---


# Mosaico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mosaic.resources/mosaic-01.png){width="128px"}

![](mosaic.resources/mosaic-02.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

&quot;Faceties&quot; crea un mapa de degradado existente, suave y con pendiente mediante un efecto de pasada múltiple [Deformar](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md). Cuando se utiliza el mismo mapa para ambas entradas, esencialmente crece y acentúa las áreas más brillantes.

Esto resulta útil para añadir más definición a los mapas de escala de grises, como el mapa de altura, ya que puede introducir más definición en las formas.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Color</b> <i>Entrada en color/escala de grises</i> |  |
| <b>Mapa de mosaico</b> <i>Entrada en escala de grises</i> | Mapa del controlador de deformación. Puede ser igual que la primera entrada. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ejemplos</b> <i>0 - 16</i> | Determina la calidad de la muestra múltiple. |
| <b>Intensidad</b> <i>0.0 - 1.0</i> | Intensidad del efecto. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mosaic.resources/mosaic-03.png" />
        </td>
    </tr>
</table>
