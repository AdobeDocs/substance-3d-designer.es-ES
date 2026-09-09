---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Utilice el nodo Resplandor de forma para añadir efectos de resplandor a formas y texturas para crear efectos visuales luminosos y atmosféricos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Resplandor de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---


# Resplandor de forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-glow.resources/shape-glow-grayscale.png){width="128px"}

![](shape-glow.resources/shape-glow.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Crea un resplandor suave alrededor de una máscara de entrada (para la versión de escala de grises) o una forma con un canal alfa (para la versión de color). En comparación con [Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md), esto funciona de una forma más similar a otro software de edición de imágenes 2D, ya que es un efecto más completo con más controles.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo</b> <i>Suave, Preciso</i> | Cambia entre dos modos de precisión. |
| <b>Ancho</b> <i>-1.0 - 1.0</i> | Controla hasta dónde llega el brillo. |
| <b>Difusión</b> <i>0.0 - 1.0</i> | Corte / umbral para el efecto de desenfoque, hace que el resplandor parezca sólido cerca de la forma. |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Opacidad de fusión para el efecto resplandor. |
| <b>(Sombra) Color</b> <i>(Valor de color)</i> | Matiz de color que se aplicará al resplandor. |
| <b>Color de máscara</b> <i>(valor de color) (solo versión de escala de grises)</i> | Color sólido que se va a utilizar para la salida asignada de transparencia. |
| <b>La Entrada Está Premultiplicada</b> <i>Falso/Verdadero (solo versión de color)</i> | Si la entrada debe asumirse como premultiplicada. |
| <b>Salida de premultiplicación</b> <i>Falso/Verdadero</i> | Si la salida debe premultiplicarse. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-glow.resources/shapeglow-ex.png" />
        </td>
    </tr>
</table>
