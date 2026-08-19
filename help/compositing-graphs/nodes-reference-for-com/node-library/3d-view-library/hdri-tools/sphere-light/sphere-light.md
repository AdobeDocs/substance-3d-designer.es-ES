---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz de esfera para añadir fuentes de luz esférica a entornos HDRI para un mejor control de la iluminación.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz de esfera
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Luz de esfera

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-sphere-light.png){width="200px"}

## Luz de esfera

**En:** *Herramientas HDRI/vistas 3D*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una forma de esfera proyectada esféricamente. La transformación de la esfera se controla mediante un gizmo de transformación.

La Sphere Light es bastante versátil y tiene opciones que le permiten no solo generar luces redondas simples, sino también planetas u otros cuerpos celestes. Si no necesitas las opciones más avanzadas de iluminación y rotación, echa un vistazo a [Luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md).

## Entradas

* **Entrada de imagen de fondo**: *Entrada de color* Fondo opcional sobre el que componer la luz generada.
* **Entrada de imagen de forma**: *Entrada de color* Imagen opcional para asignar a la luz Esfera. Solo se usa cuando el modo Color de forma está establecido en Entrada de imagen.

### Parámetros

* **Modo de posición**: *Distancia desde origen, posición mundial*\
  Elige entre dos modos de colocación. La distancia desde origen es similar a las coordenadas polares, la esfera se establece en relación con el centro del panorama, la posición del mundo funciona como coordenadas estándar 3D.
* **Coordenadas de posición**
  * **Vector Arriba**: *Arriba Z, Arriba Y*\
    Solo con el modo Posición mundial, determine la orientación del sistema de coordenadas.
  * **Posición de mundo de esfera**: *-2.0 - 2.0*\
    Solo con el modo Posición mundial, establece la posición de la esfera en el espacio mundial.
  * **Posición**:\
    Solo con el modo de Distancia desde origen. Establece la posición en relación con el centro. Se puede manipular en la vista 2D.
  * **Distancia desde origen**: *0.0 - 20.0* Solo con modo de Distancia desde origen. Establece la distancia al origen y afecta al tamaño visible de la esfera.
* **Modo de color de forma**: *RGB, Temperatura (Kelvin), Entrada De Imagen*\
  Elija el método que desee utilizar para definir el color de la forma. La entrada de imagen permite utilizar la segunda ranura de entrada.
* **Color**: *(Valor de color)*\
  Solo con el modo Color de forma establecido en RGB. Selecciona el color de la forma.
* **Temperatura de forma**: *800.0 - 20000.0*\
  Solo con el modo Color de forma establecido en Temperatura. Establece el valor Kelvin para el color de la forma.
* **Gamma de entrada de imagen de esfera**: *sRGB, lineal*\
  Solo con el modo Color de forma establecido en Entrada de imagen. Determine cómo interpretar la entrada de imágenes de formas.
* **Rotación de esfera**: *0.0 - 1.0*\
  Solo con el modo Color de forma establecido en Entrada de imagen. Gira la esfera alrededor de su centro para orientar la imagen asignada.
* **Exposición (VE)**: *0.0 - 10.0*\
  Defina el valor de exposición para la forma generada, que se corresponde perfectamente con el valor de exposición de la imagen de fondo.
* **Radio de esfera**: *0.0 - 1.0*\
  Define el radio/tamaño de la esfera.
* **Dureza de esfera**: *0.0 - 1.0*\
  Define la dureza o la difuminación de la esfera.
* **Sombreado**: *Ninguno, Oscurecimiento de las extremidades, Luz de Sombreado*\
  Defina si se debe aplicar algún sombreado a la esfera. Permite que la esfera no aparezca como objeto sólido y sin iluminar. El oscurecimiento de las extremidades significa que aparece un ligero oscurecimiento en los bordes, la luz del Sombreado significa que la esfera está iluminada por una luz de Sombreado opcional.
* **Posición del Mundo Luz del Sombreado**: *-1.0 - 1.0*\
  Si el Sombreado se ajusta en Luz de Sombreado, la posición de la luz en la esfera se controla aquí.
* **Transparencia Penombra**: *0.0 - 1.0*\
  Si el Sombreado se define en Luz de Sombreado, controla la difuminación del sombreado.
* **Habilitar entrada de fondo**: *Falso/Verdadero*\
  Cambia el uso de la imagen de fondo opcional. Las composiciones generan luz sobre el fondo.
* **Color de fondo**: *(Valor de color)*\
  Si no se utiliza Entrada de fondo, defina aquí un valor de fondo de color sólido.
* **Gama de fondo**: *sRGB, lineal* Si se utiliza Entrada de fondo, establezca cómo interpretar la entrada de fondo.

## Imágenes de ejemplo

![](../../../../../../assets/sphere-light-ex.gif)

![](../../../../../../assets/spherelight-ex1.png)

</td>
</tr>
</table>
