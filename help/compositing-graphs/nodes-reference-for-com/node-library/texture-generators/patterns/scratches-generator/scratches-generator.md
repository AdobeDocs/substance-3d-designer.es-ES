---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: Utilice el nodo Generador de Scratches para crear patrones de arañazos de procedimiento para agregar desgaste y daños a los materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generador de Scratches
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Generador de Scratches

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## Generador de Scratches (normal)

**En:** *Generadores De Texturas**/Patrones*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Esto coloca arañazos aleatorios con muchas opciones de personalización, por ejemplo, lo que le permite establecer la dirección, la extensión y la distorsión.

Existe una versión especial de Generador de Scratches, Generador de Scratches Normal, que genera Mapas Normales basados en la profundidad de estos arañazos. La mayoría de las opciones son exactamente las mismas, pero tiene algunos parámetros adicionales claramente marcados para los ajustes de Normal (véase a continuación).

## Parámetros

* **Número de spline**: *1 - 512* Cantidad de arañazos (splines) que se deben colocar.
* **Segmentos Máximos Por Spline**: *2 - 256* Cantidad de segmentos/subdivisiones a lo largo de un rasguño. Produce curvas y distorsiones más suaves. El efecto es más apreciable con valores de Distorsión más altos.
* **Rotación de spline**: *0.0 - 1.0* Rotación uniforme de todas las splines, para orientarlas en una dirección.
* **Rotación aleatoria de spline**: *0.0 - 1.0* Variación del ángulo, gira aleatoriamente cada spline.
* **Escala de spline**: *0.0 - 1.0* Ajusta de manera uniforme todas las splines.
* **Aleatoria de escala de spline**: *0.0 - 1.0* Ajusta aleatoriamente cada spline de forma individual.
* **Distorsión spline**: *0.0 - 1.0* Nivel de distorsión uniforme en todas las splines.
* **Aleatorio de Distorsión de spline**: *0.0 - 1.0* Aleatoriza el nivel de distorsión de cada spline individualmente.
* **Frecuencia de Distorsión spline**: *0.0 - 1.0* Establece la frecuencia de distorsión y controla la escala de los detalles de distorsión.
* **Ancho de spline**: *0.0 - 2.0* Establece el ancho de todas las splines de manera uniforme.
* **Aleatorio de ancho de spline**: *0.0 - 1.0* Aleatoriza la anchura de spline de cada spline individualmente.
* **Aleatorio de posición de spline**: *0.0 - 1.0* Aleatoriza la posición de cada spline individualmente. Cuanto menor sea este valor, más splines se agruparán en el centro del lienzo. Se puede utilizar para crear puntos de arañazos.
* **Establecer ancho de spline en px**: *Falso/Verdadero* Determina las unidades utilizadas para la configuración de ancho de spline.
* **Aleatorio de luminancia (solo versión de escala de grises)**: *0.0 - 1.0* Aleatoriza la luminancia de cada spline individualmente.
* **Intensidad normal (solo versión normal)**: *0.0 - 1.0* Establece globalmente la intensidad del efecto Normal para cada spline.
* ** Aleatorio de intensidad normal **(solo versión normal)****: *0.0 - 1.0*Aleatoriza la intensidad normal de cada spline individualmente.
* ** Formato normal **(Solo versión normal)****: *DirectX, OpenGL*\
  Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).
* **Modo de transición**: *Ninguna, Inicio, Fin, Inicio + Fin* Establece si las splines se desvanecen y en qué dirección.
* **Longitud de transición**: *0.0 - 1.0* Establece la longitud del efecto de transición, si está habilitado anteriormente.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
