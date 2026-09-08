---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-4.html"
breadcrumb-title: ''
description: Usa el nodo de Celdas 4 para generar patrones celulares avanzados para crear efectos de textura orgánica y biológica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELDAS 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---


# CELDAS 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Celdas 4 - Icono](../../../../../../assets/cells_4.png "Celdas 4 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los <b>Celdas</b> ruidos de pared.

A cada celda se le asigna un color plano, que puede ser aleatorio o una muestra de una imagen de entrada.

Consulte también: [Celdas 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Celdas 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Celdas 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Escala de grises</i> |  |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | El ruido generado como un mapa de bits en escala de grises. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>Entero</i> | Subdivisión de la cuadrícula utilizada para generar los mosaicos de ruido.    Un valor más alto provoca que se dibujen más mosaicos y que el ruido sea más denso. |
| <b>Desorden</b> <i>Flotador</i> | Desplaza los ingredientes del ruido.    Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> <i>Flotador</i> | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.    Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |
| <b>Origen de color</b> <i>Entero</i> | Origen del color plano aplicado a las celdas:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>Aleatorio:</i></b> Use un color aleatorio controlado por la semilla aleatoria del nodo</li> <li data-preserve-html="true"><b><i>Pseudorandom:</i></b> Use un color aleatorio predefinido por un valor de conjunto de usuarios independiente</li> <li data-preserve-html="true"><b><i>Entrada de imagen:</i></b> Utilice el color muestreado en la ubicación de la celda en la imagen de entrada</li> </ul> |
| <b>Semilla pseudoaleatoria</b> <i>Entero</i>   *Disponible cuando &#39;Color source&#39; está establecido en &#39;Pseudorandom&#39;* | Permite cambiar la semilla del color por separado de la semilla del nodo. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Celdas 4 - Ejemplo 1](../../../../../../assets/cells_4_1.png "Celdas 4 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Celdas 4 - Ejemplo 2](../../../../../../assets/noise_cells_4_v2_speed0.3_aniso0.6.gif "Celdas 4 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
