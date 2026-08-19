---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz de forma para añadir fuentes de luz con forma personalizada a entornos HDRI para conseguir efectos de iluminación creativos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# Luz de forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## Luz de forma

**En:** *Herramientas HDRI/vistas 3D*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una forma rectangular proyectada esféricamente. La transformación de la forma se controla mediante un gizmo de transformación.

## Entradas

* **Entrada de imagen de fondo**: *Entrada de color* Fondo opcional sobre el que componer la luz generada.
* **Entrada de imagen de forma**: *Entrada de color* Imagen opcional para asignar a la luz Esfera. Solo se usa cuando el modo Color de forma está establecido en Entrada de imagen.

## Parámetros

* **Matriz de formas**
  * **Matriz**: *(Matriz de transformación)*\
    Control de transformación para el resultado. El resultado se puede modificar interactuando directamente con el lienzo.
  * **Desplazamiento**: *-2.0 - 2.0*\
    Mueve o traduce el resultado. El resultado se puede modificar interactuando directamente con el lienzo.
* **Forma**: *Rectángulo, disco*\
  Elige la forma que quieres colocar.
* **Modo de color de forma**: *RGB, Temperatura (Kelvin), Entrada De Imagen*\
  Elija el método que desee utilizar para definir el color de la forma. La entrada de imagen permite utilizar la segunda ranura de entrada.
* **Color**: *(Valor de color)*\
  Solo con el modo Color de forma establecido en RGB. Selecciona el color de la forma.
* **Temperatura de forma**: *800.0 - 20000.0*\
  Solo con el modo Color de forma establecido en Temperatura. Establece el valor Kelvin para el color de la forma.
* **Gamma de entrada de imagen de forma**: *sRGB, lineal*\
  Solo con el modo Color de forma establecido en Entrada de imagen. Determine cómo interpretar la entrada de imágenes de formas.
* **Exposición de forma (EV)**: *0.0 - 10.0*\
  Defina el valor de exposición para la forma generada, que se corresponde perfectamente con el valor de exposición de la imagen de fondo.
* **Dureza de forma**: *0.0 - 1.0*\
  Defina la dureza de los bordes de la forma.
* **Exposición de zona interactiva (EV)**: *0.0 - 10.0*\
  Definir exposición de zona interactiva central. Tenga en cuenta que esto no es muy visible en el modo de RGB.
* **Tamaño de zona interactiva**: *0.0 - 1.0*\
  Tamaño de la zona interactiva central.
* **Difuminación de zona interactiva**: *0.0 - 1.0*\
  Caída del punto de conexión central.
* **Posición del área interactiva**: *0.0 - 1.0*\
  Posición X e Y de la zona interactiva central.
* **Habilitar entrada de fondo**: *Falso/Verdadero*\
  Cambia el uso de la imagen de fondo opcional. Las composiciones generan luz sobre el fondo.
* **Color de fondo**: *(Valor de color)*\
  Si no se utiliza Entrada de fondo, defina aquí un valor de fondo de color sólido.
* **Gama de fondo**: *sRGB, lineal* Si se utiliza Entrada de fondo, establezca cómo interpretar la entrada de fondo.

## Imágenes de ejemplo

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>
