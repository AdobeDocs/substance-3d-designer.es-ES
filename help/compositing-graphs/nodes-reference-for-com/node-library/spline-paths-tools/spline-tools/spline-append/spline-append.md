---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: Utilice el nodo Anexar spline para anexar varias splines juntas y crear rutas continuas más largas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Append spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 29dd2e6adc826f63ee26defc0032b0e52d4e30fb
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Append spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-append.resources/spline-append-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Las splines se empaquetan como una lista. Este nodo anexa una lista de splines de entrada (conjunto #2) a una lista existente (conjunto #1).

El orden de las listas se mantiene, lo que significa que si se agrega una lista D-E-F a una lista A-B-C, se obtiene una lista A-B-C-D-E-F.

</td>
</tr>
</table>

>[!TIP]
>
> Tenga en cuenta el orden en el que se anexan las splines, ya que este orden se tiene en cuenta en otros nodos, como [Dispersión en splines](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md), los nodos [Puente de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md), etc.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa n.º 1</b> <i>Escala de grises</i> | Vista previa del primer conjunto de splines de entrada como una imagen en escala de grises. |
| <b>Códigos Spline #1</b> <i>Color</i> | Las coordenadas del primer conjunto de puntos de splines de entrada codificados en los canales RGBA de una imagen de color.<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline #1</b> <i>Color</i> | Datos adicionales del primer conjunto de splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de división #1</b> <i>Entero</i> | Número de splines de entrada en el primer conjunto. |
| <b>Vista previa n.º 2</b> <i>Escala de grises</i> | Vista previa del segundo conjunto de splines de entrada como una imagen en escala de grises. |
| <b>Spline #2 Coords</b> <i>Color</i> | Las coordenadas del segundo conjunto de puntos de splines de entrada codificados en los canales RGBA de una imagen de color.<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline #2</b> <i>Color</i> | Datos adicionales del segundo conjunto de splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de división #2</b> <i>Entero</i> | Número de splines de entrada en el segundo conjunto. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de salida como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de salida codificados en los canales RGBA de una imagen en color.<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de salida codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de salida. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Voltear spline #1 dirección</b> <i>Booleano</i> | Invierte la dirección de las splines en el primer conjunto. |
| <b>Voltear dirección de spline #2</b> <i>Booleano</i> | Invierte la dirección de las splines en el segundo conjunto. |
| <b>Vista previa</b> |  |
| <b>Cantidad de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de previsualización. Un valor más alto produce una línea más suave. |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Muestra un punto al principio de la spline y una punta de flecha al final en la salida de previsualización. |
| <b>Mostrar sobre de Thickness</b> <i>Booleano</i> | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Thickness (px)</b> <i>Flotador</i> | Ajusta el thickness de la visualización de la spline en píxeles en la salida de previsualización. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](spline-append.resources/SplineAppend-Demo.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](spline-append.resources/SplineAppend-Graph.jpg "Ejemplo de nodo 2")

</td>
</tr>
</table>

![Demostración de nodo](spline-append.resources/SplineAppend-Demo2.gif "Demostración de nodo")
