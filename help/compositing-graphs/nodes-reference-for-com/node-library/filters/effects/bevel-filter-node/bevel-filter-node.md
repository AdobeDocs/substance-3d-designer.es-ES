---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo Filtro biselado para crear bordes biselados en formas y motivos para añadir profundidad y dimensión.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bisel (nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---


# Bisel (nodo de filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## Bisel

**En:** *Filtros/Efectos*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza un efecto de biselado de bordes en un mapa de altura de escala de grises de entrada. Devuelve tanto el mapa de altos biselado como el mapa de normales en función de dicho mapa de altos.

Este es un nodo útil para aplicar perfiles de curva exactos en un mapa de altura básico y perfectamente binario (blanco y negro de alto contrato).

## Parámetros

### Entradas

* **entrada**: *Entrada en escala de grises*\
  Mapa de altura para convertir.
* **Curva personalizada**: *Entrada en escala de grises*\
  Degradado que determina la curva/pendiente exacta. Lo ideal es un nodo lineal de degradado, en el que se pueda realizar cualquier tipo de ajuste, como [Niveles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) o [Curvas](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md). Solo está activo cuando &quot;Usar curva personalizada&quot; es True.

### Parámetros

* **Distancia**: *-1.0 - 1.0* Hasta dónde debe llegar el efecto biselado.
* **Tipo de esquina**: *Redondo, Angular* Indica si el perfil biselado debe ser redondeado o recto.
* **Suavizado**: *0.0 - 5.0* Cuánto suavizado (desenfoque) adicional realizar después del bisel.
* **Usar desenfoque no uniforme**: *False/True* Especifica si el suavizado se debe realizar de manera no uniforme.
* **Usar curva personalizada**: *Falso/Verdadero* Cambia el uso de tu propia curva de height personalizada. Consulte más arriba para obtener más información.
* **Intensidad normal**: *0.0 - 50.0* Intensidad del mapa normal generado.
* **Formato normal**: *DirectX, OpenGL*\
  Cambiar entre diferentes formatos de Mapa normal (invierte el canal verde).

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
