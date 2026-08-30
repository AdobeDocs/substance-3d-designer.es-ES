---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/constant-nodes.html"
breadcrumb-title: ''
description: Acceda a nodos constantes en los gráficos de funciones de Substance 3D Designer para definir parámetros y valores constantes.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Constant
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Constante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---


# Constante

Los nodos constantes son una forma de crear un valor estático para utilizarlo dentro de las gráficas de funciones de Substance. A diferencia de [variables](../../../../function-graphs/variables/variables.md), no se pueden modificar externamente.

Además, esta página proporciona información adicional para cada tipo de datos y casos prácticos habituales.

## Enteros

Los enteros constantes generan números enteros y tienen un paso de 1.

[Se pueden convertir a Float,](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) lo que se recomienda hacer cuando se realiza cualquier operación más compleja que las adiciones, las resta y las comparaciones simples.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo entero](constant-nodes.resources/fn-constant-integer.png "Icono de tipo entero")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entero</b>

Un entero tiene un solo componente. Resulta útil como índice para realizar selecciones, como:

* seleccionar una opción presentada al usuario como un menú desplegable (consulte &#39;Lista desplegable&#39; en [esta página](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)).
* seleccionando la entrada de un nodo [Multi switch](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md).<b></b>

>[!IMPORTANT]
>
> <b>Los enteros negativos</b> en las funciones de parámetro *no se admiten*. Consulte [esta página](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md) en la sección &quot;Problemas técnicos&quot; para obtener una solución alternativa.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer2 type icon](constant-nodes.resources/fn-constant-integer2.png "Integer2 type icon")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entero2</b>

Un nodo Integer2 genera un vector entero estático de 2 componentes con componentes (X, Y).

Integer2 no es común, pero se usa, por ejemplo, para establecer mosaicos X e Y 2D en un [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer3 type icon](constant-nodes.resources/fn-constant-integer3.png "Integer3 type icon")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entero3</b>

Un nodo Integer3 genera un vector entero estático de 3 componentes con componentes (X, Y, Z).

El entero 3 no es común y es poco probable que se encuentre mucho.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo entero4](constant-nodes.resources/fn-constant-integer4.png "Icono de tipo entero4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entero4</b>

Un nodo Integer4 genera un vector entero estático de 4 componentes con componentes (X, Y, Z, W).

El entero 4 no es común y es poco probable que se encuentre mucho.<b>\
</b>

</td>
</tr>
</table>

## Flotantes

Los valores flotantes constantes generan números fraccionarios, no números enteros, lo que significa que siempre tendrán valores después del signo decimal y pueden aumentar o disminuir en pasos menores que 1 (valor predeterminado de 0,01).

[Los valores flotantes se pueden convertir a enteros](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), pero se redondearán hacia arriba o hacia abajo al entero más cercano, lo que significa que se pierden los datos y la precisión.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo flotante](constant-nodes.resources/fn-constant-float.png "Icono de tipo flotante")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flotador</b>

Un flotador, tiene un solo componente, el (1) se omite del nombre para la brevedad. Flotante es muy común y se utiliza para cualquier valor que requiera un control preciso en forma de regulador o ángulo. Puede encontrarlo en casi todos los parámetros de Node. También es el tipo de datos preferido para un valor de escala de grises.<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo Float2](constant-nodes.resources/fn-constant-float2.png "Icono de tipo Float2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Un nodo Float2 genera un vector flotante estático de 2 componentes. Los componentes se denominan X, Y. Float2 es bastante común y se utiliza para [coordenadas de muestreo](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) y para [Desplazamientos de transformación](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo Float3](constant-nodes.resources/fn-constant-float3.png "Icono de tipo Float3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Un nodo Float3 genera un vector flotante estático de 3 componentes. Los componentes se denominan X,Y,Z. Float3 es poco común, se usa principalmente para representar [coordenadas de escala 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) y como una forma más sencilla de almacenar color sin datos de Alpha.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo flotante4](constant-nodes.resources/fn-constant-float4.png "Icono de tipo flotante4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Un objeto Float4 genera un vector float estático de 4 componentes. Los componentes se denominan X,Y,Z,W. Float4 es muy común, ya que es la forma preferida de almacenar y establecer la información de color [donde los datos XYZW representan valores RGBA.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)<b>\
</b>

</td>
</tr>
</table>

## Otros

Existen dos tipos de datos adicionales en los gráficos de funciones de Substance: booleanos y cuerdas. Se introdujeron cadenas junto al nodo [Text](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) en la versión 6 de Designer.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo booleano](constant-nodes.resources/fn-constant-boolean.png "Icono de tipo booleano")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Booleano</b>

Un valor booleano es el tipo de datos más simple que existe, ya que sólo conoce dos estados: Verdadero o Falso, 1 o 0. Está representado por el color blanco. No es posible intercambiar entre Boolean y Integer sin [Casting](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) o mediante [nodos lógicos.](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) Un valor booleano es bastante común y es una forma excelente de controlar el flujo de una función o gráfico; un uso típico sería para un [nodo de conmutador.](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo de cadena](constant-nodes.resources/fn-constant-string.png "Icono de tipo de cadena")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Cadena</b>

Un nodo de cadena genera una cadena estática, un fragmento de texto. Es el tipo de datos más exótico disponible en Functions y, por lo general, no se puede utilizar mucho junto con otros nodos Function. Su objetivo principal es funcionar como salida final para el [Nodo de texto.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

</td>
</tr>
</table>
