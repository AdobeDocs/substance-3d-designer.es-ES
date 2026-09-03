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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# Rasguños direccionales

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Arañazos direccionales - Icono](directional-scratches.resources/directional-scratches-01.png "Arañazos direccionales - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dispersión aleatoria de patrones de arañazos con ángulo y tamaño ajustables.

</td>
</tr>
</table>

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
| <b>anisotropía de desorden</b> <i>Flotador</i> | Controla el intervalo de direcciones del desplazamiento aplicado por el parámetro <b>Disorder</b>, donde un valor más alto produce una dirección más estrecha y definida.    La dirección se controla mediante el parámetro <b>Ángulo de anisotropía de desorden</b>. |
| <b>ángulo de anisotropía de desorden</b> <i>Flotador</i> | Controla la dirección del desplazamiento aplicado por el parámetro <b>Disorder</b>, cuando el parámetro <b>Disorder anisotropía</b> no es cero. |
| <b>Ángulo</b> <i>Flotador</i> | El ángulo utilizado para establecer la dirección de los arañazos, en número de vueltas y comenzando desde la derecha horizontal. |
| <b>Ángulo aleatorio</b> <i>Flotador</i> | Cantidad máxima de variación aleatoria aplicada al valor <b>Angle</b>, en número de vueltas. |
| <b>Cantidad de patrón</b> <i>Flotador</i> | Un multiplicador para la cantidad de patrones de arañazos que se están dispersando. |
| <b>Tamaño de trama</b> <i>Float2</i> | Tamaño del cuadro delimitador del motivo de borrador.    El valor Y controla la longitud máxima de los arañazos. |
| <b>Tamaño de patrón aleatorio</b> <i>Float2</i> | Un multiplicador para la cantidad aleatoria de reducción de escala aplicada a los arañazos.    El valor Y se aplica a la longitud de los arañazos. |
| <b>Desplazamiento de mosaico</b> <i>Float2</i> | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 1](directional-scratches.resources/directional-scratches-02.png "Arañazos direccionales - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 2](directional-scratches.resources/directional-scratches-03.gif "Arañazos direccionales - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 3](directional-scratches.resources/directional-scratches-04.gif "Arañazos direccionales - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 4](directional-scratches.resources/directional-scratches-05.gif "Arañazos direccionales - Ejemplo 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arañazos direccionales - Ejemplo 5](directional-scratches.resources/directional-scratches-06.gif "Arañazos direccionales - Ejemplo 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
