---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-2d-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación 2D polinomial para transformar splines con operaciones de traslación, rotación y escala.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación 2D spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Transformación 2D spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-2d-transform-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aplica una transformación global a todas las splines de entrada, incluida la inversión de su dirección.

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

<b>Voltear dirección</b> *Boolean* Invierte la dirección de la spline.

<b>Transformar matriz</b> *Float4* Matriz de transformación aplicada a las splines.\
Existen tres modos de edición de los parámetros matriciales:\
*- Gizmo de transformación*: retocar los controles del gizmo que se muestra en la vista 2D cuando se selecciona el nodo Transformación 2D polinomial;\
*- Rotación/Ampliación*: Controle individualmente la rotación y el estiramiento de las splines. Tenga en cuenta que los valores siempre se aplican en relación con la transformación actual. Por ejemplo, aplicar una anchura del 50 % dos veces da como resultado una anchura del 25 %;\
*- Valores de matriz*: Haga clic en el botón Editar valores de matriz para introducir directamente los valores numéricos sin procesar de la matriz.

<b>Desplazamiento</b> *Flotante2* Aplica un desplazamiento de posición a las splines en X (horizontal) e Y (vertical).

+++Vista previa
<b>Mostrar ayuda de dirección</b> *Booleano* Muestra un punto al principio de la spline y una punta de flecha al final en la salida de vista previa.

<b>Mostrar sobre de Thickness</b> *Booleano*\
Muestra líneas adicionales en los bordes del thickness de la spline.

<b>Cantidad de segmentos</b> *Entero* Ajusta el número de segmentos utilizados para dibujar la visualización de la spline en la salida de la vista previa.\
Un valor más alto produce una línea más suave.

<b>Thickness (px)</b> *Flotante* Ajusta el thickness de la visualización de la spline en píxeles en la salida de la vista previa.

+++

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant2-After.jpg" alt="Spline2DTransform-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/Spline2DTransform-Variant1-After.jpg" alt="Spline2DTransform-Variant1-After">
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

![Ejemplo de nodo 1](../../../../../../assets/Spline2DTransform-Demo1.gif "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
