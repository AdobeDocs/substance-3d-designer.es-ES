---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface/the-graph-view/node-alignment-tools.html"
breadcrumb-title: ''
description: Utilice las herramientas de alineación de nodos para organizar y alinear los nodos en la vista de gráficos para obtener gráficos más limpios y legibles.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node alignment tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Herramientas de alineación de nodos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 1%

---


# Herramientas de alineación de nodos

![Barra de herramientas de alineación de nodos](node-alignment-tools.resources/node-alignment-tools-01.png "Barra de herramientas de alineación de nodos"){zoomable="yes"}

Las herramientas de alineación de nodos le permiten organizar los nodos en gráficos para mejorar su legibilidad y experiencia de creación. Ofrecen acciones para alinear nodos, distribuirlos uniformemente y ajustarlos a la cuadrícula.

Actúan en los <b>nodos seleccionados actualmente solo</b>.

>[!NOTE]
>
> Mét. abreviados de teclado
> 
> Algunas acciones tienen métodos abreviados de teclado para un acceso rápido: H, V y S. Se muestran entre paréntesis en la siguiente lista de acciones.
> 
> Tenga en cuenta que esto anulará cualquier método abreviado de teclado [asignado a los nodos](../../../interface/preferences-window/preferences-window.md).

## Alineaciones

Los nodos podrán alinearse horizontal y verticalmente, con tres modos para cada eje:

### Alineaciones horizontales

<b>![](node-alignment-tools.resources/node-alignment-tools-02.png) Izquierda:</b> Alinea el lado izquierdo de los nodos seleccionados con el lado izquierdo del nodo más a la izquierda.

<b>![](node-alignment-tools.resources/node-alignment-tools-03.png) Centro (H):</b> Alinea el centro horizontal de los nodos seleccionados con el centro horizontal del cuadro delimitador que los rodea.

<b>![](node-alignment-tools.resources/node-alignment-tools-04.png) Derecha:</b> Alinea el lado derecho de los nodos seleccionados con el lado derecho del nodo más a la derecha.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Herramientas de alineación de nodos: left](node-alignment-tools.resources/node-alignment-tools-05.gif "Herramientas de alineación de nodos: left"){zoomable="yes"}

*Izquierda*

</td>
<td style="border: 0;" valign="top">

![Herramientas de alineación de nodos: center](node-alignment-tools.resources/node-alignment-tools-06.gif "Herramientas de alineación de nodos: centro"){zoomable="yes"}

*Centro*

</td>
<td style="border: 0;" valign="top">

![Herramientas de alineación de nodos: right](node-alignment-tools.resources/node-alignment-tools-07.gif "Herramientas de alineación de nodos: derecho"){zoomable="yes"}

*Derecha*

</td>
</tr>
</table>

### Alineaciones verticales

<b>![](node-alignment-tools.resources/node-alignment-tools-08.png) superior:</b> Alinea el lado superior de los nodos seleccionados con el lado superior del nodo superior.

<b>![](node-alignment-tools.resources/node-alignment-tools-09.png) Medio (V):</b> Alinea el centro vertical de los nodos seleccionados con el centro vertical del cuadro delimitador que los rodea.

<b>![](node-alignment-tools.resources/node-alignment-tools-10.png) Inferior:</b> Alinea el lado inferior de los nodos seleccionados con el lado inferior del nodo inferior.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Herramientas de alineación de nodos: top](node-alignment-tools.resources/node-alignment-tools-11.gif "Herramientas de alineación de nodos: superior"){zoomable="yes"}

*Superior*

</td>
<td style="border: 0;" valign="top">

![Herramientas de alineación de nodos: middle](node-alignment-tools.resources/node-alignment-tools-12.gif "Herramientas de alineación de nodos: central"){zoomable="yes"}

*Medio*

</td>
<td style="border: 0;" valign="top">

![Herramientas de alineación de nodos: bottom](node-alignment-tools.resources/node-alignment-tools-13.gif "Herramientas de alineación de nodos: inferior"){zoomable="yes"}

*Inferior*

</td>
</tr>
</table>

### Apilar

La opción <b>Apilar </b>opción ![](node-alignment-tools.resources/node-alignment-tools-14.png) le permite <b>evitar cualquier superposición</b> al usar alineaciones. Esta opción está activada de forma predeterminada.

Cuando se activa, los nodos se moverán lo más lejos posible a la posición de referencia hasta que colisionen con otro nodo de la selección. Esto los apila de manera efectiva en el eje seleccionado con un margen de una celda de cuadrícula media entre cada nodo.

![Herramientas de alineación de nodos: apilamiento](node-alignment-tools.resources/node-alignment-tools-15.gif "Herramientas de alineación de nodos: apilamiento"){zoomable="yes"}

## Distribuciones

Los nodos se pueden distribuir uniformemente entre los nodos en cada extremo de la selección actual en el eje deseado.

<b>![](node-alignment-tools.resources/node-alignment-tools-16.png) horizontalmente: </b> Los nodos se distribuyen uniformemente entre los nodos izquierdo y derecho de la selección.

<b>![](node-alignment-tools.resources/node-alignment-tools-17.png) verticalmente: </b> Los nodos se distribuyen uniformemente entre los nodos superior e inferior de la selección.

El objetivo de las distribuciones es <b>espaciar incluso</b> entre los nodos, independientemente de su tamaño.

Cuando varios nodos tienen sus centros perfectamente alineados en el eje seleccionado, permanecen y se <b>tratan como uno</b> en la distribución. El *mayor* de los nodos alineados se usa para calcular el espaciado uniforme.

Tenga en cuenta que cuando el tamaño total de los nodos seleccionados es mayor que el espacio disponible en el eje seleccionado, puede producirse una superposición.

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

![Herramientas de alineación de nodos: distribución horizontal](node-alignment-tools.resources/node-alignment-tools-18.gif "Herramientas de alineación de nodos: distribución horizontal"){zoomable="yes"}

*Horizontalmente*

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Herramientas de alineación de nodos: distribución vertical](node-alignment-tools.resources/node-alignment-tools-19.gif "Herramientas de alineación de nodos: distribución vertical"){zoomable="yes"}

*Verticalmente*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

## Ajuste de cuadrícula

La acción <b>Ajustar (S) ![](node-alignment-tools.resources/node-alignment-tools-20.png)</b> mueve cada nodo seleccionado de forma que su esquina superior izquierda se sitúe en el punto más cercano de la cuadrícula media.

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Herramientas de alineación de nodos: ajuste de cuadrícula](node-alignment-tools.resources/node-alignment-tools-21.gif "Herramientas de alineación de nodos: ajuste de cuadrícula"){zoomable="yes"}

</td>
</tr>
</table>
