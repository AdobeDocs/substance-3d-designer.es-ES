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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Previsualización de exposición

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hdr-exposure-preview.png){width="200px"}

## Previsualización de exposición

**En:** *Herramientas HDRI/vistas 3D*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo auxiliar para previsualizar los pasos de exposición. El usuario establece un valor mínimo y máximo, el nodo genera una imagen mucho más grande con un número de versiones expuestas de la entrada original. Las diferentes versiones siempre se apilan horizontalmente, la cantidad depende de la resolución del nodo o gráfico.

## Parámetros

* **Exposición máxima (VE)**: *-8.0 - 8.0*\
  Exposición máxima de la imagen superior más brillante.
* **Exposición Mínima (EV)**: *-8.0 - 8.0* Exposición mínima de la imagen inferior más oscura.

## Imágenes de ejemplo

![](../../../../../../assets/exp-preview-ex.png)

</td>
</tr>
</table>
