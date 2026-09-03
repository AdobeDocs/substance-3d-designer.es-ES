---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: Utilice el nodo Color del filtro mediano para reducir el ruido y conservar los bordes en las texturas de color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color del filtro mediano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Color del filtro mediano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Color del filtro mediano: icon](median-filter-color.resources/median-filter-color-01.png "Color del filtro mediano: icon")

<b>En:</b> Filtros > Desenfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este filtro suaviza el ruido de una imagen al tiempo que conserva los bordes.

Para cada píxel, el nodo calcula un valor de color según el valor medio de los píxeles vecinos.

</td>
</tr>
</table>

>[!NOTE]
>
> Consulte también [Escala de grises del filtro mediano](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Color</i> | Imagen de color a la que se debe aplicar el filtro. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Color</i> | La imagen de color calculada aplicando el filtro a la imagen de color de entrada. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Tamaño del núcleo</b> *Entero* | Un núcleo es un grupo específico de valores utilizados en los cálculos de un filtro. En este contexto, son los valores de los píxeles vecinos.<br><br>Por cada píxel, el filtro toma todos los vecinos alrededor de ese píxel en un núcleo cuadrado y calcula el valor medio de todos los vecinos.<br><br>Este parámetro controla el tamaño de ese núcleo cuadrado, en píxeles. Un núcleo más grande produce un efecto de suavizado más fuerte y de mayor alcance a costa de algunos detalles.<br><br>*- 3x3:* un núcleo de 3 píxeles de ancho y 3 píxeles de alto, con un total de 8 píxeles vecinos.<br>*- 5x5:* un núcleo de 5 píxeles de ancho y 5 píxeles de alto, con un total de 24 píxeles vecinos. |
| <b>Tipo de filtro</b> *Entero* | El cálculo aplicado a los vecinos muestreados en el núcleo.<br><br>*- Mediana:* Use el valor de mediana de todos los vecinos directamente.<br>*- MLMAD:* Significa &#39;Mediana de la desviación absoluta de la mediana mínima&#39;. La desviación explica la diferencia entre un valor y la mediana. En lugar de utilizar el valor de la mediana directamente, que puede ser sesgado por un píxel anómalo con una desviación alta, el método MLMAD utiliza la mediana de todas las desviaciones. Este método produce un efecto de suavizado más fuerte que puede aplanar las áreas según el tamaño del núcleo. |
| <b>Afectar alfa</b> *Booleano* | Controla si el filtro se debe aplicar al canal alfa de la imagen. Cuando *True*, el canal alfa no cambia. |

## Ejemplos

<table>
  <tr>
    <td>
      <img src="median-filter-color.resources/median-filter-color-02.png" alt="MedianFilter_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="median-filter-color.resources/median-filter-color-03.png" alt="MedianFilter_Variant2B">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-color.resources/median-filter-color-04.png" alt="MedianFilter_Variant3A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="median-filter-color.resources/median-filter-color-05.png" alt="MedianFilter_Variant3B">
      <br><i>Después De</i>
    </td>
  </tr>
</table>
