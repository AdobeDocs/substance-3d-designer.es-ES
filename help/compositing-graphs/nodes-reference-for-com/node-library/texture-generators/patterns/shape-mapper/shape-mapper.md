---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: Utilice el nodo Asignador de formas para asignar formas a texturas con transformaciones y posiciones personalizables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Asignador de formas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# Asignador de formas

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Asignador de formas - Icono](../../../../../../assets/shape_mapper.png "Asignador de formas - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Motivos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Proyecta una imagen de entrada a lo largo de un círculo o un polígono.

La proyección deforma la imagen para que siga el contorno de la forma y hace que se ajuste exactamente a una cantidad especificada de veces sin espacios.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Entradas

</td>
<td style="border: 0;" valign="top">

### Salidas

</td>
<td style="border: 0;" valign="top">

### Parámetros

</td>
<td style="border: 0;" valign="top">

### Ejemplos

</td>
</tr>
</table>

## Entradas

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises* | Patrón que debe colocarse a lo largo de la forma. |

## Salidas

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises* | Resultado de la proyección del motivo a lo largo de la forma, como un mapa de bits en escala de grises. |

## Parámetros

|  |  |
| --- | --- |
| Entero <b>Shape</b> | Define el tipo de forma a lo largo de la cual se deben colocar los patrones:<ul data-preserve-html="true"> <li data-preserve-html="true">Círculo</li> <li data-preserve-html="true">Polígono</li> </ul> |
| <b>Cantidad de patrón</b> Entero | Cantidad de patrones colocados a lo largo de la forma seleccionada. |
| <b>Vincular segmentos con cantidad de patrón</b> Booleano *Disponible cuando &#39;Shape&#39; está establecido en &#39;Polygon&#39;* | Utilice <b>Importe de patrón</b> como número de <b>segmentos</b>.   Esto evita que los patrones se ajusten alrededor de las esquinas, lo que garantiza un aspecto recto y coherente. |
| <b>Segmentos</b> Entero *Disponible cuando &#39;Forma&#39; está establecido en &#39;Polígono&#39; y &#39;Vincular segmentos con cantidad de patrón&#39; está establecido en &#39;Falso&#39;* | Cantidad de segmentos del polígono a lo largo de los cuales se colocan los patrones.   Los segmentos tienen *un tamaño uniforme* y todos los vértices están *equidistantes del centro*, por lo que al aumentar la cantidad de segmentos, el polígono converge hacia un círculo. |
| Flotador <b>Radius</b> | Un multiplicador para el radio de la forma, donde 1.0 es la mitad de la longitud del lado más corto de la imagen. |
| <b>Ancho</b> Flotante | Un multiplicador para la anchura de los patrones a lo largo de la forma, donde 1.0 es la mitad de la longitud del lado más corto de la imagen. |
| Flotador <b>Rotation</b> | Cantidad de rotación aplicada a la forma, en número de vueltas en el sentido de las agujas del reloj desde la derecha horizontal. |
| <b>Voltear uno en dos</b> Boolean | Voltee verticalmente una forma cada otra. |
| <b>Modo de filtrado</b> Entero | El método de filtrado aplicado a los patrones colocados a lo largo de la forma:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Más cercano:</i> Aplica el valor del píxel proyectado más cercano tal cual, lo que da como resultado un aspecto más nítido pero suavizado.</li> <li data-preserve-html="true"><i>Bilineal:</i> Aplica un filtro bilineal para interpolar el píxel proyectado con sus vecinos, para obtener un aspecto más suave y borroso.</li> </ul> |
| <b>Expansión no cuadrada</b> Boolean | En las imágenes no cuadradas, mantiene la forma generada en forma cuadrada y expande la generación de imágenes a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
