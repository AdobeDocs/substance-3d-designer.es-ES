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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Variable Iterar y $number

![](../../../../assets/iterate-1.jpg)

El nodo Iteración procesará los nodos conectados a la salida derecha durante el tiempo especificado por el valor Iteraciones.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/1-iteration.png"/></div> | 1 iteración: el motivo gaussiano se procesa una vez |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../../../assets/10-iterations.png"/></div> | 10 iteraciones: el motivo gaussiano se procesa 10 veces en el mismo lugar |

Cuando se utiliza un nodo de iteración, se puede utilizar la variable $number para obtener el valor de iteración actual. $number es un valor flotante que comienza en 0.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

Esta función, definida en el parámetro Desplazamiento de patrón, se ejecutará 10 veces, una por cada patrón.

El primer patrón tiene un valor $number igual a 0 y, a continuación, se procesa en la coordenada (0, 0). El segundo patrón tiene un valor de $number igual a 1 y, a continuación, se procesa en la coordenada (0,1, 0) (1 x 0,1 = 0,1) y así sucesivamente para los patrones siguientes.

Ejemplo de descarga: [iterate\_node.sbs](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/sddoc/files/102400023/102367299/1/1423458106000/iterate-node.sbs)
