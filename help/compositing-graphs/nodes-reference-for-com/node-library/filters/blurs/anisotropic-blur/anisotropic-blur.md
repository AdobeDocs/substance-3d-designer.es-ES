---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: Utilice el nodo Desenfoque anisotrópico para aplicar efectos de desenfoque direccional para crear efectos de desenfoque de movimiento y de desenfoque.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desenfoque anisotrópico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# Desenfoque anisotrópico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

## Desenfoque anisotrópico (escala de grises)

**En:** *Filtros/Desenfoques*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza un [desenfoque direccional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md) de alta calidad, con algunas configuraciones para personalizar la apariencia. También conocido como &quot;desenfoque de movimiento&quot;.

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utiliza &quot;Desenfoque anisotrópico&quot; para las entradas de color o &quot;Desenfoque anisotrópico en escala de grises&quot; para las entradas de escala de grises.

## Parámetros

* **Intensidad**: *0,0 - 16,0* Intensidad (radio) del desenfoque. Cuanto más alto sea este valor, mayor será el desenfoque.
* **Anisotropía**: *0.0 - 1.0* Direccionalidad del desenfoque. Establecer esto en 0.0 es lo mismo que realizar un desenfoque normal.
* **Ángulo**: *0.0 - 1.0* Establece el ángulo para la dirección del desenfoque.
* **Calidad**: *0 - 1* Cambia entre un[desenfoque de cuadro](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) y un desenfoque de HQ internamente. Intercambia velocidad por calidad.

## Imágenes de ejemplo

![](../../../../../../assets/aniso-blur-example.gif)

</td>
</tr>
</table>
