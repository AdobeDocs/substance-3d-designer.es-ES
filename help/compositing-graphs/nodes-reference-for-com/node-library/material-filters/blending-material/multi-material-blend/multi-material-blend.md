---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de varios materiales para fusionar varios materiales y crear combinaciones de materiales complejas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de varios materiales
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# Fusión de varios materiales

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## Fusión de varios materiales

**En:** *Filtros/Fusión De Materiales*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo combina varios materiales en función de un mapa de ID de material/ID de color, uno que se puede hornear desde una malla. Se requieren hasta 16 materiales completos diferentes, con cualquier tipo de canales que habilites en el grupo Canales.

El nodo es muy útil cuando se texturizan accesorios completos, ya que permite la parametrización completa de los materiales, al tiempo que se combinan dinámicamente todos. Perfecto para aplicar texturas a accesorios simples o complejos que tengan pasteles de ID adecuados, o incluso para crear Substance de &quot;plantillas&quot; totalmente canalizados que se ajusten completamente a los estándares del equipo.

Tenga en cuenta que cuando se utiliza este material, el material 1, Ranura 1 es siempre el material por defecto y aparecerá en cualquier lugar donde no aparezca ningún otro material. Es por eso que no se puede configurar un color para él. Si quieres jugar a esta caja fuerte, puedes, por ejemplo, conectar un [Material base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) que esté establecido en negro áspero.

## Parámetros

### Entradas

* **1-16 Ranuras completas de materiales** La cantidad de ranuras viene determinada por el menú desplegable **Materiales**.
* **Id. de color**: *Entrada de color*\
  Mapa de ID de color al horno.

### Parámetros

* **Materiales**: *2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16* Define la cantidad máxima de diferentes materiales que se deben mezclar.
* **Canales**\
  Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Material 2-16** Aparece un grupo por cada material habilitado.
  * **Color**: *(Valor de color)*Color que se selecciona del mapa de ID que coincide con esta ranura de material.
  * **Rugosidad**: *0.01 - 1.0* Sangrado en los colores vecinos.
  * **Relleno**: *0.0 - 1.0* Dureza de las transiciones: contraste de máscara.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
