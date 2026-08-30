---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
breadcrumb-title: ''
description: Utilice el nodo Selección de trazados para seleccionar y filtrar trazados específicos de una lista de trazados en función de criterios.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selección de trazados
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# Selección de trazados

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](paths-select.resources/paths-select-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de trazado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aísle un trazado entre varios contenidos en Trazados.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Etiqueta</b> <i>Tipo</i> | Una lista de los segmentos codificados de las rutas. Conecte esta entrada al resultado de [Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a otro nodo de procesamiento de rutas. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Rutas</b> <i>Color</i> | Los trazados se introducen con un solo trazado. Puedes usar [rutas de vista previa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para hacerte una idea de lo que representa el resultado, usar otro nodo de procesamiento de rutas o escribirlo en [rutas de acceso a spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para procesarlo aún más como splines. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de selección</b> <i>Entero</i> | El método utilizado para seleccionar las rutas:<br>*- Por id.:* Selecciona la ruta de la lista cuyo índice coincide con el especificado en <b>Id. de ruta</b>;<br>*- Por longitud:* Selecciona las rutas cuya longitud es superior o inferior al umbral especificado en <b>Longitud de destino</b>. |
| <b>Id. de ruta</b> <i>Entero</i> (disponible cuando el <b>Modo de selección</b> está establecido en *Por id.*) | El índice de la ruta de acceso seleccionada.<br>Un valor mayor que el número de rutas de acceso de <b>Rutas *genera*</b> un resultado en blanco. |
| <b>Longitud mayor o menor?</b> <i>Booleano</i> (disponible cuando el <b>Modo de selección</b> está establecido en *Por longitud*) | Controla si la selección debe incluir una longitud mayor o menor que la <b>Longitud de destino</b>. |
| <b>Longitud de destino</b> <i>Flotante</i> (disponible cuando el <b>Modo de selección</b> está establecido en *Por longitud*) | Umbral de longitud utilizado para seleccionar splines. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="paths-select.resources/PathsSelect-Variant2.jpg" alt="PathsSelect-Variant2">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
