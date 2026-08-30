---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Utilice el nodo 3D linear gradient para crear degradados lineales basados en la posición de mundo 3D para efectos espaciales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---


# 3D linear gradient

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-linear-gradient.resources/3d-linear-gradient.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Crea un degradado volumétrico basado en el mapa de posición de entrada. Genera de forma efectiva una transición de negro a blanco entre 2 puntos en el espacio 3D. Se ha diseñado para su uso únicamente con el motor de GPU.

Consulte también [Máscara de volumen 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) para ver un efecto similar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de posición de puntos</b> <i>Posiciones UV, Posiciones Espaciales Mundiales</i> | Elija si los puntos de degradado funcionan en el espacio UV (funciona mejor cuando se establecen en Vista 2D) o en coordenadas 3D, si desea introducir manualmente una posición exacta. |
| <b>Punto 1</b> | Punto inicial del degradado. Pueden ser coordenadas 2D o 3D basadas en el modo de posición. |
| <b>Punto 2</b> | Punto final del degradado. Pueden ser coordenadas 2D o 3D basadas en el modo de posición. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-linear-gradient.resources/3d-gradient.gif" />
        </td>
    </tr>
</table>
