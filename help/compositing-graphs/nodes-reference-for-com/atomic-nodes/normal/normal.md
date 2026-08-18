---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: Utilice el nodo Normal para procesar y manipular texturas de mapa normales para controlar los detalles y la iluminación de la superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# Normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Normal](../../../../assets/comp_normal_1.png "Nodo atómico: Normal"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Calcula un mapa de normales a partir de una imagen de escala de grises interpretada como un mapa de altura.

El nodo convierte un mapa de escala de grises de entrada en una salida de mapa Normal de espacio tangente. Dispone de varias opciones de usuario para definir la intensidad y la codificación.

</td>
</tr>
</table>

Es un nodo muy útil que se utiliza a menudo para convertir entradas de mapas de height en mapas normales para materiales listos en tiempo real. Hay alternativas para encontrar en [Sobel Normal](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) y Height A Unidades Mundiales Normales.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Conectores de salida

</td>
<td style="border: 0;" valign="top">

### Ejemplos

</td>
</tr>
</table>

## Parámetros

|  |  |
| --- | --- |
| <b>Intensidad</b> *Flotador* | Modifica la intensidad del mapa de height.   Establece la intensidad con la que se interpreta el mapa de height de entrada para convertirlo en normal. Según los mapas de entrada, los valores superiores a 100 tienen poco más efecto. |
| <b>Formato normal</b> *Booleano* | Invierte las coordenadas Y del mapa de height (OpenGL).   Define cómo se codifica el canal verde (Y). Básicamente un interruptor &quot;Flip Green/Y&quot;. |
| <b>Contenido del canal del Alpha</b> *Booleano* | Rellene el canal alfa del mapa normal con la textura de entrada.   Rellenar Alpha Con Entrada/Forzar Alpha A 1:  Esto permite que el canal del Alpha se establezca en sólido, en lugar de utilizar la entrada como un Alpha adicional. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises* PRINCIPAL | Imagen de entrada interpretada como un mapa de height. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Color* |  |

## Ejemplos

*Próximamente.*
