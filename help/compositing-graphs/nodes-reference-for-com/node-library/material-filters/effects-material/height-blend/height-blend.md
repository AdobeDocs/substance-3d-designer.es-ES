---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de Height para fusionar texturas basadas en mapas de height para crear transiciones de materiales realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Fusión de height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## Fusión de height

**En:** *Filtros/Efectos De Materiales*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Combina dos mapas de altura en función de la información de height. Genera un mapa de altura fusionado, pero también una máscara de blanco y negro que se puede utilizar en otros lugares.

Esto resulta útil cuando tiene que combinar dos mapas de altura de alta calidad, pero no necesariamente un material completo, como se requiere para [Mezcla de Height de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md).

## Parámetros

### Entradas

* **Height superior**: *Entrada en escala de grises*
* **Height inferior**: *Entrada en escala de grises*
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Desplazamiento de Height**: *0.0 - 1.0* Desplaza los mapas de altura para que el nivel de fusión se mueva a lo largo del eje del height. Este es el control principal de la fusión.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste de la fusión y perfecciona las transiciones.
* **Modo**: *height equilibrado, prioridad de height inferior* Cambia entre dos modos de fusión diferentes.
* **Opacidad**: *0.0 - 1.0*\
  Opacidad de fusión del height en primer plano, lo funde hacia dentro o hacia fuera.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
