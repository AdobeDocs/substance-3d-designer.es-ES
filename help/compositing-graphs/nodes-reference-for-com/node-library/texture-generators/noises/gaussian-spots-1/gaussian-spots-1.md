---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-1.html"
breadcrumb-title: ''
description: Utilice el nodo Manchas gaussianas 1 para generar patrones de manchas gaussianas para crear variaciones y detalles de texturas orgánicas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Manchas gaussianas 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78ee271bee643682c3815dd1657d66accb2f31c4
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# Manchas gaussianas 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Manchas gaussianas 1 - Icono](../../../../../../assets/gaussian_spots_1.png "Manchas gaussianas 1 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los suaves <b>ruidos gaussianos</b>.\
Según el nodo [Ruido gaussiano](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), con degradados más estrechos.

Consulte también: [Manchas gaussianas 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-2/gaussian-spots-2.md)

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

![Manchas gaussianas 1 - Ejemplo 1](../../../../../../assets/gaussian_spots_1_1.png "Manchas gaussianas 1 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Manchas gaussianas 1 - Ejemplo 2](../../../../../../assets/noise_gaussian_spots_1_v2_speed0.6_aniso0.gif "Manchas gaussianas 1 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Manchas gaussianas 1 - Ejemplo 3](../../../../../../assets/noise_gaussian_spots_1_v2_speed0.6_aniso1.gif "Manchas gaussianas 1 - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Manchas gaussianas 1 - Ejemplo 4](../../../../../../assets/noise_gaussian_spots_1_v2_speed0.3_aniso0.6.gif "Manchas gaussianas 1 - Ejemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
