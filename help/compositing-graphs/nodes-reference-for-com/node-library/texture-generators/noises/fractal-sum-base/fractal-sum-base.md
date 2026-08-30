---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: Utilice el nodo Base de Suma fractal para generar patrones de ruido fractal base para crear texturas orgánicas complejas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: base de suma fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# base de suma fractal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Base de Suma fractal - Icono](fractal-sum-base.resources/fractal_sum_base.png "Base de Suma fractal - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Ruido fractal personalizable con un rango y equilibrio de octavas ajustables.

La familia de ruidos <b>Suma fractal</b> se basa en este nodo.

Consulte también: [Suma fractal 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Suma fractal 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Suma fractal 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [Suma fractal 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>Rugosidad</b> <i>Flotador</i> | El equilibrio de las octavas de ruido.    Un valor más alto hará que las octavas de frecuencia más alta sean más visibles. |
| <b>Mín. nivel</b> <i>Entero</i> | La octava mínima utilizada en el ruido.    Un valor más alto produce una frecuencia de ruido más alta. |
| <b>Máx. nivel</b> <i>Entero</i> | La octava máxima utilizada en el ruido.    Un valor más alto produce una frecuencia de ruido más alta. |
| <b>Desorden</b> <i>Flotador</i> | Desplaza los ingredientes del ruido.    Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> <i>Flotador</i> | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.    Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |
| <b>Contraste</b> <i>Flotador</i> | El contraste del resultado final. |
| <b>Opacidad global</b> <i>Flotador</i> | Opacidad de las octavas de ruido sumadas en el resultado final.    Un valor alto puede dar lugar a que las áreas se quemen hasta quedar blancas. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Base de Suma fractal - Ejemplo 1](fractal-sum-base.resources/fractal_sum_base_1.png "Base de Suma fractal - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Base de Suma fractal - Ejemplo 2](fractal-sum-base.resources/noise_fractal_sum_base_v2_speed0.6_aniso0.gif "Base de Suma fractal - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
