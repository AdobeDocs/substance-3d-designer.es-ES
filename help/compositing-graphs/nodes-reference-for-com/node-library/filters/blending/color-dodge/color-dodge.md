---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-dodge.html"
breadcrumb-title: ''
description: Utilice el nodo de fusión Sobreexponer color para aclarar texturas reduciendo el contraste para crear efectos de iluminación y resplandor.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Dodge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobreexposición del color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 10%

---


# Sobreexposición del color

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-dodge.png){width="128px"}

## Sobreexposición del color

**En:** *Filtros/Fusión*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza una fusión Sobreexponer color. Matemáticamente, la fórmula es Fondo / (1-Primer plano).

## Parámetros

### Entradas

* **Primer plano**: *Entrada de color*
* **Fondo**: *Entrada de color*
* **Máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Opacidad**: *0.0 - 1.0*\
  Fusión de opacidad entre primer plano y fondo.
* **Fusión de Alpha**: *Falso/Verdadero*\
  Alterna la fusión de los canales alfa Primer plano y Fondo. Si se establece en False, se omite el canal alfa del primer plano.

## Imágenes de ejemplo

</td>
</tr>
</table>
