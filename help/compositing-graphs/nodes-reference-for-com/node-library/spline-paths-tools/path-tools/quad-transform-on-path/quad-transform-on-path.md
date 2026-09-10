---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación cuádruple en trazado para aplicar transformaciones cuadráticas a elementos de curvas de trazado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación cuádruple en trazado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 29dd2e6adc826f63ee26defc0032b0e52d4e30fb
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Transformación cuádruple en trazado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](quad-transform-on-path.resources/quad-transform-on-paths-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de trazado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Deforme trazados con 4 manejadores.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Rutas</b> <i>Color</i> | Una lista de los segmentos codificados de las rutas. Conecte esta entrada al resultado de un nodo de procesamiento de [Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a otro nodo de procesamiento de *Path*. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Rutas</b> <i>Color</i> | Los trazados transformados. Puedes usar [rutas de vista previa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para hacerte una idea de lo que representa el resultado, usar otro nodo de procesamiento de rutas o escribirlo en [rutas de acceso a spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para procesarlo aún más como splines. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>p00</b> <i>Float2</i> | Posición del control superior izquierdo. |
| <b>p01</b> <i>Float2</i> | Posición del control superior derecho. |
| <b>p02</b> <i>Float2</i> | Posición del control inferior izquierdo. |
| <b>p03</b> <i>Float2</i> | Posición del control inferior derecho. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/QuadTransformOnPaths-Variant1-After.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/QuadTransformOnPaths-Variant2-After.jpg" alt="QuadTransformOnPaths-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](quad-transform-on-path.resources/QuadTransformOnPaths-Demo2.gif "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](quad-transform-on-path.resources/QuadTransformOnPaths-Demo1.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
