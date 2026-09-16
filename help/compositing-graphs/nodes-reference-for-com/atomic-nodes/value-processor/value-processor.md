---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ""
description: Utilice el nodo Procesador de valor para procesar y manipular valores de textura mediante operaciones matemáticas para ajustes personalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Procesador de valor
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%
---

# Procesador de valor

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Nodo atómico: Procesador de valores](value-processor.resources/comp_valueprocessor_1.png "Nodo atómico: Procesador de valores"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Calcula un [gráfico de funciones de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) y genera su resultado.

Es comparable a un [procesador de píxeles](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), con la diferencia de que no calcula una función para cada píxel, sino un solo valor y lo hace [disponible en un gráfico de Substance](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="value-processor.resources/value-processor-tooltip.gif" alt="información sobre herramientas del procesador de valores" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>


>[!TIP]
>
> Este nodo es un buen punto de partida para obtener información acerca de [gráficos de funciones de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Asimismo, tenga en cuenta que trabajar con este tipo de gráfico y realizar operaciones matemáticas es obligatorio para obtener cualquier elemento de este nodo.


## Parámetros

|  |  |
| --- | --- |
| <b>Función de procesador de valores</b> *Cualquier tipo de valor disponible* | [Gráfico de funciones de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) evaluado para calcular el valor de salida. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Imagen de entrada #</b> *Escala de grises/Color* | Use un nodo [Sample color](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) o [Sample grayscale](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) para obtener acceso a los valores de la entrada del índice especificado. |


## Ejemplos

*Próximamente.*
