---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Utilice el nodo Flood Fill a color de escala de grises para rellenar regiones conectadas con colores de escala de grises para crear motivos monocromos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill a GrayscaleColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---


# Flood Fill a escala de grises/color

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-grayscale.png){width="128px"}

![](../../../../../../assets/floodfill-to-color.png){width="128px"}

## Flood Fill a escala de grises/color aleatoria

**En:** *Filtros/Efectos*

**&#x200B;**&#x200B;Simple&#x200B;**&#x200B;**

</td>
<td style="border: 0;" valign="top">

## Descripción

Utiliza datos del Flood Fill para generar muestras de valores de escala de grises o de color. A diferencia de [Flood Fill a escala de grises aleatoria](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), estos dos nodos permiten un mayor control para establecer la variación y los tonos exactos, con un mapa de entrada adicional adicional para determinar el valor base que se debe aleatorizar según la celda.

Es un sistema potente para dar a cada célula un valor o color único, pero aún así retener el control y basarlo en una entrada predeterminada.

## Parámetros

### Entradas

* **Flood Fill**: *Entrada de color*
* **Entrada de escala de grises/color**: *Entrada de escala de grises/color*

### Parámetros

* **Ajuste de luminancia/color**: *-1.0 - 1.0* Establezca el sesgo o valor base del nodo. Cuando se utiliza una entrada de escala de grises o de color, se utiliza para cambiar ese valor inicial como punto de partida.
* **Aleatorio de luminancia/color**: *-1.0 - 1.0* Establecer la cantidad de variación.

</td>
</tr>
</table>
