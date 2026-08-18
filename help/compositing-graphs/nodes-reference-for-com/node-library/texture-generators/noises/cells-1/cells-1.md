---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-1.html"
breadcrumb-title: ''
description: Usa el nodo Celdas 1 para generar patrones celulares básicos para crear efectos de textura orgánica y biológica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELDAS 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 1%

---


# CELDAS 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Celdas 1 - Icono](../../../../../../assets/cells_1.png "Celdas 1 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los <b>Celdas</b> ruidos de pared.

Los patrones seleccionados por el usuario se dispersan y se superponen mediante un modo de fusión Máx.

Vea también: [Celdas 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Celdas 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md), [Celdas 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| Flotador <b>Disorder</b> | Desplaza los ingredientes del ruido.    Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> Flotador | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.    Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |
| Flotador <b>anisotropía de desorden</b> | Controla el intervalo de direcciones del desplazamiento aplicado por el parámetro <b>Disorder</b>, donde un valor más alto produce una dirección más estrecha y definida.    La dirección se controla mediante el parámetro <b>Ángulo de anisotropía de desorden</b>. |
| <b>Ángulo de anisotropía del desorden</b> Flotante | Controla la dirección del desplazamiento aplicado por el parámetro <b>Disorder</b> cuando el parámetro &#39;Disorder anisotropía&#39; no es cero. |
| Entero <b>Pattern</b> | Forma base dispersa en la imagen generada. |
| <b>Tamaño de patrón</b> Float2 | Un multiplicador para el tamaño de un patrón disperso en su celda., donde 1.0 es el rango completo de la celda. |
| <b>Escala de patrón</b> Float | Un multiplicador para <b>Pattern size</b>, donde 1.0 es el tamaño completo. |
| Flotador <b>aleatorio de luminancia</b> | Rango de luminancia restado aleatoriamente de las celdas, donde 1 es el rango completo. |
| Flotador <b>Ángulo</b> | El ángulo utilizado para establecer la dirección de las celdas, en número de vueltas y comenzando desde la derecha horizontal. |
| Flotador <b>Ángulo aleatorio</b> | Cantidad máxima de variación aleatoria aplicada al valor <b>Angle</b>, en número de vueltas. |
| <b>Desplazamiento del azulejo</b> Float2 | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> Boolean | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Celdas 1 - Ejemplo 1](../../../../../../assets/cells_1_1.png "Celdas 1 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Celdas 1 - Ejemplo 2](../../../../../../assets/noise_cells_1_v2_speed0.3_aniso0.3.gif "Celdas 1 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Celdas 1 - Ejemplo 3](../../../../../../assets/noise_cells_1_v2_speed0.5_aniso0.6.gif "Celdas 1 - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Celdas 1 - Ejemplo 4](../../../../../../assets/noise_cells_1_v2_speed0.3_aniso0.6.gif "Celdas 1 - Ejemplo 4"){zoomable="yes"}

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
