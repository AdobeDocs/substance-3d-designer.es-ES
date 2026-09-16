---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ""
description: Utilice el nodo Normal para procesar y manipular las texturas de mapa de normales para controlar los detalles e iluminación de la superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%
---

# Normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Normal](normal.resources/comp_normal_1.png "Nodo atómico: Normal")

</td>
<td style="border: 0;" valign="top">

Calcula un mapa de normales a partir de una imagen de escala de grises interpretada como un mapa de altura.

El nodo convierte un mapa de escala de grises de entrada en una salida de Mapa de normales de espacio tangente. Dispone de varias opciones de usuario para definir la intensidad y la codificación.

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="normal.resources/normal-tooltip.gif" alt="información sobre herramientas normal" /></div>

Es un nodo muy útil que se utiliza a menudo para convertir entradas de mapa de altura en mapas de normales para materiales listos en tiempo real. Hay alternativas para encontrar en [Sobel Normal](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) y Height A Unidades Mundiales Normales.



## Parámetros

|  |  |
| --- | --- |
| <b>Intensidad</b> *Flotante* | Modifica la intensidad del mapa de altura.   Establece la intensidad con la que se interpreta el mapa de altura de entrada para convertirlo en normal. Según los mapas de entrada, los valores superiores a 100 tienen poco más efecto. |
| <b>Formato normal</b> *Booleano* | Invierte las coordenadas Y del mapa de altura (OpenGL).   Define cómo se codifica el canal verde (Y). Básicamente un interruptor &quot;Flip Green/Y&quot;. |
| <b>Contenido de canal alfa</b> *Booleano* | Rellene el canal alfa del mapa de normales con la textura de entrada.   Rellenar Alpha Con Entrada/Forzar Alpha A 1:  Esto permite que el canal alfa se establezca en sólido, en lugar de utilizar la entrada como un Alpha adicional. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises* PRINCIPAL | Imagen de entrada interpretada como un mapa de altura. |


## Ejemplos

*Próximamente.*
