---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Utilice el nodo Selector de material para seleccionar materiales basados en datos de malla para crear efectos de textura de varios materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selector de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# Selector de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

<b>En:</b> Generadores basados en malla > Utilidades

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Convierte un mapa de ID a todo color en una máscara binaria, en blanco y negro. Permite mezclar y combinar diferentes colores en una máscara.

Esto es útil si no desea usar [Fusión de varios materiales](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) y prefiere usar la máscara manualmente o, alternativamente, si desea usar manualmente esas mismas máscaras en otras ubicaciones.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Materiales</b> <i>1 - 16</i> | Define el número de materiales para los que está activada la combinación. |
| <b>Habilitar material #1-16</b> <i>Falso/Verdadero</i> | Cambia la fusión y combinación de colores en la máscara de salida final. Se puede activar para todos los colores que desee combinar. |
| <b>Material #1-16</b> <i>(Valor de color)</i> | Selector de color para el color de los materiales que se convertirá a blanco y negro. |
| <b>Parámetros del selector de color</b> | Modifica la fusión y conversión del color a blanco y negro. |
| <b>Rugosidad</b> <i>0.01 - 1.0</i> | Cuánto mezclar con los colores vecinos. |
| <b>Relleno</b> <i>0.0 - 1.0</i> | Nitidez de la transición, como Contraste. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/matselector-ex.png" />
        </td>
    </tr>
</table>
