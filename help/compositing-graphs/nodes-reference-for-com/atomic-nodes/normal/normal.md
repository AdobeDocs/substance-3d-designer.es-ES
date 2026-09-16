---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ""
description: Utilice el nodo Normal para procesar y manipular texturas de mapa normales para controlar los detalles y la iluminación de la superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 7%
---

# Normal

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Nodo atómico: Normal](normal.resources/comp_normal_1.png "Nodo atómico: Normal"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0;" valign="top">

Calcula un mapa de normales a partir de una imagen de escala de grises interpretada como un mapa de altura.

El nodo convierte un mapa de escala de grises de entrada en una salida de mapa Normal de espacio tangente. Dispone de varias opciones de usuario para definir la intensidad y la codificación.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="normal.resources/normal-tooltip.gif" alt="información sobre herramientas normal" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

Es un nodo muy útil que se utiliza a menudo para convertir entradas de mapas de height en mapas normales para materiales listos en tiempo real. Hay alternativas para encontrar en [Sobel Normal](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) y Height A Unidades Mundiales Normales.



## Parámetros

|  |  |
| --- | --- |
| <b>Intensidad</b> *Flotador* | Modifica la intensidad del mapa de height.   Establece la intensidad con la que se interpreta el mapa de height de entrada para convertirlo en normal. Según los mapas de entrada, los valores superiores a 100 tienen poco más efecto. |
| <b>Formato normal</b> *Booleano* | Invierte las coordenadas Y del mapa de height (OpenGL).   Define cómo se codifica el canal verde (Y). Básicamente un interruptor &quot;Flip Green/Y&quot;. |
| <b>Contenido del canal del Alpha</b> *Booleano* | Rellene el canal alfa del mapa normal con la textura de entrada.   Rellenar Alpha Con Entrada/Forzar Alpha A 1:  Esto permite que el canal del Alpha se establezca en sólido, en lugar de utilizar la entrada como un Alpha adicional. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises* PRINCIPAL | Imagen de entrada interpretada como un mapa de height. |


## Ejemplos

*Próximamente.*
