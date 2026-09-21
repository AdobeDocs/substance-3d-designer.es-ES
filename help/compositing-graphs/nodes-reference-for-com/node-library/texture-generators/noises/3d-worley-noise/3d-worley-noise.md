---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ""
description: Utilice el nodo Ruido Worley 3D para generar ruido Worley basado en la posición 3D para crear efectos de textura volumétrica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido Worley 3D
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 6%
---

# Ruido Worley 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-worley-noise.resources/3d-worley.png){width="128px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Uno de los ruidos más versátiles y avanzados de la biblioteca, genera un ruido Worley en el espacio 3D, basado en un mapa de posición de entrada. Tiene muchas opciones que lo hacen mucho más potente que los ruidos basados en [Celdas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) o [Distancia](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md) estándar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>1 - 64</i> | Establezca la escala global del efecto. |
| <b>Tamaño</b> <i>0.0 - 1.0</i> | Realice escalas no uniformes en los ejes X, Y y Z por separado. |
| <b>Modo</b> <i>Euclidean, Manhattan, Chebyshev, Minkowski</i> | Cambie la métrica de distancia. Permite algunos tipos de ruido muy diferentes. |
| <b>Número de Minkowski</b> <i>0.0 - 20.0</i> | Solo con la métrica de distancia de Minkowski. Fusiones entre diferentes tipos de métricas. |
| <b>Estilo</b> <i>F1, F2, F2-F1, Borde, Color aleatorio</i> | Defina la matemática de combinación de métricas. Permite muchas más combinaciones. |
| <b>Ancho de borde</b> <i>0.0 - 1.0</i> | Cuando la función matemática de combinación de bordes está activa, controla la anchura del borde. |
| <b>Redondez</b> <i>0.0 - 1.0</i> | Sólo disponible en los modos F1, F2 y F2-F1. Establece la posición intermedia del nivel. |
| <b>Invertir</b> <i>Falso/Verdadero</i> | Invierte el resultado. |

## Ejemplos

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="3d-worley-noise.resources/3d-worley-ex04.png" class="modal-image" alt="Ruido Worley 3D - Ejemplo 1" />
        </td>
        <td style="border: 0;">
            <img src="3d-worley-noise.resources/3d-worley-ex03.png" class="modal-image" alt="Ruido Worley 3D - Ejemplo 2" />
        </td>
        <td style="border: 0;">
            <img src="3d-worley-noise.resources/3d-worley-ex02.png" class="modal-image" alt="Ruido Worley 3D - Ejemplo 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="3d-worley-noise.resources/3d-worley-ex01.png" class="modal-image" alt="Ruido Worley 3D - Ejemplo 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>
