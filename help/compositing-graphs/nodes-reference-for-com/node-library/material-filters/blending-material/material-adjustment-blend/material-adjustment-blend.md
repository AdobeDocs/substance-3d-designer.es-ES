---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de ajuste de material para fusionar ajustes de material entre materiales para ajustar los efectos de composición.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de Ajuste de Material
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# Fusión de Ajuste de Material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-adjustment-blend.resources/material-adjustment-blend.png){width="128px"}

<b>En:</b> Filtros de material > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo permite ajustar todos y cada uno de los canales de un material completo, basándose en una máscara. Su objetivo es facilitar y agilizar el flujo de trabajo de materiales.

Resulta útil si desea ajustar algunos canales de un material (por ejemplo, hacer que la difusión sea más brillante y la rugosidad más oscura) basándose en la misma máscara.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara de ID de color</b> <i>Entrada de color</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |
| <b>Máscara de escala de grises</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/Brillo en lugar de Metálico/Rugosidad.<br><br>Esto también habilita y deshabilita la apariencia de los grupos relevantes del canal. |
| <b>Difuso</b> | Realiza operaciones de ajuste en el canal de Difuso, en áreas definidas por la máscara. |
| <b>Color base</b> | Realiza operaciones de ajuste en el canal de Color base, en áreas definidas por la máscara. |
| <b>Normal</b> |  |
| <b>Intensidad</b> <i>0.0 - 1.0</i> | Bajar tonos Intensidad normal |
| <b>Specular</b> | Realiza operaciones de ajuste en el canal de Specular, en áreas definidas por la máscara. |
| <b>Emisivo</b> | Realiza operaciones de ajuste en el canal Emissive, en áreas definidas por la máscara. |
| <b>Brillo</b> | Realiza operaciones de ajuste en el canal Brillo, en áreas definidas por la máscara. |
| <b>Rugosidad</b> | Realiza operaciones de ajuste en el canal Rugosidad (Roughness), en áreas definidas por la máscara. |
| <b>Metálico</b> | Realiza operaciones de ajuste en el canal Metálico, en áreas definidas por la máscara. |
| <b>Specular level</b> | Realiza operaciones de ajuste en el canal de Specular level, en áreas definidas por la máscara. |
| <b>Oclusión de ambiente</b> | Realiza operaciones de ajuste en el canal Oclusión ambiente, en áreas definidas por la máscara. |
| <b>Height</b> | Realiza operaciones de ajuste en el canal de Height, en áreas definidas por la máscara. |
| <b>Opacidad</b> | Realiza operaciones de ajuste en el canal Opacidad, en áreas definidas por la máscara. |
| <b>Máscara de ID de color</b> <i>Falso/Verdadero</i> | Establezca esta opción para utilizar la Máscara de ID de color en lugar de la máscara de escala de grises. |
| <b>Rugosidad</b> <i>0.01 - 1.0</i> | Si la Máscara de ID de color está activada, esto determina la extensión del color de selección de ID de color. |
| <b>Color</b> <i>(Valor de color)</i> | Define el color que se debe elegir del mapa de ID de color y la máscara. |
| <b>Relleno</b> <i>0.0 - 1.0</i> | Determina el contraste o las transiciones de fusión de la máscara de ID de color. |
