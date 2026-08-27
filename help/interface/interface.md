---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface.html"
breadcrumb-title: ''
description: Obtenga más información sobre la interfaz del espacio de trabajo de Substance 3D Designer, incluidas las vistas, los paneles y las opciones de personalización.
helpx_creative_field: ""
helpx_description: Designer > Workspace
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Workspace
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 1%

---


# Workspace

El área de trabajo se divide en áreas separadas llamadas <b>muelles</b>, que se pueden [redimensionar, mover y desacoplar](../interface/customizing-your-wor/customizing-your-workspace.md) de la ventana principal de Designer en un muelle flotante.

El diseño de conexión predeterminado de Designer es el siguiente:

![Ventana principal de Substance 3D Designer](../assets/interface-overview.jpg "Ventana principal de Substance 3D Designer")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Menú principal y barra de herramientas <b>1</b>

Explorador de <b>2</b>

Vista de gráfico <b>3</b>

</td>
<td style="border: 0;" valign="top">

Propiedades de <b>4</b>

Vista 2D <b>5</b>

</td>
<td style="border: 0;" valign="top">

Vista 3D <b>6</b>

Biblioteca <b>7</b>

</td>
</tr>
</table>

>[!NOTE]
>
> Escala de interfaz
> 
> Designer adquiere la escala específica de los elementos de la interfaz de usuario *del sistema operativo*. Por lo tanto, cualquier ajuste en la escala de la interfaz de usuario debe realizarse en la configuración de visualización del sistema operativo.
> 
> Para garantizar que la configuración de visualización se aplique correctamente en Designer, *cierre sesión* de la sesión de usuario del sistema operativo y vuelva a iniciar sesión después de cambiar esta configuración.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Menú principal y barra de herramientas

La barra de herramientas principal te permite acceder a menús adicionales, como la [ventana de preferencias](../interface/preferences-window/preferences-window.md) y tiene algunos botones para crear rápidamente un nuevo gráfico y paquete de Substance.

</td>
<td style="border: 0;" valign="top">

![Menú principal y barra de herramientas](../assets/mainmenu-1.png "Menú principal y barra de herramientas")

</td>
</tr>
</table>

* <b>Archivo: </b>Le permite crear nuevos paquetes y recursos, así como guardar y cerrar los paquetes en los que esté trabajando actualmente. Las funciones de este menú también están disponibles como botones rápidos en esta barra de herramientas.
* <b>Editar: </b>Proporciona funciones para deshacer y rehacer (disponibles como botones rápidos a continuación), así como acceso a [Preferencias](../interface/preferences-window/preferences-window.md), para la personalización en profundidad.
* <b>Herramientas:</b> controla el Substance Engine y te permite acceder al Administrador de complementos.
* <b>Windows:</b> Permite ocultar o mostrar cualquiera de las ventanas (algunas están ocultas de forma predeterminada) y permite restablecer el diseño de la ventana a los valores predeterminados.
* <b>Ayuda: </b>Proporciona acceso a información adicional y recursos en línea, como la Academia Substance o este sitio web de documentación.

## Explorer

[La ventana del explorador](the-explorer-window/the-explorer-window.md) es la forma principal de interactuar con cualquier tipo de archivo y recurso. Ofrece más opciones que el menú Archivo de la barra de herramientas principal Aquí es donde se inician y terminan todas las sesiones de trabajo.

![Explorador](../assets/explorer-4.png "Explorador")

## Vista de gráfico

[El conjunto acoplado de la vista de gráfico](../interface/the-graph-view/the-graph-view.md) es la ventana más importante de Substance 3D Designer. Muestra las redes nodales de cualquier tipo de gráfica disponible en Designer ([gráficas de Substance](../compositing-graphs/substance-compositing-graphs.md), [gráficas de funciones de Substance](../function-graphs/function-graphs.md), [gráficas FX-Map](../function-graphs/fxmaps/fxmaps.md)) y le permite crearlas y editarlas.

![Vista de gráfico](../assets/graph-6.png "Vista de gráfico")

## Propiedades

[Properties dock](properties/properties.md) es la ventana más técnica. Siempre es sensible al contexto y presentará reguladores, menús desplegables y otros elementos que cambian el comportamiento de un recurso o nodo seleccionado.

![Propiedades](../assets/properties-15.jpg "Propiedades")

## Vista 2D

[La vista 2D](../interface/2d-view/2d-view.md) es la herramienta de previsualización más sencilla. Trabaja en estrecha colaboración con el Gráfico: al hacer doble clic en cualquier nodo de la vista de gráficos, el resultado visual se mostrará en la vista 2D.

![Vista 2D](../assets/2d-view-1.jpg "Vista 2D")

## Vista 3D

[La vista 3D](../interface/3d-view/3d-view.md) es la ventana de vista previa más interactiva y avanzada. A diferencia de la vista 2D, utiliza varios mapas de salida diferentes para procesar un material completo. Esto significa que verá todos los canales representados, como Color base, Normal y Rugosidad.

![Vista 3D](../assets/3dview-3.jpg "Vista 3D")

## Biblioteca

[El dock de la biblioteca](../interface/the-library/the-library.md) proporciona acceso a todo el contenido incluido en la biblioteca de Designer de forma predeterminada, así como a tu [contenido personalizado](../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md). Para comprender mejor la diferencia entre los nodos atómicos y los nodos de instancia de la biblioteca, asegúrese de leer [Información general sobre nodos](https://helpx.adobe.com/substance-designer/using/nodes-overview.html).

![Biblioteca](../assets/library-3.jpg "Biblioteca")
