---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/distance.html"
breadcrumb-title: ""
description: Utilice el nodo Distancia para calcular mapas de distancia de formas para crear máscaras y efectos procedimientos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distancia
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 8%
---

# Distancia

<table>
<tr style="border: 0;">
<td width="20%" style="border: 0;" valign="top">

![Nodo atómico: Distancia](distance.resources/comp_distance_1.png "Nodo atómico: Distancia"){width="100%"}

</td>
<td style="border: 0;" valign="top">

Busca la posición del píxel blanco más cercano en una máscara y emite un degradado desde esa posición o el color en esa posición en una imagen de origen.

Este nodo crea un fundido lineal saliente (degradado) a partir de cualquier píxel del valor máximo de entrada superior a 0,5 en escala de grises.

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="distance.resources/distance-tooltip.gif" alt="información sobre herramientas de distancia" /></div>

El fundido exterior de expansión finalizará tan pronto como se encuentre con otra celda: nunca se superpondrán. Internamente, esto es realmente calcular y mostrar la distancia al píxel más cercano > 0,5, con el nodo de distancia definido como una abrazadera/máximo.

Un mapa de origen opcional permite combinar las celdas con la textura de un mapa de entrada secundario.

El nodo de distancia no es un nodo fácil de dominar, pero sus principales casos prácticos son la expansión de las máscaras existentes de una manera fiable (en comparación con el desenfoque y el ajuste del contraste), la generación de celdas de ruido de tipo Voronoi y el biselado de formas existentes con un perfil lineal nítido (que se puede reasignar más adelante).

Consulte los siguientes [ejemplos](#examples) para obtener más información.



## Parámetros

|  |  |
| --- | --- |
| <b>Modo de color</b> *Booleano* | Alterna entre una imagen de salida en escala de grises y en color. También cambia el tipo de entrada &quot;Entrada de origen&quot;. |
| <b>Distancia máxima</b> *Flotante* | Ajusta la distancia máxima para detectar el borde más cercano de la máscara, en píxeles. |
| <b>Combinar origen/distancia</b> *Booleano* | Determine cómo se combina la &#39;entrada de origen&#39; opcional con las celdas finales.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Combinar:</i> Combina el valor de &quot;entrada de origen&quot; con la máscara lineal de atenuación. Si la entrada &quot;Source input&quot; está conectada, su valor se combina con la distancia calculada.</li> <li data-preserve-html="true"><i>Solo origen:</i> Solo genera color sólido a partir de la &#39;entrada de origen&#39;.</li> </ul> |
| <b>Modo de distancia</b> *Entero* | Selecciona el método que calcula la distancia al borde más cercano de la máscara extraída:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Euclidean:</i> Suma de diferencias X/Y cuadradas.</li> <li data-preserve-html="true"><i>Manhattan:</i> Suma de valores absolutos de diferencias X/Y.</li> <li data-preserve-html="true"><i>Chebyshev:</i> Máximo de valores absolutos de diferencias X/Y.</li> </ul>  <div><img alt="Ejemplos del modo Distancia" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_copy_copy_copy_row-yj03rtt-column-0i13nfd_image" src="distance.resources/distance-comparison.jpg" title="Ejemplos del modo Distancia"/></div> |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada de máscara</b> *Escala de grises* PRINCIPAL | Una máscara de escala de grises, cuyos bordes deben calcularse como un valor de distancia.   Se extrae una máscara binaria de la imagen, utilizando un valor de umbral de 0,5, donde todos los valores por encima de este umbral son blancos y todos los valores por debajo son negros. |
| <b>Entrada de origen</b> *Color/Escala de grises* | Imagen en escala de grises opcional desde la que se debe copiar el valor de píxel en el borde más cercano de &quot;Entrada de máscara&quot;. |


## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex01.gif)

</td>
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex02.gif)

</td>
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex03.gif)

</td>
</tr>
</table>
