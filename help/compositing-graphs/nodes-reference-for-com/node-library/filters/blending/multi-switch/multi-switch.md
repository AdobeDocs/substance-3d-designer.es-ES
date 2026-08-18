---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Utilice el nodo Conmutador múltiple para cambiar entre varias texturas de entrada en función de un selector para la selección de texturas condicionales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conmutador múltiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# Conmutador múltiple

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

## Interruptor múltiple (escala de grises)

**En:** *Filtros/Fusión*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Actúa como un switch-box, pasando solamente a través de la entrada definida por el parámetro &#39;Input Selection&#39;. Por lo tanto, si hay dos entradas conectadas, solo se devolverá una de ellas (sin modificar), dependiendo de la elección del usuario.

Muy útil para añadir muchas opciones diferentes en un gráfico. Combinado con [exponer](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)(preferiblemente como lista desplegable), es posible realizar muchas personalizaciones.

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utilice &quot;Multi Switch&quot; para las entradas de color y &quot;Multi Switch Grayscale&quot; para las entradas de escala de grises.

## Parámetros

### Entradas

* **Entrada 1-20**: *Entrada de color*

### Parámetros

* **Número de entrada**: *2 - 20* Cantidad de entradas para exponer. Importante: no elimina las conexiones cuando se reduce el número.
* **Selección de entrada**: *1 - 20* Qué entrada se devuelve como resultado.

## Imágenes de ejemplo

</td>
</tr>
</table>
