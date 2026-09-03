---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación 2D de trazado para transformar trazados con operaciones de traslación, rotación y escala.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación 2D de trazado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 2%

---


# Transformación 2D de trazado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](path-2d-transform.resources/path-2d-transform-01.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de trazado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Transforma trazados con un gizmo.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Rutas</b> <i>Color</i> | Una lista de los segmentos codificados de las rutas. Conecte esta entrada al resultado de [Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a otro nodo de procesamiento de rutas. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Rutas</b> <i>Color</i> | Los trazados transformados. Puedes usar [rutas de vista previa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para hacerte una idea de lo que representa el resultado, usar otro nodo de procesamiento de rutas o escribirlo en [rutas de acceso a spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para procesarlo aún más como splines. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Transformar matriz</b> <i>Float4</i> | Matriz de transformación aplicada a las splines. Hay tres modos de edición de los parámetros matriciales disponibles:<br>*- Gizmo de transformación:* retocar los controladores del gizmo que se muestra en el [vista 2D](../../../../../../interface/2d-view/2d-view.md) cuando se selecciona el nodo Transformar spline 2D;<br>*- Rotación/Estirar:* Controle individualmente la rotación y el estiro de las splines. Tenga en cuenta que los valores siempre se aplican en relación con la transformación actual. Por ejemplo, si aplica una anchura del 50 % dos veces, se obtiene una anchura del 25 %;<br>*- Valores de matriz:* Haga clic en el botón <b>Editar valores de matriz</b> para introducir directamente los valores numéricos sin formato de la matriz. |
| <b>Desplazamiento</b> <i>Float2</i> | Aplica un desplazamiento de posición a las splines en X (horizontal) e Y (vertical). |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/path-2d-transform-02.jpg" alt="PathsPolygon_Variant1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/path-2d-transform-03.jpg" alt="Paths2DTransform-Variant1">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/path-2d-transform-02.jpg" alt="PathsPolygon_Variant1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/path-2d-transform-04.jpg" alt="Paths2DTransform-Variant2">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
