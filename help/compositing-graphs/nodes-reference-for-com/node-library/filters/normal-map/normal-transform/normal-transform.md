---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación normal para aplicar transformaciones a los mapas normales conservando correctamente las direcciones vectoriales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Transformación normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## Transformación normal

**En:** *Filtros/Mapa Normal*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

De forma similar al nodo de Transformación 2D atómica, esto permite la transformación de los mapas normales sin romper el espacio-tangente, en su lugar se recalcula sobre la marcha, lo que resulta en mapas normales siempre correctos.

## Parámetros

* **Matrix2x2**: *(Matriz de transformación):*\
  Gire o escale la entrada.
* **Desplazamiento**: *-0,5 - 0,5*\
  Mueve o traduce el resultado. Cuando el control Transformación está presente, el resultado se puede modificar interactuando directamente con el lienzo.
* **Formato normal**: *DirectX, OpenGL*\
  Cambiar entre diferentes Formatos de mapa de normales (invierte el canal verde)

</td>
</tr>
</table>
