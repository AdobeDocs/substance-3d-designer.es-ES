---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-grayscale.html"
breadcrumb-title: ''
description: Utilice el nodo Escala de grises del asignador de puente de spline para enlazar texturas entre dos splines con asignación de escala de grises.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Bridge Mapper Escala de grises
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---


# Spline Bridge Mapper Escala de grises

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-bridge-mapper-grayscale-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Asigna una imagen en escala de grises a través de una lista de splines de entrada para que la imagen atraviese las splines en orden.

</td>
</tr>
</table>

>[!TIP]
>
> La asignación va desde la primera spline de la lista hasta la última y atraviesa las splines intermedias siguiendo estrictamente el orden de estas splines en la lista.
> 
> Por lo tanto, debe tener en cuenta el orden en el que se añaden las splines de antemano.

>[!NOTE]
>
> Vea también [Color del asignador de puentes polinómicos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-col/spline-bridge-mapper-color.md).

## Conectores de entrada

<b>Códigos polinómicos</b> *Color* Coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen en color:

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

<b>Mapa de color </b>*Escala de grises* Imagen de entrada en escala de grises que se debe asignar a las splines de entrada.

## Conectores de salida

<b>Color</b> *Escala de grises* El resultado de asignar la imagen de color de entrada a través de las splines, como una imagen en escala de grises.

<b>Height</b> *Escala de grises* El height de las splines asignadas a través de las splines, como una imagen en escala de grises.

<b>UV</b> *Color* Los UV (es decir, coordenadas) de la imagen asignada, codificados en los canales rojo (U) y verde (V) de una imagen en color.

<b>Máscara</b> *Escala de grises* Máscara de la asignación a través de las splines.

## Parámetros

<b>Cantidad de segmentos</b> *Entero* Las splines se simplifican en segmentos antes de que las coordenadas de la imagen las atraviesen.\
Una mayor cantidad de segmentos produce una asignación más fluida a lo largo de las curvas.

<b>Reducir el estiramiento de UV</b> *Booleano* Ajusta el método utilizado para interpolar las coordenadas de la imagen de una spline a la siguiente para minimizar la ampliación cuando la distancia entre las splines es irregular.

<b>Escala de UV</b> *Float2* Ajusta la escala de las coordenadas de la imagen. Los valores más altos dan como resultado una imagen de mosaico más denso.

<b>Rotación UV</b> *Float* Rota las coordenadas de la imagen alrededor de su centro.

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-After.jpg" alt="SplineBridgeMapperGrayscale-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineBridgeMapper-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-After1.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineBridgeMapperGrayscale-Graph.jpg "Ejemplo de nodo 2")

</td>
</tr>
</table>
