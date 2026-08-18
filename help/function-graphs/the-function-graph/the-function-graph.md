---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/the-function-graph.html"
breadcrumb-title: ''
description: Obtenga más información sobre los gráficos de funciones de Substance en Designer para crear funciones personalizadas y redes de nodos reutilizables.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs > The Substance function graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gráfico de funciones del Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Similitudes con una gráfica de Substance

A primera vista, el gráfico de funciones del Substance es muy similar a un gráfico del Substance y el flujo de trabajo es casi el mismo.

![Gráfico de funciones de Substance](../../assets/image2015-12-18-11-29-28.png "Gráfico de funciones de Substance")

## La navegación es similar

En el gráfico de funciones Substance, puede crear y organizar los nodos del mismo modo que lo haría en un gráfico Substance.

puede acceder a los nodos de la misma manera:

* Desde la biblioteca
* pulsando la barra espaciadora o la tecla Tab
* haciendo clic con el botón derecho y utilizando el menú Agregar nodo

### El flujo de trabajo es similar

Como en el gráfico Substance, construirá su función encadenando series de nodos, cada uno de ellos usando el resultado generado por el (los) anterior(es).

El resultado definirá el valor de un parámetro o el resultado del nodo del procesador de píxeles.

## Diferencias con una gráfica de Substance

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Los nodos

Los nodos disponibles en el gráfico de funciones del Substance son completamente diferentes de los que encontraría en un gráfico del Substance.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![lista de nodos del gráfico de funciones del Substance](../../assets/image2015-12-18-13-46-55.png "lista de nodos del gráfico de funciones del Substance")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### El resultado

A diferencia de los Substance, una función sólo puede tener una salida.

Otro punto a tener en cuenta es que no hay un nodo de salida específico donde se conecte el resultado final. En su lugar, puede marcar directamente como salida, el nodo que genera el resultado esperado:

</td>
<td style="border: 0;" valign="top">

![nodo de salida del gráfico de funciones de Substance](../../assets/image2015-12-18-13-49-43.png "nodo de salida del gráfico de funciones de Substance")

</td>
</tr>
</table>

#### ¿Cómo se define el nodo de salida?

Para definir la salida, haga clic con el botón derecho en el nodo que genera la salida esperada y haga clic en *Establecer como nodo de salida:*

![Definiendo el nodo de salida](../../assets/setoutputnode.gif "Definiendo el nodo de salida")

>[!WARNING]
>
> <b>Compruebe dos veces el tipo de resultado generado</b>
> 
> Si observa que *Establecer como nodo de salida* está atenuado, significa que el valor generado por el nodo es diferente del valor esperado por el parámetro o el procesador de píxeles.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

En cuanto a los Substance, puede importar funciones realizadas en otro gráfico. Para abrir el gráfico de referencia, haga clic con el botón derecho en él y seleccione &quot;Abrir referencia&quot;:

</td>
<td style="border: 0;" valign="top">

![Gráfico de funciones de Substance con referencia abierta](../../assets/image2017-6-27-10-44-55.png "Gráfico de funciones de Substance con referencia abierta")

</td>
</tr>
</table>

Si tiene un subgráfico que contiene varias funciones, puede arrastrarlo y soltarlo directamente en un gráfico de funciones de Substance y elegir la función que desea importar en la lista que aparece:

![Eliminar gráfico de funciones del Substance del paquete](../../assets/sbsdrag.gif "Eliminar gráfico de funciones del Substance del paquete")
