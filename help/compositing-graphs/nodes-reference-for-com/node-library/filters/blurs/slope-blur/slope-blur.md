---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: Utilice el nodo Desenfoque de Pendiente para aplicar efectos de desenfoque direccional basados en pendientes de mapa de height para crear desenfoque de movimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desenfoque de pendiente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# Desenfoque de pendiente

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

## Desenfoque de pendiente (escala de grises)

**En:** *Filtros/Desenfoques*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza un desenfoque avanzado de alta calidad en el que la Anisotropía/dirección se controla mediante un &quot;mapa de Pendiente&quot; en escala de grises. Imagínatelo como el efecto Desenfoque de Pendiente siguiendo las pendientes del Mapa de Pendiente como si fuera un Mapa de altura, similar a [Deformación direccional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) (en el que se basa internamente).

Este es uno de los desenfoques más interesantes y potentes de Designer. Se puede utilizar para lograr algunos efectos muy interesantes e inesperados, como desconchar y desgastar los bordes o manchas y fugas de dirt o óxido.

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utiliza &quot;Desenfoque de Pendiente&quot; para las entradas de color o &quot;Desenfoque de Pendiente en escala de grises&quot; para las entradas de escala de grises.

## Parámetros

### Entradas

* **Pendiente**: *Entrada en escala de grises* mapa de Pendiente para controlar el ángulo de la anisotropía. Debe contener idealmente degradados inclinados; las transiciones duras y nítidas no funcionarán bien.

### Parámetros

* **Ejemplos**: *0 - 32* La cantidad de muestras afecta la calidad a expensas de la velocidad.
* **Intensidad**: *0.0 - 16.0*\
  Cantidad o intensidad del desenfoque.
* **Modo**: *Desenfocar, Mín., Máx.*|\
  Modo de fusión para las pasadas de desenfoque consiguientes. &quot;Desenfocar&quot; se comporta más como un [Desenfoque Anisotrópico](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) estándar, mientras que Min &quot;comerá&quot; las áreas existentes y Max &quot;manchará&quot; las áreas blancas.

## Imágenes de ejemplo

![](../../../../../../assets/slopeblur01.gif)

![](../../../../../../assets/slopeblur02.gif)

</td>
</tr>
</table>
