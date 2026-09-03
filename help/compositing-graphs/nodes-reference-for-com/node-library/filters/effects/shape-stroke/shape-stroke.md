---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: Utilice el nodo Trazo de forma para agregar contornos de trazo a las formas para crear bordes y efectos de borde.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trazo de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# Trazo de forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-stroke.resources/shape-stroke-01.png){width="128px"}

![](shape-stroke.resources/shape-stroke-02.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Añade un trazo o contorno alrededor de una máscara en blanco y negro (para la versión de escala de grises) o una forma con un canal alfa (para la versión de color), como puede estar familiarizado con otras aplicaciones de edición de imágenes 2D. Se puede ver como una versión más completa de [Edge Detect](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md).

Muy útil para una variedad de efectos de edición de imágenes.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ancho</b> <i>-1.0 - 1.0</i> | Anchura del efecto de trazo. |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Opacidad global del efecto. |
| <b>(contorno) Color</b> <i>(Valor de color)</i> | Color utilizado para el efecto de contorno. |
| <b>Color de máscara</b> <i>(valor de color) (solo versión de escala de grises)</i> | Color sólido que se va a utilizar para la salida asignada de transparencia. |
| <b>La Entrada Está Premultiplicada</b> <i>Falso/Verdadero (solo versión de color)</i> | Si la entrada debe asumirse como premultiplicada. |
| <b>Salida de premultiplicación</b> <i>Falso/Verdadero</i> | Si la salida debe premultiplicarse. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-stroke.resources/shape-stroke-03.png" />
        </td>
    </tr>
</table>
