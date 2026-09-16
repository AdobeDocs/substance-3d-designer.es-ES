---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ""
description: Utilice el nodo Deformar para aplicar efectos de distorsión a las texturas para crear efectos de deformación y desplazamiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deformar
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 9%
---

# Deformar

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Nodo atómico: Deformar](warp.resources/comp_warp_1.png "nodo atómico: Deformar"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0;" valign="top">

Desplaza los valores de píxeles de la imagen de entrada en función de las pendientes calculadas a partir de una entrada de degradado independiente, lo que provoca una deformación.

A diferencia de la Deformación direccional, este nodo se aleja uniformemente de las áreas blancas, en una dirección definida por la pendiente o el degradado de la Entrada de degradado.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="warp.resources/warp-tooltip.gif" alt="información sobre herramientas de deformación" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

El nodo puede ser un poco complicado de trabajar, ya que el resultado del efecto depende en gran medida de la entrada de degradado: los pequeños ajustes en el degradado pueden suponer una gran diferencia visual con los mismos valores de intensidad. Asegúrate de jugar con el contraste, la luminancia y la escala de la entrada de degradado, así como con el regulador de intensidad de este nodo.

Si está familiarizado con los mapas normales, puede imaginar que el funcionamiento de este nodo es similar a convertir la entrada de degradado en un [mapa normal](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) y, a continuación, distorsionar la entrada base en la dirección definida por los vectores del mapa normal. De hecho, lo mismo se puede lograr con [Deformación vectorial](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md). También se pueden encontrar efectos similares en [Desenfoque de Pendiente](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).



## Parámetros

|  |  |
| --- | --- |
| <b>Intensidad</b> *Flotador* | Define la intensidad de la deformación. |
| <b>Modo de filtrado de entrada</b> *Booleano* | Controla si se utiliza el filtrado más cercano o bilineal para muestrear Input. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises/Color* PRINCIPAL | La imagen en color o en escala de grises. |
| <b>Entrada de degradado</b> *Escala de grises* | La pendiente del degradado de la imagen de entrada en escala de grises determina el efecto de deformación en la imagen de salida. |


## Ejemplos

*Próximamente.*
