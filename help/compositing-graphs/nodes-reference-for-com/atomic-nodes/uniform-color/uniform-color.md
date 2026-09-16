---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ""
description: Utilice el nodo Color uniforme para generar texturas de color uniforme para crear rellenos de color sólido y capas base.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color uniforme
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 7%
---

# Color uniforme

<table>
<tr style="border: 0;">
<td style="border: 0; width: 30%; vertical-align: top">

![Nodo atómico: Color uniforme](uniform-color.resources/comp_uniform_1.png "Nodo atómico: Color uniforme")

</td>
<td style="border: 0; vertical-align: top">

Genera un valor de escala de grises o de color plano.

Es un nodo simple que se utiliza muy a menudo como punto de partida para añadir colores o crear valores específicos.

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="uniform-color.resources/uniform-color-tooltip.gif" alt="información sobre herramientas de uniforme de color" /></div>


>[!TIP]
>
> Optimización del rendimiento
> 
> Estos dos ajustes reducen el tiempo de cálculo del nodo y el espacio de memoria:
> 
> * Si se necesita un valor de escala de grises, asegúrese de cambiar el [modo de color](#parameters) del nodo a &#39;Escala de grises&#39;.
> * Como el resultado del nodo es un color plano, puede utilizar la resolución más baja posible. Establezca el parámetro &#39;[Output size](../../../../compositing-graphs/output-size/output-size.md)&#39; del nodo para usar el [método de herencia](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) &#39;Absoluto&#39; y una resolución de 16x16 píxeles.


## Parámetros

|  |  |
| --- | --- |
| <b>Modo de color</b> *Booleano* | Alterna entre una imagen de salida en escala de grises y en color. |
| <b>Color de salida</b> *Flotante/Flotante4* | Selecciona el color plano que se va a utilizar en la imagen de salida.   Cuando se utiliza el modo de color &quot;Color&quot;, el canal alfa se utiliza para la opacidad, donde 0 es totalmente transparente y 1 es completamente opaco. |


## Ejemplos

*Próximamente.*
