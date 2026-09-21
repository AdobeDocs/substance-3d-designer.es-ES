---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-3.html"
breadcrumb-title: ""
description: Utilice el nodo Messy Fibers 3 para generar patrones de fibra complejos para crear efectos de texturas textiles y de tejidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fibras sucias 3
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%
---

# Fibras sucias 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fibras sucias 3 - Icono](messy-fibers-3.resources/messy_fibers_3.png "Fibras sucias 3 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los ruidos estructurados de las <b>fibras desordenadas</b>.

Consulte también: [Fibras sucias 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md), [Fibras sucias 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md)

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
| <b>ángulo de anisotropía de desorden</b> <i>Flotador</i> | Controla la dirección del desplazamiento aplicado por el parámetro <b>Disorder</b> cuando el parámetro &#39;Disorder anisotropía&#39; no es cero. |
| <b>Ángulo</b> <i>Flotador</i> | Ángulo utilizado para definir la dirección de las roscas, en número de vueltas y comenzando desde la derecha horizontal. |
| <b>Ángulo aleatorio</b> <i>Flotador</i> | Cantidad máxima de variación aleatoria aplicada al valor <b>Angle</b>, en número de vueltas. |
| <b>Luminancia aleatoria</b> <i>Flotador</i> | Rango de luminancia restado aleatoriamente de las roscas, donde 1 es el rango completo. |
| <b>Desplazamiento de mosaico</b> <i>Float2</i> | Controla la posición de la parte del plano infinito utilizada para procesar el ruido. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="messy-fibers-3.resources/messy_fibers_3_1.png" class="modal-image" alt="Fibras sucias 3 - Ejemplo 1" />
        </td>
        <td style="border: 0;">
            <img src="messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso0.gif" class="modal-image" alt="Fibras sucias 3 - Ejemplo 2" />
        </td>
        <td style="border: 0;">
            <img src="messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso1.gif" class="modal-image" alt="Fibras sucias 3 - Ejemplo 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="messy-fibers-3.resources/noise_messy_fibers_3_v2_speed0.1_aniso0.6.gif" class="modal-image" alt="Fibras sucias 3 - Ejemplo 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>
