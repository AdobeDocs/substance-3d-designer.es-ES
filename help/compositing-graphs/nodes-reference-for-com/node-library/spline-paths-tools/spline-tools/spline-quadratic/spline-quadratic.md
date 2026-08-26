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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# Spline (cuadrático)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (Quadratic): icon](../../../../../../assets/spline-quadratic-icon.png "Spline (Quadratic): icon")

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

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Vista previa</b> *Escala de grises* | Vista previa de las splines de entrada como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> *Color* | Las coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen en color: <b>R</b> - Posición X <b>G</b> - Posición Y <b>B</b> - Height <b>A</b> - Datos empaquetados:          - Firma: La spline está cerrada (negativa) o abierta (positiva);          - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> *Color* | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color:  <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Sin Usar |
| <b>Cantidad de spline</b> *Entero* | Número de splines de entrada. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Vista previa</b> *Escala de grises* | Vista previa de las splines de salida como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> *Color* | Las coordenadas de los puntos de las splines de salida codificados en los canales RGBA de una imagen en color:  <b>R</b> - Posición X <b>G</b> - Posición Y <b>B</b> - Height <b>A</b> - Datos empaquetados:          - Firma: La spline está cerrada (negativa) o abierta (positiva);          - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> *Color* | Datos adicionales de las splines de salida codificadas en los canales RGBA de una imagen en color:  <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Sin Usar |
| <b>Cantidad de spline</b> *Entero* | Número de splines de salida. |

## Parámetros

|  |  |
| --- | --- |
| <b>Voltear dirección</b> *Booleano* | Invierte la dirección de la spline. |
| <b>Distribución uniforme</b> *Booleano* | Cuando *True*, los puntos de la spline se espacian uniformemente de principio a fin. |
| <b>Anexar spline de entrada</b> *Booleano* | Agrega la spline generada al final de la lista de splines conectadas a las entradas <b>Spline</b>. |
| <b>Corrección no cuadrada</b> *Booleano* | Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas. Esto también afecta a la distribución uniforme. |
| <b>Smoothness</b> *Flotador* | Ajusta el *rango del arco* formado por la spline, donde 1 significa que la longitud completa de la spline es arqueada y 0 significa que la spline es completamente recta. El arco avanza desde el punto <b>p3</b> a lo largo de la spline hasta sus extremidades. |

+++Altura

|  |  |
| --- | --- |
| <b>Iniciar height</b> *Flotador* | Ajusta el height del punto <b>p1</b> en el que un valor inferior significa una ubicación más baja o más profunda.  Esto afecta al height de la spline en <b>p1</b>. |
| <b>Finalizar height</b> *Flotador* | Ajusta el height del punto <b>p3</b> en el que un valor inferior significa una ubicación más baja o más profunda.  Esto afecta al thickness de la spline en <b>p3</b>. |
| <b>height de tangente automática</b> *Booleano* | Ajusta el height del punto <b>p3</b> en el que un valor inferior significa una ubicación más baja o más profunda.  Esto afecta al thickness de la spline en <b>p3</b>. |
| <b>height Tangent</b> *Flotador* | Ajusta el height controlado por las tangentes controladas por el punto <b>p2</b>.  Esto afecta al height a lo largo de la spline a medida que se aleja de <b>p1</b> y se adentra en <b>p3</b>.   *Nota:* Este parámetro solo está disponible cuando <b>height de tangente automática</b> está establecido en &#39;False&#39;. |


+++

+++Grosor

|  |  |
| --- | --- |
| <b>Iniciar thickness</b> *Flotador* | Ajusta el thickness del punto <b>p1</b>. Esto afecta al thickness de la spline en <b>p1</b>.   El Thickness *Note:* lo utilizan nodos Spline específicos. |
| <b>Finalizar thickness</b> *Flotador* | Ajusta el thickness del punto <b>p3</b>. Esto afecta al thickness de la spline en <b>p3</b>.   El Thickness *Note:* lo utilizan nodos Spline específicos. |
| <b>thickness de tangente automática</b> *Booleano* | Establece automáticamente el thickness de las tangentes polinomiales para que se interpolen linealmente desde el <b>Thickness inicial</b> hasta el <b>Thickness final</b>.   El Thickness *Note:* lo utilizan nodos Spline específicos. |
| <b>thickness Tangent</b> *Flotador* | Ajusta el thickness controlado por las tangentes controladas por el punto <b>p2</b>.  Esto afecta al thickness a lo largo de la spline a medida que se aleja de <b>p1</b> y se adentra en <b>p3</b>.   El Thickness *Note:* lo utilizan nodos Spline específicos.  *Nota 2:* Este parámetro solo está disponible cuando <b>thickness de tangente automática</b> está establecido en &#39;False&#39;. |


+++

+++Puntos y coordenadas

|  |  |
| --- | --- |
| <b>p1</b> *Float2* | Establece la posición del punto <b>p1</b> en el espacio de textura. |
| <b>p2</b> *Float2* | Establece la posición del punto <b>p2</b> en el espacio de textura.  El punto <b>p2</b> controla las *tangentes* de los puntos <b>p1</b> y <b>p3</b>. |
| <b>p3</b> *Float2* | Establece la posición del punto <b>p3</b> en el espacio de textura. |


+++

+++Vista previa

|  |  |
| --- | --- |
| <b>Mostrar tangentes</b> *Booleano* | Muestra la tangente del punto de salida <b>p1</b> y la tangente del punto de entrada <b>p3</b> en la salida <b>Preview</b>.Invierte la dirección de la spline. |
| <b>Mostrar ayuda de dirección</b> *Booleano* | Muestra un punto al principio de la spline y una punta de flecha al final en la salida <b>Preview</b>. |
| <b>Mostrar envolvente de thickness</b> *Booleano* | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Importe de segmentos</b> *Entero* | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de <b>Preview</b>.  Un valor más alto produce una línea más suave. |
| <b>Thickness (px)</b> *Flotador* | Ajusta el thickness en píxeles de la visualización de spline en la salida de <b>Preview</b>. |


+++

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratic): Ejemplo 1](../../../../../../assets/spline-quadratic-example-1.png "Spline (Quadratic): Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (Quadratic): Ejemplo 2](../../../../../../assets/spline-quadratic-example-2.png "Spline (Quadratic): Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratic): Demostración](../../../../../../assets/spline-quadratic-demo.gif "Spline (Quadratic): Demostración"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
