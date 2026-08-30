---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: Utilice el nodo Filtro de estación para aplicar efectos estacionales a los materiales y así crear variaciones de primavera, verano, otoño e invierno.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filtro de temporada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---


# Filtro de temporada

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](season-filter.resources/default-icon.png){width="128px"}

<b>En:</b> Filtros de material > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo añade efectos como un nivel de agua animado, nieve, hielo y/o musgo.

Ten en cuenta que este es un filtro antiguo que no pretende ser completamente correcto para la PBR. Se conserva principalmente por motivos de compatibilidad o heredados, aunque puede seguir siendo útil en algunos casos. Se pueden encontrar versiones más recientes correctas de la PBR en [Snow Cover](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) y [Water Level](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

El nodo requiere un conjunto adecuado de entradas de material, principalmente con un mapa de altura o mapa normal decentemente detallado.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Avanzado</b> |  |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Máscara</b> <i>Falso/Verdadero</i> | Activa o desactiva el uso del mapa de máscara. |
| <b>Intensidad de luz</b> <i>0.0 - 1.0</i> | Intensidad de la luz (fingida). |
| <b>Ángulo claro</b> <i>0.0 - 1.0</i> | Ángulo de incidencia de la luz (falsificada) |
| <b>Efecto</b> |  |
| <b>Efecto de Height o normal</b> <i>Height, normal</i> | Selecciona qué mapa de entrada controla los efectos. |
| <b>Nivel de agua</b> <i>0.0 - 1.0</i> | Sube o baja el nivel del agua en función del Height/Información normal. |
| <b>Detalles del agua</b> <i>0.0 - 1.0</i> | Define la cantidad de detalles en el agua. |
| <b>Refracción</b> <i>0.0 - 1.0</i> | Define la cantidad de refracción falsa en el efecto. |
| <b>Reflejo</b> <i>0.0 - 1.0</i> | Define la cantidad de reflejo falso en el efecto. |
| <b>Distancia de reflejo</b> <i>0.0 - 1.0</i> | Controla los elementos visuales de reflejo. |
| <b>Ángulo de reflejo</b> <i>0.0 - 1.0</i> | Controla los elementos visuales de reflejo. |
| <b>Dirección de flujo</b> <i>0.0 - 1.0</i> | Controla el flujo de animación (utilice Substance Player para visualizar). |
| <b>Hielo</b> <i>0.0 - 1.0</i> | Establece la congelación del agua. |
| <b>Detalles de hielo</b> <i>0.0 - 1.0</i> | Define la cantidad de detalles en el hielo. |
| <b>Snow</b> <i>0.0 - 1.0</i> | Define la cantidad de cobertura de nieve. |
| <b>Musgo</b> <i>0.0 - 1.0</i> | Define la cantidad de cobertura de musgo. |
| <b>Escala de musgo</b> <i>1 - 4</i> | Establece la escala de la textura de musgo generada. |
| <b>Color de musgo</b> <i>(Valor de color)</i> | Define el color del musgo. |
| <b>Color de agua</b> <i>(Valor de color)</i> | Define el color del agua, incluida la alfa/opacidad. |
| <b>Fusión</b> |  |
| <b>Intensidad de Difuso</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la difusión. |
| <b>Intensidad de Color base</b> <i>0.0 - 1.0</i> | Intensidad de fusión del color base. |
| <b>Intensidad normal</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la Normal. |
| <b>Intensidad del Specular</b> <i>0.0 - 1.0</i> | Fusión del Specular. |
| <b>Intensidad de Brillo</b> <i>0.0 - 1.0</i> | Fuerza de fusión del Brillo. |
| <b>Intensidad de rugosidad</b> <i>0.0 - 1.0</i> | Fuerza de fusión de la rugosidad. |
| <b>Intensidad de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Fuerza de fusión de la Oclusión ambiente. |
| <b>Intensidad de Height</b> <i>0.0 - 1.0</i> | Fusión del Height. |
