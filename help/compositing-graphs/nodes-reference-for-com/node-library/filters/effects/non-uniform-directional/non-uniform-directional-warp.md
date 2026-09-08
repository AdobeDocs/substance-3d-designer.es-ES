---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: Utilice el nodo Non Uniform Directional Warp para aplicar una deformación direccional no uniforme y crear efectos de distorsión variados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Non Uniform Directional Warp
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 5%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Deformación de dirección no uniforme es una versión avanzada de [Deformación direccional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) que permite que la intensidad y la dirección de la deformación se controlen mediante una entrada de imagen. Permite mucho más control y puede crear una distorsión de imagen muy útil e interesante, en el mismo vano que [Desenfoque de Pendiente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

Se diferencia de [Multi Deformación direccional](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) en que permite el control sobre el ángulo a través de una entrada de mapa personalizada, mientras que Multi Deformación direccional solo permite que la dirección se controle a través de parámetros. Esto significa que puede crear efectos finales y curvos avanzados que de lo contrario no serían posibles.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada en escala de grises</i> | Mapa base al que se aplicará la deformación. |
| <b>Entrada de intensidad</b> <i>Entrada en escala de grises</i> | El mapa de máscara obligatorio que controla la intensidad del efecto de deformación debe ser de escala de grises. |
| <b>Entrada de ángulo de deformación</b> <i>Entrada en escala de grises</i> | El mapa de máscara obligatorio que controla el ángulo del efecto de deformación debe ser de escala de grises. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 20.0</i> | Define la intensidad del efecto de deformación y la distancia que se deben expulsar los píxeles. |
| <b>Ángulo de deformación</b> <i>0.0 - 1.0</i> | Define el ángulo o la dirección en la que se aplica el efecto Deformar. |
| <b>Multiplicador de entrada de ángulo de deformación</b> <i>0.0 - 1.0</i> | Define el efecto del mapa de entrada de ángulo de deformación. El mapa de entrada de ángulo de deformación se utilizará para interpolar de 0 al valor de este parámetro. |
| <b>Modo de seguimiento</b> <i>Mín., Máx., Promedio</i> | Define cómo se mezclan los rastros. |
| <b>Longitud del rastro</b> <i>0.0 - 1.0</i> | Establece la longitud de los rastros. |
| <b>Fundido de seguimiento</b> <i>0.0 - 1.0</i> | Establece cuánto debe desaparecer cada pista |
| <b>Curva de seguimiento</b> <i>-1.0 - 1.0</i> | Solo tiene efecto si el fundido de seguimiento no es 0. Define cómo se comporta el efecto de atenuación. |
