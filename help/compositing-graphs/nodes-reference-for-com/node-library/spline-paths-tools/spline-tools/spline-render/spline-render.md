---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---


# Procesamiento de spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-render-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja cadenas de segmentos a lo largo de la entrada <b>Splines</b> sobre la entrada <b>Background</b>.

</td>
</tr>
</table>

## Conectores de entrada

<b>Fondo </b>*Escala de grises* Imagen de escala de grises sobre la que se deben dibujar las splines.

<b>Códigos polinómicos</b> *Color* Coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen en color:\
Posición <b> R</b> - X\
<b> G</b> - Posición Y\
<b> B</b> - Height\
<b>A</b> - Datos empaquetados:\
* Firmar: La spline está cerrada (negativa) o abierta (positiva);\
* Valor absoluto: Thickness + 1.

<b>Datos de spline</b> *Color* Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - No utilizado\
<b> A</b> - No utilizado

<b>Cantidad de spline</b> *Entero* Número de splines de entrada.

## Conectores de salida

<b>Salida</b> *Escala de grises*\
La imagen resultante de dibujar las splines de entrada en la parte superior del fondo.

## Parámetros

<b>Modo</b> *Entero* Método para seleccionar las splines que se deben dibujar:
* *Dibujar lista de spline*: Dibujar todas las splines en la lista de entrada;
* *Dibujar una spline*: Dibuje sólo la spline especificada de la lista de entrada;
* *Dibujar rango de spline*: Dibuje sólo las splines del rango especificado en la lista de entrada.

<b>Dibujar índice de spline</b> *Entero* (disponible cuando &#39;Mode&#39; está establecido en &#39;Draw Single Spline&#39;)El índice de la spline que se debe dibujar.

<b>Dibujar rango de spline</b> *Integer2* (Disponible cuando &#39;Mode&#39; está establecido en &#39;Draw Spline Range&#39;)Intervalo de índices de las splines que se deben dibujar.

<b>Mostrar ayuda de dirección</b> *Booleano* Para cada spline, dibuja un punto al principio de la spline y una punta de flecha al final.

<b>Cantidad de segmentos</b> *Entero* Ajusta el número de segmentos dibujados a lo largo de las splines.\
Un valor más alto produce líneas más suaves.

<b>Cantidad de spline de sobre</b> *Entero*\
Número de segmentos duplicados que se deben dibujar a lo largo del thickness de cada spline.

<b>Inicio</b> *Flotante* Desplaza el inicio de la parte de la spline que se debe dibujar.\
El valor representa la longitud normalizada de la spline.

<b>Fin</b> *Flotante* Desplaza el extremo de la parte de la spline que se debe dibujar.\
El valor representa la longitud normalizada de la spline.

<b>Modo Tamaño Thickness</b> *Integer* Método para calcular el thickness de los segmentos dibujados:
* *Imagen*: el valor se normaliza en el espacio de textura, donde 1 es la anchura completa de la imagen. el thickness es relativo a la resolución de textura;
* *Píxel*: el valor es un número absoluto de píxeles en la textura, donde 1 es un píxel completo. El thickness es independiente de la resolución de la textura.

<b>Thickness (imagen)</b> *Float* (disponible cuando el modo de tamaño de Thickness está establecido en Imagen): el thickness de los segmentos dibujados se normalizó en el espacio de textura, donde 1 es el ancho completo de la imagen.

<b>Thickness (px)</b> *Flotante* (disponible cuando el modo &quot;Tamaño de Thickness&quot; está establecido en Píxel): el thickness de los segmentos dibujados como un número absoluto de píxeles en la textura, donde 1 es un píxel completo.

<b>Habilitar uniones</b> *Boolean* Rellena los espacios entre los segmentos individuales dibujados a lo largo de las splines, usando discos.

<b>Corrección no cuadrada </b>*Booleano* Ajusta la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones no cuadradas.\
Esto también afecta a la distribución uniforme.

+++Color
<b>Intensidad de fondo</b> *Float* El valor se multiplicó por la imagen de entrada de fondo.

<b>Estilo de spline</b> *Integer* Método utilizado para colorear las splines:
* *sólido*: Los segmentos se dibujan utilizando un valor de escala de grises uniforme;
* *Degradado*: Se aplica un degradado de negro a blanco a lo largo de cada cadena de segmentos de principio a fin;
* *Height*: El height de las splines se utiliza como valor de escala de grises para dibujar los segmentos.

<b>Color de spline</b> *Float* Valor de escala de grises uniforme utilizado para dibujar los segmentos.\
Cuando se selecciona un estilo de spline distinto de &quot;sólido&quot;, este color se multiplica por el color con estilo.

<b>Luminancia aleatoria</b> *Float* Para cada cadena de segmentos sin cortar de una spline, aplica un desplazamiento aleatorio en el intervalo especificado al valor de escala de grises utilizado para dibujar esa cadena.

<b>Modo de fusión</b> *Entero* Método de fusión de los colores del fondo y de los segmentos superpuestos dibujados a lo largo de las splines:
* *Máx.*: Se utiliza el valor más brillante;
* *Agregar*: Los valores se suman.

+++

+++Segmentos aleatorios
<b>Inicio de segmentos aleatorios</b> *Float* Ajusta la probabilidad de que se corte la cadena de segmentos más cercana al inicio de la spline.

<b>Fin de segmentos aleatorios</b> *Float* Ajusta la probabilidad de que se corte la cadena de segmentos más cerca del final de la spline.

<b>Desplazamiento aleatorio</b> *Float* Establece la cantidad máxima de desplazamiento aplicado a cada segmento de corte a lo largo de su normal.\
Este parámetro no tiene efecto cuando Inicio y Fin están establecidos en 0.

<b>Centro de desplazamiento aleatorio</b> *Flotante* Desplaza el centro del desplazamiento aleatorio aplicado a cada segmento de corte a lo largo de su eje normal.

+++

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-Before.jpg" alt="SplineRender-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-After.jpg" alt="SplineRender-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-After.jpg" alt="SplineRender-Variant1-After">
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
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant3.jpg" alt="SplineRender-Variant3">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](../../../../../../assets/SplineRender-Demo.gif "Ejemplo de nodo 1")

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
