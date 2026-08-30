---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
breadcrumb-title: ''
description: Utilice el nodo Poly Quadratic polinomial para crear splines cuadráticas complejas con varios puntos de control.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Poly Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (poli cuadrático)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# Spline (poli cuadrático)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-poly-quadratic.resources/spline-poly-quadratic-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una spline en varios puntos. La cantidad y las ubicaciones de estos puntos pueden ser arbitrarias o recopilarse a partir de un nodo [Lista de puntos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md).

</td>
</tr>
</table>

La trayectoria de la spline se puede suavizar alejándola de sus puntos intermediarios, en el sentido de que cada punto intermediario es el punto de encuentro de las tangentes &quot;out&quot; e &quot;in&quot; de sus vecinos.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de entrada como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Firma: La spline está cerrada (negativa) o abierta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |
| <b>Vista previa de puntos</b> <i>Escala de grises</i> | Vista previa de los puntos como una imagen en escala de grises. |
| <b>Lista de puntos de entrada</b> <i>Color</i> | (disponible cuando &quot;Usar lista de puntos de entrada&quot; es True) Una lista de puntos codificados en los canales RGBA de una imagen de color:<br><b>R</b> - X position<br><b>G</b> - Y position<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Parte entera: Smoothness;<br> - Parte fraccional: Thickness. |
| <b>Número de punto</b> <i>Entero</i> | (disponible cuando &quot;Usar lista de puntos de entrada&quot; es True) El número de puntos. |

>[!IMPORTANT]
>
> Los conectores <b>Point List</b> y <b>Point Number</b> son *incompatibles* con los conectores <b>Spline Code</b>, <b>Spline Data</b> y <b>Spline Amount</b>, ya que se basan en datos diferentes.

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de salida como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de salida codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Firma: La spline está cerrada (negativa) o abierta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de salida codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de salida. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Importe de puntos</b> <i>Entero</i> | Número arbitrario de puntos utilizados para crear la spline. |
| <b>Modo de conexión de spline de entrada</b> <i>Entero</i> | Método utilizado para conectar las splines de entrada:<br>- <i>Automático:</i> El final de la última spline de entrada está conectado al inicio de la spline generada y el final de la spline generada está conectado al inicio de la primera spline de entrada;<br>- <i>Manual:</i> Puede especificar cuál de las splines de entrada debe estar conectada a las extremidades de la spline generada y en qué parte de las splines de entrada deben aterrizar estas conexiones. |
| <b>Cerrar spline</b> <i>Booleano</i> | Controla si el punto final de la spline debe conectarse a su punto inicial.<br>El suavizado aplicado a la spline en los puntos inicial y final se especifica mediante los valores de Smoothness de esos puntos. |
| <b>Voltear dirección</b> <i>Booleano</i> | Invierte la dirección de la spline. |
| <b>Usar lista de puntos de entrada</b> <i>Booleano</i> | Utilice la lista de puntos suministrados a los conectores de entrada Lista de puntos de entrada y Número de punto en lugar de una lista arbitraria de puntos.<br>Un nodo [Lista de puntos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md) puede proporcionar la lista de puntos. |
| <b>Conectar inicio a spline de entrada</b> <i>Booleano</i> | Si es True, el inicio de la spline generada se conecta al último punto de la última spline de las splines de entrada. |
| <b>Iniciar índice de spline de conexión</b> <i>Entero</i> | (Disponible cuando &quot;Input Spline Connection Mode&quot; está establecido en &quot;Manual&quot; y &quot;Connect Start to Input Spline&quot; está establecido en &quot;True&quot;) El índice de la spline de entrada que debe conectarse al inicio de la spline generada. |
| <b>Iniciar posición de conexión</b> <i>Flotador</i> | (Disponible cuando &quot;Input Spline Connection Mode&quot; está establecido en &quot;Manual&quot; y &quot;Connect Start to Input Spline&quot; está establecido en &quot;True&quot;) Posición en la spline de entrada seleccionada donde debe aterrizar la conexión con el inicio de la spline generada.<br>Este valor es la longitud normalizada de la spline de entrada seleccionada. |
| <b>Conectar extremo a spline de entrada</b> <i>Booleano</i> | Si es True, el final de la spline generada se conecta al primer punto de la primera spline de las splines de entrada. |
| <b>Finalizar índice de spline de conexión</b> <i>Entero</i> | (Disponible cuando &quot;Input Spline Connection Mode&quot; se define en &quot;Manual&quot; y &quot;Connect End to Input Spline&quot; se define en &quot;True&quot;) Índice de la spline de entrada que debe conectarse al final de la spline generada. |
| <b>Finalizar posición de conexión</b> <i>Flotador</i> | (Disponible cuando &quot;Input Spline Connection Mode&quot; está establecido en &quot;Manual&quot; y &quot;Connect End to Input Spline&quot; está establecido en &quot;True&quot;) Posición en la spline de entrada seleccionada donde debe aterrizar la conexión al extremo de la spline generada.<br>Este valor es la longitud normalizada de la spline de entrada seleccionada. |
| <b>Distribución uniforme</b> <i>Booleano</i> | Si es True, los puntos de la spline se espacian uniformemente de principio a fin. |
| <b>Anexar spline de entrada</b> <i>Booleano</i> | Agrega la spline generada al final de la lista de splines conectadas a las entradas <b>Spline</b>. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas.<br>Esto también afecta a la distribución uniforme. |
| <b>Ajuste de Smoothness global</b> <i>Flotador</i> | Aplica un desplazamiento uniforme al valor de smoothness de todos los puntos.<br>El valor de smoothness resultante se fija al intervalo [0;1]. |
| <b>Propiedades de puntos</b> |  |
| <b>Propiedades de p#</b> <i>Float3</i> | Establece las propiedades del punto p#.<br>- <i>Height:</i> Ajusta el height del punto donde un valor inferior significa una ubicación más baja o más profunda;<br>- <i>Smoothness:</i> Desplaza el inicio del suavizado de la spline en p#, donde un valor de 0 da como resultado una trayectoria dura y 1 en una completamente suave;<br>- <i>Thickness:</i> Ajusta el thickness de la spline en p#. El thickness se utiliza en nodos Spline específicos. |
| <b>Coordenadas de puntos</b> |  |
| <b>p#</b> <i>Float2</i> | Establece la posición del punto p# en el espacio de textura. |
| <b>Vista previa</b> |  |
| <b>Mostrar tangentes</b> <i>Booleano</i> | Muestra las tangentes de los puntos p1 y p3 a p2 en la salida de previsualización. |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Muestra un punto al principio de la spline y una punta de flecha al final en la salida de previsualización. |
| <b>Mostrar sobre de Thickness</b> <i>Booleano</i> | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Mostrar etiqueta de puntos</b> <i>Booleano</i> | Para cada punto, muestra el nombre del punto junto a él en la salida &quot;Vista previa&quot;. |
| <b>Tamaño de etiqueta de puntos</b> <i>Flotador</i> | (Disponible cuando &#39;Mostrar etiqueta de puntos&#39; está establecido en &#39;Verdadero&#39;) El tamaño de la etiqueta para cada punto en el espacio de textura, donde 0,1 es una décima parte del ancho de la textura. |
| <b>Mostrar puntos</b> <i>Booleano</i> | Muestra los puntos de control de la spline. |
| <b>Tamaño de puntos</b> <i>Flotador</i> | (Disponible cuando &#39;Mostrar puntos&#39; está establecido en &#39;Verdadero&#39;) El radio de los puntos en el espacio de textura, donde 0,1 es una décima parte del ancho de la textura. |
| <b>Cantidad de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de vista previa.<br>Un valor más alto produce una línea más suave. |
| <b>Thickness (px)</b> <i>Flotador</i> | Ajusta el thickness de la visualización de la spline en píxeles en la salida de previsualización. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-poly-quadratic.resources/SplinePolyQuadratic-Variant1-Before.jpg" alt="SplinePolyQuadratic-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-poly-quadratic.resources/SplinePolyQuadratic-Variant1-After.jpg" alt="SplinePolyQuadratic-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](spline-poly-quadratic.resources/SplinePolyQuadratic-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
