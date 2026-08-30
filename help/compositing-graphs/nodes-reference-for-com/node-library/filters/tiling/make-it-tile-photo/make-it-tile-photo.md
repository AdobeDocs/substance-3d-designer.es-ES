---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Utilice el nodo Hacer fotografía en mosaico para convertir fotografías en texturas de mosaico perfectas para la creación de materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hacer que la fotografía en mosaico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---


# Hacer que la fotografía en mosaico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-photo.resources/make-it-tile-photo.png)

![](make-it-tile-photo.resources/make-it-tile-photo-grayscale.png)

<b>En:</b> Filtros > Mosaico

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo proporciona la funcionalidad de reparación de bordes para cualquier imagen que no pueda estar en mosaico debido a bordes no continuos. No afecta a nada que no sean los bordes de la imagen de entrada. Si desea ajustar la escala o el mosaico de diferentes maneras, consulte [Parche del mosaico Make It Tile](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Deformación de máscara H</b> <i>-100.0 - 100.0</i> | Introduce la deformación en el eje horizontal para evitar transiciones no definidas. |
| <b>Deformación de máscara V</b> <i>-100.0 - 100.0</i> | Introduce la deformación en el eje vertical, para evitar transiciones no definidas. |
| <b>Tamaño de máscara H</b> <i>0.0 - 1.0</i> | Establece hasta dónde llega horizontalmente el borde de transición. |
| <b>Tamaño de máscara V</b> <i>0.0 - 1.0</i> | Establece hasta dónde llega verticalmente el borde de transición. |
| <b>Precisión de máscara H</b> <i>0.0 - 1.0</i> | Establece el grado de suavidad horizontal de la transición. |
| <b>Precisión de máscara V</b> <i>0.0 - 1.0</i> | Define la suavidad vertical de la transición. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-photo.resources/mit-photo-ex.png" />
        </td>
    </tr>
</table>
