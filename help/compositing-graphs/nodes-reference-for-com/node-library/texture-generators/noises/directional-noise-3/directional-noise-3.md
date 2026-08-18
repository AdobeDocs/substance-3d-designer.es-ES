---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-3.html"
breadcrumb-title: ''
description: Utilice el nodo Ruido direccional 3 para generar patrones de ruido direccional con tres octavas para crear texturas direccionales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RUIDO DIRECCIONAL 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 2%

---


# RUIDO DIRECCIONAL 3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruido direccional 3 - Icono](../../../../../../assets/directional_noise_3.png "Ruido direccional 3 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los <b>ruidos de Ruido direccional</b>.

Consulte también: [Ruido direccional 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md), [Ruido direccional 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md), [Ruido direccional 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

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
| Flotador <b>Ángulo</b> | El ángulo utilizado para establecer la dirección del ruido, en número de vueltas y comenzando desde la derecha horizontal. |
| Flotador <b>Ángulo aleatorio</b> | Cantidad máxima de variación aleatoria aplicada al valor <b>Angle</b>, en número de vueltas. |
| <b>Desplazamiento del azulejo</b> Float2 | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> Boolean | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido direccional 3 - Ejemplo 1](../../../../../../assets/directional_noise_3_1.png "Ruido direccional 3 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido direccional 3 - Ejemplo 2](../../../../../../assets/noise_directional_noise_3_v2_speed0.6_aniso0.gif "Ruido direccional 3 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido direccional 3 - Ejemplo 3](../../../../../../assets/noise_directional_noise_3_v2_speed0.6_aniso1.gif "Ruido direccional 3 - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido direccional 3 - Ejemplo 4](../../../../../../assets/noise_directional_noise_3_v2_speed0.3_aniso0.6.gif "Ruido direccional 3 - Ejemplo 4"){zoomable="yes"}

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
