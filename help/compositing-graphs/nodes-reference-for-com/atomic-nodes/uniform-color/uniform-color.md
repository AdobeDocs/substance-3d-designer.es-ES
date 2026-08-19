---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ''
description: Utilice el nodo Color uniforme para generar texturas de color uniformes para crear rellenos de color sólido y capas base.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 8%

---


# Color uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Uniform color](../../../../assets/comp_uniform_1.png "Atomic node: Color uniforme"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Genera un valor de escala de grises o de color plano.

Es un nodo simple que se utiliza muy a menudo como punto de partida para añadir colores o crear valores específicos.

</td>
</tr>
</table>

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

>[!TIP]
>
> Optimización del rendimiento
> 
> Estos dos ajustes reducen el tiempo de cálculo del nodo y el espacio de memoria:
> 
> * Si se necesita un valor de escala de grises, asegúrese de cambiar el [modo de color](#parameters) del nodo a &#39;Escala de grises&#39;.
> * Como el resultado del nodo es un color plano, puede utilizar la resolución más baja posible. Establezca el parámetro &#39;[Output size](../../../../compositing-graphs/output-size/output-size.md)&#39; del nodo para usar el [método de herencia](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) &#39;Absoluto&#39; y una resolución de 16x16 píxeles.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parámetros

</td>
<td style="border: 0;" valign="top">

### Conectores de salida

</td>
<td style="border: 0;" valign="top">

### Ejemplos

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Parámetros

|  |  |
| --- | --- |
| <b>Modo de color</b> *Booleano* | Alterna entre una imagen de salida en escala de grises y en color. |
| <b>Color de salida</b> *Float/Float4* | Selecciona el color plano que se va a utilizar en la imagen de salida.   Cuando se utiliza el modo de color &quot;Color&quot;, el canal del Alpha se utiliza para la opacidad, donde 0 es completamente transparente y 1 es completamente opaco. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Color/Escala de grises* |  |

## Ejemplos

*Próximamente.*
