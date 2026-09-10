---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo Metal Weathering para añadir efectos realistas de óxido y corrosión a los materiales metálicos basados en la geometría de malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metal Weathering
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 14%

---


# Metal Weathering

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-weathering.resources/metal-weathering.png){width="128px"}

<b>En:</b> Generadores Basados En Malla > Meteorización

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>WS normal</b> <i>Entrada de color</i> | Mapa normaldel espacio mundial hecho un bake utilizado para efectos internos y enmascaramiento. |
| <b>Oclusión de ambiente</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. |
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Avanzado</b> |  |
| <b>Formato normal</b> <i>Direct X, Open GL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Máscara</b> <i>Falso/Verdadero</i> | Activa o desactiva el uso del mapa de máscara. |
| <b>Efecto</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>Suciedad</b> <i>0.0 - 1.0</i> |  |
| <b>Bordes Con </b> <i>0.0 - 1.0</i> |  |
| <b>Descascarillado de Pintura</b> <i>0.0 - 1.0</i> |  |
| <b>Óxido</b> <i>0.0 - 1.0</i> |  |
| <b>Descascarillado de Óxido</b> <i>0.0 - 1.0</i> |  |
| <b>Óxido Verdigris</b> <i>Óxido, Verdigris</i> |  |
| <b>Escala de Grietas de Pintura</b> <i>1.0 - 16.0</i> |  |
| <b>Intensidad de deformación de Grietas de Pintura</b> <i>0.0 - 1.0</i> |  |
| Escala de Scratches de <b>Bordes afilados</b> <i>1.0 - 32.0</i> |  |
| <b>Intensidad de deformación de los Scratches de bordes afilados</b> <i>0.0 - 1.0</i> |  |
| <b>Color de metal crudo</b> <i>(Valor de color)</i> |  |
| <b>Color de Specular de metal crudo</b> <i>(Valor de color)</i> |  |
| <b>Valor de Brillo de metal sin procesar</b> <i>(valor de escala de grises)</i> |  |
| <b>Valor de rugosidad de metal crudo</b> <i>(valor de escala de grises)</i> |  |
| <b>Fusión</b> |  |
| <b>Intensidad de Difuso</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la difusión. |
| <b>Intensidad de Color base</b> <i>0.0 - 1.0</i> | Intensidad de fusión del color base. |
| <b>Intensidad normal</b> <i>0.0 - 64.0</i> | Intensidad de fusión de la Normal. |
| <b>Intensidad del Specular</b> <i>0.0 - 1.0</i> | Fusión del Specular. |
| <b>Intensidad de Brillo</b> <i>0.0 - 1.0</i> | Fuerza de fusión del Brillo. |
| <b>Intensidad de rugosidad</b> <i>0.0 - 1.0</i> | Fuerza de fusión de la rugosidad. |
| <b>Intensidad metálica</b> <i>0.0 - 1.0</i> | Intensidad de fusión del metal. |
| <b>Intensidad de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Fuerza de fusión de la Oclusión ambiente. |
| <b>Intensidad de Height</b> <i>0.0 - 1.0</i> | Fusión del Height. |
