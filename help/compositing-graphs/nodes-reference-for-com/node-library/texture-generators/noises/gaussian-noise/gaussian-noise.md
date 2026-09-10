---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-noise.html"
breadcrumb-title: ''
description: Usa el nodo Ruido gaussiano para generar patrones de ruido distribuidos gaussianos para crear texturas y variaciones orgánicas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido gaussiano
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# Ruido gaussiano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruido gaussiano - Icono](gaussian-noise.resources/gaussian_noise-1.png "Ruido gaussiano - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Ruido suave derivado de la combinación de degradados en los que los valores pasan de negro a blanco después de una distribución normal, similar a la curva de una campana.

Consulte también: [Manchas gaussianas 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-1/gaussian-spots-1.md), [Manchas gaussianas 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-2/gaussian-spots-2.md)

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
| <b>anisotropía de desorden</b> <i>Flotador</i> | Controla el intervalo de direcciones del desplazamiento aplicado por el parámetro <b>Disorder</b>, donde un valor más alto produce una dirección más estrecha y definida.    La dirección está controlada por el parámetro <b>ángulo de anisotropía de desorden</b>. |
| <b>ángulo de anisotropía de desorden</b> <i>Flotante</i> | Controla la dirección del desplazamiento aplicado por el parámetro <b>Disorder</b>, cuando el parámetro <b>Disorder anisotropía</b> no es cero. |
| <b>Desplazamiento de mosaico</b> <i>Flotante2</i> | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido gaussiano - Ejemplo 1](gaussian-noise.resources/gaussian_noise-1_1.png "Ruido gaussiano - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido gaussiano - Ejemplo 2](gaussian-noise.resources/noise_gaussian_noise_v2_speed0.6_aniso0.gif "Ruido gaussiano - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido gaussiano - Ejemplo 3](gaussian-noise.resources/noise_gaussian_noise_v2_speed0.6_aniso1.gif "Ruido gaussiano - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido gaussiano - Ejemplo 4](gaussian-noise.resources/noise_gaussian_noise_v2_speed0.3_aniso0.6.gif "Ruido gaussiano - Ejemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
