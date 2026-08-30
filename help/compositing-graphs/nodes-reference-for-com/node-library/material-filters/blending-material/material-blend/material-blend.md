---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de material para fusionar materiales enteros mediante máscaras para crear efectos de material compuesto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de materiales
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# Fusión de materiales

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-blend.resources/material-blend.png){width="128px"}

<b>En:</b> Filtros de material > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

La Fusión de material es el equivalente multicanal de material completo de [el nodo de Fusión atómica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Se mezcla entre dos materiales completos (todos los canales posibles) basados en una máscara de escala de grises, u opcionalmente basados en un solo color de una Máscara de ID de color.

Este nodo es útil si desea fusionar dos materiales y tener un mapa en escala de grises, pero no hace un bake el ID de color completo. Si tienes un ID de color para hacer un bake y deseas fusionar más de dos materiales, te recomendamos que uses la [Fusión de varios materiales](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>IDcolor</b> <i>Entrada de color</i> | Mapa de ID de color Hecho un bake opcional. |
| <b>Máscara de escala de grises</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo cuando utilice mapas de Specular/Brillo en lugar de Metálico/Rugosidad, por ejemplo. |
| <b>Difusión</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Color base</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Normal</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Specular</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Emissive</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Brillo</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Rugosidad</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Metálico</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Specular level</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Oclusión de ambiente</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Height</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Opacidad</b> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Fusión de opacidad entre primer plano y fondo |
| <b>Modo De Fusión</b> <i>Normal, Agregar, Restar, Multiplicar, Agregar/Sub, Máx., Mín., Cambiar</i> |  |
| <b>Máscara de ID de color</b> <i>Falso/Verdadero</i> | Utilice Máscara de ID de color en lugar de máscara de escala de grises. Tenga en cuenta que esto es solo para un color! |
| <b>Color</b> <i>(Valor de color)</i> | Qué color elegir y convertir en blanco. |
| <b>Rugosidad</b> <i>0.01 - 1.0</i> | La medida en que el color que has elegido se fusiona con los colores vecinos. |
| <b>Relleno</b> <i>0.0 - 1.0</i> | Contraste de transición del color elegido. |
