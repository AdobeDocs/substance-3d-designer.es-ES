---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-render.html"
breadcrumb-title: ''
description: Utilice el nodo Procesamiento de histograma para visualizar los datos del histograma como una textura para el análisis y la depuración.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderizado de histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---


# Renderizado de histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de escala de grises Kuwahara anisotrópico](../../../../../../assets/histogram_render.png "Icono de escala de grises Kuwahara anisotrópico"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja el histograma de una imagen en escala de grises.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Conectores de salida

</td>
<td style="border: 0;" valign="top">

### Parámetros

</td>
</tr>
</table>

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises* PRINCIPAL | Imagen para la que se debe dibujar el histograma. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises* | Visualización del histograma calculada a partir de la imagen de entrada. |

## Parámetros

|  |  |
| --- | --- |
| <b>Resolución del histograma</b> *Entero* | Anchura del histograma. Un valor más alto permite una distribución de valor más fina.   Las resoluciones disponibles son, en píxeles:  256, 512, 1024, 2048, 4096 |
| <b>Escala automática</b> *Booleano* | Si es &quot;True&quot;, reasigna el histograma para utilizar el height completo de la imagen.   Cuando es &#39;False&#39;, cada columna utiliza tantos píxeles en height como se reproduzca un valor en la imagen de entrada. |
| <b>Escala</b> *Flotador* | Escala el histograma verticalmente, donde un valor de 1 es el height completo del histograma. |
| <b>Muestreo</b> *Entero* | Método de filtrado de la imagen del histograma, que afecta al resultado cuando la resolución del histograma y la resolución de procesamiento no coinciden:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Bilineal:</b> aplica filtros bilineales al histograma, lo que produce puntos interpolados</li> <li data-preserve-html="true"><b>Más cercano:</b> muestra el píxel más cercano sin ningún filtro, lo que da como resultado pasos planos</li> </ul> |
| <b>Voltear eje Y</b> *Booleano* | Cuando es &quot;True&quot;, refleja el histograma verticalmente. |

## Ejemplos

Renderizado de histograma ![: Ejemplo 1](../../../../../../assets/histogram_render_example_1.png "Renderizado de histograma: Ejemplo 1"){zoomable="yes"}

Renderizado de histograma ![: Ejemplo 2](../../../../../../assets/histogram_render_example_2.png "Renderizado de histograma: Ejemplo 2"){zoomable="yes"}
