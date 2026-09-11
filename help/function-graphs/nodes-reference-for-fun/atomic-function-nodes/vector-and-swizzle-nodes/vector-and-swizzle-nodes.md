---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/vector-and-swizzle-nodes.html"
breadcrumb-title: ''
description: Utilice nodos vectoriales y de deslizar en los gráficos de funciones de Substance 3D Designer para manipular los datos y componentes vectoriales.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Vector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vector
user-guide-description: ''
user-guide-title: ''
source-git-commit: 81c39001686736d41614fd59247d53e6d8438def
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 5%

---


# Nodos Vector y Swizzle

Los nodos vectoriales y de torsión permiten construir y deconstruir nodos vectoriales desde y en componentes independientes, respectivamente.Son similares a [Combinación RGBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) y [Dividir RGBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), pero luego para Gráficos de funciones. También son un método excelente para convertir entre tipos de datos vectoriales, ya que [Casting](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) no es una opción en muchos casos.

## Nodos vectoriales

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Los nodos vectoriales permiten combinar vectores o elementos con menos componentes en vectores con más componentes. Existen algunas reglas o limitaciones específicas para los nodos de vectores:

* Los nodos vectoriales tienen **solo dos entradas**, incluso si el vector resultante tiene más de 2 componentes.
* Las entradas de vectores **no están limitadas a un tipo**: pueden tomar cualquier componente menor como entrada.
* El orden del resultado final viene determinado por el **orden de las Entradas**.

Esto significa que es mejor utilizar los siguientes métodos:

* Construir un vector 4 de dos maneras: o bien conecte dos vectores de 2 componentes, o bien conecte un vector de 1 componente y otro de 3 componentes.
* Si desea construir un vector de 3 o 4 componentes a partir de enteros o Flotante individuales, primero debe hacer al menos una combinación de vector 2 antes de poder combinarlos en un vector de 3 componentes.

Piense bien en el orden de las conexiones. El orden de conexión de las entradas se ilustra a continuación.

![](vector-and-swizzle-nodes.resources/vector-int1.png){width="200px"}

Ejemplo de Conexión izquierda: primero un Entero(1) y después un Entero 3. El resultado es el siguiente

| Salida | X | Y | Z | An |
| --- | --- | --- | --- | --- |
| Entrada 1 | 0 |  |  |  |
| Entrada 2 |  | 1 | 2 | 4 |

![](vector-and-swizzle-nodes.resources/vector-int2.png){width="200px"}

Ejemplo a la izquierda intercambia las entradas alrededor del primer ejemplo, primero Entero 3 y, a continuación, un Entero(1).

| Salida | X | Y | Z | An |
| --- | --- | --- | --- | --- |
| Entrada 1 | 1 | 2 | 4 |  |
| Entrada 2 |  |  |  | 0 |

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectorint4.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectorint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectorint3.png"/></div> |
| --- | --- | --- |
| **Vector Integer2** | **Entero vectorial3** | **Entero vectorial4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectofloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectofloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="vector-and-swizzle-nodes.resources/fn-vector-vectofloat4.png"/></div> |
| **Flotante de vector2** | **Flotante de vector3** | **Flotante de vector4** |

</td>
</tr>
</table>

## Girar nodos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Los nodos de Swizzle deconstruyen o dividen componentes de vectores de varios componentes, lo que le permite utilizar los componentes X, Y, Z y W individualmente, así como intercambiarlos. Se aplican las siguientes reglas y limitaciones:

* Los nodos Swizzle tienen **solo una salida**.
* Los nodos de conexión **toman cualquier entrada** del tipo correcto (Int o Flotante).

### Componentes divididos

El caso de uso más común de Swizzle es utilizarlo para dividir componentes, como frenar un Integer4 en 4 enteros individuales. Las limitaciones significan que necesitará cuatro nodos de Referenciar entero separados para esto.

Cualquier otro tipo de división también es posible para un Integer4, como dos Integer2, o un Integer y un Integer3, una vez más teniendo en cuenta que cada resultado necesita su propio nodo.

### Intercambiar/deslizar componentes

Como su nombre indica, Swizzle se puede utilizar para cambiar el orden de los valores o incluso sobrescribir los valores. Puede cambiar el orden de X,Y,Z,W a W,Y,X,Z, y puede cambiar los valores de X,Y,Z,W a X,X,X,W, por ejemplo.

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzleint1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzleint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzleint3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzleint4.png"/></div> |
| --- | --- | --- | --- |
| **Referenciar entero** | **Giro** **Entero2** | **Giro** **Entero3** | **Giro** **Entero4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzlefloat1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzlefloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzlefloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c3_image" src="vector-and-swizzle-nodes.resources/fn-vector-swizzlefloat4.png"/></div> |
| **Swizzle** **Flotante** | **Swizzle** **Flotante2** | **Swizzle** **Flotante3** | **Swizzle** **Flotante4** |

</td>
</tr>
</table>
