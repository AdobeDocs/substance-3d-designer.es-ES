---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Utilice el nodo Conmutador múltiple para cambiar entre varias texturas de entrada en función de un selector para la selección de textura condicional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conmutador múltiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Conmutador múltiple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-switch.resources/multi-switch-01.png){width="128px"}

![](multi-switch.resources/multi-switch-02.png){width="128px"}

<b>En:</b> Filtros > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Actúa como un switch-box, pasando solamente a través de la entrada definida por el parámetro &#39;Input Selection&#39;. Por lo tanto, si hay dos entradas conectadas, solo se devolverá una de ellas (sin modificar), dependiendo de la elección del usuario.

Muy útil para añadir muchas opciones diferentes en un gráfico. Combinado con [exponer](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)(preferiblemente como lista desplegable), es posible realizar muchas personalizaciones.

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utilice &quot;Multi Switch&quot; para las entradas de color y &quot;Multi Switch Grayscale&quot; para las entradas de escala de grises.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-20</b> <i>Entrada de color</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Número de entrada</b> <i>2 - 20</i> | Cantidad de entradas que se van a exponer. Importante: no elimina las conexiones cuando se reduce el número. |
| <b>Selección de entrada</b> <i>1 - 20</i> | Qué entrada se devuelve como resultado. |
