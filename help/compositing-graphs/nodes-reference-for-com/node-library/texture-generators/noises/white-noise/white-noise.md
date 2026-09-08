---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: Utilice el nodo Ruido blanco para generar patrones de ruido blanco para crear variaciones de textura y efectos aleatorios.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido blanco
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# Ruido blanco

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruido blanco - Icono](../../../../../../assets/white_noise_v2.png "Ruido blanco - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera un ruido blanco mediante uno de los tres métodos que tienen como objetivo diferentes formas de histograma: uniforme, gaussiano y triangular.

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
| <b>Distribución de ruido</b> <i>Entero</i> | El método de distribución de los ingredientes para seleccionar una forma de histograma:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Uniforme:</i> Un histograma plano.</li> <li data-preserve-html="true"><i>Gaussiano:</i> Histograma que representa una distribución normal, similar a una curva de campana.</li> <li data-preserve-html="true"><i>Triángulo:</i> Un histograma triangular.</li> </ul> |
| <b>Desorden</b> <i>Flotador</i> | Desplaza los ingredientes del ruido.    Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> <i>Flotador</i> | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.    Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido blanco - Ejemplo 1](../../../../../../assets/white_noise_v2_1.png "Ruido blanco - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido blanco - Ejemplo 2](../../../../../../assets/white_noise_v2_speed0.6_aniso0.gif "Ruido blanco - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
