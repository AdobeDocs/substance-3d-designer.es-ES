---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: Utilice el nodo Lighting Cancel High Frequencies para quitar los detalles de iluminación de alta frecuencia de las texturas para el análisis de materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Iluminación Cancelar altas frecuencias
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---


# Iluminación Cancelar altas frecuencias

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/lighting-cancel-high-frequencies.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Similar a [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), pero más adecuado para imágenes a todo color (no desatura tanto el resultado), este nodo intenta cancelar los detalles de iluminación pequeños y alta frecuencia.

Consulte también [Cancelación de iluminación con frecuencias bajas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md) y la opción más avanzada recomendada: [Paso alto de luminancia](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> <i>0.0 - 1.0</i> | Intensidad del efecto de cancelación de iluminación. |
| <b>Radio</b> <i>0.0 - 10.0</i> | Radio o tamaño de los detalles de iluminación que se van a cancelar. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/lighting-cancel-highfrequencies-example.png" />
        </td>
    </tr>
</table>
