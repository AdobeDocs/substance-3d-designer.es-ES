---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: Utilice el nodo Scratches direccionales para crear patrones de rayado direccionales para añadir efectos de desgaste y daños a los materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rasguños direccionales
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---


# Rasguños direccionales

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Arañazos direccionales - Icono](../../../../../../assets/directional_scratches.png "Arañazos direccionales - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dispersión aleatoria de patrones de arañazos con ángulo y tamaño ajustables.

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
| Flotador <b>Ángulo</b> | El ángulo utilizado para establecer la dirección de los arañazos, en número de vueltas y comenzando desde la derecha horizontal. |
| Flotador <b>Ángulo aleatorio</b> | Cantidad máxima de variación aleatoria aplicada al valor <b>Angle</b>, en número de vueltas. |
| <b>Cantidad de patrón</b> Float | Un multiplicador para la cantidad de patrones de arañazos que se están dispersando. |
| <b>Tamaño de patrón</b> Float2 | Tamaño del cuadro delimitador del motivo de borrador.    El valor Y controla la longitud máxima de los arañazos. |
| <b>Tamaño de patrón aleatorio</b> Float2 | Un multiplicador para la cantidad aleatoria de reducción de escala aplicada a los arañazos.    El valor Y se aplica a la longitud de los arañazos. |
| <b>Desplazamiento del azulejo</b> Float2 | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> Boolean | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 1](../../../../../../assets/directional_scratches_1.png "Arañazos direccionales - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 2](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.gif "Arañazos direccionales - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 3](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.6.gif "Arañazos direccionales - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 4](../../../../../../assets/noise-directional-scrat-1.gif "Arañazos direccionales - Ejemplo 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 5](../../../../../../assets/noise-directional-scrat-2.gif "Arañazos direccionales - Ejemplo 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



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
