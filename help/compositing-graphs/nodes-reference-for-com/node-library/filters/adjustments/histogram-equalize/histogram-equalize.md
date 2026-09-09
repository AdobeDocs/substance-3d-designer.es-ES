---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: Utilice el nodo Ecualización de histograma para redistribuir las intensidades de píxeles para mejorar el contraste y el brillo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ecualización del histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# Ecualización del histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ecualización del histograma: icon](histogram-equalize.resources/histogram_equalize.png "Ecualización de histograma: icon"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Ecualiza el histograma de una imagen de escala de grises, ajustando eficazmente los valores de escala de grises con el fin de lograr una distribución igual.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Escala de grises</i> PRINCIPAL | Imagen para la que se debe igualar el histograma. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | Imagen resultante con ecualización de histograma aplicada. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Resolución del histograma</b> *Entero* | Anchura del histograma. Un valor más alto permite una distribución de valor más fina.   Las resoluciones disponibles son, en píxeles:  256, 512, 1024, 2048, 4096 |
| <b>Suavizado de histograma</b> *Flotador* | El histograma se puede suavizar redistribuyendo los valores de escala de grises de la imagen para igualar la *diferencia* entre cada valor.   Este parámetro ajusta la intensidad de ese suavizado. |

## Ejemplos

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

![Ecualización del histograma: Ejemplo 1](histogram-equalize.resources/histogram_equalize_example_3.png "Ecualización de histograma: Ejemplo 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_before.jpg" alt="histogram_equalize_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_after.jpg" alt="histogram_equalize_example_2_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

![Ecualización del histograma: Ejemplo 2](histogram-equalize.resources/histogram_equalize_example_5.png "Ecualización de histograma: Ejemplo 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_before.jpg" alt="histogram_equalize_example_4_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_after.jpg" alt="histogram_equalize_example_4_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

![Ecualización del histograma: Ejemplo 3](histogram-equalize.resources/histogram_equalize_example_6.png "Ecualización de histograma: Ejemplo 3"){zoomable="yes"}
