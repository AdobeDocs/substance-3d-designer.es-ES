---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: Utilice el nodo Coincidencia de color para hacer coincidir los colores entre texturas para crear paletas de colores uniformes y armonizar texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Coincidencia de color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# Coincidencia de color

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-match.resources/color-match-3.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Intenta hacer coincidir el rango de *color de origen* definido con un rango de *color de destino*, con compatibilidad con ranuras de entrada para definir el origen y el destino.

Para obtener versiones más sencillas, vea [Reemplazar rango de color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) o [Reemplazar color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada de color</i> | Entrada principal que modificar para el resultado. |
| <b>Color de origen</b> <i>Entrada de color</i> | Ranura de entrada para el color de origen, que solo se usa cuando el modo de color de origen está establecido en *Entrada*. |
| <b>Color de destino</b> <i>Entrada de color</i> | Ranura de entrada para el color de destino, que solo se usa cuando el modo de color de destino está establecido en *Entrada*. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de color de origen</b> <i>Promedio, parámetro, entrada</i> | Establece si el color de origen se define calculando el promedio de la imagen de entrada, estableciendo un parámetro o utilizando una ranura de entrada. |
| <b>Color de origen</b> <i>(Valor de color)</i> | Si el modo de color de origen está establecido en *Parámetro*, este parámetro determina el color de origen. |
| <b>Modo de color de destino</b> <i>Parámetro, entrada de imagen</i> | Establece si el color de origen se define calculando el promedio de la imagen de entrada, estableciendo un parámetro o utilizando una ranura de entrada. |
| <b>Color de destino</b> <i>(Valor de color)</i> | Si el modo de color de destino está establecido en *Parámetro*, este parámetro determina el color de destino. |
| <b>Variación de color personalizada</b> <i>Falso/Verdadero</i> | Permite una variación de color adicional. |
| <b>Variación de color</b> | Establece las variaciones de tono, crominancia o luminancia en el resultado si está activado. |
| <b>Usar máscara</b> <i>Falso/Verdadero</i> | Cambia el uso de Entrada o Salida de máscara, en función del modo de máscara que se muestra a continuación. |
| <b>Modo de máscara</b> <i>Parámetro, entrada</i> | El modo de parámetros emite una máscara que detalla el cambio de color. El modo de entrada permite que una máscara controle la intensidad del efecto Coincidencia de color. |
| <b>Máscara</b> | Genera una máscara que muestra dónde se aplicó exactamente el efecto Coincidencia de color, con controles adicionales para suavizar y desenfocar la máscara resultante. |
