---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/get-nodes.html"
breadcrumb-title: ''
description: Acceso Obtén nodos en los gráficos de funciones de Substance 3D Designer para recuperar datos y valores variables.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variables
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 6%

---


# Variables

Las variables son una forma de <b>almacenar valores</b> para buscarlos más tarde (<b>Obtener</b>) o modificarlos (<b>Establecer</b>).

![Substance function graph - Get float](../../../../assets/assign-getfloat.gif "Substance function graph - Get float"){zoomable="yes"}

Lo que hace un nodo Get esencialmente es capturar una variable dinámica y devolverla de la salida de los nodos Get para utilizarla en una función. Estos nodos Get forman el vínculo entre los parámetros de entrada definidos en los [parámetros de gráfico](../../../../compositing-graphs/graph-parameters/graph-parameters.md) y las [funciones de parámetro](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).

Cada vez que utilice un nodo Get, debe elegir un valor disponible en el menú desplegable. Los nodos de obtención <b>tomarán un valor del tipo correspondiente</b>. Eso significa que solo verá opciones válidas en el menú de un nodo Get, nunca podrá elegir una opción no válida. Si una variable no está disponible, significa que el tipo no coincide

Hay un número de <b> variables de &quot;sistema&quot;</b>: variables especiales predefinidas que no se pueden declarar. Estos son muy importantes, y para los nodos a continuación se enumera qué variables del sistema están disponibles.

Cuando un parámetro está [expuesto](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), consiste en aplicarle una función de parámetro que solo incluye un nodo Get del tipo correcto.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Obtener

</td>
<td style="border: 0;" valign="top">

### Establecer

</td>
<td style="border: 0;" valign="top">

### Está definido

</td>
</tr>
</table>

## Obtener

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Obtener float2 - Icono](../../../../assets/fn_variables_getfloat2.png "Obtener float2 - Icono"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Estos nodos permiten obtener el valor de una variable que existe *en el ámbito actual*.

El nombre de la variable que se va a obtener se establece en el conjunto acoplado Propiedades.

</td>
</tr>
</table>

&#39;Obtener&#39; nodos algunas limitaciones que debe tener en cuenta:

* <b>Se escriben</b>, por lo que debe asegurarse de que la variable contiene un valor del mismo tipo que el nodo. Los desajustes de tipo se notifican en la Console.
* <b>No comprueban la existencia de la variable</b> en el ámbito actual. Las variables no encontradas se registran en la Console.
* En funciones complejas que utilizan nodos de flujo de control como Secuencia, tenga en cuenta el <b>orden en el que se establecen y obtienen las variables</b>. Cuando Designer detecta un caso de &quot;Obtener antes de establecer&quot;, se informa de él en la Consola.

>[!NOTE]
>
> Variables incorporadas
> 
> Varios nodos &#39;Get&#39; ofrecerán variables integradas para acceder a los valores existentes de acuerdo con el contexto actual, por ejemplo: la posición de píxel actual en un procesador de píxeles, el modo de mosaico actual de un nodo, ...
> 
> Todas las variables integradas se enumeran en [esta página dedicada](../../../../function-graphs/variables/system-variables/system-variables.md).

### Obtener nodos

+++Flotantes
![Obtener float - Icono](../../../../assets/fn_variables_getfloat.png "Obtener float - Icono"){width="200px"}



Obtener flotante

![Obtener float2 - Icono](../../../../assets/fn_variables_getfloat2.png "Obtener float2 - Icono"){width="200px"}



Obtener flotante 2

![Obtener float3 - Icono](../../../../assets/fn_variables_getfloat3.png "Obtener float3 - Icono"){width="200px"}



Obtener flotante 3

![Obtener float4 - Icono](../../../../assets/fn_variables_getfloat4.png "Obtener float4 - Icono"){width="200px"}



Obtener flotante 4

+++

+++Enteros
![Obtener entero - Icono](../../../../assets/fn_variables_getint.png "Obtener entero - Icono"){width="200px"}



Obtener entero

![Obtener entero2 - Icono](../../../../assets/fn_variables_getint2.png "Obtener entero2 - Icono"){width="200px"}



Obtener entero 2

![Obtener entero3 - Icono](../../../../assets/fn_variables_getint3.png "Obtener entero3 - Icono"){width="200px"}



Obtener entero 3

![Obtener entero4 - Icono](../../../../assets/fn_variables_getint4.png "Obtener entero4 - Icono"){width="200px"}



Obtener entero 4

+++

+++Otros
![Obtener booleano - Icono](../../../../assets/fn_variables_getboolean.png "Obtener booleano - Icono"){width="200px"}



Obtener booleano

![Obtener cadena - Icono](../../../../assets/fn_variables_getstring.png "Obtener cadena - Icono"){width="200px"}



Obtener cadena

+++

## Establecer

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Conjunto: Icono de nodo](../../../../assets/fn_variables_set.png "Establecer: Icono de nodo"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Texto

</td>
</tr>
</table>

## Está definido

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![&#x200B; está definido: El icono de nodo](../../../../assets/fn_variables_isdefined.png " está definido: Icono de nodo"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Texto

</td>
</tr>
</table>
