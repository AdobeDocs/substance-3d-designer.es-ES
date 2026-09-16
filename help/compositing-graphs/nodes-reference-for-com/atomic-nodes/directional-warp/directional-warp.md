---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ""
description: Utilice el nodo Deformación direccional para aplicar una distorsión direccional a las texturas para crear efectos de flujo y movimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deformación direccional
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 9%
---

# Deformación direccional

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Nodo atómico: Deformación direccional](directional-warp.resources/comp_directionalwarp_1.png "Nodo atómico: Deformación direccional"){width="100%"}

**<b>En:</b> nodos atómicos**

</td>
<td style="border: 0;" valign="top">

Desplaza los píxeles en una dirección especificada según un mapa de intensidad, lo que puede provocar una deformación.

Deforma una entrada en una dirección definida por el usuario, multiplicada por un mapa de intensidad definido por el usuario. Funciona de forma similar a Deformar, pero solo en una dirección específica.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="directional-warp.resources/directional-warp-tooltip.gif" alt="información sobre herramientas de deformación direccional" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

El nodo Deformar es un nodo bastante sencillo pero útil que sirve como base para otros efectos más avanzados. Hay alternativas más avanzadas, como otros nodos de interés relacionados, como [Desenfoque de Pendiente](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md) y [Deformación vectorial](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md).



## Parámetros

|  |  |
| --- | --- |
| <b>Intensidad</b> *Flotante* | Define la intensidad de la deformación. |
| <b>Ángulo de deformación</b> *Flotante* | Define el ángulo del efecto de deformación, en número de vueltas. |
| <b>modo de filtro de entrada</b> *Booleano* | Controla si se usa el filtrado más cercano o bilineal para muestrear <b>Input</b>. |
| <b>Desplazamiento del mapa de intensidad</b> *Flotante* | Este valor se resta de los valores de imagen <b>Intensity input</b>. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises/Color* PRINCIPAL | Imagen de entrada de color o escala de grises en la que se debe aplicar el efecto de deformación. |
| <b>Entrada de intensidad</b> *Escala de grises* | Imagen en escala de grises que define la cantidad de deformación que se debe aplicar a la imagen <b>Input</b>. |


## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Deformación direccional - Ejemplo 1](directional-warp.resources/dir-warp.gif "Deformación direccional - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Deformación direccional - Ejemplo 2](directional-warp.resources/dir-warp02.gif "Deformación direccional - Ejemplo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Deformación direccional - Ejemplo 3](directional-warp.resources/dir-warp03.gif "Deformación direccional - Ejemplo 3"){zoomable="yes"}

</td>
</tr>
</table>
