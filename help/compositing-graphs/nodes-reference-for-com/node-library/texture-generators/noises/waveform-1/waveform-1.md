---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: Utilice el nodo Forma de onda 1 para generar patrones de forma de onda para crear texturas orgánicas y variaciones de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma de onda 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%

---


# Forma de onda 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Forma de onda 1 - Icono](waveform-1.resources/waveform_01_v2.png "Forma de onda 1 - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Disposición horizontal de patrones seleccionados por el usuario apilados en una forma similar a una forma de onda.

</td>
</tr>
</table>

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | El ruido generado como un mapa de bits en escala de grises. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ejemplos</b> <i>Entero</i> | La cantidad de patrones colocados a lo largo del eje X para dibujar la forma de onda, donde un valor más bajo da como resultado un aspecto más escalonado. |
| <b>Función</b> <i>Entero</i> | Función utilizada para dibujar la forma de onda.   Esto controla el tamaño vertical del motivo colocado en cada muestra:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Ruido de valor:</i> Una distribución aleatoria de valores</li> <li data-preserve-html="true"><i>Coseno:</i> Los valores siguen la progresión de una función de coseno</li> <li data-preserve-html="true"><i>Función personalizada:</i> Utilice una función creada por el usuario para controlar los valores</li> </ul> |
| <b>Función personalizada</b> <i>Flotador</i>   *Disponible cuando &#39;Function&#39; está establecido en &#39;Custom function&#39;* | Calcula el tamaño vertical del motivo colocado en cada muestra.   Variables disponibles:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> (<i>float</i>) Posición del patrón en el eje X. Se puede utilizar para seleccionar patrones.</li> </ul> |
| <b>Rugosidad</b> <i>Flotador</i> | Interpola entre una forma de onda limpia y suave con una que es más áspera y distribuida uniformemente.    Esto se puede considerar como señal limpia frente a ruido blanco. |
| <b>Escala</b> <i>Entero</i> | El espacio horizontal de la forma de onda visible en la imagen. |
| <b>Amplitud mínima</b> <i>Flotador</i> | El valor mínimo (o thickness) de la forma de onda. |
| <b>Amplitud máxima</b> <i>Flotador</i> | El valor máximo (o thickness) de la forma de onda. |
| <b>Ruido</b> <i>Flotador</i> | Aplica ruido a la forma de onda que resta aleatoriamente de su alcance vertical. |
| <b>Posición</b> <i>Entero</i> | Posición de la forma de onda en la imagen:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Centrado:</i> El origen está en el centro vertical de la imagen</li> <li data-preserve-html="true"><i>Inferior:</i> El origen está en la parte inferior de la imagen</li> </ul> |
| <b>Patrón</b> <i>Entero</i> | Patrón colocado en cada muestra de la forma de onda. |
| <b>Variación de patrón</b> <i>Flotador</i> | Existe un ajuste adicional disponible para algunos patrones. |
| <b>Desorden</b> <i>Flotador</i> | Desplaza los valores de la forma de onda.    Se puede utilizar para animarlo. |
| <b>Velocidad del desorden</b> <i>Flotador</i> | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.    Se puede utilizar para controlar la velocidad del desplazamiento al animar la forma de onda. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Forma de onda 1 - Ejemplo 1](waveform-1.resources/waveform_01_v2_speed0.1_aniso0.gif "Forma de onda 1 - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
