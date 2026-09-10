---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/bnw-spots-1.html"
breadcrumb-title: ''
description: Utilice el nodo Manchas BnW 1 para generar patrones de manchas en blanco y negro para crear variaciones de textura y máscaras de detalles.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > BnW spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: BnW spots 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# BnW spots 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Manchas BnW 1 - Icono](bnw-spots-1.resources/bnw_spots_1.png "Manchas BnW 1 - Icono"){width="200px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Variación de los ruidos de los puntos gruesos <b>blanco y negro (BnW)</b>.

Consulte también: [Puntos BnW 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-2/bnw-spots-2.md), [Puntos BnW 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-3/bnw-spots-3.md)

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
| <b>Desorden</b> <i>Flotante</i> | Desplaza los ingredientes del ruido.    Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> <i>Flotante</i> | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.    Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |
| <b>anisotropía de desorden</b> <i>Flotante</i> | Controla el intervalo de direcciones del desplazamiento aplicado por el parámetro <b>Disorder</b>, donde un valor más alto produce una dirección más estrecha y definida.    La dirección se controla mediante el parámetro <b>Ángulo de anisotropía de desorden</b>. |
| <b>ángulo de anisotropía de desorden</b> <i>Flotador</i> | Controla la dirección del desplazamiento aplicado por el parámetro <b>Disorder</b>, cuando el parámetro <b>Disorder anisotropía</b> no es cero. |
| <b>Rugosidad</b> <i>Flotador</i> | El equilibrio de las octavas de ruido, donde un valor más alto hará que las octavas de mayor frecuencia sean más visibles. |
| <b>Desplazamiento de mosaico</b> <i>Float2</i> | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Manchas BnW 1 - Ejemplo 1](bnw-spots-1.resources/bnw_spots_1_1.png "Manchas BnW 1 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Manchas BnW 1 - Ejemplo 2](bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.6_aniso0.gif "Manchas BnW 1 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Manchas BnW 1 - Ejemplo 3](bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.6_aniso1.gif "Manchas BnW 1 - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Manchas BnW 1 - Ejemplo 4](bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.3_aniso0.6.gif "Manchas BnW 1 - Ejemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
