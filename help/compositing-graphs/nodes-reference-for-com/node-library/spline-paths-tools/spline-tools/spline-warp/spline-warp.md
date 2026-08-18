---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: Utilice el nodo Deformación polinomial para deformar texturas a lo largo de trazados polinomiales con el fin de crear motivos curvos y orgánicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deformación polinomial
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---


# Deformación polinomial

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-warp-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Desplaza las splines de entrada en función del mapa de intensidad de entrada o del mapa vectorial.

La intensidad del efecto de deformación se puede ajustar a lo largo de la spline mediante los controles de atenuación.

</td>
</tr>
</table>

## Conectores de entrada

<b>Vista previa</b> *Escala de grises* Vista previa de las splines de entrada como una imagen en escala de grises.

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

<b>Mapa de intensidad</b> *Escala de grises* (disponible cuando &quot;Usar mapa vectorial&quot; está establecido en &quot;Falso&quot;)\
Imagen de escala de grises de entrada utilizada para controlar la dirección y la intensidad del efecto de deformación en las splines de entrada.\
El color de cada píxel de la imagen especifica un multiplicador para desplazar los puntos de la spline a lo largo de su normal (es decir, la dirección perpendicular a la spline), hasta el grupo completo de la imagen.\
El [0; 1] los valores de la imagen se reasignan al [-1; 1] rango cuando se lee como multiplicador: 0 y 1 desplazan la spline en la misma distancia pero en direcciones opuestas. 0,5 deja la spline en su lugar.

<b>Mapa de vectores</b> *Escala de grises* (disponible cuando &#39;Usar mapa vectorial&#39; está establecido en &#39;Verdadero&#39;): la imagen de color de entrada utilizada para controlar la dirección y la intensidad del efecto de deformación en las splines de entrada.\
El color de cada píxel de la imagen especifica un vector (X, Y) cuyas coordenadas se codifican en los canales rojo (X) y verde (Y). +X es la derecha y +Y es abajo.\
El [0; 1] los valores de la imagen se reasignan al [-1; 1] rango cuando se lee como coordenadas vectoriales: 0 rojo desplaza puntos hacia la izquierda y 0 verde desplaza puntos hacia arriba. El color rojo y verde de 0,5 deja la spline en su lugar.

<b>Curva de atenuación</b> *Escala de grises* Imagen que describe una curva utilizando los valores de su primera fila de píxeles.\
Cuando el parámetro Utilizar curva de atenuación se establece en True, esta entrada se utiliza para controlar la atenuación del efecto de deformación cerca del inicio y el final de la spline.\
La curva proporciona un perfil para la atenuación, donde el primer píxel de la fila es la intensidad del efecto de deformación al principio de la spline y el último es la intensidad al final. El valor de escala de grises es la intensidad.\
Puede utilizar un nodo Curva para crear la curva.

## Conectores de salida

<b>Vista previa</b> *Escala de grises* Vista previa de las splines de salida como una imagen en escala de grises.

<b>Códigos polinómicos</b> *Color* Coordenadas de los puntos de las splines de salida codificados en los canales RGBA de una imagen en color.\
    Posición <b>R</b> - X\
    <b>G</b> - Posición Y\
    <b>B</b> - Height\
    <b>A</b> - Datos empaquetados:\
        * Firmar: La spline está cerrada (negativa) o abierta (positiva);\
        * Valor absoluto: Thickness + 1.

<b>Datos de spline</b> *Color* Datos adicionales de las splines de salida codificadas en los canales RGBA de una imagen en color.\
    <b>R</b> - Tangentes X\
    <b>G</b> - Tangentes Y\
    <b>B</b> - Sin usar\
    <b>A</b> - Sin usar

<b>Cantidad de spline</b> *Entero* Número de splines de salida.

## Parámetros

<b>Intensidad de deformación</b> *Flotador* Intensidad de desplazamiento de las splines.

<b>Centro de deformación</b> *Float* Especifica el valor de mapa de intensidad que corresponde a dejar las splines en su lugar.\
Un valor de 0 o 1 significa que las splines solo se pueden desplazar en un lado.

<b>Modo de muestreo</b> *Integer* Método de asignación de los valores de mapa de intensidad o mapa vectorial a las splines:\
*- Espacio de textura*: Los valores se aplican a las splines donde se colocarían si se colocan en una textura utilizando las coordenadas UV de la textura. Esto aplica efectivamente el valor a las splines &quot;in situ&quot;;\
*- Horizontal a lo largo de la spline*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), donde cada fila se aplica a una spline diferente de arriba abajo;\
*- Hora. a lo largo de la spline (rand. desplazamiento X)*: Los valores se aplican directamente a las coordenadas de las splines codificadas (véase la entrada Spline Coords), con un desplazamiento horizontal aleatorio en el mapa de escala para cada spline (es decir, cada fila en Spline Coords);\
*- Hora. a lo largo de la spline (rand. desplazamiento Y)*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento vertical aleatorio en el mapa de escala para cada spline (es decir, cada fila de códigos de spline).

