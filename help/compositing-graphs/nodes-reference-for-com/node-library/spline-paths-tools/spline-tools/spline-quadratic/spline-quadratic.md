---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
breadcrumb-title: ''
description: Utilice el nodo Cuadrático polinomial para crear polinomiales cuadráticos suaves con tres puntos de control.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (cuadrático)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---


# Spline (cuadrático)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (Quadratic): icon](spline-quadratic.resources/spline-quadratic-01.png "Spline (Quadratic): icon")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una única spline entre dos puntos <b>p1</b> y <b>p3</b> en ubicaciones arbitrarias.

La trayectoria de la spline está controlada por la tangente ‘out’ de <b>p1</b> y la tangente ‘in’ de <b>p3</b>, *both* controlados por un solo punto <b>p3</b>.

La extensión del arco formado por la spline es *ajustable*, por lo que parte de su trayectoria desde sus extremidades puede permanecer recta.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de entrada como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Firma: La spline está cerrada (negativa) o abierta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Tangents Z<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de salida como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de salida codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Firma: La spline está cerrada (negativa) o abierta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de salida codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Tangents Z<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de salida. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Voltear dirección</b> <i>Booleano</i> | Invierte la dirección de la spline. |
| <b>Distribución uniforme</b> <i>Booleano</i> | Cuando <i>True</i>, los puntos de la spline se espacian uniformemente de principio a fin. |
| <b>Anexar spline de entrada</b> <i>Booleano</i> | Agrega la spline generada al final de la lista de splines conectadas a las entradas <b>Spline</b>. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas. Esto también afecta a la distribución uniforme. |
| <b>Smoothness</b> <i>Flotador</i> | Ajusta el <i>rango del arco</i> formado por la spline, donde 1 significa que la longitud completa de la spline es arqueada y 0 significa que la spline es completamente recta. El arco avanza desde el punto <b>p3</b> a lo largo de la spline hasta sus extremidades. |
| <b>Height</b> |  |
| <b>Iniciar height</b> <i>Flotador</i> | Ajusta el height del punto <b>p1</b> en el que un valor inferior significa una ubicación más baja o más profunda.<br>Esto afecta al height de la spline en <b>p1</b>. |
| <b>Finalizar height</b> <i>Flotador</i> | Ajusta el height del punto <b>p3</b> en el que un valor inferior significa una ubicación más baja o más profunda.<br>Esto afecta al thickness de la spline en <b>p3</b>. |
| <b>height de tangente automática</b> <i>Booleano</i> | Ajusta el height del punto <b>p3</b> en el que un valor inferior significa una ubicación más baja o más profunda.<br>Esto afecta al thickness de la spline en <b>p3</b>. |
| <b>height Tangent</b> <i>Flotador</i> | Ajusta el height controlado por las tangentes controladas por el punto <b>p2</b>.<br>Esto afecta al height a lo largo de la spline a medida que se retira de <b>p1</b> y va a <b>p3</b>.<br><i>Nota:</i> Este parámetro solo está disponible cuando <b>height de tangente automática</b> está establecido en &#39;False&#39;. |
| <b>Thickness</b> |  |
| <b>Iniciar thickness</b> <i>Flotador</i> | Ajusta el thickness del punto <b>p1</b>. Esto afecta al thickness de la spline en <b>p1</b>.<br><i>Nota:</i> nodos de spline específicos utilizan el Thickness Spline. |
| <b>Finalizar thickness</b> <i>Flotador</i> | Ajusta el thickness del punto <b>p3</b>. Esto afecta al thickness de la spline en <b>p3</b>.<br><i>Nota:</i> nodos específicos de spline utilizan el Thickness Spline. |
| <b>thickness de tangente automática</b> <i>Booleano</i> | Establece automáticamente el thickness de las tangentes polinomiales para que se interpolen linealmente desde el <b>Thickness de inicio</b> hasta el <b>Thickness de fin</b>.<br><i>Nota:</i> nodos polinomiales específicos utilizan el Thickness. |
| <b>thickness Tangent</b> <i>Flotador</i> | Ajusta el thickness controlado por las tangentes controladas por el punto <b>p2</b>.<br>Esto afecta al thickness a lo largo de la spline a medida que se aleja de <b>p1</b> y va al Thickness <b>p3</b>.<br><i>Nota:</i> nodos de spline específicos lo utilizan.<br><i>Nota 2:</i> Este parámetro solo está disponible cuando <b>thickness de tangente automática</b> está establecido en &#39;False&#39;. |
| <b>Coordenadas de puntos</b> |  |
| <b>p1</b> <i>Float2</i> | Establece la posición del punto <b>p1</b> en el espacio de textura. |
| <b>p2</b> <i>Float2</i> | Establece la posición del punto <b>p2</b> en el espacio de textura.<br>El punto <b>p2</b> controla las <i>tangentes</i> de los puntos <b>p1</b> y <b>p3</b>. |
| <b>p3</b> <i>Float2</i> | Establece la posición del punto <b>p3</b> en el espacio de textura. |
| <b>Vista previa</b> |  |
| <b>Mostrar tangentes</b> <i>Booleano</i> | Muestra la tangente del punto de salida <b>p1</b> y la tangente del punto de entrada <b>p3</b> en la salida <b>Preview</b>. Invierte la dirección de la spline. |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Muestra un punto al principio de la spline y una punta de flecha al final en la salida <b>Preview</b>. |
| <b>Mostrar envolvente de thickness</b> <i>Booleano</i> | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Importe de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de <b>Preview</b>.<br>Un valor más alto produce una línea más suave. |
| <b>Thickness (px)</b> <i>Flotador</i> | Ajusta el thickness en píxeles de la visualización de spline en la salida de <b>Preview</b>. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratic): Ejemplo 1](spline-quadratic.resources/spline-quadratic-02.png "Spline (Quadratic): Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (Quadratic): Ejemplo 2](spline-quadratic.resources/spline-quadratic-03.png "Spline (Quadratic): Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratic): Demostración](spline-quadratic.resources/spline-quadratic-04.gif "Spline (Quadratic): Demostración"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
