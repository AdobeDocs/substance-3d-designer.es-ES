---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Añada comentarios a los gráficos de Substance 3D Designer para documentar el flujo de trabajo y explicar las conexiones de nodos.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Comentario
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# Comentario

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Icono de comentario](../../../../assets/graphatomic-comment_1.png "Icono de comentario")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Un comentario es simplemente un fragmento de texto flotante que se puede colocar en cualquier parte de un gráfico.

Está pensado para anotar y explicar partes de un gráfico. Su propiedad <b>Description</b> contiene el texto que se muestra.

</td>
</tr>
</table>

>[!NOTE]
>
> Los comentarios tienen saltos de línea automáticos que intentan minimizar su huella en un gráfico.

## Creación de comentarios

El tipo predeterminado de comentario se coloca independientemente de los nodos del gráfico.

Se puede crear de las siguientes maneras:

+++Menú Nodo
Presione <b>Barra espaciadora</b> en la vista Gráfica para abrir el <b>menú Nodo</b> y seleccione el elemento Comentario en la lista.

Escriba &quot;comentario&quot; en el campo de búsqueda para que aparezca el elemento y lo encuentre más rápidamente.

+++

+++Método abreviado
Si hay un método abreviado de teclado asignado al elemento &quot;Comentario&quot; en [Preferencias](../../../../interface/preferences-window/preferences-window.md), presione ese método abreviado cuando la vista de gráficos esté seleccionada.

+++

+++Menú contextual
En la vista de gráficos, presione <b>RMB</b> en cualquier objeto o en espacio vacío y seleccione la opción <b>Agregar comentario</b>.

+++

+++Barra de herramientas de gráficos
En la barra de herramientas de la vista de gráficos, haz clic en el botón &quot;Comentario&quot; en la <b>Paleta de nodos</b>.

+++

+++Biblioteca
En la biblioteca, seleccione la categoría <b>Elementos de gráfico</b> y, a continuación, arrastre y suelte el elemento &#39;Comentario&#39; en la vista de gráfico.

+++

>[!TIP]
>
> Cuando se crea un comentario, su propiedad &#39;Description&#39; adquiere el enfoque automáticamente para que pueda editar inmediatamente el texto del comentario.

## Comentarios de los padres

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Un comentario de elemento primario es un comentario *asociado a un nodo específico* en el gráfico para que, cuando se mueva el nodo, le siga el comentario y, cuando se elimine el nodo, se elimine el comentario junto con él.

Los comentarios que se crean cuando se selecciona actualmente un *nodo único*, o a través del menú contextual de un solo nodo, se asignan a ese nodo como elemento primario.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Comentarios: Comentarios de los padres](../../../../assets/graph-comment_parented.gif "Comentarios: Comentarios de los padres")

</td>
</tr>
</table>

## formato de HTML

Se puede dar formato al texto mediante etiquetas de HTML. Este formato se activa y desactiva mediante el botón ![](../../../../assets/graph-frames_html-markup-button.png) <b>marcado de HTML</b> en la propiedad <b>Description</b> del comentario.

>[!TIP]
>
> Obtenga más información sobre esta característica en la sección <b>Descripción</b> de la documentación de [Marcos](../../../../interface/the-graph-view/graph-items/frame/frame.md).

![Comentarios: Marcado de HTML](../../../../assets/graph-comment_html-markup.gif "Comentarios: Marcado de HTML")
