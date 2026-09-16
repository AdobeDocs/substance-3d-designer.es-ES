---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/grayscale-conversion.html"
breadcrumb-title: ""
description: Utilice el nodo Conversión de escala de grises para convertir texturas de color a escala de grises mediante distintos métodos de conversión.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Grayscale conversion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conversión de escala de grises
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 7%
---

# Conversión de escala de grises

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Nodo atómico: Conversión de escala de grises](grayscale-conversion.resources/comp_grayscaleconversion_1.png "Nodo atómico: Conversión en escala de grises"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Convierte una imagen en color a escala de grises ponderando la luminancia de cada canal de color.

Este nodo se puede utilizar como un método optimizado para extraer un canal de escala de grises de una imagen en color, estableciendo todos los valores de &#39;Grosores de canal&#39; en 0, excepto el canal deseado, que debe establecerse en 1.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="grayscale-conversion.resources/grayscale-conversion-tooltip.gif" alt="información sobre herramientas de conversión de escala de grises" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

La mayoría de los nodos se pueden configurar para que se impriman en escala de grises o en color, donde se prefiere el primero por razones de sencillez y rendimiento.

De hecho, se recomienda trabajar en escala de grises desde el principio y colorear las imágenes más adelante en el flujo de trabajo, utilizando, por ejemplo, un nodo [Mapa de degradado](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md).

Esto significa que, por lo general, un nodo de conversión de escala de grises solo se reserva para los casos en los que desee convertir específicamente una imagen en color a escala de grises. En esos casos, echa un vistazo a [Conversión avanzada de escala de grises](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/grayscale-conversion-adv/grayscale-conversion-advanced.md) y [Color para enmascarar](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-to-mask/color-to-mask.md).



## Parámetros

|  |  |
| --- | --- |
| <b>Grosores de canal</b> *Float4* | Define el grosor de cada uno de los canales RGBA en la conversión de escala de grises.   De forma predeterminada, se realiza una división uniforme entre los canales del RGB. |
| <b>Acoplar alfa</b> *Booleano* | Establece el comportamiento del Alpha en el resultado final de la escala de grises, ya que los valores de escala de grises no pueden contener información del Alpha.   Cuando es *True*, la conversión de escala de grises se multiplica por el canal Alpha de la imagen de entrada |
| <b>Valor de fondo</b> *Flotador* | Establece el valor de fondo base cuando la entrada tiene una máscara alfa. Es decir, determina qué píxeles deben tratarse como transparentes.   *Disponible cuando &#39;Acoplar alfa&#39; está establecido en &#39;Verdadero&#39;.* |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Color* PRINCIPAL | La imagen de color que se va a procesar. |


## Ejemplos

*Próximamente.*
