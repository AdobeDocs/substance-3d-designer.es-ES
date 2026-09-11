---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: Utilice el nodo Procesamiento de spline para procesar splines como texturas con anchura, color y modos de fusión personalizables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Procesamiento de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# Procesamiento de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-render.resources/spline-render-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja cadenas de segmentos a lo largo de la entrada <b>Splines</b> sobre la entrada <b>Background</b>.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Fondo</b> <i>Escala de grises</i> | Imagen de escala de grises sobre la que se deben dibujar las splines. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Firma: La spline está cerrada (negativa) o abierta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | La imagen resultante de dibujar las splines de entrada en la parte superior del fondo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo</b> <i>Entero</i> | Método para seleccionar las splines que se deben dibujar:<br>- <i>Dibujar lista de spline</i>: Dibujar todas las splines en la lista de entrada;<br>- <i>Dibujar una spline</i>: Dibuje solo la spline especificada de la lista de entrada;<br>- <i>Dibujar rango de spline</i>: Dibuje sólo las splines del rango especificado en la lista de entrada. |
| <b>Dibujar índice de spline</b> <i>Entero</i> | (Disponible cuando &quot;Modo&quot; está definido como &quot;Dibujar una spline&quot;) El índice de la spline que debe dibujarse. |
| <b>Dibujar rango de spline</b> <i>Entero2</i> | (Disponible cuando &quot;Modo&quot; está definido como &quot;Dibujar rango de spline&quot;) El rango de índices de las splines que deben dibujarse. |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Para cada spline, dibuja un punto al principio de la spline y una punta de flecha al final. |
| <b>Cantidad de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos dibujados a lo largo de las splines.<br>Un valor más alto genera líneas más suaves. |
| <b>Cantidad de spline de sobre</b> <i>Entero</i> | Número de segmentos duplicados que se deben dibujar a lo largo del thickness de cada spline. |
| <b>Inicio</b> <i>Flotante</i> | Desplaza el inicio de la parte de la spline que se debe dibujar.<br>El valor representa la longitud normalizada de la spline. |
| <b>Fin</b> <i>Flotante</i> | Desplaza el extremo de la parte de la spline que se debe dibujar.<br>El valor representa la longitud normalizada de la spline. |
| <b>Modo Tamaño Thickness</b> <i>Entero</i> | Método para calcular el thickness de los segmentos dibujados:<br>- <i>Imagen</i>: el valor se normaliza en el espacio de textura, donde 1 es la anchura completa de la imagen. El thickness es relativo a la resolución de textura;<br>- <i>Píxel</i>: el valor es un número absoluto de píxeles en la textura, donde 1 es un píxel completo. El thickness es independiente de la resolución de la textura. |
| <b>Thickness (imagen)</b> <i>Flotador</i> | (disponible cuando &quot;Modo de tamaño de Thickness&quot; está establecido en Imagen) El thickness de los segmentos dibujados se normaliza en el espacio de textura, donde 1 es el ancho completo de la imagen. |
| <b>Thickness (px)</b> <i>Flotador</i> | (disponible cuando &quot;Modo de tamaño de Thickness&quot; está establecido en Píxel) El thickness de los segmentos dibujados como un número absoluto de píxeles en la textura, donde 1 es un píxel completo. |
| <b>Habilitar uniones</b> <i>Booleano</i> | Rellena los espacios entre los segmentos individuales dibujados a lo largo de las splines, utilizando discos. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas.<br>Esto también afecta a la distribución uniforme. |
| <b>Color</b> |  |
| <b>Intensidad de fondo</b> <i>Flotador</i> | El valor se multiplica por la imagen de entrada de fondo. |
| <b>Estilo de spline</b> <i>Entero</i> | Método utilizado para colorear las splines:<br>- <i>Solid</i>: Los segmentos se dibujan utilizando un valor de escala de grises uniforme;<br>- <i>Degradado</i>: Se aplica un degradado de negro a blanco a lo largo de cada cadena de segmentos de principio a fin;<br>- <i>Height</i>: El height de las splines se utiliza como valor de escala de grises para dibujar los segmentos. |
| <b>Color de spline</b> <i>Flotador</i> | Valor de escala de grises uniforme utilizado para dibujar los segmentos.<br>Cuando se selecciona un estilo de spline distinto de &quot;sólido&quot;, este color se multiplica por el color con estilo. |
| <b>Luminancia aleatoria</b> <i>Flotante</i> | Para cada cadena de segmentos sin cortar de una spline, aplica un desplazamiento aleatorio en el rango especificado al valor de escala de grises utilizado para dibujar esa cadena. |
| <b>Modo de Fusión</b> <i>Entero</i> | Método de fusión de los colores del fondo y de los segmentos superpuestos dibujados a lo largo de las splines:<br>- <i>Máx.</i>: Se usa el valor más brillante;<br>- <i>Agregar</i>: Los valores se suman. |
| <b>Segmentos aleatorios</b> |  |
| <b>Inicio de segmentos aleatorios</b> <i>Flotante</i> | Ajusta la probabilidad de que se corte la cadena de segmentos más cercana al inicio de la spline. |
| <b>Fin de segmentos aleatorios</b> <i>Flotante</i> | Ajusta la probabilidad de que se corte la cadena de segmentos más cerca del final de la spline. |
| <b>Desplazamiento aleatorio</b> <i>Flotante</i> | Define la cantidad máxima de desplazamiento aplicada a cada segmento de corte a lo largo de su normal.<br>Este parámetro no tiene efecto cuando Start y End están establecidos en 0. |
| <b>Centro de desplazamiento aleatorio</b> <i>Flotante</i> | Desplaza el centro del desplazamiento aleatorio aplicado a cada segmento de corte a lo largo de su eje normal. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/SplineRender-Variant2-Before.jpg" alt="SplineRender-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-render.resources/SplineRender-Variant2-After.jpg" alt="SplineRender-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-render.resources/SplineRender-Variant1-After.jpg" alt="SplineRender-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-render.resources/SplineRender-Variant3.jpg" alt="SplineRender-Variant3">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](spline-render.resources/SplineRender-Demo.gif "Ejemplo de nodo 1")

</td>
</tr>
</table>
