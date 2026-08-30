---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/technical-issues/warnings-and-errors.html"
breadcrumb-title: ''
description: Encuentre soluciones a errores y advertencias comunes en Substance 3D Designer para solucionar problemas rápidamente.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Warnings and errors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Advertencias y errores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 4%

---


# Advertencias y errores

Esta página explica los informes de advertencias y mensajes de error que pueden aparecer en [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html), y los vínculos a advertencias y solución de problemas basados en su origen.

## Información general

Al trabajar en proyectos en Designer, pueden aparecer advertencias y mensajes de error que le notifican de un problema en el proyecto:

* **Las advertencias** se muestran en *texto amarillo* y señalan a tu atención un problema que puede dar lugar a un resultado no deseado debido a la falta de entrada o a una configuración incorrecta. Normalmente *no bloquean* tu trabajo.
* Los **errores** se muestran en texto *rojo* y denotan un cálculo erróneo, un resultado inesperado o la incapacidad de realizar una tarea. Suelen *bloquear* tu trabajo.

Por lo general, las advertencias y los errores se muestran en el elemento que los activó y *aparecen en cada elemento primario* de ese elemento. A continuación se muestra una lista de lugares comunes donde se notifican advertencias y errores:

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Explorer

Para cualquier elemento del panel [Explorer](../../interface/the-explorer-window/the-explorer-window.md) que tenga una advertencia, dicha advertencia se muestra con un icono ![](warnings-and-errors.resources/warning-icon.png) en el extremo derecho de la entrada del elemento en la lista. Deje el cursor sobre ese icono durante unos segundos para mostrar una *información sobre herramientas* que enumere todas las advertencias en detalle.

Siguen estas reglas:

* Si el elemento está anidado bajo cualquier otro elemento (p. ej., una carpeta), aparecen advertencias a ese elemento si está contraído.
* Las listas de advertencias son *cumulativas*, ya que son la suma de las advertencias de un elemento *y* todas las advertencias que aparecen de sus elementos secundarios.
* Todas las advertencias notificadas por el contenido de un paquete aparecen en el elemento *package* y se agregan a las *advertencias propias* del paquete.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warning-overview-explorer.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Vista de gráfico

Para cualquier elemento del panel [Graph view](../../interface/the-graph-view/the-graph-view.md) que tenga una advertencia, dicha advertencia se muestra con texto en color en la *esquina inferior izquierda* de la ventana gráfica. Si la advertencia la desencadena un nodo específico, dicho nodo tendrá un distintivo de advertencia ![](warnings-and-errors.resources/warning-badge.png). Deje el cursor en esa insignia durante unos segundos para mostrar una *información sobre herramientas* que enumere todas las advertencias en detalle.

Siguen estas reglas:

* Si un gráfico de origen *creado mediante instancia* en cualquier otro gráfico de host tiene una o más advertencias, el [nodo de instancia](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) de ese gráfico de origen tendrá una advertencia *única* de `The referenced data has some warnings`.
* Las listas de advertencias son *cumulativas*, ya que son la suma de las advertencias del gráfico *y* todas las advertencias de sus nodos secundarios.
* Todas las advertencias de un gráfico aparecen en el elemento que representa ese gráfico en el panel Explorador.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warning-overview-graph.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Propiedades

Para cualquier elemento del panel [Properties](../../interface/properties/properties.md) que tenga una advertencia, dicha advertencia se muestra con un icono ![](warnings-and-errors.resources/warning-icon.png) en el extremo derecho de la entrada del elemento en la lista. Deje el cursor sobre ese icono durante unos segundos para mostrar una *información sobre herramientas* que enumere todas las advertencias en detalle.

Siguen estas reglas:

* Si el elemento está anidado bajo cualquier otro elemento (p. ej., un encabezado de sección), aparecen advertencias a ese elemento si está contraído.
* Las listas de advertencias son *cumulativas*, ya que son la suma de las advertencias de un elemento *y* todas las advertencias que aparecen de sus elementos secundarios.
* Si el [gráfico de funciones](../../function-graphs/function-graphs.md) aplicado a un [parámetro de entrada](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) tiene una o más advertencias, el elemento del parámetro tendrá una *advertencia única de* `The [x] parameter's function has some warnings`.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warning-overview-properties.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Consola

Se informa tanto de advertencias como de errores en el panel **Consola**, al que puedes acceder a través del menú **Windows** en el [menú principal](../../interface/the-main-toolbar/the-main-toolbar.md). Puede aislar advertencias y errores del resto de las entradas de la consola estableciendo la configuración de **Canal** en `ErrorMgr`.

>[!NOTE]
>
> Dado que todo el texto de la consola es *seleccionable*, puedes usar este panel para *copiar fácilmente advertencias y mensajes de error* y pegarlos en la herramienta **Búsqueda local** de esta documentación o en cualquier motor de búsqueda de Internet. Esto acelera la búsqueda de instrucciones para solucionar problemas.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warning-overview-console.png){width="256px"}

</td>
</tr>
</table>

### Mensajes con &quot;(# veces)&quot;

En la *advertencia o error* se desencadenó *más de una vez* en un elemento *y* en cualquiera de sus elementos secundarios, estas advertencias se *combinarán en uno* y aparecerá el sufijo `(# times)`, lo que te permite saber cuántas veces se notificó esta advertencia o error.

## Categorías

A continuación se muestra una lista de advertencias y errores que puede encontrar en Designer, ordenados según su origen. Los títulos de las categorías están vinculados a su página dedicada, que ofrece explicaciones y guías de solución de problemas para resolver cada problema.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Advertencias en los gráficos de Substance

* No se ha definido ningún nodo de salida
* La función del parámetro `[x]` tiene algunas advertencias
* Los datos a los que se hace referencia tienen algunas advertencias
* Recurso de referencia no encontrado
* El nodo de texto utiliza una fuente no válida

</td>
<td style="border: 0;" valign="top">

### Advertencias en los gráficos de funciones

* No se ha definido ningún nodo de salida
* El nodo de salida actual devuelve un valor de tipo x
* Algunos nodos Get no tienen un nombre de variable
* Algunos nodos Set no tienen un nombre de variable

</td>
</tr>
</table>

### Advertencias de dependencias

* Paquete dependiente no válido
* Compruebe que el alias &quot;x&quot; está definido en el proyecto
* No se encuentra ningún archivo que coincida con este recurso
* Archivo vinculado no encontrado
* Espacio de color no encontrado
* Recurso de referencia no encontrado
* Los mosaicos UV se asignan varias veces
* Mosaicos UV no válidos
