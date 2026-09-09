---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: Utilice el nodo Cambiar para cambiar entre dos texturas de entrada basadas en una máscara para la selección de texturas condicionales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cambiar
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---


# Cambiar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](switch.resources/switch-1.png){width="128px"}

![](switch.resources/switch-grayscale.png){width="128px"}

<b>En:</b> Filtros > Fusión

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Un nodo de conmutador simple de 2 posiciones. Devuelve Input 1 o Input 2 en función de la configuración del parámetro Switch. El resultado no se ha modificado. Consulte [Conmutador múltiple](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) para obtener una versión más avanzada.

Muy útil para exponer una opción booleana (Verdadero/Falso) en un gráfico, donde solo necesita un botón y no una lista desplegable compleja para toda una selección de opciones.

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utilice &quot;Cambiar&quot; para las entradas de color y &quot;Cambiar escala de grises&quot; para las entradas de escala de grises.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1 (True)</b> <i>Entrada de color o escala de grises</i> |  |
| <b>Entrada 2 (False)</b> <i>Entrada de color o escala de grises</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cambiar</b> <i>Falso/Verdadero</i> | Cambia entre Input 1 (True) y 2 (False). |
