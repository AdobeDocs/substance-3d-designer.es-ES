---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/warnings-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Conozca las advertencias en los Substance que componen gráficos y aprenda a resolver problemas y errores comunes.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Warnings in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Advertencias en los gráficos de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 1%

---


# Advertencias en los gráficos de Substance

Esta página muestra mensajes de advertencias y errores que pueden activar [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) en Substance 3D Designer, y ofrece pasos comunes de solución de problemas para cada uno.

Las advertencias se muestran en la información sobre herramientas del icono de advertencia para el recurso de gráfico en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md), así como en la esquina inferior izquierda de la [vista de gráfico](../../interface/the-graph-view/the-graph-view.md) si el gráfico está cargado.

## ![(error)](warnings-in-substance-compositing-graphs.resources/error.svg) No se ha definido ningún nodo de salida

El gráfico no tiene un nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md).

**![(marca)](warnings-in-substance-compositing-graphs.resources/check.svg) Solución**

Agregue uno o más nodos [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) al gráfico y conéctele el resultado del último nodo de una secuencia.

>[!NOTE]
>
> Las plantillas de gráficos disponibles en el cuadro de diálogo [Nuevo gráfico](../creating-compositing-gra/creating-a-substance-compositing-graph.md) tienen nodos de salida preestablecidos listos para usarse.

![Solucionar advertencia &#39;No se definió ningún nodo de salida&#39;](warnings-in-substance-compositing-graphs.resources/warnings-comp-output.gif "Solucionar advertencia &#39;No se definió ningún nodo de salida&#39;"){width="512px"}

### ![(error)](warnings-in-substance-compositing-graphs.resources/error.svg) La función del parámetro *[x]* tiene algunas advertencias

El [gráfico de funciones](../../function-graphs/function-graphs.md) aplicado al parámetro especificado del nodo especificado tiene al menos una advertencia.\
El parámetro node se especifica entre corchetes después de la etiqueta del nodo, siguiendo la plantilla Node[Parameter].

E.g. Color uniforme[Color de salida], Procesador de píxeles[Función por píxel]

**![(marca)](warnings-in-substance-compositing-graphs.resources/check.svg) Solución**

Localice el nodo que emite la advertencia por su etiqueta e insignia de advertencia en la [vista Gráfica](../../interface/the-graph-view/the-graph-view.md) y, a continuación, selecciónelo para mostrar sus propiedades en el panel [Propiedades](../../interface/properties/properties.md). Busque el parámetro que emite la advertencia y abra su función haciendo clic en el botón **Editar función**.

A continuación, evalúe las advertencias que aparecen en la esquina inferior izquierda de la vista de gráfico y resuelva los problemas. Puede consultar la página [Advertencias en gráficos de funciones](../../function-graphs/warnings-function-graphs/warnings-in-function-graphs.md) para obtener información sobre advertencias de solución de problemas en gráficos de funciones.

![Solucionar error &#39;La función de parámetro tiene algunas advertencias&#39; advertencia](warnings-in-substance-compositing-graphs.resources/warnings-comp-param-function.gif "Solucionar error &#39;La función de parámetro tiene algunas advertencias&#39; advertencia")

### ![(error)](warnings-in-substance-compositing-graphs.resources/error.svg) Los datos a los que se hace referencia tienen algunas advertencias

El recurso al que hace referencia un nodo tiene una o más advertencias. Estos son algunos nodos que hacen referencia a un recurso:

* Un nodo [graph instance](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) hace referencia a un gráfico
* Un nodo [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) hace referencia a un [recurso Bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* Un nodo [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) hace referencia a un [recurso SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* Un nodo [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) hace referencia a un [recurso Font](../../resources/font-resource/font-resource.md)

**![(marca)](warnings-in-substance-compositing-graphs.resources/check.svg) Solución**

En el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md), busque el recurso al que se hace referencia y solucione todas las advertencias provocadas por el recurso:

* Para gráficos, consulte otros elementos de esta página
* Para cualquier otro tipo de recurso, consulte la página [Advertencias de las dependencias](../../resources/warnings-from-dep/warnings-from-dependencies.md)

![Solucionar error &#39;Los datos de referencia tienen algunas advertencias&#39; advertencia](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-data.gif "Solucionar error &#39;Los datos de referencia tienen algunas advertencias&#39; advertencia")

### No se encontró el recurso de referencia ![(error)](warnings-in-substance-compositing-graphs.resources/error.svg)

No se encontró el recurso al que hace referencia un nodo en la ruta guardada en el archivo [Substance 3D](https://www.adobe.com/es/products/substance3d/3d-augmented-reality.html) (SBS). Estos son algunos nodos que hacen referencia a un recurso:

* Un nodo [graph instance](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) hace referencia a un gráfico
* Un nodo [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) hace referencia a un [recurso Bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* Un nodo [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) hace referencia a un [recurso SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* Un nodo [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) hace referencia a un [recurso Font](../../resources/font-resource/font-resource.md)

**![(marca)](warnings-in-substance-compositing-graphs.resources/check.svg) Solución**

Para nodos [graph instance](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)

Compruebe que el gráfico de origen existe en el paquete ubicado en la ruta guardada en su atributo **Package**.\
Si no es así, elimine el nodo de instancia y sustitúyalo por un nodo de instancia que haga referencia a un paquete válido. Como alternativa, puede volver a crear el paquete y el gráfico al que hace referencia el nodo de la instancia y luego volver a cargar el paquete host haciendo clic en RMB en él en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md) y seleccionando la opción **Volver a cargar** en el menú contextual.

Para los nodos [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md), [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) o [Texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

Busque los recursos a los que se hace referencia en el panel Explorador y compruebe que existen en la ubicación guardada en su atributo **Ruta de archivo**.\
Si no lo hacen, haga clic en RMB en el elemento de recurso en el Explorador y seleccione **Reubicar...Opción** en el menú contextual para establecer un nuevo archivo de destino válido para ese recurso.

![Solucionar advertencia de &quot;Recurso de referencia no encontrado&quot;](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-resource.gif "Solucionar advertencia de &quot;Recurso de referencia no encontrado&quot;")

### ![(error)](warnings-in-substance-compositing-graphs.resources/error.svg) El nodo de texto usa una fuente no válida

Un nodo [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) hace referencia a una fuente que no se puede cargar o analizar correctamente.

<b>![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Solución</b>

Seleccione el nodo [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) y tome nota del valor de su propiedad <b>Font</b>. Busca el archivo de origen de esa fuente en tu sistema y asegúrate de que esté *en buen estado*, por ejemplo, usándola en otra aplicación como un editor de texto. Reemplace la fuente por un archivo de fuente saludable según sea necesario o cambie el nodo Texto a otra fuente.
