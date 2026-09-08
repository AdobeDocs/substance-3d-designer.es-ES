---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ''
description: Utilice el nodo Mezcla de canales para reorganizar los canales de color en las texturas para crear efectos de color e intercambiar canales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Orden aleatorio de canales
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---


# Orden aleatorio de canales

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Reorganización de canales](../../../../assets/comp_shuffle.png "Nodo atómico: Mezcla de canales"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Reorganiza los canales de color de una o dos imágenes de entrada en la imagen de salida.

Es decir, toma dos entradas y le permite devolver una salida donde cualquiera de los canales Rojo, Verde, Azul y Alfa se intercambian o se establecen en cualquiera de los canales de la entrada.

Básicamente, te permite empaquetar e intercambiar canales de RGB de cualquier forma posible. Las entradas de escala de grises se tratan como si fueran de color: El rojo, el verde, el azul y el Alpha devuelven los mismos valores.

</td>
</tr>
</table>

El Mezcla de canales tiene opciones básicas, pero en la mayoría de los casos de empaquetado de canales o de eliminación y configuración de canales alfa es más rápido usar [Combinación RGBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md), [División RGBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), [Combinación de Alpha](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md) y [División de Alpha](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md). Están configurados para realizar acciones predeterminadas que no requieren cambiar varios parámetros y convertir a escala de grises posteriormente. Si buscas una versión más avanzada con más opciones de fusión, consulta [Mezclador de canales](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md).

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
| <b>Canal rojo</b> *Entero* | Elija el canal de origen que se insertará en el canal rojo de la imagen de salida. |
| <b>Canal verde</b> *Entero* | Elija el canal de origen que se insertará en el canal verde de la imagen de salida. |
| <b>Canal azul</b> *Entero* | Elija el canal de origen que se insertará en el canal azul de la imagen de salida. |
| <b>canal de Alpha</b> *Entero* | Elija el canal de origen que se insertará en el canal alfa de la imagen de salida. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada 1</b> *Color/Escala de grises* PRINCIPAL | Imagen de entrada principal. |
| <b>Entrada 2</b> *Color/Escala de grises* | Imagen de entrada secundaria. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises/Color* |  |

## Ejemplos

*Próximamente.*
