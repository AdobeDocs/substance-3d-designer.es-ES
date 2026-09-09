---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Utilice el nodo Sector de Simetría para dividir texturas a lo largo de los ejes de simetría y crear patrones y efectos reflejados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sector de simetría
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# Sector de simetría

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry-slice.resources/mirror-2.png){width="128px"}

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de operación de Simetría/duplicación complejo. Permite una gran variedad de operaciones geométricas con control total, pero requiere cierta experimentación.

En comparación con [Mirror](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) y [Simetría](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md), este nodo tiene muchas más opciones.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de Simetría</b> <i>0 - 6</i> | Seleccione geometría de simetría/línea simétrica. Las opciones son Horizontal, Vertical, Diagonal izquierda-derecha, Diagonal derecha-izquierda, Invertir vertical, Esquina y Esquina diagonal. |
| <b>Modo de transferencia</b> <i>0 - 6</i> | modo de Fusión. Las opciones son: |
| <b>Fusionar</b> <i>0.0 - 1.0</i> | Fusión la imagen original en el resultado. |
| <b>Voltear lado</b> <i>Falso/Verdadero</i> | Voltea el origen, lo que significa que se invierte el lado de origen de la operación. La simetría de izquierda a derecha, por ejemplo, se convierte en de derecha a izquierda. |
| <b>Voltear lado2</b> <i>Falso/Verdadero</i> | Solo se utiliza cuando el modo de Simetría es 5 o 6. Voltear origen de esquina. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry-slice.resources/symslice.png" />
        </td>
    </tr>
</table>
