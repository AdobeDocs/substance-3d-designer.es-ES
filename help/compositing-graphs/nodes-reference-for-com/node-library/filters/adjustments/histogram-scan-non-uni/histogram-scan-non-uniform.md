---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: Utilice el nodo No uniforme de exploración de histograma para realizar una exploración no uniforme del histograma para obtener una corrección de color avanzada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exploración de histograma no uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Exploración de histograma no uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan-non-uniform.resources/histogram-scan-non-uniform-01.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Versión avanzada de [Histogram Scan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), con controles adicionales y entrada para controlar el efecto a nivel de píxel, en lugar de hacerlo uniformemente en toda la imagen. Se puede utilizar para conseguir un contraste y transiciones aún más intrincados en las máscaras.

Es mucho más complejo de usar que la [exploración por histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) normal, así que asegúrate de estar familiarizado con eso antes de intentar usar la versión no uniforme.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada en escala de grises</i> | Resultado de origen que modificar. |
| <b>Mapa de posición</b> <i>Entrada en escala de grises</i> | Ranura de entrada para controlar el parámetro Posición. Se activa cuando &quot;Usar entrada de posición&quot; se establece en True. El rango de valor efectivo es pequeño y depende del ajuste y el mapa de contraste. |
| <b>Mapa de contraste</b> <i>Entrada en escala de grises</i> | Ranura de entrada para controlar el parámetro de contraste. Se activa cuando &quot;Utilizar entrada de contraste&quot; se establece en True. El rango de valor efectivo es pequeño. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Usar entrada de posición</b> <i>Falso/Verdadero</i> | Alterne el uso de la ranura de entrada Mapa de posición. |
| <b>posición</b> <i>0.0 - 1.0</i> | Controla o modifica los resultados del mapa para controlar la configuración de posición. |
| <b>Usar entrada de contraste</b> <i>Falso/Verdadero</i> | Alterne el uso de la ranura de entrada Mapa de contraste. |
| <b>contraste</b> <i>0.0 - 1.0</i> | Controla o modifica los resultados del mapa para controlar la configuración del contraste. |
