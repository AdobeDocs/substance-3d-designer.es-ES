---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: Utilice el nodo Varios Colores Equalizer para ecualizar los colores en varios canales de textura para un procesamiento coherente de materiales digitalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Varios Colores Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# Varios Colores Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-color-equalizer.resources/color-equalizer-multi.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Esta es la versión de entrada múltiple de [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Unifica las diferencias de color y elimina los matices no deseados a una escala que el usuario puede seleccionar. Está pensado principalmente para fotos de varios ángulos, que luego se combinan con [Multi-Ángulo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Multi-Ángulo a Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulta el [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) original para obtener más información.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-8</b> <i>Entrada de color</i> | Múltiples entradas para procesar. |
| <b>Entrada de máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Recuento de entradas</b> <i>1 - 8</i> | Define el número de entradas que se procesarán en paralelo. |
| <b>Mosaico de entrada</b> <i>Falso/Verdadero</i> | Conserva opcionalmente el mosaico en los bordes. |
| <b>Radio</b> <i>0.0 - 50.0</i> | Define el radio de ecualización. Un radio mayor solo eliminará las grandes diferencias de color. Esto requiere un ajuste para cada imagen. |
| <b>Equilibrio de brillo/oscuridad</b> <i>0.0 - 1.0</i> | Configuración de sesgo para dejar o quitar matices más oscuros. |
| <b>Variación de color personalizada</b> <i>Falso/Verdadero</i> | Permite variar el efecto hacia un color especificado por el usuario. |
| <b>Variación de color</b> | Solo está activo si la opción Variación de color personalizada está activada. Los ajustes permiten seleccionar un desplazamiento de matiz hacia el que ecualizar. |
| <b>Tono</b> <i>0.0 - 360.0</i> |  |
| <b>Croma</b> <i>0.0 - 1.0</i> |  |
| <b>Luminancia</b> <i>0.0 - 1.0</i> |  |
| <b>Origen de máscara</b> <i>Ninguno, promedio de imagen, parámetro de color, entrada</i> | Establece si se debe producir alguna máscara. El parámetro de color habilita los ajustes adicionales que se indican a continuación. La entrada cambia a una entrada de máscara definida por el usuario. |
| <b>Máscara</b> | Solo está activo con máscaras de parámetros de color. Contiene parámetros de máscara adicionales para determinar la máscara en función de la propia imagen. Los siguientes parámetros permiten convertir con precisión un matiz en una máscara binaria en la que se aplica la ecualización. Tenga en cuenta que los efectos del parámetro Radio pueden ser mucho menos pronunciados al utilizar estos ajustes. |
| <b>Color</b> <i>(Valor de color)</i> |  |
| <b>Intervalo de tono</b> <i>0.0 - 360.0</i> |  |
| <b>Rango de croma</b> <i>0.0 - 1.0</i> |  |
| <b>Rango de luminancia</b> <i>0.0 - 1.0</i> |  |
| <b>Desenfocar</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
