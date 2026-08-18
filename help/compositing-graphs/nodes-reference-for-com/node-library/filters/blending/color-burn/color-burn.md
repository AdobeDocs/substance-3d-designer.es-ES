---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: Utilice el nodo de fusión Subexposición de color para oscurecer las texturas aumentando el contraste para crear efectos de sombras y subexposición.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Subexposición de color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# Subexposición de color

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-burn.png){width="128px"}

## Subexposición de color

**En:** *Filtros/Fusión*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza una fusión de Subexponer color entre Primer plano y Fondo. Matemáticamente la fórmula es 1 - (1-Fondo) / Primer plano.

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
