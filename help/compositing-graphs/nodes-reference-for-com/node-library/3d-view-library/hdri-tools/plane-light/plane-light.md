---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz plana para añadir fuentes de luz planas a entornos HDRI para el control de iluminación direccional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz plana
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# Luz plana

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-plane-light.png){width="200px"}

## Luz plana

**En:** *Herramientas HDRI/vistas 3D*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una forma de plano proyectada esféricamente. El plano se puede colocar y orientar en 3D mediante los parámetros de entrada.

Difiere de la sencilla [luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) en que tiene opciones de colocación más avanzadas fuera de una proyección de Distancia desde origen más simple, y se pueden aplicar más patrones y máscaras, similar a [luz de línea](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

## Entradas

* **Entrada de imagen de fondo**: *Entrada de color*\
  Fondo opcional sobre el que componer la luz generada.
* **Entrada de imagen de forma**: *Entrada de color*\
  Imagen opcional para asignar a la luz de línea. Solo se usa cuando el modo Color de forma está establecido en Entrada de imagen.
* **Entrada de imagen de motivo**: *Entrada en escala de grises*\
  Imagen de motivo personalizado, utilizada cuando el parámetro &quot;Motivo&quot; se define en &quot;Entrada de imagen&quot;.

## Parámetros

* **Modo de posición**: *Suelo/Techo, Distancia desde origen, Posiciones Mundiales*\
  Seleccione entre tres modos de colocación diferentes. Tierra/techo y Distancia desde origen admiten la manipulación en la vista 2D, las posiciones de Mundo solo se pueden cambiar a través de las propiedades, pero sí admiten una ubicación más exacta.
* **Mostrar cuadrícula de tierra**: *Falso/Verdadero*\
  Función auxiliar para permitir que se dibuje una cuadrícula de tierra de depuración. Ayuda a estimar la posición de las líneas en el espacio.
* **Coordenadas de posición**
  * **Vector Arriba**: *Arriba Z, Arriba Y*\
    Solo con el modo Posición mundial, determine la orientación del sistema de coordenadas.
  * **Posición UV del plano**:\
    Solo con suelo / techo y Distancia desde origen. Establece la posición del plano en el espacio UV.
  * **Posición Mundial del Avión**: *-2.0 - 2.0*\
    Solo con el modo Posiciones Mundiales. Establece la posición del plano en el espacio mundial. No se admite la interacción de vista 2D.
  * **Height absoluto de plano**: *0.0 - 1.0*\
    Solo con el modo de posición de suelo / techo, establece el height absoluto desde el techo. Utilice Mostrar cuadrícula de suelo para estimar mejor la posición.
  * **Distancia desde origen**: *0.0 - 1.0*\
    Solo con el modo de posición de Distancia desde origen. Establece la distancia desde el centro del panorama para ambos puntos.
* **Modo de color de forma**: *RGB, Temperatura (Kelvin), Entrada De Imagen*\
  Elija el método que desee utilizar para definir el color de la forma. La entrada de imagen permite utilizar la segunda ranura de entrada.
* **Color**: *(Valor de color)*\
  Solo con el modo Color de forma establecido en RGB. Selecciona el color de la forma.
* **Temperatura**: *800.0 - 20000.0*\
  Solo con el modo Color de forma establecido en Temperatura. Establece el valor Kelvin para el color de la forma.
* **Modo UV de imagen de forma**: *Ampliar, Ampliar sólo el medio, Repetir + Espaciado*\
  Solo con el modo Color de forma establecido en Entrada de imagen. Define cómo se aplica la imagen a la forma de línea y determina el comportamiento de la repetición UV.
* **Espaciado de repetición de la imagen de forma**: *0.0 - 1.0*\
  Solo con el modo Color de forma definido en Entrada de imagen y con el modo UV definido en Repetir + Espaciado. Define el espaciado cuando la imagen se repite a lo largo de la línea.
* **Gamma de imagen de forma**: *sRGB, lineal*\
  Solo con el modo Color de forma establecido en Entrada de imagen. Determine cómo interpretar la entrada de imágenes de formas.
* **Exposición (VE)**: *0.0 - 10.0*\
  Defina el valor de exposición para la forma generada, que se corresponde perfectamente con el valor de exposición de la imagen de fondo.
* **Escala de plano**: *0.0 - 1.0*\
  Establecer una escala uniforme de la forma Plano.
* **Tamaño de plano**: *0.0 - 1.0*\
  Defina el tamaño no uniforme de la forma Plano.
* **Rotación de plano**: *0.0 - 1.0*\
  Girar plano a lo largo de su eje central.
* **Patrón**: *Cuadrado liso, Cuadrado afilado, Cono, Hemisferio, Entrada de imagen*\
  Seleccione la forma de motivo que desea utilizar.
* **Dureza del motivo**: *0.0 - 1.0*\
  Definir dureza/contraste para el patrón.
* **Modo UV De Patrón**: *Ampliar, Ampliar sólo el medio*\
  Define cómo usar la máscara de motivo secundaria, aplicada sobre la imagen de forma.
* **Habilitar recorte de tierra**: *Falso/Verdadero*\
  Active esta opción si el plano se puede recortar mediante un plano de tierra o se sigue mostrando al pasar por debajo de él. Utilice Mostrar cuadrícula de suelo para estimarlo mejor.
* **Height de tierra**: *-2.0 - 0.0*\
  Ajuste el height de masa para el recorte.
* **Habilitar entrada de fondo**: *Falso/Verdadero*\
  Cambia el uso de la imagen de fondo opcional. Las composiciones generan luz sobre el fondo.
* **Color de fondo**: *(Valor de color)*\
  Si no se utiliza Entrada de fondo, defina aquí un valor de fondo de color sólido.
* **Gama de fondo**: *sRGB, lineal* Si se utiliza Entrada de fondo, establezca cómo interpretar la entrada de fondo.

## Imágenes de ejemplo

![](../../../../../../assets/plane-light-ex.gif)

</td>
</tr>
</table>
