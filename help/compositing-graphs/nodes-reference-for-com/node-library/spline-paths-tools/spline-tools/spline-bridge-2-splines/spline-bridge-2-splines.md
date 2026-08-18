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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1247'
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

## Conectores de entrada

<b>Vista previa n.º 1</b> *Escala de grises* Vista previa de las splines de entrada #1 como imagen en escala de grises.

<b>Códigos polinómicos #1</b> *Color* Coordenadas de los puntos de las splines de entrada #1 codificados en los canales RGBA de una imagen en color.\
    Posición <b>R</b> - X\
    <b>G</b> - Posición Y\
    <b>B</b> - Height\
    <b>A</b> - Datos empaquetados:\
        * Firmar: La spline está cerrada (negativa) o abierta (positiva);\
        * Valor absoluto: Thickness + 1.

<b>Datos de spline #1</b> *Color* Datos adicionales de las splines de entrada #1 codificadas en los canales RGBA de una imagen en color.\
    <b>R</b> - Tangentes X\
    <b>G</b> - Tangentes Y\
    <b>B</b> - Sin usar\
    <b>A</b> - Sin usar

<b>Cantidad de spline #1</b> *Entero* Número de splines de entrada #1.

<b>Vista previa n.º 2</b> *Escala de grises* Vista previa de las splines de entrada #2 como imagen en escala de grises.

<b>Códigos polinómicos #2</b> *Color* Coordenadas de los puntos #2 de las splines de entrada codificados en los canales RGBA de una imagen en color.\
    Posición <b>R</b> - X\
    <b>G</b> - Posición Y\
    <b>B</b> - Height\
    <b>A</b> - Datos empaquetados:\
        * Firmar: La spline está cerrada (negativa) o abierta (positiva);\
        * Valor absoluto: Thickness + 1.

<b>Datos de spline #2</b> *Color* Datos adicionales de las splines de entrada #2 codificadas en los canales RGBA de una imagen en color.\
    <b>R</b> - Tangentes X\
    <b>G</b> - Tangentes Y\
    <b>B</b> - Sin usar\
    <b>A</b> - Sin usar

<b>Cantidad de spline #2</b> *Entero* Número de splines de entrada #2.

<b>Iniciar curva de longitud de tangente</b> *Escala de grises* (disponible cuando &quot;Tipo de splines de puente&quot; está establecido en &quot;Curva cúbica&quot;)Imagen que describe una curva utilizando los valores de su primera fila de píxeles.\
Esta entrada se utiliza para controlar la longitud de las tangentes de salida para el punto inicial de cada spline generada a lo largo de la spline #1.\
Puede utilizar un nodo Curva para crear la curva.

<b>Iniciar curva de rotación tangente</b> *Escala de grises* (disponible cuando &quot;Tipo de splines de puente&quot; está establecido en &quot;Curva cúbica&quot;)Imagen que describe una curva utilizando los valores de su primera fila de píxeles.\
Esta entrada se utiliza para controlar la rotación de las tangentes de ‘salida’ para el punto inicial de cada spline generada a lo largo de la spline #1.\
El valor de escala de grises de la imagen representa un número de vueltas.\
Puede utilizar un nodo Curva para crear la curva.

<b>Curva de longitud de tangente final</b> *Escala de grises* (disponible cuando &quot;Tipo de splines de puente&quot; está establecido en &quot;Curva cúbica&quot;)Imagen que describe una curva utilizando los valores de su primera fila de píxeles.\
Esta entrada se utiliza para controlar la longitud de las tangentes de entrada para el punto final de cada spline generada a lo largo de la spline #2.\
Puede utilizar un nodo Curva para crear la curva.

<b>Finalizar curva de rotación de tangente</b> *Escala de grises* (disponible cuando &quot;Tipo de splines de puente&quot; está establecido en &quot;Curva cúbica&quot;)Imagen que describe una curva utilizando los valores de su primera fila de píxeles.\
Esta entrada se utiliza para controlar la rotación de las tangentes &quot;in&quot; para el punto final de cada spline generada a lo largo de la spline #2.\
El valor de escala de grises de la imagen representa un número de vueltas.\
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

<b>Cantidad de splines de puente</b> *Entero* Número de splines generados a lo largo de la spline #1 a la spline #2.

