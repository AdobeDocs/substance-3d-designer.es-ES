---
helpx_url: ""
breadcrumb-title: ''
description: Acceda a nodos constantes en Substance 3D Designer para definir valores constantes en los gráficos de Substance.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Constante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# Constante

Los nodos constantes son una forma de crear un valor estático para utilizarlo dentro de los gráficos de Substance.

Puede encontrar estos nodos en la sección **Valores > Constantes** de la biblioteca.\
Todos incluyen un nodo [Procesador de valor](../../atomic-nodes/value-processor/value-processor.md) simple que genera el valor.

+++ Nodos constantes en la biblioteca

![constantes-library.png](constant.resources/constants-library.png)

+++

<p style="text-align: center;"><img src="./constant.resources/constants-float-01.png" alt="Nodo Flotante constante" /></p>

## Enteros

Los enteros constantes generan números enteros y tienen un paso de 1.

[Se pueden convertir a Float,](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) lo que se recomienda hacer cuando se realiza cualquier operación más compleja que las adiciones, las resta y las comparaciones simples.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo entero](constant.resources/fn-constant-integer.png "Icono de tipo entero")

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

![Integer2 type icon](constant.resources/fn-constant-integer2.png "Integer2 type icon")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entero2</b>

Un nodo Integer2 genera un vector entero estático de 2 componentes con componentes (X, Y).

Un caso de uso común de Integer2 es establecer los tamaños de cuadrícula X e Y, como en el nodo [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer3 type icon](constant.resources/fn-constant-integer3.png "Integer3 type icon")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entero3</b>

Un nodo Integer3 genera un vector entero estático de 3 componentes con componentes (X, Y, Z).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo entero4](constant.resources/fn-constant-integer4.png "Icono de tipo entero4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Entero4</b>

Un nodo Integer4 genera un vector entero estático de 4 componentes con componentes (X, Y, Z, W).

</td>
</tr>
</table>

## Flotantes

Los valores de Flotante constante generan números fraccionarios, es decir, admiten valores después del signo decimal y se pueden ajustar en pasos menores que 1. (Valor predeterminado: 0,01)

[Los valores flotantes se pueden convertir a enteros](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), pero se redondearán hacia arriba o hacia abajo al entero más cercano, lo que significa que se pierden los datos y la precisión.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo flotante](constant.resources/fn-constant-float.png "Icono de tipo flotante")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flotador</b>

Un Flotante tiene un solo componente y se utiliza muy a menudo para cualquier valor individual que requiera precisión.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo Float2](constant.resources/fn-constant-float2.png "Icono de tipo Float2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Un nodo Flotante2 genera un vector de 2 componentes con componentes (X, Y).

Flotante2 se suele usar para [coordenadas de muestreo](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md), [transformaciones de desplazamiento](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md) y manipulación general de vectores 2D.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo Float3](constant.resources/fn-constant-float3.png "Icono de tipo Float3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Un nodo Flotante3 genera un vector de 3 componentes (X, Y, Z).

Flotante3 se usa principalmente para trabajar con objetos 3D y [coordenadas de escala 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), como en [nodos 3D SDF](../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions), y como una forma más sencilla de almacenar colores de RGB, es decir, sin Alpha.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo flotante4](constant.resources/fn-constant-float4.png "Icono de tipo flotante4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Un Flotante4 genera un vector de 4 componentes (X, Y, Z, W).

Flotante4 es la forma preferida de almacenar y establecer información de color donde los valores XYZW se asignan a RGBA, como en el [nodo de Color uniforme](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md).

</td>
</tr>
</table>

## No numérico

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icono de tipo booleano](constant.resources/fn-constant-boolean.png "Icono de tipo booleano")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Booleano</b>

Un valor booleano es el tipo de datos más simple que existe, ya que sólo conoce dos estados: <code>true</code> o <code>false</code>.

Este tipo es bastante común cuando se trabaja con parámetros de alternancia y condiciones [If/Else](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md).<br>Los booleanos son una manera simple y eficiente de controlar el flujo de una función o gráfico, por ejemplo, usando un [nodo de conmutador](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md).

</td>
</tr>
</table>
