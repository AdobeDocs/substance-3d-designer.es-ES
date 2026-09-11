---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-1.html"
breadcrumb-title: ''
description: Utilice el nodo Suma fractal 1 para generar patrones de ruido fractal sumando varias octavas para crear texturas detalladas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SUMA FRACTAL 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1241ebb4d1e67c9ed9d86285a6397ddc335e0f37
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---


# SUMA FRACTAL 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Suma fractal 1 - Icono](fractal-sum-1.resources/fractal_sum_1.png "Suma fractal 1 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los <b>ruidos de Suma fractal</b>.

Consulte también: [base de Sumas fractal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md), [Suma fractal 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Suma fractal 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [Suma fractal 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>Desorden</b> <i>Flotador</i> | Desplaza los ingredientes del ruido.    Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> <i>Flotador</i> | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.    Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Suma fractal 1 - Ejemplo 1](fractal-sum-1.resources/fractal_sum_1_1.png "Suma fractal 1 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Suma fractal 1 - Ejemplo 2](fractal-sum-1.resources/noise_fractal_sum_1_v2_speed0.6_aniso0.gif "Suma fractal 1 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
