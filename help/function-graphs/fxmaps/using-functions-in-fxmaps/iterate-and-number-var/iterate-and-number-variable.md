---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: Aprenda a utilizar variables de número e iteración en FXMaps para crear patrones de bucle y variaciones de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variable de número e iteración
user-guide-description: ''
user-guide-title: ''
source-git-commit: 65a0ec6dc38e7595406c0c531be72ad1670dfb86
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Iterar y variable `$number`

![](iterate-and-number-variable.resources/iterate-1.jpg)

El nodo Iteración procesará los nodos conectados a la salida derecha durante el tiempo especificado por el valor Iteraciones.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="iterate-and-number-variable.resources/1-iteration.png"/></div> | 1 iteración: el motivo gaussiano se procesa una vez |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="iterate-and-number-variable.resources/10-iterations.png"/></div> | 10 iteraciones: el motivo gaussiano se procesa 10 veces en el mismo lugar |

Al utilizar un nodo iterado, puede utilizar la variable `$number` para obtener el valor de iteración actual. `$number` es un valor flotante y comienza en 0.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

Esta función, definida en el parámetro Desplazamiento de patrón, se ejecutará 10 veces, una por cada patrón.

El primer patrón tiene un valor `$number` igual a 0 y se representa a continuación en la coordenada (0, 0). El segundo patrón tiene un valor `$number` igual a 1 y, a continuación, se representa en la coordenada (0,1, 0) (1 x 0,1 = 0,1) y así sucesivamente para los patrones siguientes.
