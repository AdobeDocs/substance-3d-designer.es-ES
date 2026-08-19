---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface/the-graph-view/graph-items/dot-node.html"
breadcrumb-title: ''
description: Utilice nodos de puntos y nodos de portal en Substance 3D Designer para crear puntos de conexión y organizar el flujo de gráficos.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nodo de punto (también Portal)
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---


# Nodo de punto (también Portal)

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Icono de nodo de punto](../../../../assets/graphatomic-dot_1.png "Icono de nodo de punto")

</td>
<td width="100.00%" style="border: 0;" valign="top">

El nodo <b>Dot</b> es un ayudante que te permite simplificar y limpiar gráficos redireccionando y agrupando conexiones. Resulta especialmente útil para gráficos con muchas conexiones largas que se ejecutan sobre otras conexiones o nodos.

Un par de nodos Dot se pueden usar como <b>portales</b> para ocultar una conexión que se extiende a larga distancia, o en lugares donde el enrutamiento de la conexión sería difícil.

</td>
</tr>
</table>

## Creación de nodos Punto

Los nodos de punto se pueden añadir en cualquier tipo de gráfico, de cualquiera de las siguientes maneras:

+++Insertar en vínculo
Mantenga presionada la tecla <b>Alt</b> mientras pasa el ratón sobre una conexión para mostrar la vista previa del nodo Punto y, a continuación, haga clic en LMB para agregar un nodo Punto en la conexión de esa ubicación.

![Insertando un nodo de punto](../../../../assets/dot-node-insert-optim.gif "Insertando un nodo de punto"){width="512px"}



+++

+++Conector de nodo
Presione la tecla <b>Alt</b> mientras arrastra una nueva conexión desde un conector de nodo para insertar un nodo Punto en esa ubicación.

Puede continuar arrastrando la nueva conexión y repetir la operación para enrutar esa conexión como desee.

![Punto: Creando desde el conector](../../../../assets/graph-dot_create-from-connector.gif "Punto: Creando desde el conector")



+++

+++Menú Nodo
Presione <b>Barra espaciadora</b> para mostrar el <b>menú Nodo</b> y, a continuación, seleccione el elemento &quot;Punto&quot; o escriba &quot;punto&quot; en el campo de búsqueda para que aparezca el elemento y lo encuentre más rápidamente.

![Nodo punto en el menú Nodo](../../../../assets/dot-node-insert-menu.png "Nodo punto en el menú Nodo")



+++

>[!TIP]
>
> Cuando se crea un nodo de punto, su propiedad &#39;Name&#39; adquiere el enfoque automáticamente para que pueda editar inmediatamente el nombre del nodo.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Combinación de vínculos

Presione ALT y mueva un nodo Punto sobre los vínculos para combinar conexiones de varios nodos.

</td>
<td style="border: 0;" valign="top">

![Combinando vínculos](../../../../assets/dot-node-congrenate-links-optim.gif "Combinando vínculos"){width="512px"}

</td>
</tr>
</table>

## Portales

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Nodo de punto como portal - icono](../../../../assets/DotNode_Portal-1.png "Nodo de punto como portal - icono")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Los nodos de puntos se pueden usar como <b>portales</b> para enviar datos a una larga distancia en el gráfico sin tener un enlace largo y engorroso que perjudique la legibilidad. Esto oculta de forma efectiva el vínculo entre los nodos Dot.

</td>
</tr>
</table>

![Nodo de punto como portal](../../../../assets/DotNode_Portal.gif "Nodo de punto como portal")

### Creación de portales

Se crea automáticamente un portal entre dos nodos Punto (un transmisor y un receptor) cuando se denomina el nodo Punto transmisor. Para asignar un nombre a un nodo de punto, se establece un identificador único en su propiedad <b>Name</b>.

Cuando en un gráfico existen uno o más nodos Punto con nombre, cualquier nodo Punto se puede conectar a él como receptor mediante:

* Crear un enlace entre la entrada del receptor y la salida de un transmisor;
* Seleccionando el nombre del transmisor en la propiedad <b>Portal de entrada</b> del receptor.

La duplicación o copia de receptores mantiene su conexión al transmisor como un portal.

### Identificación de portales

Los nodos de puntos utilizados como portales tienen un icono de señal inalámbrica situado junto al conector utilizado como portal.

Al seleccionar cualquier nodo de punto utilizado como portal, se muestran sus conexiones ocultas a otros portales como una línea discontinua.

### Eliminación de portales

Un portal se elimina cuando se borra el <b>Nombre</b> del transmisor, o cuando se borra la conexión oculta:

* Seleccionar un portal, seleccionar la conexión oculta y eliminarla;
* Seleccionando el receptor y presionando el botón <b>X</b> junto al menú desplegable <b>Portal de entrada</b> en las propiedades.

>[!IMPORTANT]
>
> El uso de nodos de puntos como portales no se admite en [gráficos FX-Map](../../../../function-graphs/fxmaps/fxmaps.md).

Eche un vistazo a este tutorial sobre los nodos Punto como portales:
