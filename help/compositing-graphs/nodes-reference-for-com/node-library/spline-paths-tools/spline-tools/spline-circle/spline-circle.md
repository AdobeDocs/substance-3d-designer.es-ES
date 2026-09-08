---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: Utilice el nodo Círculo polinómico para crear splines circulares para generar formas y patrones redondos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Círculo polinómico
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---


# Círculo polinómico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-circle-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una única spline con forma de círculo.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de entrada como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen de color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |

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
| <b>Radio del círculo</b> <i>Flotador</i> | Ajusta el radio del círculo en el espacio de textura. |
| <b>Círculo previo a la rotación</b> <i>Flotador</i> | Aplica una rotación al círculo base antes de aplicar Tamaño. |
| <b>Tamaño de círculo</b> <i>Float2</i> | Ajusta el tamaño horizontal (X) y el tamaño vertical (Y) del círculo. |
| <b>Círculo posterior a la rotación</b> <i>Flotador</i> | Aplica una rotación al círculo base después de aplicar Tamaño. |
| <b>Posición del círculo</b> <i>Float2</i> | Establece la posición del centro del círculo en el espacio de textura. |
| <b>Iniciar Thickness</b> <i>Flotador</i> | Ajusta el thickness del punto inicial del círculo. Este thickness se interpola a lo largo de la spline hasta el Thickness Final.<br>Nota: El thickness se utiliza en nodos Spline específicos. |
| <b>Finalizar Thickness</b> <i>Flotador</i> | Ajusta el thickness del punto final del círculo. Este thickness se interpola a lo largo de la spline hasta el Thickness Inicio.<br>Nota: El thickness se utiliza en nodos Spline específicos. |
| <b>Iniciar Height</b> <i>Flotador</i> | Ajusta el height del punto inicial del círculo, donde un valor inferior significa una ubicación más baja o más profunda. Este height se interpola a lo largo de la spline hasta el Height final. |
| <b>Finalizar Height</b> <i>Flotador</i> | Ajusta el height del punto final del círculo en el que un valor inferior significa una ubicación más baja o más profunda. Este height se interpola a lo largo de la spline desde el Height Inicio. |
| <b>Recortar</b> <i>Float2</i> | Desplaza los puntos inicial y final de la spline a lo largo del círculo. Estos valores se normalizan. |
| <b>Espiral</b> <i>Flotador</i> | Desplaza el punto inicial del círculo desde su radio hasta su centro. La distancia desde el centro se interpola a lo largo de la spline hasta el final de la spline. Este valor está normalizado. |
| <b>Giros en espiral</b> <i>Flotador</i> | Define el número de vueltas realizadas por la espiral alrededor de su centro. |
| <b>Potencia espiral</b> <i>Flotador</i> | Aplica una curva de potencia a la distancia desde el centro utilizada para dibujar la espiral. Un valor superior a uno significa que una porción mayor de la espiral permanece cerca del centro. |
| <b>Voltear dirección</b> <i>Booleano</i> | Invierte la dirección de la spline. |
| <b>Distribución uniforme</b> <i>Booleano</i> | Si es True, los puntos de la spline se espacian uniformemente de principio a fin. |
| <b>Anexar spline de entrada</b> <i>Booleano</i> | Agrega la spline generada al final de la lista de splines conectadas a las entradas <b>Spline</b>. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas. Esto también afecta a la distribución uniforme. |
| <b>Vista previa</b> |  |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Muestra un punto al principio de la spline y una punta de flecha al final en la salida de previsualización. |
| <b>Mostrar sobre de Thickness</b> <i>Booleano</i> | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Cantidad de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de previsualización. Un valor más alto produce una línea más suave. |
| <b>Thickness (px)</b> <i>Flotador</i> | Ajusta el thickness en píxeles de la visualización de la spline en la salida de previsualización. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](../../../../../../assets/SplineCircle-Variant1.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineCircle-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo 3](../../../../../../assets/SplineCircle-Variant2.jpg "Ejemplo 3")

</td>
<td style="border: 0;" valign="top">

![Ejemplo 4](../../../../../../assets/SplineCircle-Variant3.jpg "Ejemplo 4")

</td>
</tr>
</table>
