---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
breadcrumb-title: ''
description: Utilice el nodo Cuantificar escala de grises para reducir el número de niveles de escala de grises para los efectos de posterización.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cuantificar escala de grises
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Cuantificar escala de grises

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Cuantificar escala de grises](../../../../../../assets/quantize-grayscale.png "Icono Cuantificar escala de grises"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una única spline con forma de círculo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Pasos</b> *Entero* | El número de valores separados a los que se debe aproximar el rango de entrada. |
| <b>Desplazamiento</b> *Flotador* | Aplica un desplazamiento al intervalo de entrada, que *desplaza* los resultados a lo largo del intervalo. |
| <b>Pendiente</b> *Flotador* | Aplica un degradado de pendiente a las *transiciones* entre valores aproximados, hasta el *intervalo completo de un paso*. |
| <b>Curva de Pendientes</b> *Entero* | Establece el método de adquisición de la curva para la pendiente establecida por el parámetro <b>Pendiente</b>:<ul data-preserve-html="true"> <li data-preserve-html="true">*Lineal*: Aplica una curva lineal que da como resultado una pendiente recta</li> <li data-preserve-html="true">*Paso suave*: Aplica una curva paso a paso suave, lo que da como resultado una pendiente suave</li> <li data-preserve-html="true">*Entrada de curva*: Aplica la curva descrita por el mapa de entrada <b>Curve Input</b>. Puede usar un nodo [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para describir esta curva con una gran cantidad de control.</li> </ul> |

## Ejemplos

![Ejemplo 1](../../../../../../assets/quantizegrayscale.gif "Ejemplo 1")

![Ejemplo 2](../../../../../../assets/quantizegrayscale.png "Ejemplo 2")
