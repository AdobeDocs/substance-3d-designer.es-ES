---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise.html"
breadcrumb-title: ''
description: Utilice el nodo Ruido de humedad para generar patrones de humedad y condensación para crear efectos de superficie húmeda.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido de humedad 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---


# Ruido de humedad 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruido de humedad 1 - Icono](../../../../../../assets/moisture_noise_1.png "Ruido de humedad 1 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Variación de los sonidos ricos y esponjosos de <b>Moisture</b>.

Discos de diferente dureza y tamaño y dispersos y añadir o restar del color de abajo, a partir de una base gris.

Consulte también: [Ruido de humedad 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise-2/moisture-noise-2.md)

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
| <b>Ángulo de anisotropía del desorden</b> Flotante | Controla la dirección del desplazamiento aplicado por el parámetro <b>Disorder</b>, cuando el parámetro <b>Disorder anisotropía</b> no es cero. |
| <b>Tamaño de patrón</b> Float2 | Un multiplicador para el tamaño de un patrón disperso., donde 1.0 es su tamaño de dispersión original. |
| <b>Ángulo del motivo</b> Flotante | Ángulo utilizado para definir la dirección del motivo disperso, en número de vueltas y comenzando desde la derecha horizontal. |
| <b>Ángulo de patrón aleatorio</b> Flotante | La cantidad máxima de variación aleatoria aplicada al valor <b>ángulo de motivo</b>, en número de vueltas. |
| <b>Opacidad global</b> Float | La opacidad de todos los ingredientes del ruido, donde 0.0 resulta en una base gris plano y 1.0 es el resultado de la adición o resta completa aplicada por los ingredientes. |
| <b>Desplazamiento del azulejo</b> Float2 | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> Boolean | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido de humedad 1 - Ejemplo 1](../../../../../../assets/moisture_noise_1_1.png "Ruido de humedad 1 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido de humedad 1 - Ejemplo 2](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso0.gif "Ruido de humedad 1 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido de humedad 1 - Ejemplo 3](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso1.gif "Ruido de humedad 1 - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido de humedad 1 - Ejemplo 4](../../../../../../assets/noise_moisture_noise_1_v2_speed0.3_aniso0.6.gif "Ruido de humedad 1 - Ejemplo 4"){zoomable="yes"}

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
