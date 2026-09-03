---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: Usa instancias y subgráficos de gráficos para crear componentes de gráficos reutilizables y flujos de trabajo de materiales modulares.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Instancias y subgráficos de gráficos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# Instancias y subgráficos de gráficos

![](graph-instances-sub-graphs.resources/graph-instances-sub-graphs-01.png)

Las instancias de gráficos son nodos que <b>hacen referencia a otro gráfico</b>. Un gráfico al que hace referencia un nodo de instancia en un gráfico de host puede denominarse <b>subgráfico</b> del gráfico de host.

El uso de instancias hace que un gráfico sea reutilizable muchas veces en uno o más gráficos, incluso en diferentes paquetes.

## ¿Por qué debería utilizar instancias de gráficos?

<b>Dividir gráficos en varios subgráficos</b> te permite trabajar *mucho* de manera más eficiente<b>.</b>

Cada vez que esté duplicando una cadena de nodos en Designer, probablemente podría dividirla en un subgráfico para que sea más fácil reutilizarla y actualizarla.

>[!NOTE]
>
> En la sección [Gráficos de Substance de muestra](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) de esta documentación hay disponible un archivo de proyecto que muestra una configuración simple de un subgráfico para un filtro *personalizado*.

### ¿Cómo se crea una instancia de gráfico?

Arrastre un gráfico A desde el Explorador a otro gráfico B para crear un <b>nodo de instancia</b> que haga referencia al gráfico A.

Los nodos se pueden dividir rápidamente en un nuevo gráfico al seleccionar los nodos y utilizar la opción &quot;Crear gráfico a partir de la selección&quot; del menú contextual. A continuación, se le pedirá que defina el identificador del nuevo gráfico, que debe ser único.

Tenga en cuenta que si los nodos seleccionados estuvieran conectados a otros nodos del gráfico, también debe crear nodos [Input](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) y [Output](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) en el nuevo gráfico para transferir estas conexiones al subgráfico.

Además, la sustitución de los nodos originales por un nodo de instancia que haga referencia al nuevo gráfico se debe realizar manualmente posteriormente.

Por último, debe decidir si el subgráfico debe exponerse a los usuarios cuando publique su proyecto en un archivo SBSAR compartible. Consulte el parámetro &#39;Exposed in SBSAR&#39; en las [propiedades del gráfico](../../../compositing-graphs/graph-parameters/graph-parameters.md).

### Una palabra sobre la herencia

Otra ventaja de usar subgráficos es que cada instancia de un subgráfico puede <b>adaptarse al contexto</b> en el que se usa. En otras palabras, dos instancias de un mismo gráfico pueden tener diferentes resoluciones de salida, profundidades de bits y modos de mosaico.

Este es un <b>concepto esencial</b> del trabajo en Substance y te recomendamos que obtengas más información sobre la [herencia en gráficos de gráficos](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) cuando estés listo para seguir adelante con las instancias.

Tenga en cuenta que, aunque los conceptos de instancia de gráfica y subgráfico también se aplican a las gráficas de funciones de Substance, la herencia, tal y como se describe en esa página, sólo se aplica a las gráficas de Substance.

### ¿Puedo añadir mis propias instancias de gráficos a la biblioteca de nodos?

<b>Sí, es posible </b>, pero requiere una configuración específica. Obtén más información en la página [Administración de contenido y filtros personalizados](../../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) de esta documentación.

### ¿Se puede inspeccionar el gráfico de origen de una instancia de gráfico?

![(marca)](graph-instances-sub-graphs.resources/check.svg) Sí y *solo* para instancias de gráficos cargados desde un **archivo Substance 3D (SBS)**. Estos nodos de instancia tienen una etiqueta *rojo oscuro*.\
Haga clic con el botón derecho en el nodo para abrir su menú contextual y seleccione la opción **Abrir referencia**.

>[!NOTE]
>
> Al inspeccionar el gráfico de origen, puede utilizar los datos de entrada del gráfico de la instancia si la opción **Edición en contexto** está *marcada* en la sección **Gráfico** de [Preferencias](../../../interface/preferences-window/preferences-window.md).

![(menos)](graph-instances-sub-graphs.resources/forbidden.svg) *No* es posible inspeccionar gráficos cargados desde **instancias de recurso de Substance 3D (SBSAR)**, ya que ya están compiladas. Solo puede cargar el recurso en el panel **Explorador** para inspeccionar la lista de gráficos expuestos y sus parámetros. Estos nodos de instancia tienen una etiqueta *green*.\
Haga clic con el botón derecho en el nodo para abrir su menú contextual y seleccione la opción **Cargar paquete**.

>[!NOTE]
>
> **Nodos atómicos**
> 
> Los nodos *Atomic* se implementan directamente a través del código en el motor del Substance y son *no* instancias de gráficas, de ahí el nombre atomic: son los *bloques de construcción más pequeños* para *todos* los demás nodos en [gráficos de Substance](../../../compositing-graphs/substance-compositing-graphs.md).
