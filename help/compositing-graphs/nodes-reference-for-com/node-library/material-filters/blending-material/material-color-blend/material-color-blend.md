---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de color de material para fusionar canales de color entre materiales para crear efectos de material compuesto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de color de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# Fusión de color de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend.png){width="128px"}

<b>En:</b> Filtros de material > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo permite realizar ajustes en un material completo multicanal mediante la fusión de colores sólidos en la parte superior. Esta es la principal diferencia con [Fusión de ajuste de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), que solo permite ajustes de tipo [Niveles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) en los canales, mientras que este nodo usa ajustes de tipo [Fusión](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) con un color sólido.

Este nodo es muy útil cuando desea introducir una sugerencia de color plano en un Difuso o Color base, o cuando desea &quot;acoplar&quot; otros canales mediante un valor de color sólido definido.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>IDcolor</b> <i>Entrada de color</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |
| <b>Máscara de escala de grises</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo cuando utilice mapas de Specular/Brillo en lugar de Metálico/Rugosidad, por ejemplo. |
| <b>Difusión</b> |  |
| <b>Color</b> <i>(Valor de color)</i> | El valor de color que se debe fusionar en la parte superior del canal de Difuso. |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo. |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> | Modo de Fusión para utilizar en la operación. |
| <b>Color base</b> | Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión. |
| <b>Normal</b> |  |
| <b>Origen</b> <i>Height, máscara</i> |  |
| <b>Modo De Fusión</b> <i>Combinar, Fusión</i> |  |
| <b>Intensidad de Height</b> <i>0.0 - 1.0</i> |  |
| <b>Opacidad del Height</b> <i>0.0 - 1.0</i> |  |
| <b>Formato</b> <i>DirectX, OpenGL</i> |  |
| <b>Specular</b> | Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión. |
| <b>Emissive</b> | Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión. |
| <b>Brillo</b> | Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión. |
| <b>Rugosidad</b> | Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión. |
| <b>Metálico</b> | Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión. |
| <b>Specular level</b> | Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión. |
| <b>Oclusión de ambiente</b> | Fusiona un color sólido en la parte superior de este canal con opciones como en el grupo Difusión. |
| <b>Height</b> | Fusión un color sólido en la parte superior de este canal con opciones como en el grupo de Difuso. |
| <b>Opacidad</b> | Fusión un color sólido en la parte superior de este canal con opciones como en el grupo de Difuso. |
| <b>Máscara de ID de color</b> <i>Falso/Verdadero</i> | Utilice Máscara de ID de color en lugar de máscara de escala de grises. Tenga en cuenta que esto es solo para un color.<br><br>Habilita todas las opciones siguientes. |
| <b>Color</b> <i>(Valor de color)</i> | Qué color elegir y convertir en blanco. |
| <b>Rugosidad</b> <i>0.01 - 1.0</i> | La medida en que el color que has elegido se fusiona con los colores vecinos. |
| <b>Relleno</b> <i>0.0 - 1.0</i> | Contraste de transición del color elegido. |
