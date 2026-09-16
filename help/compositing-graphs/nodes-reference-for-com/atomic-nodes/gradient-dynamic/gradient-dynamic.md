---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ""
description: Utilice el nodo Degradado (dinámico) para crear degradados dinámicos que se puedan controlar mediante valores y parámetros de entrada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Degradado (dinámico)
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 8%
---

# Degradado (dinámico)

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Nodo atómico: Dinámica de degradado](gradient-dynamic.resources/comp_dyngradient_1.png "Nodo atómico: Dinámica de degradado"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Reasigna los valores de escala de grises de una imagen utilizando un degradado proporcionado por una fila o columna de píxeles de otra imagen.

Sirve como una ligera alternativa al nodo de degradado, pero a diferencia del nodo de degradado, las teclas de color de degradado no se definen internamente, sino que proceden de una entrada externa.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="gradient-dynamic.resources/gradient-dynamic-tooltip.gif" alt="información sobre herramientas dinámica de degradado" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Esto permite evitar principalmente el problema en el que los parámetros no se pueden exponer, ya que los parámetros de color se mueven fuera del nodo. Esto es lo que lo hace &quot;dinámico&quot;.

Aunque el Degradado (dinámico) no es un nodo difícil de usar por sí mismo, sus casos de uso son un poco más avanzados: la mayoría de los usos estándar se pueden cubrir mediante el nodo Degradado normal.

Este nodo entra en juego cuando está demasiado limitado por el sistema de claves del editor de degradados y desea que los colores y las posiciones de rampa se controlen mediante otras entradas, parámetros y partes del gráfico.

Como alternativa, el regulador Posición de entrada de degradado se puede utilizar para alternar entre varios degradados almacenados dentro de una sola entrada de pendiente.



## Parámetros

|  |  |
| --- | --- |
| <b>Direccionamiento de degradado</b> *Booleano* | Define si el degradado se repite (mosaico) o se sujeta.   Este parámetro determina cómo se controlan los píxeles de la entrada de escala de grises de los HDR de rango [0, 1]: sujetado o plegado hasta [0, 1]. |
| <b>Orientación del degradado</b> *Entero* | Define el eje a lo largo del cual se debe muestrear la entrada de degradado:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Horizontal:</i> Muestrear una fila de píxeles en el eje X.</li> <li data-preserve-html="true"><i>Vertical:</i> Muestrear una columna de píxeles en el eje Y.</li> </ul> |
| <b>Posición de entrada de degradado</b> *Flotador* | Posición normalizada de la fila o columna de píxeles que se van a muestrear en la &#39;Entrada de degradado&#39;. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada en escala de grises</b> *Escala de grises* PRINCIPAL | Imagen en escala de grises que se va a reasignar. |
| <b>Entrada de degradado</b> *Color/Escala de grises* | El degradado se muestra a partir de esta imagen |


## Ejemplos

*Próximamente.*
