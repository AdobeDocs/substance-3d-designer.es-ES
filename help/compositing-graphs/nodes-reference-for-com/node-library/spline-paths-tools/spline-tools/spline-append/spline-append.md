---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: Utilice el nodo Anexar spline para anexar varias splines juntas y crear rutas continuas más largas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Append spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# Append spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-append-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Las splines se empaquetan como una lista. Este nodo anexa una lista de splines de entrada (conjunto #2) a una lista existente (conjunto #1).

El orden de las listas se mantiene, lo que significa que si se agrega una lista D-E-F a una lista A-B-C, se obtiene una lista A-B-C-D-E-F.

</td>
</tr>
</table>

>[!TIP]
>
> Tenga en cuenta el orden en el que se anexan las splines, ya que este orden se tiene en cuenta en otros nodos, como [Dispersión en splines](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md), los nodos [Puente de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md), etc.

## Conectores de entrada

<b>Vista previa n.º 1</b> *Escala de grises* Vista previa del primer conjunto de splines de entrada como imagen en escala de grises.

<b>Códigos Spline #1</b> *Color* Coordenadas de los puntos del primer conjunto de splines de entrada codificados en los canales RGBA de una imagen en color.\
Posición <b>R</b> - X\
<b>G</b> - Posición Y\
<b>B</b> - Height\
<b>A</b> - Datos empaquetados:\
* Firmar: La spline está cerrada (negativa) o abierta (positiva);\
* Valor absoluto: Thickness + 1.

<b>Datos de spline #1</b> *Color* Datos adicionales del primer conjunto de splines de entrada codificadas en los canales RGBA de una imagen en color.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Sin usar\
<b>A</b> - Sin usar

<b>Cantidad de división #1</b> *Entero* Número de splines de entrada en el primer conjunto.

<b>Vista previa n.º 2</b> *Escala de grises* Vista previa del segundo conjunto de splines de entrada como una imagen en escala de grises.

<b>Spline #2 Coords</b> *Color* Coordenadas del segundo conjunto de puntos de splines de entrada codificados en los canales RGBA de una imagen en color.\
Posición <b>R</b> - X\
<b>G</b> - Posición Y\
<b>B</b> - Height\
<b>A</b> - Datos empaquetados:\
* Firmar: La spline está cerrada (negativa) o abierta (positiva);\
* Valor absoluto: Thickness + 1.

<b>Datos de spline #2</b> *Color* Datos adicionales del segundo conjunto de splines de entrada codificadas en los canales RGBA de una imagen en color.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Sin usar\
<b>A</b> - Sin usar

<b>Cantidad de división #2</b> *Entero* Número de splines de entrada en el segundo conjunto.

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

<b>Voltear spline #1 Dirección </b>*Boolean* Invierte la dirección de las splines en el primer conjunto.

<b>Voltear spline #2 Dirección </b>*Boolean* Invierte la dirección de las splines en el segundo conjunto.

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

![Ejemplo de nodo 1](../../../../../../assets/SplineAppend-Demo.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineAppend-Graph.jpg "Ejemplo de nodo 2")

</td>
</tr>
</table>

![Demostración de nodo](../../../../../../assets/SplineAppend-Demo2.gif "Demostración de nodo")
