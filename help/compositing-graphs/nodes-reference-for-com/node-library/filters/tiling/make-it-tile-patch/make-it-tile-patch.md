---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Utilice el nodo Hacer parche de mosaico para aplicar parches y crear texturas de mosaico perfectas a partir de imágenes de entrada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hacer que parche de azulejo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Hacer que parche de azulejo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-patch.png)

![](../../../../../../assets/make-it-tile-patch-grayscale.png)

## Parche del mosaico Make It (Escala de grises)

**En:** *Filtros/Mosaico*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo es un mosaico semialeatorio basado en la cuadrícula. Toma un parche de entrada y lo sella, intentando convertirlo en una imagen de mosaico sin demasiadas repeticiones, según su configuración.

Útil para cuando se dispone de un pequeño parche de textura y se desea crear una textura de mosaico a mayor escala a partir de ella.

Ten en cuenta que esto es diferente de la [Foto de Hacer Azulejo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), que principalmente corrige los bordes.

Para hacer esto con todo un material, consulte [Mosaico automático inteligente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

## Parámetros

* **Tamaño de máscara**: *0.0 - 1.0* Tamaño de la máscara redonda usada al sellar el parche.
* **Precisión de máscara**: *0.0 - 1.0* Precisión de difuminado/smoothness de la máscara.
* **Deformación de máscara**: *-100.0 - 100.0* Introduce deformación en los bordes de la máscara. Es útil para evitar transiciones suaves e indefinidas entre parches.
* **Ancho del tamaño del motivo**: *0.0 - 1000.0* Cambia el ancho del parche de forma no uniforme.
* **height de tamaño de trama**: *0.0 - 1000.0* Cambia el height del parche de forma no uniforme.
* **Trastorno**: *0.0 - 1.0*\
  Introduce la aleatoriedad de la traducción, cambiando ligeramente los parches.
* **Variación de tamaño**: *0.0 - 100.0* Introduce la variación de tamaño de la máscara.
* **Octava**: *0 - 6* Este es el control principal que determina el tamaño global.
* **Rotación**: *-360.0 - 360.0* Gira previamente el parche.
* **Variación de rotación**: *0.0 - 360.0* Introduce una rotación aleatoria para cada sello de parche.
* **Color de fondo**: *(Valor de color)*Define el color de fondo para las áreas en las que no aparece ningún parche.
* **Variación de color**: *0.0 - 1.0 (solo versión de color)*Introduce la variación de color por parche.
* **Variación de luminosidad** *(solo versión de escala de grises)*Introduce variación de luminosidad por parche.

## Imágenes de ejemplo

![](../../../../../../assets/patch-ex.gif)

</td>
</tr>
</table>
