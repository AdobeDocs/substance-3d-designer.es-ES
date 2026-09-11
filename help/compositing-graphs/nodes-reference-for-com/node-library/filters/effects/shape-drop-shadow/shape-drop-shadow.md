---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Utilice el nodo Sombra paralela de formas para agregar efectos de sombra paralela a formas para crear profundidad y dimensión en texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombra paralela de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Sombra paralela de forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-drop-shadow.resources/shape-dropshadow-grayscale.png){width="128px"}

![](shape-drop-shadow.resources/shape-dropshadow.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza el conocido efecto &quot;Sombra paralela&quot; de otro software de procesamiento de imágenes 2D, sobre una máscara de entrada en blanco y negro (para la versión de escala de grises) o una imagen con transparencia (para la versión de color).

Difiere del efecto [Sombras](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) en que devuelve imágenes con transparencia total aplicada, lo que hace que el efecto sea más completo y similar al que esperarías de otro software.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ángulo</b> <i>0.0 - 1.0</i> | Ángulo de incidencia de la luz (falsa). |
| <b>Distancia</b> <i>-0.5 - 0.5</i> | Distancia a la que se desplaza la sombra hacia abajo o se aleja de la forma. |
| <b>Tamaño</b> <i>0.0 - 1.0</i> | Controla el desenfoque/difuminado de la sombra. |
| <b>Difusión</b> <i>0.0 - 1.0</i> | Límite/umbral para el efecto de desenfoque, hace que la sombra se extienda aún más. |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Opacidad de fusión para el efecto de sombra. |
| <b>(Sombra) Color</b> <i>(Valor de color)</i> | Matiz de color que se aplicará a la sombra. |
| <b>Color de máscara</b> <i>(valor de color) (solo versión de escala de grises)</i> | Color sólido que se va a utilizar para la salida asignada de transparencia. |
| <b>La Entrada Está Premultiplicada</b> <i>Falso/Verdadero (solo versión de color)</i> | Si la entrada debe asumirse como premultiplicada. |
| <b>Salida de premultiplicación</b> <i>Falso/Verdadero</i> | Si la salida debe premultiplicarse. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-drop-shadow.resources/dropshadowex.png" />
        </td>
    </tr>
</table>
