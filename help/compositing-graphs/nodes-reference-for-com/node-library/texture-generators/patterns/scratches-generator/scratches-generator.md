---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 8%

---


# Generador de Scratches

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](scratches-generator.resources/scratches-generator-01.png)

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Esto coloca arañazos aleatorios con muchas opciones de personalización, por ejemplo, lo que le permite establecer la dirección, la extensión y la distorsión.

Existe una versión especial de Generador de Scratches, Generador de Scratches Normal, que genera Mapas Normales basados en la profundidad de estos arañazos. La mayoría de las opciones son exactamente las mismas, pero tiene algunos parámetros adicionales claramente marcados para los ajustes de Normal (véase a continuación).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Número de spline</b> <i>1 - 512</i> | Cantidad de arañazos (splines) que se deben colocar. |
| <b>Segmentos Máximos Por Spline</b> <i>2 - 256</i> | Cantidad de segmentos/subdivisiones a lo largo de un rasguño. Produce curvas y distorsiones más suaves. El efecto es más apreciable con valores de Distorsión más altos. |
| <b>Rotación de spline</b> <i>0.0 - 1.0</i> | Rotación uniforme de todas las splines, para orientarlas en una dirección. |
| <b>Rotación aleatoria de spline</b> <i>0.0 - 1.0</i> | Variación del ángulo: gira aleatoriamente cada spline. |
| <b>Escala de spline</b> <i>0.0 - 1.0</i> | Escala de manera uniforme todas las splines. |
| <b>Aleatoria de escala de spline</b> <i>0.0 - 1.0</i> | Escala aleatoriamente cada spline individualmente. |
| <b>Distorsión spline</b> <i>0.0 - 1.0</i> | Nivel de distorsión uniforme en todas las splines. |
| <b>Aleatorio de Distorsión de spline</b> <i>0.0 - 1.0</i> | Aleatoriza el nivel de distorsión de cada spline individualmente. |
| <b>Frecuencia de Distorsión spline</b> <i>0.0 - 1.0</i> | Define la frecuencia de la distorsión y controla la escala de los detalles de la distorsión. |
| <b>Ancho de spline</b> <i>0.0 - 2.0</i> | Establece la anchura de todas las splines de manera uniforme. |
| <b>Aleatorio de ancho de spline</b> <i>0.0 - 1.0</i> | Aleatoriza la anchura de spline de cada spline individualmente. |
| <b>Aleatorio de posición de spline</b> <i>0.0 - 1.0</i> | Aleatoriza la posición de cada spline individualmente. Cuanto menor sea este valor, más splines se agruparán en el centro del lienzo. Se puede utilizar para crear puntos de arañazos. |
| <b>Establecer ancho de spline en px</b> <i>Falso/Verdadero</i> | Determina las unidades utilizadas para los ajustes de anchura de spline. |
| <b>Luminancia aleatoria (solo versión de escala de grises)</b> <i>0.0 - 1.0</i> | Aleatoriza la luminancia de cada spline individualmente. |
| <b>Intensidad normal (solo versión normal)</b> <i>0.0 - 1.0</i> | Define globalmente la intensidad del efecto Normal para cada spline. |
| <b>Aleatorio de intensidad normal (solo versión normal)</b> <i>0.0 - 1.0</i> | Aleatoriza la intensidad normal de cada spline individualmente. |
| <b>Formato normal (solo versión normal)</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Modo de transición</b> <i>Ninguno, Inicio, Fin, Inicio + Fin</i> | Establece si las splines se desvanecen y en qué dirección. |
| <b>Longitud de transición</b> <i>0.0 - 1.0</i> | Define la longitud del efecto de transición, si está activado anteriormente. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-generator-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-generator-03.png" />
        </td>
    </tr>
</table>
