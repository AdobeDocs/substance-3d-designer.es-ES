---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/levels.html"
breadcrumb-title: ""
description: Utilice el nodo Niveles para ajustar el brillo, el contraste y la gama tonal de las texturas para la corrección y mejora del color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Levels
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Niveles
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 3%
---

# Niveles

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Nodo atómico: Niveles](levels.resources/comp_levels_1.png "Nodo atómico: Niveles"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0;" valign="top">

Ajusta el rango tonal global y el equilibrio de color de las sombras, los tonos medios y las iluminaciones de una imagen.

El nodo Niveles permite reasignar los tonos de una entrada mediante la configuración de factores de reasignación de entrada y salida, presentados en una interfaz de histograma familiar de otros editores de imágenes 2D.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="levels.resources/levels-tooltip.gif" alt="información sobre herramientas niveles" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

Es uno de los nodos principales y más útiles de Substance 3D Designer y se utiliza con frecuencia para reasignar y ajustar valores en un gráfico, ya que proporciona la interfaz más precisa y precisa para cambiar valores.

Si bien es un nodo importante, para algunos casos de uso la interfaz puede ser un poco engorrosa, así que asegúrate de buscar [Niveles automáticos](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md), [Contraste/Luminosidad](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md) y [Análisis de histograma](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) para encontrar alternativas.



El nodo ofrece dos interfaces para ajustar sus valores: histograma y reguladores. Puede cambiar entre ellos con el botón derecho en la barra de encabezado &quot;Parámetros específicos&quot;:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

El botón amarillo resaltado alterna la interfaz entre los reguladores de valor del histograma (superior) (inferior)

</td>
<td width="66.67%" style="border: 0;" valign="top">

![](levels.resources/levels-2-1.png)

![](levels.resources/levels-1-1.png)

</td>
</tr>
</table>

|  |  |
| --- | --- |
| <b>Nivel bajo</b> *Float/Float4* | Define los niveles de iluminación baja de la imagen de entrada. Reasigna valores bajos de entrada para que se vuelvan negros completos. |
| <b>Nivel alto</b> *Float/Float4* | Define los niveles de resaltado de la imagen de entrada.  Reasigna valores altos de entrada para que se vuelvan blancos completos. |
| <b>Nivel a mediados de</b> *Float/Float4* | Define los niveles de medios tonos de la imagen de entrada.  Reasigna los valores medios de entrada para que se conviertan en gris medio. |
| <b>Nivel de salida bajo</b> *Float/Float4* | Define los niveles de iluminación baja de la imagen de salida.  Ajusta los valores de negro de salida para definir el límite. |
| <b>Nivel de iluminación de salida</b> *Flotante/Flotante4* | Define los niveles de resaltado de la imagen de salida.  Ajusta los valores de blanco de salida para definir el límite. |
| <b>Abrazadera intermedia</b> *Booleano* | Determina si el valor de entrada transformado se fija en [0, 1] antes de calcular el nivel de salida. |

## Guía de uso

Echa un vistazo a esta descripción general en vídeo del nodo Niveles y su editor de histogramas:

### Acciones rápidas

En la barra de encabezado &quot;Parámetros específicos&quot;, encontrará botones para acceder a las prácticas funciones del histograma:

![Acciones rápidas de nodos de niveles](levels.resources/levels-2.png "Acciones rápidas de nodos de niveles")

<b>1 - Invertir:</b> Intercambia los valores de los parámetros &#39;Nivel de salida bajo&#39; y &#39;Nivel de iluminación de salida&#39;.

<b>2 - Nivel automático:</b> Ajusta automáticamente los valores de los parámetros &quot;Nivel de baja iluminación de entrada&quot; y &quot;Nivel de iluminación de entrada&quot; respectivamente al valor más bajo y más alto presente en la imagen.

<b>3 - Interfaces de conmutación:</b> Cambia entre los editores de histograma y de regulador.

### Histograma

El editor del histograma está diseñado para ajustes visuales rápidos donde realmente no se necesitan valores precisos y exponer parámetros no es importante. En general, es la forma más rápida y sencilla de trabajar con Niveles.

![](levels.resources/levels-histo.gif)

En función del tipo de entrada (color o escala de grises), puede utilizar el menú desplegable situado sobre el histograma para elegir el canal que desea modificar.

### Reguladores

El editor de reguladores elimina cualquier editor visual y presenta solo reguladores numéricos, útiles principalmente si desea fijar o reasignar valores muy exactos, o si pretende [exponer cualquiera de estos parámetros](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), ya que esto solo es posible en el editor de reguladores.

Los reguladores cambian en función de una entrada de color o escala de grises: Las entradas de color crean 4 reguladores para cada canal RGBA por separado, la escala de grises solo tiene un único regulador, lo que facilita el trabajo. Consulte la lista de parámetros anterior para obtener una explicación de cada regulador.

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises/Color* PRINCIPAL | Imagen que se va a procesar. |


## Ejemplos

*Próximamente.*
