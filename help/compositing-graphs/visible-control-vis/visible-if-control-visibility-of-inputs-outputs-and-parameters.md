---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/visible-if-control-visibility-of-inputs-outputs-and-parameters.html"
breadcrumb-title: ''
description: Aprenda a utilizar expresiones visibles if en Substance 3D Designer para controlar la visibilidad de los parámetros en función de las condiciones.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Visible if expressions
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visible si las expresiones
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1511dc8cc9a91529359172ad81cd2c1c0606448f
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# Visible si las expresiones

La expresión &#39;Visible if&#39; le permite <b>controlar la visibilidad</b> de las entradas, salidas y parámetros en los gráficos.

Al [exponer parámetros](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), es posible que desee ocultar o mostrar parámetros o conectores de nodo en función del estado de otros parámetros. Por ejemplo, un control deslizante solo se muestra cuando un botón de parámetro booleano está establecido en `true`, porque de lo contrario no tendría ningún efecto y eso podría confundir a los usuarios.

Para ello, puede introducir una *expresión lógica* en la propiedad <b>Visible if</b> de:

* [parámetro de entrada](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) de un gráfico;
* un nodo [Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) de gráfico;
* el nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) de un gráfico.

![Cambiar la visibilidad del parámetro de entrada](../../assets/visible-if-example.gif "Cambiar la visibilidad del parámetro de entrada"){width="512px"}

Si la expresión lógica se evalúa como `true`, el parámetro, entrada o salida se muestra en todos los [nodos de instancia](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) que representan el gráfico actual. De lo contrario, está *oculto*.

Son posibles condiciones complejas, siempre que sea válida la expresión lógica en la que se indican dichas condiciones.

>[!NOTE]
>
> Cavidades
> 
> * Esta característica *solo* afecta a si un parámetro o conector se muestra en la interfaz de usuario, y no tiene *ningún efecto* en los cálculos y el resultado de un gráfico.
> * Al exponer o aplicar una función a cualquier parámetro utilizado en instrucciones &#39;Visible if&#39;, esas instrucciones se *omitirán* y se establecerán de forma predeterminada en &#39;true&#39;.

>[!IMPORTANT]
>
> Aunque esta funcionalidad funciona dentro del ecosistema de Substance 3D, es posible que algunas integraciones no la admitan. Si no se admite, la condición de visibilidad se establece de forma predeterminada en `true`.

## Escribir expresiones &#39;Visible if&#39;

### ACCESO A PARÁMETROS DE ENTRADA

Cualquier expresión visible si necesita utilizar al menos una entrada, se puede realizar mediante la siguiente sintaxis:

```
input.identifier 

input["identifier"]
```


>[!WARNING]
>
> El **identificador** debe ser el nombre *exacto* de la propiedad **Identificador** de un parámetro de entrada existente y debe escribirse *distingue entre mayúsculas y minúsculas*. *no puede* hacer referencia a un parámetro mediante su etiqueta.\
>  Si no existe un parámetro al que se hace referencia o la expresión lógica no es válida, se muestra una *advertencia* en la propiedad **Visible if**.

### OPERADORES DISPONIBLES

Los campos &quot;Visible if&quot; aceptan los siguientes parámetros:

* Entradas booleanas, flotantes y enteras.
* Valores de `true` y `false` (distingue mayúsculas de minúsculas, sin mayúsculas)
* `.x` : acceder al subparámetro
* `&&`<b> </b>: y
* `||`<b> </b>: o
* `!`<b> </b>: no
* `<`<b>, </b>`>`<b>, </b>`<=`<b>, </b>`>=`<b>, </b>`==`<b>, </b>`!=` : comparación
* `()` : paréntesis

### DEBE EVALUARSE SIEMPRE A BOOLEANOS

Una expresión Visible If se usa como condición para una instrucción &quot;IF&quot;, lo que significa que siempre debe dar como resultado `true` o `false`.

* Los valores booleanos pueden evaluarse directamente como condición. Un botón simple con un valor booleano no requiere más de esto. Véanse los ejemplos siguientes, primer caso;
* Los parámetros no booleanos generalmente requieren una operación *comparison*. Consulte los operadores de comparación, a continuación para ver algunos ejemplos;
* Algunos valores no booleanos pueden ser *true* o *false*, lo que significa que pueden evaluarse como `true` de `false`, p. ej. un valor entero de `0` se evalúa como false.

## Ejemplos

| Condición (&quot;Si&quot;) | Fórmula | Nota |
| --- | --- | --- |
| True | ` input["my_input"]   input.my_input `  ` input["my_input"] == true   input.my_input == true ` | my\_input es un valor booleano |
| False | ` !input["my_input"]   !input.my_input `  ` input["my_input"] == false   input.my_input == false `  ` input["my_input"] != true   input.my_input != true ` | my\_input es un valor booleano |
| Menor que | ` input["my_input"] < 3   input.my_input < 3 ` | my\_input es un valor entero |
| Igual | ` input["param1"] == 2   input.param1 == 2 ` | param1 es un valor flotante o entero |
| Menor que | ` input["my_input"].y < 3   input.my_input.y < 3 ` | my\_input es un valor flotante o entero con uno o más componentes, por ejemplo, float2(x, y), integer3(x, y, z) |
| O | ` input["param1"] \|\| input["param2"]   input.param1 \|\| input.param2 ` | param1 y param2 son valores booleanos |
| Y | ` input["param1"] > 0 && input["param2"] > 1   input.param1 > 0 && input.param2 > 1 ` | param1 y param2 son valores flotantes o enteros |
