---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines.html"
breadcrumb-title: ''
description: Utilice el nodo Puente polinómico para enlazar texturas entre dos splines con el fin de crear conexiones perfectas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (2 Splines)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Puente de spline (2 splines)
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---


# Puente de spline (2 splines)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-bridge-2splines-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera splines de <b>Spline #1</b> a <b>Spline #2</b> a lo largo de estas splines. Las splines generadas pueden ser lineales (rectas) o curvadas (Bézier cúbico).

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Si los datos proporcionados a las entradas <b>Spline #1</b> y <b>Spline #2</b> contienen más de una spline, solo se utilizará la última spline de cada lista.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa n.º 1</b> <i>Escala de grises</i> | La previsualización de las splines de entrada #1 como una imagen en escala de grises. |
| <b>Códigos polinómicos #1</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada #1 codificados en los canales RGBA de una imagen en color.<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline #1</b> <i>Color</i> | Datos adicionales de las splines de entrada #1 codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline #1</b> <i>Entero</i> | Número de splines de entrada #1. |
| <b>Vista previa n.º 2</b> <i>Escala de grises</i> | Vista previa de las splines de entrada n.º 2 como imagen en escala de grises. |
| <b>Códigos polinómicos #2</b> <i>Color</i> | Las coordenadas de los puntos #2 de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline #2</b> <i>Color</i> | Datos adicionales de las splines de entrada #2 codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline #2</b> <i>Entero</i> | Número de splines de entrada #2. |
| <b>Iniciar curva de longitud de tangente</b> <i>Escala de grises</i> (disponible cuando &#39;Tipo de splines de puente&#39; está establecido en &#39;Curva cúbica&#39;) | Imagen que describe una curva utilizando los valores de su primera fila de píxeles.<br>Esta entrada se utiliza para controlar la longitud de las tangentes &#39;out&#39; para el punto inicial de cada spline generada a lo largo de la spline #1.<br>Puede utilizar un nodo Curve para crear la curva. |
| <b>Iniciar curva de rotación tangente</b> <i>Escala de grises</i> (disponible cuando &#39;Tipo de splines de puente&#39; está establecido en &#39;Curva cúbica&#39;) | Imagen que describe una curva utilizando los valores de su primera fila de píxeles.<br>Esta entrada se utiliza para controlar la rotación de las tangentes &#39;out&#39; para el punto inicial de cada spline generada a lo largo de la spline #1.<br>El valor de escala de grises de la imagen representa un número de vueltas.<br>Puede usar un nodo Curva para crear la curva. |
| <b>Curva de longitud de tangente final</b> <i>Escala de grises</i> (disponible cuando &#39;Tipo de splines de puente&#39; está establecido en &#39;Curva cúbica&#39;) | Imagen que describe una curva utilizando los valores de su primera fila de píxeles.<br>Esta entrada se utiliza para controlar la longitud de las tangentes &#39;in&#39; para el punto final de cada spline generada a lo largo de la spline #2.<br>Puede utilizar un nodo Curva para crear la curva. |
| <b>Finalizar curva de rotación de tangente</b> <i>Escala de grises</i> (disponible cuando &#39;Tipo de splines de puente&#39; está establecido en &#39;Curva cúbica&#39;) | Imagen que describe una curva utilizando los valores de su primera fila de píxeles.<br>Esta entrada se utiliza para controlar la rotación de las tangentes &#39;in&#39; para el punto final de cada spline generada a lo largo de la spline #2.<br>El valor de escala de grises de la imagen representa un número de vueltas.<br>Puede usar un nodo Curva para crear la curva. |

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
| <b>Cantidad de splines de puente</b> <i>Entero</i> | Número de splines generadas a lo largo de la spline #1 a la spline #2. |
| <b>Tipo de splines de puente</b> <i>Entero</i> | Tipo de spline que se genera:<br><br>- Lineal: una spline recta de principio a fin;<br>- Curva cúbica: una spline curva de principio a fin, la curva se controla mediante la longitud y el ángulo de los puntos inicial y final. |
| <b>Iniciar spline #1</b> <i>Flotador</i> | Desplaza la ubicación a lo largo de la spline #1 desde donde se generan las splines. El valor es la longitud normalizada de la spline #1.<br>Un valor más alto hace que el mismo número de splines se empaqueten más juntas. |
| <b>Iniciar spline #2</b> <i>Flotador</i> | Desplaza la posición a lo largo de la spline #2 desde donde se generan las splines. El valor es la longitud normalizada de la spline #2.<br>Un valor más alto produce el mismo número de splines que se empaquetan más juntas. |
| <b>Finalizar spline #1</b> <i>Flotador</i> | Desplaza la ubicación a lo largo de la spline #1 hasta el lugar en el que se generan las splines. El valor es la longitud normalizada de la spline #1.<br>Un valor más bajo hace que se empaquete más estrechamente el mismo número de splines. |
| <b>Finalizar spline #1</b> <i>Flotador</i> | Desplaza la ubicación a lo largo de la spline 2 hasta el lugar en el que se generan las splines. El valor es la longitud normalizada de la spline #2.<br>Un valor inferior hace que el mismo número de splines se empaqueten más juntas. |
| <b>Desplazamiento de spline #1</b> <i>Flotador</i> | Aplica un desplazamiento al punto inicial de todas las splines a lo largo de la spline #1. El valor es la longitud normalizada de la spline #1.<br>Las splines que coinciden con el principio o el final de la spline se dejan allí. |
| <b>Desplazamiento de spline #2</b> <i>Flotador</i> | Aplica un desplazamiento al punto inicial de todas las splines a lo largo de la spline #2. El valor es la longitud normalizada de la spline #2.<br>Las splines que coinciden con el principio o el final de la spline se dejan allí. |
| <b>Inicio aleatorio de desplazamiento</b> <i>Flotador</i> | Aplica un desplazamiento aleatorio al punto inicial de cada spline a lo largo de la spline #1. El valor es la distancia normalizada entre las splines de la spline #1.<br>Cuando se dejan en 0, las splines se espacian uniformemente entre los puntos de la spline #1 de inicio y de la spline #1 de fin. |
| <b>Fin aleatorio de desplazamiento</b> <i>Flotador</i> | Aplica un desplazamiento aleatorio al punto final de cada spline a lo largo de la spline #2. El valor es la distancia normalizada entre las splines de la spline #2.<br>Cuando se dejan en 0, las splines se espacian uniformemente entre los puntos de la spline #2 de inicio y de la spline #2 de fin. |
| <b>Inicio de longitud de tangente</b> <i>Flotante</i> (disponible cuando &#39;Bridge Splines Type&#39; está establecido en &#39;Cubic Bezier&#39;) | Longitud de la tangente &#39;out&#39; para el punto inicial de la spline #1 de todas las splines generadas. |
| <b>Final de longitud de tangente</b> <i>Flotante</i> (disponible cuando &#39;Bridge Splines Type&#39; está establecido en &#39;Cubic Bezier&#39;) | Longitud de la tangente &#39;in&#39; para el punto final de la spline #2 de todas las splines generadas. |
| <b>Inicio de rotación de tangentes</b> <i>Flotante</i> (disponible cuando &#39;Bridge Splines Type&#39; está establecido en &#39;Cubic Bezier&#39;) | Rotación de la tangente &#39;out&#39; para el punto inicial de la spline #1 de todas las splines generadas.<br>El valor es un número de vueltas. |
| <b>Fin de rotación tangente</b> <i>Flotante</i> (disponible cuando &#39;Bridge Splines Type&#39; está establecido en &#39;Cubic Bezier&#39;) | Rotación de la tangente &#39;in&#39; para el punto final de la spline #2 de todas las splines generadas.<br>El valor es un número de vueltas. |
| <b>Vista previa</b> |  |
| <b>Cantidad de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de previsualización. Un valor más alto produce una línea más suave. |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Muestra un punto al principio de la spline y una punta de flecha al final en la salida de previsualización. |
| <b>Mostrar sobre de Thickness</b> <i>Booleano</i> | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Thickness (px)</b> <i>Flotador</i> | Ajusta el thickness de la visualización de la spline en píxeles en la salida de previsualización. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridge-2Splines_Variant1-Before.jpg" alt="SplineBridge-2Splines_Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridge-2Splines_Variant1-After.jpg" alt="SplineBridge-2Splines_Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineBridge-2Splines_Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
