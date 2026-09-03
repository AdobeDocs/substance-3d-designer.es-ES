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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---


# Fusión de varios materiales

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-material-blend.resources/multi-material-blend-01.png){width="128px"}

<b>En:</b> Filtros de material > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo combina varios materiales en función de un mapa de ID de material/ID de color, uno que se puede hacer un bake desde una malla. Se requieren hasta 16 materiales completos diferentes, con cualquier tipo de canales que habilites en el grupo Canales.

El nodo es muy útil cuando se texturizan accesorios completos, ya que permite la parametrización completa de los materiales, al tiempo que se combinan dinámicamente todos. Perfecto para aplicar texturas a accesorios simples o complejos que tengan hagas un bake de ID adecuados, o incluso para crear Substance de &quot;plantillas&quot; totalmente canalizados que se ajusten completamente a los estándares del equipo.

Tenga en cuenta que cuando se utiliza este material, el material 1, Ranura 1 es siempre el material por defecto y aparecerá en cualquier lugar donde no aparezca ningún otro material. Es por eso que no se puede configurar un color para él. Si quieres jugar a esta caja fuerte, puedes, por ejemplo, conectar un [Material base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) que esté establecido en negro áspero.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>1-16 ranuras de material completo</b> | La cantidad de ranuras viene determinada por el menú desplegable <b>Materiales</b>. |
| <b>Id. de color</b> <i>Entrada de color</i> | Mapa de ID de color hecho un bake. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Materiales</b> <i>2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16</i> | Define la cantidad máxima de diferentes materiales que se deben fusionar. |
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Material 2-16</b> | Aparece un grupo para cada material activado. |
| <b>Color</b> <i>(Valor de color)</i> | Color que se debe seleccionar en el mapa de ID que coincide con esta ranura de material. |
| <b>Rugosidad</b> <i>0.01 - 1.0</i> | Sangra en los colores vecinos. |
| <b>Relleno</b> <i>0.0 - 1.0</i> | Dureza de las transiciones: contraste de máscara. |
