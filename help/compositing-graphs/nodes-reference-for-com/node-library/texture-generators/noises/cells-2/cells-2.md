---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-2.html"
breadcrumb-title: ''
description: Use el nodo Celdas 2 para generar patrones celulares intermedios para crear efectos de textura orgánica y biológica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELDAS 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 3%

---


# CELDAS 2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Celdas 2 - Icono](../../../../../../assets/cells_2.png "Celdas 2 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los <b>Celdas</b> ruidos de pared.

Máscara binaria de las celdas con un thickness de pared ajustable.

Consulte también: [Celdas 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Celdas 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md), [Celdas 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Salidas

</td>
<td style="border: 0;" valign="top">

### Parámetros

</td>
<td style="border: 0;" valign="top">

### Ejemplos

</td>
</tr>
</table>

## Salidas

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises* | El ruido generado como un mapa de bits en escala de grises. |

## Parámetros

|  |  |
| --- | --- |
| Entero <b>Scale</b> | Subdivisión de la cuadrícula utilizada para generar los mosaicos de ruido.    Un valor más alto provoca que se dibujen más mosaicos y que el ruido sea más denso. |
| <b>Ancho del borde</b> Flotante | Ajusta el thickness de las paredes entre las celdas, como proporción de la cuadrícula. (Es decir, no depende de la resolución) |
| Booleano <b>Invert</b> | Cambia los blancos y negros de la imagen de salida. |
| Flotador <b>Disorder</b> | Desplaza los ingredientes del ruido.    Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> Flotador | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.    Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |
| <b>Expansión no cuadrada</b> Boolean | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Celdas 2 - Ejemplo 1](../../../../../../assets/cells_2_1.png "Celdas 2 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Celdas 2 - Ejemplo 2](../../../../../../assets/noise_cells_2_v2_speed0.3_aniso0.6.gif "Celdas 2 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
