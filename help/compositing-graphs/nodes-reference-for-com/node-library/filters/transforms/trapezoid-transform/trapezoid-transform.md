---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/trapezoid-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformar trapezoide para aplicar la distorsión trapezoidal a las texturas para crear efectos de corrección de Perspectiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Trapezoid Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación trapezoide
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# Transformación trapezoide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/trapeze-transform.png){width="128px"}

![](../../../../../../assets/trapeze-transform-grayscale.png){width="128px"}

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de transforme especial que modifica la entrada de una forma de deformación de Perspectiva/trapezoide. Tiene control para estirar superior e inferior. Los valores pueden ir más allá de los límites para conseguir efectos más fuertes.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Estire superior</b> <i>0.0 - 1.0</i> | Establezca la cantidad de estirar o aplastar en la parte superior. |
| <b>Estirar abajo</b> <i>0.0 - 1.0</i> | Establezca la cantidad de estirar o aplastar en el fondo. |
| <b>Color de fondo</b> <i>(valor de escala de grises/color)</i> | Defina el color de fondo sólido en caso de que el mosaico esté desactivado. |
| <b>Muestreo</b> <i>Bilineal, Más Cercana</i> | Definir la calidad de muestreo. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/trapeze-example.gif" />
        </td>
    </tr>
</table>
