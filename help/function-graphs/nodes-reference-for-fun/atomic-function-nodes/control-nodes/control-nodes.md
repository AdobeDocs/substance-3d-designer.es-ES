---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/control-nodes.html"
breadcrumb-title: ''
description: Acceso a nodos de control en gráficos de funciones de Substance 3D Designer para controlar la lógica de flujo y ejecución.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Control
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 1%

---


# Nodos de control

Esta página describe nodos de [Gráficos de funciones](../../../../function-graphs/the-function-graph/the-function-graph.md) cuyo propósito es controlar el *flujo de ejecución*.

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo If...Else](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/IfElse_Node.jpg "Nodo If...Else")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## If...Else

De forma similar a los lenguajes de programación, el... El nodo Else introduce la posibilidad de filtrar el resultado según condiciones predefinidas.

</td>
</tr>
</table>

Utilizará este nodo junto con los [nodos lógicos](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) y los [nodos de comparación](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) que le ayudarán a generar la condición que desea comprobar.

+++Conectores de entrada
<b>Condición</b> *Booleano*\
Condición que controla el resultado del nodo.

<b>Si</b> *Tipo de variable* El valor de salida del nodo si <b>Condition</b> es *True*.

<b>Else</b> *Tipo de variable* El valor de salida del nodo si <b>Condition</b> es *False*.

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo de secuencia](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/Sequence_Node.jpg "Nodo de secuencia")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Secuencia

Garantiza que una parte del gráfico se calcule antes que otra.

</td>
</tr>
</table>

Esto es fundamental para controlar el estado de las variables, ya que se crean, leen y actualizan.

Puede obtener más información sobre el nodo Sequence en la página [Uso de los nodos Set/Sequence](../../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) de esta documentación.

+++Conectores de entrada
<b>En</b> *Tipo de variable*\
La parte del gráfico que se debe calcular primero

<b>Último</b> *Tipo de variable*\
La parte del gráfico que se debe calcular en último lugar

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo de bucle entero](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/WhileLoop-Node.jpg "Nodo Bucle entero")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## While Loop

Ejecuta la bifurcación <b>Init</b> una vez y, a continuación, itera sobre el <b>Cond. de salida</b> y <b>Loop Body</b> se bifurca hasta que <b>Exit Cond.</b> branch devuelve *True*.

Una vez completado el bucle, el nodo genera el resultado de la última iteración del <b>Cuerpo de bucle</b>.

</td>
</tr>
</table>

Los bucles tienen un número máximo de iteraciones implícitas que se pueden deshabilitar definiéndolo en -1.

Las variables conservan su valor en todas las iteraciones y se puede acceder a ellas en la condición de salida (Exit Cond.).\
Esto significa que puede añadir a un valor de índice cada iteración y comprobar su valor en la condición de salida para controlar el número de bucles que necesita.

>[!IMPORTANT]
>
> Nodos conectados al <b>Id. de salida</b> y las ramas <b>Loop Body</b> no se pueden conectar a otras ramas del gráfico.

+++Conectores de entrada
<b>Init.</b> *Tipo de variable*\
La parte del gráfico que se calcula antes de la primera iteración, es decir, el inicio del bucle.

<b>Cond. de salida</b> *Booleano*\
La condición que debe ser verdadera para que se detenga el bucle. Se recalcula en cada iteración.\
*Nota:* El número máximo de iteraciones sigue limitado al parámetro <b>Máximo de iteraciones</b>.

<b>Cuerpo de bucle</b> *Tipo de variable*\
El gráfico que se beneficia del bucle. Se recalcula en cada iteración.

+++

+++Parámetros
<b>Máx. iteraciones</b> *Entero*\
Número máximo de iteraciones realizadas por el nodo.\
El nodo deja de iterar cuando se cumple primero cualquiera de los siguientes criterios: se alcanza este número máximo o se cumple la condición de salida .\
Este máximo se puede deshabilitar estableciendo el valor en *-1*. En ese punto, solo la condición de salida puede detener las iteraciones.

Estableciendo &#39;Máx. iteraciones&#39; a -1 mejora el rendimiento en bucles pequeños, ya que hay un contador menos para realizar el seguimiento y actualizar.

Sin embargo, tenga en cuenta cómo está configurado el nodo, ya que es posible producir un <b>bucle infinito</b> que puede hacer que Designer deje de responder.

+++

Eche un vistazo a este tutorial sobre el nodo While Loop:
