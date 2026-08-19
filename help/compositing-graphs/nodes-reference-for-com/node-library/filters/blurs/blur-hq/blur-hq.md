---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: Utilice el nodo HQ de desenfoque para aplicar efectos de desenfoque de alta calidad a las texturas para crear resultados de desenfoque suaves y de aspecto profesional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desenfocar alta calidad
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---


# Desenfocar alta calidad

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/blur-hq-1.png){width="128px"}

![](../../../../../../assets/blur-hq-grayscale.png){width="128px"}

## Desenfocar HQ (escala de grises)

**En:** *Filtros/Desenfoques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza un desenfoque gaussiano de alta calidad en el resultado. Mucho mejor que [el desenfoque estándar de la caja atómica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [.](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utilice &quot;Desenfocar HQ&quot; para las entradas de color o &quot;Desenfocar HQ en escala de grises&quot; para las entradas de escala de grises.

## Parámetros

* **Intensidad**: *0.0 - 16.0*\
  Intensidad (radio) del desenfoque. Cuanto más alto sea este valor, mayor será el desenfoque.
* **Calidad**: *0 - 1* Aumenta la cantidad de muestreo interno para obtener una calidad aún mayor, a una velocidad de cálculo reducida.

## Imágenes de ejemplo

![](../../../../../../assets/hqblur-example.gif)

</td>
</tr>
</table>
