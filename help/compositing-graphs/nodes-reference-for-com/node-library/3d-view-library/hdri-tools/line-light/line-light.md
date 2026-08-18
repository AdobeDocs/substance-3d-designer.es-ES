---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz de línea para crear fuentes de luz lineal en entornos HDRI para simular iluminación fluorescente y de banda.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz de línea
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---


# Luz de línea

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-line-light.png){width="200px"}

## Luz de línea

**En:** *Herramientas HDRI/vistas 3D*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una forma de línea proyectada esféricamente basada en las coordenadas de dos puntos en el espacio. En comparación con [Luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md), tiene más opciones para orientar formas y aplicar patrones repetidos a la forma de luz.

Los modos de posicionamiento para este nodo son ligeramente más complejos que otros nodos de luz HDRI. Se recomienda probar algunos modos de tamaño diferentes para encontrar cuál funciona para su escenario.

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
  * **Punto 1 Posición UV**:\
    Solo con suelo / techo y Distancia desde origen. Establece la posición del primer punto en el espacio UV.
  * **Posición UV del punto 2**:\
    Solo con suelo / techo y Distancia desde origen. Establece la posición del segundo punto en el espacio UV.
  * **Posición Mundial Punto 1**: *-2.0 - 2.0*\
    Solo con el modo Posiciones Mundiales. Establece el primer punto en el espacio de entorno. No se admite la interacción de vista 2D.
  * **Posición Mundial Punto 2**: *-2.0 - 2.0*\
    Solo con el modo Posiciones Mundiales. Establece el segundo punto en el espacio de entorno. No se admite la interacción de vista 2D.
  * **Height absoluto de línea**: *0.0 - 1.0*\
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
* **Rotación de línea**: *0.0 - 1.0*\
  Gira la línea a lo largo del eje de su longitud. La línea se trata como una tarjeta plana cuando se gira.
* **Thickness de línea**: *0.0 - 1.0*\
  Establece el thickness de la tarjeta de línea.
* **Patrón**: *Cuadrado liso, Cuadrado afilado, Cono, Hemisferio, Entrada de imagen*\
  Seleccione la forma de motivo que desea utilizar.
* **Dureza del motivo**: *0.0 - 1.0*\
  Definir la dureza/contraste del patrón.
* **Modo UV De Patrón**: *Ampliar, Ampliar sólo el medio, Repetir + Espaciado*\
  Define cómo usar la máscara de motivo secundaria, aplicada sobre la imagen de forma.
* **Espaciado de repetición de motivo**: *0.0 - 1.0*\
  Solo si el modo UV de motivo está definido en Repetir + Espaciado. Defina el espaciado entre patrones repetidos.
* **Habilitar recorte de tierra**: *Falso/Verdadero*\
  Activar recorte de dibujo de líneas. El efecto no es visible al utilizar el modo de colocación Tierra/Techo.
* **Height de tierra**: *-2.0 - 0.0*\
  Define el height relativo del plano de redondeo, que se utiliza para el recorte. Afecta a la cuadrícula de suelo dibujada.
* **Habilitar entrada de fondo**: *Falso/Verdadero*\
  Cambia el uso de la imagen de fondo opcional. Las composiciones generan luz sobre el fondo.
* **Color de fondo**: *(Valor de color)*\
  Si no se utiliza Entrada de fondo, defina aquí un valor de fondo de color sólido.
* **Gama de fondo**: *sRGB, lineal* Si se utiliza Entrada de fondo, establezca cómo interpretar la entrada de fondo.

## Imágenes de ejemplo

![](../../../../../../assets/line-light-ex.gif)

</td>
</tr>
</table>
