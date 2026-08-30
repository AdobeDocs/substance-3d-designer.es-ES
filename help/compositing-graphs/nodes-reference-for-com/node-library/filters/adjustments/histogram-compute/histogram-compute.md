---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: Utilice el nodo Histograma computado para calcular datos de histograma de texturas para su análisis y procesamiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cálculo del histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---


# Cálculo del histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cálculo de histograma: icon](histogram-compute.resources/histogram_compute.png "Histograma: icon"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Calcula el histograma de una imagen en escala de grises.

El histograma se codifica como una fila de píxeles en una imagen, donde cada valor de píxel es la *población* del valor de color que coincide con la posición de píxel en el eje X.\
Por ejemplo, un valor de píxel de 75 a (0,25, 0) significa que hay 75 píxeles que tienen el valor de color de 0,25 en la imagen.

</td>
</tr>
</table>

El nodo también genera la *función de distribución acumulativa* (CDF) calculada para la imagen.

Las herramientas personalizadas se pueden crear utilizando los datos calculados por el nodo, como las máscaras personalizadas, como se muestra a continuación en la sección &#39;Ejemplos&#39;.

>[!IMPORTANT]
>
> Todos los valores fuera del rango [0,1] se sujetan, por lo que el histograma puede no ser preciso para HDR imágenes.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Escala de grises</i> PRINCIPAL | Imagen para la que se debe calcular el histograma. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Histograma</b> <i>Escala de grises</i> | El histograma calculado para la imagen de entrada, codificado como una fila de píxeles donde cada valor de píxel es la *población* del valor de color que coincide con la posición de píxel en el eje X.   Por ejemplo, un valor de píxel de 75 a (0,25, 0) significa que hay 75 píxeles que tienen el valor de color de 0,25 en la imagen. |
| <b>CDF</b> <i>Escala de grises</i> | Resultado de la *función de distribución acumulativa* (CDF) calculada para la imagen, codificada en una fila de píxeles en la que cada píxel es la suma de todos los valores de píxeles a su izquierda.   Esa suma se *normaliza* respecto al número total de píxeles de la imagen. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Resolución del histograma</b> *Entero* | Anchura del histograma. Un valor más alto permite una distribución de valor más fina.   Las resoluciones disponibles son, en píxeles:  256, 512, 1024, 2048, 4096 |

## Ejemplos

![Cálculo de histograma: Ejemplo 1](histogram-compute.resources/histogram_compute_example_1.jpg "Cálculo de histograma: Ejemplo 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>
