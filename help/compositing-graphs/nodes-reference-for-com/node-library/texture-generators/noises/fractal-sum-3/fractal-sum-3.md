---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-3.html"
breadcrumb-title: ''
description: Utilice el nodo de la Suma fractal 3 para generar ruido fractal con tres octavas para crear patrones de texturas orgánicas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SUMA FRACTAL 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# SUMA FRACTAL 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Suma fractal 3 - Icono](fractal-sum-3.resources/fractal-sum-3-01.png "Suma fractal 3 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una variación de los <b>ruidos de Suma fractal</b>.

Consulte también: [base de Sumas fractal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md), [Suma fractal 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Suma fractal 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Suma fractal 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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

![Suma fractal 3 - Ejemplo 1](fractal-sum-3.resources/fractal-sum-3-02.png "Suma fractal 3 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Suma fractal 3 - Ejemplo 2](fractal-sum-3.resources/fractal-sum-3-03.gif "Suma fractal 3 - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
