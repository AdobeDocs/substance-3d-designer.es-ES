---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: Utilice el nodo Descombinar normal para separar los datos del mapa normal combinado en componentes X, Y y Z individuales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal Descombinar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Normal Descombinar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Descombinar normal](normal-uncombine.resources/NormalUncombine.png "Icono Descombinar normal"){width="200px"}

<b>En:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Elimina de un mapa normal los detalles de la superficie descritos por un mapa de height.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Normal combinada</b> <i>Color</i> PRINCIPAL | Mapa normal del que se deben quitar los detalles. |
| <b>Height</b> <i>Escala de grises</i> | Mapa de height que representa los detalles de la superficie que deben eliminarse del mapa normal combinado. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Normal no combinada</b> <i>Color</i> | Mapa normal en el que se eliminaron los detalles de la superficie descritos por el mapa del height de entrada. |
| <b>Intensidad estimada</b> <i>Flotador</i> | Una estimación de la intensidad que debe establecerse en un nodo [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) conectado al mapa de height de entrada, para que coincida con la intensidad del mapa de entrada normal. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Formato normal</b> *Entero* | Formato del mapa normal de entrada. Invierte el canal verde de forma efectiva.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> El eje Y señala hacia arriba</li> <li data-preserve-html="true"><b>OpenGL:</b> El eje Y señala hacia abajo</li> </ul> |

## Ejemplos

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

![Descombinación normal: Ejemplo 2](normal-uncombine.resources/normal_uncombine_example_4.png "Descombinación normal: Ejemplo 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

![Descombinación normal: Ejemplo 4](normal-uncombine.resources/normal_uncombine_example_6.png "Descombinación normal: Ejemplo 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

![Descombinación normal: Ejemplo 6](normal-uncombine.resources/normal_uncombine_example_5.png "Descombinación normal: Ejemplo 6"){zoomable="yes"}
