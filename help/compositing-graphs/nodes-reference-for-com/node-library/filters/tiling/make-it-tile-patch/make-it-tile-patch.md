---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Utilice el nodo Hacer parche de mosaico para aplicar parches y crear texturas de mosaico perfectas a partir de imágenes de entrada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hacer que parche de azulejo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# Hacer que parche de azulejo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch.png)

![](make-it-tile-patch.resources/make-it-tile-patch-grayscale.png)

<b>En:</b> Filtros > Mosaico

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo es un mosaico semialeatorio basado en la cuadrícula. Toma un parche de entrada y lo sella, intentando convertirlo en una imagen de mosaico sin demasiadas repeticiones, según su configuración.

Útil para cuando se dispone de un pequeño parche de textura y se desea crear una textura de mosaico a mayor escala a partir de ella.

Ten en cuenta que esto es diferente de la [Foto de Hacer Azulejo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), que principalmente corrige los bordes.

Para hacer esto con todo un material, consulte [Mosaico automático inteligente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Tamaño de máscara</b> <i>0.0 - 1.0</i> | Tamaño de la máscara redonda utilizada para estampar el parche. |
| <b>Precisión de máscara</b> <i>0.0 - 1.0</i> | Precisión de difuminado/smoothness de la máscara. |
| <b>Deformación de máscara</b> <i>-100.0 - 100.0</i> | Introduce la deformación en los bordes de la máscara. Es útil para evitar transiciones suaves e indefinidas entre parches. |
| <b>Ancho del tamaño del motivo</b> <i>0.0 - 1000.0</i> | Cambia el ancho del parche de forma no uniforme. |
| <b>height de tamaño de motivo</b> <i>0.0 - 1000.0</i> | Cambia el height del parche de forma no uniforme. |
| <b>Desorden</b> <i>0.0 - 1.0</i> | Introduce la aleatoriedad de la traducción, cambiando ligeramente los parches. |
| <b>Variación de tamaño</b> <i>0.0 - 100.0</i> | Introduce la variación de tamaño de la máscara. |
| <b>Octava</b> <i>0 - 6</i> | Éste es el control principal que determina el tamaño global. |
| <b>Rotación</b> <i>-360.0 - 360.0</i> | Gira previamente el parche. |
| <b>Variación de rotación</b> <i>0.0 - 360.0</i> | Introduce una rotación aleatoria para cada sello de parche. |
| <b>Color de fondo</b> <i>(Valor de color)</i> | Define el color de fondo para las áreas en las que no aparece ningún parche. |
| <b>Variación de color</b> <i>0.0 - 1.0 (solo versión de color)</i> | Introduce la variación de color por parche. |
| <b>Variación de luminosidad</b> <i>(solo versión en escala de grises)</i> | Introduce la variación de luminosidad por parche. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/patch-ex.gif" />
        </td>
    </tr>
</table>
