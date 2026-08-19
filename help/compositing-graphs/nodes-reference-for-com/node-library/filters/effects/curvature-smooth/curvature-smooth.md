---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: Utilice el nodo Suavizado de curvatura para generar mapas de curvatura suaves a partir de mapas de height para la extracción de detalles de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura suave
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# Curvatura suave

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo suave de curvatura](../../../../../../assets/CurvatureSmooth.png "Icono de nodo suave de curvatura"){width="200px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Calcula la curvatura de una superficie descrita por un mapa normal.

Un mapa de curvatura representa las áreas cóncavas y convexas de una superficie.\
Las áreas planas son 50% grises. Las áreas convexas son más brillantes, mientras que las áreas cóncavas son más oscuras.

</td>
</tr>
</table>

Las áreas cóncavas y convexas también se dividen en sus propias salidas, para facilitar la selección o enmascaramiento de áreas en función de esas características.

>[!TIP]
>
> Comprueba [Curvature](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) para obtener una versión más nítida, o [Curvature Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) si necesitas más opciones.

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
| <b>Normal</b> *Color* <b>PRINCIPAL</b> | Mapa normal que describe la superficie cuya curvatura debe calcularse. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Curvatura</b> *Escala de grises* | Mapa de curvatura calculado a partir del mapa normal de entrada.   Las áreas planas son 50% grises. Las áreas convexas son más brillantes, mientras que las áreas cóncavas son más oscuras. |
| <b>Convexidad</b> *Escala de grises* | Mapa de convexidad calculado a partir del mapa normal de entrada.   Cuanto más convexa es una zona, más brillante es en el mapa.  Las áreas planas o cóncavas son negras. |
| <b>Concavidad</b> *Escala de grises* | Mapa de concavidad calculado a partir del mapa normal de entrada.   Cuanto más cóncava es una zona, más brillante es en el mapa.  Las áreas planas o convexas son negras. |

## Parámetros

|  |  |
| --- | --- |
| <b>Formato normal</b> *Entero* | Formato del mapa normal de entrada. Invierte el canal verde de forma efectiva.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> El eje Y señala hacia arriba</li> <li data-preserve-html="true"><b style="">OpenGL:</b> El eje Y señala hacia abajo</li> </ul> |

## Ejemplos

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_before.jpg" alt="curvature_smooth_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_after.jpg" alt="curvature_smooth_example_1_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Curvatura suave: Ejemplo 2](../../../../../../assets/curvature_smooth_example_2.jpg "Suavizado de curvatura: Ejemplo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Curvatura suave: Ejemplo 3](../../../../../../assets/curvature_smooth_example_3.jpg "Suavizado de curvatura: Ejemplo 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_before.jpg" alt="curvature_smooth_example_4_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_after.jpg" alt="curvature_smooth_example_4_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Curvatura suave: Ejemplo 4](../../../../../../assets/curvature_smooth_example_5.jpg "Suavizado de curvatura: Ejemplo 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Curvatura suave: Ejemplo 5](../../../../../../assets/curvature_smooth_example_6.jpg "Suavizado de curvatura: Ejemplo 5"){zoomable="yes"}

</td>
</tr>
</table>
