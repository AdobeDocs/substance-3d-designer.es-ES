---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: Utilice el nodo Lista de puntos para crear y gestionar listas de puntos para la generación de splines y trazados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lista de puntos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 1%

---


# Lista de puntos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](point-list.resources/point-list-01.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una lista de puntos que se deben recorrer mediante una spline.

Si se proporciona una lista de puntos existente a las entradas <b>Point</b>, la lista generada se anexa a la lista de entradas.

</td>
</tr>
</table>

>[!TIP]
>
> Este nodo se puede usar para proporcionar puntos al nodo [Spline (Poly Quadratic)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) para crear splines.

>[!IMPORTANT]
>
> Los conectores <b>Point List</b> y <b>Point Number</b> son *incompatibles* con los conectores <b>Spline Code</b>, <b>Spline Data</b> y <b>Spline Amount</b>, ya que se basan en datos diferentes.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de los puntos como una imagen en escala de grises. |
| <b>Entrada de lista de puntos</b> <i>Color</i> | Una lista de puntos de entrada codificados en los canales RGBA de una imagen de color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> * Parte entera: Smoothness;<br> * Parte fraccional: Thickness. |
| <b>Entrada de número de punto</b> <i>Entero</i> | Número de puntos de entrada. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de los puntos como una imagen en escala de grises. |
| <b>Lista de puntos</b> <i>Color</i> | La lista de salida de puntos codificados en los canales RGBA de una imagen de color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> * Parte entera: Smoothness;<br> * Parte fraccional: Thickness. |
| <b>Número de punto</b> <i>Entero</i> | Número de puntos de salida. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Número de punto</b> <i>Entero</i> | Número de puntos generados. |
| <b>Ajuste de Smoothness global</b> <i>Flotador</i> | Aplica un desplazamiento uniforme al valor de smoothness de todos los puntos.<br>El valor de smoothness resultante se fija al intervalo [0;1]. |
| <b>Propiedades de puntos</b> |  |
| <b>Propiedades de p#</b> <i>Float3</i> | Establece las propiedades del punto p#.<br>*- Height:* Ajusta el height del punto en el que un valor inferior significa una ubicación más baja o más profunda;<br>*- Smoothness:* Desplaza el inicio del suavizado de la spline en p#, donde un valor de 0 da como resultado una trayectoria dura y 1 en una completamente suave;<br>*- Thickness:* Ajusta el thickness de la spline en p#. El thickness se utiliza en nodos Spline específicos. |
| <b>Coordenadas de puntos</b> |  |
| <b>p#</b> <i>Float2</i> | Establece la posición del punto p# en el espacio de textura. |
| <b>Vista previa</b> |  |
| <b>Mostrar etiquetas</b> <i>Booleano</i> | Para cada punto, muestra el nombre del punto junto a él en la salida &quot;Vista previa&quot;. |
| <b>Tamaño de etiqueta</b> <i>Float</i> (disponible cuando &#39;Mostrar etiquetas&#39; está establecido en &#39;True&#39;) | El tamaño de la etiqueta para cada punto en el espacio de textura, donde 0,1 es una décima parte del ancho de la textura. |
| <b>Mostrar puntos</b> <i>Booleano</i> | Muestra los puntos en la salida de &#39;Vista previa&#39;. |
| <b>Tamaño de puntos</b> <i>Float</i> (disponible cuando &#39;Mostrar puntos&#39; está establecido en &#39;True&#39;) | El radio de los puntos en el espacio de textura, donde 0,1 es una décima parte del ancho de la textura. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](point-list.resources/point-list-02.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](point-list.resources/point-list-03.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
