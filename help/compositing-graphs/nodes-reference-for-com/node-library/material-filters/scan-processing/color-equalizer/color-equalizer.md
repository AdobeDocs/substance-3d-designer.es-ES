---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Utiliza el nodo de Color Equalizer para equilibrar las variaciones de color en los materiales escaneados y lograr un aspecto de textura uniforme.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo funciona como un [Paso alto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) de alta calidad para las diferencias de color. Cuando un Paso alto normal elimina la saturación y puede provocar una nitidez no deseada, el Color Equalizer funciona para eliminar las diferencias de color al anochecer y eliminar los matices no deseados a una escala seleccionable por el usuario.

Esto resulta muy útil si una fotografía o digitalización presenta diferencias de color no deseadas o un matiz que desea eliminar. Si ha utilizado [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), este nodo le resultará familiar.

Las opciones de enmascaramiento están pensadas para eliminar matices muy específicos o para funcionar solo en rangos de valores específicos. Úselos si cree que el efecto es demasiado amplio.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada de color</i> |  |
| <b>Entrada de máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. Solo está activo cuando Máscara está configurada como &quot;Entrada&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Mosaico de entrada</b> <i>Falso/Verdadero</i> | Conserva opcionalmente el mosaico en los bordes. |
| <b>Radio</b> <i>0.0 - 50.0</i> | Define el radio de ecualización. Un radio mayor solo eliminará las grandes diferencias de color. Esto requiere un ajuste para cada imagen. |
| <b>Equilibrio de brillo/oscuridad</b> <i>0.0 - 1.0</i> | Configuración de sesgo para dejar o quitar matices más oscuros. |
| <b>Variación de color personalizada</b> <i>Falso/Verdadero</i> | Permite variar el efecto hacia un color especificado por el usuario. |
| <b>Variación de color</b> | Solo está activo si la opción Variación de color personalizada está activada. Los ajustes permiten seleccionar un desplazamiento de matiz hacia el que ecualizar. |
| <b>Tono</b> <i>0.0 - 360.0</i> |  |
| <b>Croma</b> <i>0.0 - 1.0</i> |  |
| <b>Luminancia</b> <i>0.0 - 1.0</i> |  |
| <b>Origen de máscara</b> <i>Ninguno, promedio de imagen, parámetro de color, entrada</i> | Define si debe producirse algún tipo de enmascaramiento. El parámetro de color habilita los siguientes ajustes adicionales. La entrada cambia a una entrada de máscara definida por el usuario. |
| <b>Máscara</b> | Esta opción solo está activa con las máscaras de parámetros de color. Parámetros de enmascaramiento adicionales para determinar la máscara en función de la propia imagen. Los siguientes parámetros permiten convertir con precisión un matiz en una máscara binaria en la que se aplica la ecualización. Tenga en cuenta que los efectos del parámetro Radio pueden ser mucho menos pronunciados al utilizar estos ajustes. |
| <b>Color</b> <i>(Valor de color)</i> |  |
| <b>Intervalo de tono</b> <i>0.0 - 360.0</i> |  |
| <b>Rango de croma</b> <i>0.0 - 1.0</i> |  |
| <b>Rango de luminancia</b> <i>0.0 - 1.0</i> |  |
| <b>Desenfocar</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
