---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend.html"
breadcrumb-title: ""
description: Utilice el nodo Fusión para fusionar dos texturas mediante distintos modos de fusión para crear efectos compuestos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 8%
---

# Fusión

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Fusionar](blend.resources/comp_blend_1.png "nodo atómico: Fusionar")

</td>
<td style="border: 0;" valign="top">

Combina dos imágenes con un modo de fusión especificado y una máscara opcional.

Es el nodo más útil de todos los nodos atómicos, casi cualquier gráfico que se genere en [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) utilizará este nodo.

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="blend.resources/blend-tooltip.gif" alt="información sobre herramientas de blend" /></div>

Su funcionalidad es similar a tener dos capas una encima de la otra en [Substance 3D Painter](https://www.adobe.com/es/products/substance3d-painter.html) o [Photoshop](https://www.adobe.com/ch_fr/products/photoshop/landpa.html), que se mezclan por el modo de fusión establecido en la capa superior.

>[!TIP]
>
> Obtenga información sobre los modos de fusión disponibles en el nodo Fusión en [esta página dedicada](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md).



## Parámetros

|  |  |
| --- | --- |
| <b>Opacidad</b> *Flotador* | Opacidad de la capa frontal que se fusiona con el fondo. Funciona independientemente de la entrada Opacidad y actúa como un multiplicador adicional a la misma. |
| <b>Modo de fusión</b> *Entero* [Estático](../../../../glossary/glossary.md) | Define la operación de fusión que se va a utilizar.   Consulte la [página dedicada sobre los modos de fusión](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md). |
| <b>Fusión de Alpha</b> *Entero* [Estático](../../../../glossary/glossary.md) | Determina el comportamiento de fusión cuando las entradas de color tienen canales de Alpha:<ul data-preserve-html="true"> <li data-preserve-html="true">Utilizar alfa de origen</li> <li data-preserve-html="true">Ignorar alfa</li> <li data-preserve-html="true">Fusión de alfa recto</li> <li data-preserve-html="true">Mezcla alfa premultiplicada</li> </ul> |
| <b>Área de recorte</b> *Float4* [Static](../../../../glossary/glossary.md) | Permite definir una región de recorte personalizada que se comporte como una máscara de opacidad adicional. Cualquier área recortada muestra solo el fondo. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Primer plano</b> *Escala de grises/Color* | Capa superior o frontal de la operación de fusión. |
| <b>Fondo</b> *Escala de grises/Color* PRINCIPAL | Capa inferior o de fondo de la operación de fusión. |
| <b>Opacidad</b> *Escala de grises* | Entrada opcional de máscara de Alpha. |

>[!IMPORTANT]
>
> Los nodos de mezcla tienen entradas dinámicas que cambian entre Escala de grises y Color en función de las conexiones.<b> Un nodo de fusión solo puede fusionar dos entradas del mismo tipo: </b>.
> 
> Si se conecta una entrada de color y escala de grises al primer plano y al fondo, se producirá una línea de conexión roja discontinua, lo que indica un error de cálculo.
> 
> Esta es la razón número uno por la que los nuevos usuarios tienen problemas con las conexiones en color o en escala de grises: asegúrese de que ambas conexiones son del mismo tipo.


## Ejemplos

*Próximamente.*
