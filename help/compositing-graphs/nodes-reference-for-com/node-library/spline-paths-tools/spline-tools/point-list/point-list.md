---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: Utilice el nodo Lista de puntos para crear y gestionar listas de puntos para la generación de splines y trazados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lista de puntos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Lista de puntos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/point-list-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una lista de puntos que se deben recorrer mediante una spline.

Si se proporciona una lista de puntos existente a las entradas <b>Point</b>, la lista generada se anexa a la lista de entradas.

</td>
</tr>
</table>

>[!TIP]
>
> Este nodo se puede usar para proporcionar puntos al nodo [Spline (Poly Quadratic)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) para crear splines.

>[!IMPORTANT]
>
> Los conectores <b>Point List</b> y <b>Point Number</b> son *incompatibles* con los conectores <b>Spline Code</b>, <b>Spline Data</b> y <b>Spline Amount</b>, ya que se basan en datos diferentes.

## Conectores de entrada

<b>Vista previa </b>*Escala de grises* Vista previa de los puntos como una imagen en escala de grises.

<b>Entrada de lista de puntos</b> *Color*\
Una lista de puntos de entrada codificados en los canales RGBA de una imagen en color:\
    Posición <b>R</b> - X\
    <b>G</b> - Posición Y\
    <b>B</b> - Height\
    <b>A</b> - Datos empaquetados:\
            * Parte entera: Smoothness;\
            * Parte fraccional: Thickness.

<b>Entrada de número de punto</b> *Entero*\
Número de puntos de entrada.

## Conectores de salida

<b>Vista previa </b>*Escala de grises* Vista previa de los puntos como una imagen en escala de grises.

<b>Lista de puntos </b>*Color*\
La lista de salida de puntos codificados en los canales RGBA de una imagen en color:\
    Posición <b>R</b> - X\
    <b>G</b> - Posición Y\
    <b>B</b> - Height\
    <b>A</b> - Datos empaquetados:\
            * Parte entera: Smoothness;\
            * Parte fraccional: Thickness.

<b>Número de punto </b>*Entero*\
Número de puntos de salida.

## Parámetros

<b>Número de punto</b> *Entero* Número de puntos generados.

<b>Ajuste de Smoothness global</b> *Flotante* Aplica un desplazamiento uniforme al valor de smoothness de todos los puntos.\
El valor de smoothness resultante se fija al rango [0;1].

+++Propiedades de puntos
<b>Propiedades de p#</b> *Float3* Establece las propiedades del punto p#.\
*- Height:* Ajusta el height del punto en el que un valor inferior significa una ubicación más baja o más profunda;\
*- Smoothness:* Desplaza el inicio del suavizado de la spline en p#, donde un valor de 0 da como resultado una trayectoria dura y 1 en una completamente suave;\
*- Thickness:* Ajusta el thickness de la spline en p#. El thickness se utiliza en nodos Spline específicos.

+++

+++Puntos y coordenadas
<b>p#</b> *Float2* Establece la posición del punto p# en el espacio de textura.

+++

+++Vista previa
<b>Mostrar etiquetas</b> *Boolean*\
Para cada punto, muestra el nombre del punto junto a él en la salida &quot;Vista previa&quot;.

<b>Tamaño de etiqueta</b> *Float* (disponible cuando &#39;Mostrar etiquetas&#39; está establecido en &#39;True&#39;)\
El tamaño de la etiqueta para cada punto en el espacio de textura, donde 0,1 es una décima parte del ancho de la textura.

<b>Mostrar puntos</b> *Boolean*\
Muestra los puntos en la salida de &#39;Vista previa&#39;.

<b>Tamaño de puntos</b> *Float* (disponible cuando &#39;Mostrar puntos&#39; está establecido en &#39;True&#39;)\
El radio de los puntos en el espacio de textura, donde 0,1 es una décima parte del ancho de la textura.

+++

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](../../../../../../assets/PointList-Variant1.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/PointList-Demo1.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