<b>Tipo de splines de puente</b> *Entero* Tipo de spline que se genera:
* Lineal: una spline recta de principio a fin;
* Curva cúbica: una spline curva de principio a fin, la curva se controla mediante la longitud y el ángulo de los puntos inicial y final.

<b>Iniciar spline #1</b> *Flotante* Desplaza la ubicación a lo largo de la spline #1 desde donde se generan las splines. El valor es la longitud normalizada de la spline #1.\
Un valor más alto hace que el mismo número de splines se comprima más estrechamente.

<b>Iniciar spline #2</b> *Flotante* Desplaza la ubicación a lo largo de la spline #2 desde donde se generan las splines. El valor es la longitud normalizada de la spline #2.\
Un valor más alto hace que el mismo número de splines se comprima más estrechamente.

<b>Finalizar spline #1</b> *Flotante* Desplaza la ubicación a lo largo de la spline #1 hasta el lugar donde se generan las splines. El valor es la longitud normalizada de la spline #1.\
Un valor más bajo hace que el mismo número de splines se comprima más estrechamente.

<b>Finalizar spline #1</b> *Flotante* Desplaza la ubicación a lo largo de la spline #2 hasta el lugar donde se generan las splines. El valor es la longitud normalizada de la spline #2.\
Un valor más bajo hace que el mismo número de splines se comprima más estrechamente.

<b>Desplazamiento de spline #1</b> *Flotante* Aplica un desplazamiento al punto inicial de todas las splines a lo largo de la spline #1. El valor es la longitud normalizada de la spline #1.\
Las splines que coinciden con el principio o el final de la spline se dejan allí.

<b>Desplazamiento de spline #2</b> *Flotante* Aplica un desplazamiento al punto inicial de todas las splines a lo largo de la spline #2. El valor es la longitud normalizada de la spline #2.\
Las splines que coinciden con el principio o el final de la spline se dejan allí.

<b>Inicio aleatorio de desplazamiento</b> *Flotante* Aplica un desplazamiento aleatorio al punto inicial de cada spline a lo largo de la spline #1. El valor es la distancia normalizada entre las splines de la spline #1.\
Cuando se dejan en 0, las splines se espacian uniformemente entre los puntos Spline inicial #1 y Spline final #1.

<b>Fin aleatorio de desplazamiento</b> *Flotante* Aplica un desplazamiento aleatorio al punto final de cada spline a lo largo de la spline #2. El valor es la distancia normalizada entre las splines de la spline #2.\
Cuando se dejan en 0, las splines se espacian uniformemente entre los puntos Nº 2 de la spline inicial y Nº 2 de la spline final.

<b>Inicio de longitud de tangente</b> *Float* (Disponible cuando &quot;Tipo de splines de puente&quot; está establecido en &quot;Curva cúbica&quot;)La longitud de la tangente &quot;out&quot; para el punto inicial en la spline #1 de todas las splines generadas.

<b>Final de longitud de tangente</b> *Float* (Disponible cuando &quot;Tipo de splines de puente&quot; está establecido en &quot;Curva cúbica&quot;)Longitud de la tangente &quot;in&quot; para el punto final de la spline #2 de todas las splines generadas.

<b>Inicio de rotación de tangentes</b> *Float* (Disponible cuando &quot;Tipo de splines de puente&quot; está establecido en &quot;Curva cúbica&quot;)Rotación de la tangente &quot;out&quot; para el punto inicial en la spline #1 de todas las splines generadas.\
El valor es un número de vueltas.

<b>Fin de rotación tangente</b> *Float* (Disponible cuando &quot;Tipo de splines de puente&quot; está establecido en &quot;Curva cúbica&quot;)Rotación de la tangente &quot;in&quot; para el punto final de la spline #2 de todas las splines generadas.\
El valor es un número de vueltas.

+++Vista previa
<b>Cantidad de segmentos</b> *Entero* Ajusta el número de segmentos utilizados para dibujar la visualización de la spline en la salida de la vista previa.\
Un valor más alto produce una línea más suave.

<b>Mostrar ayuda de dirección</b> *Booleano* Muestra un punto al principio de la spline y una punta de flecha al final en la salida de vista previa.

<b>Mostrar sobre de Thickness</b> *Booleano*\
Muestra líneas adicionales en los bordes del thickness de la spline.

<b>Thickness (px)</b> *Flotante* Ajusta el thickness de la visualización de la spline en píxeles en la salida de la vista previa.

+++

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
