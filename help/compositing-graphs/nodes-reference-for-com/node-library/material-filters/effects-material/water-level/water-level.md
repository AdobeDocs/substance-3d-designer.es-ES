---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: Utilice el nodo Nivel de agua para mezclar materiales basados en el height del nivel de agua para crear efectos realistas sobre el agua.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nivel del agua
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# Nivel del agua

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](water-level.resources/water-level.png){width="128px"}

<b>En:</b> Filtros de material > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Efecto todo en uno que añade un nivel de agua a una entrada de material completa. El material de entrada debe tener un buen mapa de altura de alta calidad para que el efecto funcione. El resultado es una PBR correcta.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Nivel de agua</b> <i>0.0 - 1.0</i> | Control principal para subir o bajar el nivel del agua. |
| <b>Oscuridad del agua</b> <i>0.0 - 1.0</i> | Establece la &quot;transparencia&quot; general del agua. |
| <b>Humedad de los bordes</b> <i>0.0 - 1.0</i> | Determina el aspecto húmedo que deben tener los bordes de agua. |
| Distancia de humedad de los bordes <b>Edges</b> <i>0.0 - 1.0</i> | Define hasta dónde llegan los bordes húmedos. |
| <b>Cantidad de desenfoque de Profundidad</b> <i>0.0 - 1.0</i> | Define la cantidad de desenfoque en función de la profundidad debajo del agua. Modifica el radio de desenfoque. |
| <b>Opacidad De Desenfoque De Profundidad</b> <i>0.0 - 1.0</i> | Determina la cantidad de desenfoque de profundidad que se fusiona y se puede utilizar para reducir el efecto del desenfoque. |
| <b>Color de lodo</b> <i>(Valor de color)</i> | Define el color del efecto de lodo. |
| <b>Profundidad de lodos</b> <i>0.0 - 1.0</i> | Establece la profundidad a la que comienza a aparecer el lodo, en relación con el nivel del agua. |
| <b>Opacidad del lodo</b> <i>0.0 - 1.0</i> | Define la opacidad global del efecto de lodo. |
| <b>Frost</b> <i>0.0 - 1.0</i> | Define la cantidad de escarcha. Comienza a aparecer desde los bordes exteriores y se mueve hacia dentro. |
| <b>Intensidad de escarcha</b> <i>0.0 - 1.0</i> | Define la intensidad de la helada y controla la &quot;opacidad&quot; del efecto. |
| <b>Grietas Frost</b> <i>0.0 - 1.0</i> | Define la cantidad de grietas en las transiciones de congelado a líquido. |
| <b>Formato Normal Frost</b> <i>DirectX/OpenGL</i> | Cambia el canal verde del efecto Frost Normalmap. |
