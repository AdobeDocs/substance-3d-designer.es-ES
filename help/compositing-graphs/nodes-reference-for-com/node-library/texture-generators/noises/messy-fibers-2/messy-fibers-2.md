---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-2.html"
breadcrumb-title: ''
description: Utilice el nodo Fibras sucias 2 para generar patrones de fibra intermedios para crear texturas tejidas y textiles.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fibras sucias 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# Fibras sucias 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fibras sucias 2 - Icono](../../../../../../assets/messy_fibers_2.png "Fibras sucias 2 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los ruidos estructurados de las <b>fibras desordenadas</b>.

Consulte también: [Fibras sucias 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md), [Fibras sucias 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-3/messy-fibers-3.md)

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
| <b>ángulo de anisotropía de desorden</b> <i>Flotante</i> | Controla la dirección del desplazamiento aplicado por el parámetro <b>Disorder</b> cuando el parámetro &#39;Disorder anisotropía&#39; no es cero. |
| <b>Ángulo</b> <i>Flotante</i> | Ángulo utilizado para definir la dirección de las roscas, en número de vueltas y comenzando desde la derecha horizontal. |
| <b>Ángulo aleatorio</b> <i>Flotante</i> | Cantidad máxima de variación aleatoria aplicada al valor <b>Angle</b>, en número de vueltas. |
| <b>Número de líneas</b> <i>Flotante</i> | Cantidad de mosaico aplicado a las roscas base, donde un valor más alto da como resultado roscas más densas y delgadas. |
| <b>Desplazamiento de mosaico</b> <i>Flotante2</i> | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibras sucias 2 - Ejemplo 1](../../../../../../assets/messy_fibers_2_1.png "Fibras sucias 2 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibras sucias 2 - Ejemplo 2](../../../../../../assets/noise_messy_fibers_2_v2_speed0.1_aniso0.gif "Fibras sucias 2 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibras sucias 2 - Ejemplo 3](../../../../../../assets/noise_messy_fibers_2_v2_speed0.1_aniso1.gif "Fibras sucias 2 - Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibras sucias 2 - Ejemplo 4](../../../../../../assets/noise_messy_fibers_2_v2_speed0.1_aniso0.6.gif "Fibras sucias 2 - Ejemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
