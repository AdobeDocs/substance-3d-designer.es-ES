---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/curve.html"
breadcrumb-title: ''
description: Utilice el nodo Curva para ajustar los valores de textura mediante curvas personalizables para un control preciso del color y el brillo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Curve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curva
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 2%

---


# Curva

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Curva](curve.resources/curve-01.png "Nodo atómico: Curva"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Reasigna los valores de una imagen utilizando una curva personalizada.

El nodo proporciona una interfaz para la reasignación de tonalidad de imágenes, similar a otras aplicaciones de edición de imágenes 2D. El usuario puede colocar puntos y ajustar curvas Bézier para reasignar la entrada, que puede ser de escala de grises o de color.Es especialmente útil cuando se utiliza con transiciones de degradado para reasignarlas a un perfil de height específico, ya que permite modelar de forma muy precisa los perfiles de bisel y similares.

</td>
</tr>
</table>

A diferencia de la mayoría de los demás nodos, el nodo Curva no tiene una interfaz estándar típica con reguladores y parámetros, sino que presenta un editor de curvas completo. Consulte la siguiente sección ampliable sobre cómo usarla.

[Sin embargo, esto significa que ninguno de los parámetros de un nodo Curve se puede exponer a un subgráfico](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md). La única opción es usar un [conmutador múltiple](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) para cambiar entre diferentes perfiles de curva.

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

## Parámetros

### Editor de curvas

</td>
<td style="border: 0;" valign="top">

### Conectores de entrada

### Conectores de salida

</td>
<td style="border: 0;" valign="top">

### Ejemplos

</td>
</tr>
</table>

## Parámetros

|  |  |
| --- | --- |
| <b>Aplicar/exponer curva</b> *Booleano* | Permite copiar la curva del usuario en la salida en lugar de aplicarla a la imagen de entrada |
| <b>Direccionamiento de curvas</b> *Booleano* | Este parámetro determina cómo se gestionan los píxeles HDR fuera del rango [0, 1] en la entrada: sujetado o plegado hasta [0, 1]. |
| <b>Curva</b> *Matriz de claves de curva* | Curva personalizada utilizada para asignar los valores de escala de grises de entrada.   Se puede editar con el [editor de curvas](#curve-editor). |

## Editor de curvas

### Creación y desplazamiento de un punto

Para crear un punto, simplemente haga doble clic en cualquier parte de la vista Curva:

![](curve.resources/curve-02.gif)

### Control de la influencia de puntos

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Para obtener resultados precisos, los nodos de curva ofrecen diferentes modos para cada punto:

</td>
<td width="33.33%" style="border: 0;" valign="top">

![](curve.resources/curve-03.png)

</td>
</tr>
</table>

![](curve.resources/curve-04.png) Restablezca el modo de punto al valor predeterminado.

![](curve.resources/curve-05.png) Bloquear/Desbloquear los 2 controladores Bezier para que el usuario pueda moverlos juntos o de forma independiente.

![](curve.resources/curve-06.png) Ambos lados del punto están controlados por un controlador Bézier.

![](curve.resources/curve-07.png) El lado derecho del punto está controlado por un controlador Bézier, mientras que el lado izquierdo permanece plano.

![](curve.resources/curve-08.png) El lado izquierdo del punto está controlado por un controlador Bézier, mientras que el lado derecho permanece plano.

![](curve.resources/curve-09.png) Los lados del punto permanecen planos

![](curve.resources/curve-10.gif)

### Mostrar histograma de entrada

Puede mostrar u ocultar el histograma de su entrada simplemente haciendo clic en ![](curve.resources/curve-11.png)

![](curve.resources/curve-12.png)

### Control individual de cada canal (entrada de color)

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Cuando la entrada es un nodo de color, tiene la capacidad de ajustar la curva para cada canal:

Solo tiene que seleccionar la curva que desea ajustar en la lista desplegable situada en la parte superior derecha:

</td>
<td width="33.33%" style="border: 0;" valign="top">

![](curve.resources/curve-13.png)

</td>
</tr>
</table>

En el modo Curva de RGB, puede ocultar o mostrar las curvas de canal individuales presionando o despresionando ![](curve.resources/curve-14.png):

![](curve.resources/curve-15.png)

### Alineación, reflejo y volteo

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Si hace clic con el botón derecho en la vista de curva, obtendrá algunas opciones más.

<b>Alinear arriba:</b> Alinea los puntos seleccionados horizontalmente con el más alto.

<b>Alinear al medio:</b> Alinea los puntos seleccionados horizontalmente con el height promedio de la selección.

<b>Alinear abajo:</b> Alinea los puntos seleccionados horizontalmente con el más bajo.

</td>
<td width="50.00%" style="border: 0;" valign="top">

![](curve.resources/curve-16.png)

</td>
</tr>
</table>

<b>Distribuir horizontal/verticalmente:</b> Distribuir los puntos en el eje seleccionado

<b>Voltear horizontal/verticalmente:</b> Voltear los puntos seleccionados según el eje seleccionado.

<b>Reflejar horizontal/verticalmente:</b> Refleja toda la curva, según el eje seleccionado

### Métodos abreviados de teclado

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>LMB + Arrastrar</b>

Dibuje un cuadro de selección.

</td>
<td style="border: 0;" valign="top">

![](curve.resources/curve-17.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Mayús + Arrastrar</b>

Restrinja el movimiento en el eje X o Y.

</td>
<td style="border: 0;" valign="top">

![](curve.resources/curve-18.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Alt + LMB + Arrastrar</b>

Rompa temporalmente los controles para moverlos de forma independiente.

</td>
<td style="border: 0;" valign="top">

![](curve.resources/curve-19.gif)

</td>
</tr>
</table>

### Ajustar el encuadre de la curva

Mientras se ajustan los controladores, puede darse el caso de que uno de ellos se desplace por la vista de curva.

En ese caso, puede usar el botón ![](curve.resources/curve-20.png) para ajustar el tamaño al contenido.

El botón ![](curve.resources/curve-21.png) restablece el nivel de zoom a 1

![](curve.resources/curve-22.gif)

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises/Color* PRINCIPAL | Imagen que se va a procesar. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises/Color* |  |

## Ejemplos

*Próximamente.*
