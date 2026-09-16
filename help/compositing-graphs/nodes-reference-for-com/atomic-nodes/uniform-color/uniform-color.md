---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ""
description: Utilice el nodo Color uniforme para generar texturas de color uniformes para crear rellenos de color sólido y capas base.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color uniforme
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 7%
---

# Color uniforme

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Nodo atómico: Uniform color](uniform-color.resources/comp_uniform_1.png "Atomic node: Color uniforme"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Genera un valor de escala de grises o de color plano.

Es un nodo simple que se utiliza muy a menudo como punto de partida para añadir colores o crear valores específicos.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="uniform-color.resources/uniform-color-tooltip.gif" alt="información sobre herramientas de uniforme de color" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>



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
| <b>Color de salida</b> *Float/Float4* | Selecciona el color plano que se va a utilizar en la imagen de salida.   Cuando se utiliza el modo de color &quot;Color&quot;, el canal del Alpha se utiliza para la opacidad, donde 0 es completamente transparente y 1 es completamente opaco. |


## Ejemplos

*Próximamente.*