<b>Usar mapa vectorial</b> *Boolean* Cambia el método de desplazamiento de las splines por el uso de una entrada de mapa vectorial para especificar la dirección del desplazamiento.\
El color de cada píxel de la imagen especifica un vector (X, Y) cuyas coordenadas se codifican en los canales rojo (X) y verde (Y). +X es la derecha y +Y es abajo.\
El [0; 1] los valores de la imagen se reasignan al [-1; 1] rango cuando se lee como coordenadas vectoriales: 0 rojo desplaza puntos hacia la izquierda y 0 verde desplaza puntos hacia arriba. El color rojo y verde de 0,5 deja la spline en su lugar.

<b>Usar curva de atenuación</b> *Booleano* Permite controlar la intensidad del efecto de deformación a lo largo de una spline mediante una curva codificada en la imagen de entrada Curva de atenuación.<b></b>

<b>Mosaico de mapa de intensidad</b> *Float* (disponible cuando el &quot;Modo de muestreo&quot; no está establecido en &quot;Espacio de textura&quot;) Ajusta el mosaico del mapa de intensidad cuando se asigna directamente a las coordenadas de spline (consulte Entrada de códigos de spline).<b></b>

<b>Iniciar atenuación</b> *Float* (Disponible cuando &quot;Usar curva de atenuación&quot; está establecido en &quot;False&quot;)Un multiplicador para la atenuación del efecto de deformación cerca del inicio de la spline.\
Un valor de 1 significa que no se aplica deformación al inicio de la spline.

<b>Finalizar atenuación</b> *Float* (Disponible cuando &quot;Usar curva de atenuación&quot; está establecido en &quot;False&quot;)Un multiplicador para la atenuación del efecto de deformación cerca del final de la spline.\
Un valor de 1 significa que no se aplica deformación al final de la spline.<b></b>

<b>Recalcular tangentes</b> *Booleano* Si es True, las tangentes de una spline se vuelven a calcular después de aplicar el efecto de deformación.\
Esto garantiza que las tangentes de la spline sean coherentes con su trayectoria cuando se utilizan en nodos como Dispersión en spline o Spline Flow Mapper.

+++Vista previa
<b>Cantidad de segmentos</b> *Entero* Ajusta el número de segmentos utilizados para dibujar la visualización de la spline en la salida de la vista previa.\
Un valor más alto produce una línea más suave.

<b>Mostrar ayuda de dirección</b> *Booleano* Muestra un punto al principio de la spline y una punta de flecha al final en la salida de vista previa.

<b>Mostrar sobre de Thickness</b> *Booleano*\
Muestra líneas adicionales en los bordes del thickness de la spline.

<b>Thickness (px)</b> *Flotante* Ajusta el thickness de la visualización de la spline en píxeles en la salida de la vista previa.

<b>Intensidad de vista previa en segundo plano</b> *Flotador*\
El valor se multiplica por la imagen de entrada de vista previa de fondo.

+++

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![Ejemplo de nodo 1](../../../../../../assets/SplineWarp-Demo.gif "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">



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
