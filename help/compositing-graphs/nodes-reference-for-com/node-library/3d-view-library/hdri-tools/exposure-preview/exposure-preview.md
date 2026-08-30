---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: Utilice el nodo Previsualización de exposición para previsualizar los ajustes de exposición en entornos HDRI antes del procesamiento final.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Previsualización de exposición
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# Previsualización de exposición

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](exposure-preview.resources/hdr-exposure-preview.png){width="200px"}

<b>En:</b> Vista 3D > Herramientas HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo auxiliar para previsualizar los pasos de exposición. El usuario establece un valor mínimo y máximo, el nodo genera una imagen mucho más grande con un número de versiones expuestas de la entrada original. Las diferentes versiones siempre se apilan horizontalmente, la cantidad depende de la resolución del nodo o gráfico.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Exposición Máxima (EV)</b> <i>-8.0 - 8.0</i> | Exposición máxima de la imagen superior más brillante. |
| <b>Exposición Mínima (EV)</b> <i>-8.0 - 8.0</i> | Exposición mínima de la imagen inferior más oscura. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="exposure-preview.resources/exp-preview-ex.png" />
        </td>
    </tr>
</table>
