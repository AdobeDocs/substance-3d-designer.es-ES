---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/main-mdl-graph-concepts.html"
breadcrumb-title: ''
description: Aprenda los conceptos principales de los gráficos de Lenguaje de definición de material en Substance 3D Designer para la creación de materiales.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Main MDL graph concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conceptos principales de gráficos MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---


# Conceptos principales de gráficos MDL

Esta página presenta los conceptos principales *específicos* a [gráficos MDL](../../mdl-graphs/mdl-graphs.md) y debe entenderse bien para aprovechar al máximo este tipo de gráficos en Substance 3D Designer.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Iray

Los materiales MDL utilizan una descripción pensada para soluciones de representación basadas en la física, que admite el procesador [Iray](../../interface/3d-view/iray/iray.md) incrustado en Designer. Por lo tanto, para mostrar el resultado de un gráfico MDL *, es necesario seleccionar el procesador de Iray* en un panel [3D view](../../interface/3d-view/3d-view.md) activo.

</td>
<td style="border: 0;" valign="top">

[![Logotipo de NVIDIA Iray](main-mdl-graph-concepts.resources/iray-logo.jpg)](https://www.nvidia.com/en-us/design-visualization/iray/)

</td>
</tr>
</table>

Al crear o cargar un gráfico MDL, el primer panel de vista 3D [desanclado](../../interface/customizing-your-wor/customizing-your-workspace.md) encontrado por Designer *cambiará automáticamente* al procesador [Iray](../../interface/3d-view/iray/iray.md). Si no hay ninguna vista 3D disponible, se creará un *nuevo* panel de vista 3D y se cambiará al procesador de Iray para alojar el procesamiento del material MDL que se está editando.

Cuando el procesador de Iray está seleccionado en un panel de vista 3D, el menú Materiales de ese panel le permite cambiar entre los materiales MDL disponibles, que incluyen los materiales cargados en el panel Explorador y los materiales en la biblioteca MDL de Designer. Obtén más información sobre cómo trabajar con materiales MDL en Iray en la sección [Iray](../../interface/3d-view/iray/iray.md) de esta documentación.

## Nodo raíz

El resultado de un gráfico MDL está definido por el nodo <b>Root</b>. Cualquier nodo del gráfico se puede establecer como raíz siempre que sus datos de salida sean del tipo <b>material</b>, es decir, una *definición de material*. Un gráfico MDL puede tener *solo un nodo raíz*.

Por lo general, un nodo que se puede establecer como raíz puede ser *autosuficiente*, ya que ya contiene una definición de material que se puede personalizar pasando datos a sus *entradas*.\
Por ejemplo, si desea trabajar en un material similar al cristal, puede que desee utilizar una definición de material de cristal como nodo raíz como punto de partida, pero eso no es *obligatorio*. Muchos nodos de material son templados que pueden ser convertidos en cualquier material complejo usando la extensa lista de nodos MDL.

El nodo raíz incluye una miniatura que muestra una vista previa de su resultado actual.

![Nodo raíz del gráfico MDL](main-mdl-graph-concepts.resources/mdl-root-hl.png "Nodo raíz del gráfico MDL")

*Nodo raíz en un gráfico MDL y sus propiedades se muestran en el [panel de propiedades](../../interface/properties/properties.md)**4&rbrace;*

## Conectores y tipos

Dado que hay muchos más tipos de datos en los gráficos MDL que en otros gráficos de Designer, puede que presencie apariencias únicas de conectores de nodos. A continuación se enumeran los conceptos importantes que se deben comprender.

Forma Conector

La forma *del conector* indica si el tipo de datos es *uniforme* (círculo) o *variable* (cuadrado).

&quot;Una variable de un tipo uniforme sólo se puede establecer en un valor uniforme. Una variable de un tipo variable se puede establecer en un valor variable así como en un valor uniforme. El valor resultante en la variable siempre se considera variable&quot;. (Fuente: Sección 6.3 de la [especificación MDL](https://raytracing-docs.nvidia.com/mdl/specification/MDL_spec_1.7.2_17Jan2022.pdf))

A continuación se muestran algunos ejemplos:

* una muestra de <b>Texture</b> es *variable*, ya que los valores se ven afectados por el píxel muestreado
* un valor <b>Color</b> es *uniforme*, ya que se pasa por igual independientemente del contexto
* un <b>BRDF</b> es *variable*, ya que los valores se ven afectados por el ángulo de incidencia
* un valor <b>Float</b> o <b>Boolean</b> es *uniforme*, ya que se pasa por igual independientemente del contexto

Color del conector

El *tipo de datos* que va desde un conector de salida o que espera un conector de entrada tiene un código de color y se muestra entre paréntesis después del identificador/etiqueta al pasar el conector con el mouse (ratón).

>[!WARNING]
>
> Solo los conectores de *tipos de datos coincidentes* se pueden vincular entre sí. El único propósito del código de colores es aumentar la legibilidad con respecto al tipo de datos que se pasan en el gráfico y a qué conectores se pueden vincular.

![Tipos de conector de nodo MDL](main-mdl-graph-concepts.resources/mdl-connector-types.png "Tipos de conector de nodo MDL"){width="512px"}

*El aspecto de los conectores varía según el tipo de valor de E/S, que se muestra entre paréntesis después del identificador de E/S*

## Creación de nodos filtrados

Puedes añadir cualquier nodo disponible en la categoría <b>mdl</b> de la <b>Biblioteca</b> en el gráfico *arrastrando el nodo* desde la <b>vista de biblioteca</b> a la <b>vista de gráfico</b>, o presionando la <b>barra espaciadora</b> para abrir el menú <b>Nodo</b> en la vista de gráfico cuando *no hay nada seleccionado*. En este caso, se muestra una lista de nodos *sin filtrar*.

Sin embargo, hay casos en los que la lista de nodos del menú Nodo se filtra para mostrar únicamente los nodos del tipo de datos coincidente para la entrada o salida de destino:

* si se ha seleccionado *node* en la vista Gráfico y se presiona <b>la barra espaciadora</b>
* si hace clic en <b>LMB</b>, mantiene presionado y *arrastra* un vínculo fuera de un *conector de nodo*

Es posible que desee tener en cuenta las *reglas* aplicadas para el filtrado:

* si se muestra el menú Nodo presionando <b>barra espaciadora</b> cuando se selecciona un *nodo único*, la lista incluye nodos donde el tipo de datos de la *primera entrada* coincide con el tipo de datos de *salida* del nodo seleccionado
* si se muestra el menú Nodo presionando <b>barra espaciadora</b> cuando se seleccionan *varios* nodos, la lista incluye nodos donde el tipo de datos de la *primera entrada* coincide con el tipo de datos *salida* del *último nodo seleccionado*
* si se muestra el menú Nodo *arrastrando un vínculo* fuera de un conector *output*, la lista incluye nodos donde el tipo de datos de *primera entrada* coincide con el tipo de datos de *salida* seleccionado
* si se muestra el menú Nodo *arrastrando un vínculo* fuera de un conector *input*, la lista incluye nodos donde el tipo de datos de *output* coincide con el tipo de datos *selected input*

![Creación de nodo filtrado](main-mdl-graph-concepts.resources/mdl-filtered-node-creation.gif "Creación de nodo filtrado")

*Creación de nodos filtrados en el gráfico MDL, observe que la lista cambia según el tipo de valor del conector*

## Entradas y texturas de gráficos

Los materiales MDL pueden recibir datos de fuentes externas, en forma de valores y texturas, por ejemplo. Esto se consigue <b>exponiendo un nodo</b>, a diferencia del [gráfico del Substance](../../compositing-graphs/substance-compositing-graphs.md), donde existen nodos de entrada dedicados para este propósito.

Los datos se pueden pasar al nodo expuesto según su *tipo*. Por ejemplo, los valores de Flotante se pueden pasar a un nodo <b>float</b> expuesto, y una textura se puede pasar a un nodo <b>color</b> expuesto (en este caso, los valores RGBA del píxel muestreado se pasan como un valor de color).

![Entradas de gráficos expuestos](main-mdl-graph-concepts.resources/mdl-graph-inputs-samplers.png "Entradas de gráficos expuestos")

*Los nodos expuestos crean entradas gráficas que son tanto entradas de valor sin formato como muestras para las texturas*
