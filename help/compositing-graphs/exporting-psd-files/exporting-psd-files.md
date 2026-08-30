---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/exporting-psd-files.html"
breadcrumb-title: ''
description: Aprenda a exportar Substance que componen gráficos como archivos de PSD para su uso en Adobe Photoshop y otros flujos de trabajo de edición de imágenes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting PSD files
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportación de archivos PSD
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---


# Exportación de archivos PSD

Substance 3D Designer permite exportar texturas a un documento de Adobe Photoshop o a un archivo de PSD.Esta página explica la interfaz especial utilizada para convertir los nodos de un gráfico en capas.**Este proceso no es automático: tiene mucho control, pero es limitado y a menudo no es posible obtener una coincidencia exacta entre nodos y capas.** Además, no se garantiza que el PSD contenga las mismas salidas que el gráfico, a menos que se configure explícitamente para ello. En general, cuanto más preciso y correcto desea ser, más esfuerzo necesita del usuario. En general, lo único que se puede replicar de forma no destructiva es [Fusionar nodos](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Las capas de ajuste no son compatibles, como tampoco lo son los estilos de capa o cualquier otra cosa más allá de los modos de fusión de capa.

[Substance 3D Designer también puede exportar a archivos de mapa de bits.](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

## Cuadro de diálogo Exportar de PSD

El cuadro de diálogo Exportar PSD solo se puede abrir con un método. En la [vista de gráfico](../../interface/the-graph-view/the-graph-view.md) del gráfico que deseas exportar a PSD, haz clic en el botón ![](exporting-psd-files.resources/image2019-9-17-14-44-17.png) <b>Herramientas</b> y selecciona <b>Exportador de PSD</b>. La interfaz se hace visible en <b>Graph View</b>.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Interfaz de usuario del exportador PSD](exporting-psd-files.resources/psd-dialog.png "Interfaz de usuario del exportador PSD")

</td>
<td style="border: 0;" valign="top">

1. <b>Nombre de archivo y ubicación:</b> configure la carpeta y el nombre de archivo para la exportación aquí. Pulse el botón Exportar para realizar el proceso de exportación.
1. <b>Agregar grupo:</b> Agrega un grupo de capas
1. <b>Lista desplegable Agregar capa:</b> elija uno de los dos métodos para agregar una capa. Las capas también se pueden agregar *arrastrando nodos con el botón secundario del mouse* a la pila.
1. <b>Quitar capa desplegable:</b> quita las capas seleccionadas o todas las capas.
1. <b>Layerstack:</b> es el trabajo de configuración más frecuente si se realiza aquí. La interfaz refleja las opciones limitadas en Photoshop. Configure aquí el nombre de la capa, el modo de fusión y la opacidad. Si una capa tiene dos miniaturas, la segunda miniatura representa el canal del Alpha.

</td>
</tr>
</table>

## Flujo de trabajo

Como Photoshop no admite directamente materiales de varias salidas, hay varias formas de configurar el PSD. A continuación se muestra un resumen del método más común.

* Configure varias carpetas para todos los resultados. Una carpeta para Basecolor, una para Normal, una para Rugosidad, etc.
* Con el botón derecho del ratón, arrastre y suelte los resultados en el grupo adecuado. Si quieres mantener las cosas simples, el PSD puede quedarse solo en esto.
* Para expandir más el PSD: vuelva a trabajar a la izquierda del gráfico y suelte los pasos intermedios relevantes del gráfico en el grupo adecuado. No será posible compartir capas entre salidas o grupos.

En el raro caso de que el PSD sea el resultado más importante, puede crear el gráfico de modo que solo utilice los modos de fusión. En ese caso, debería ser posible volver a crear una versión más editable del gráfico como un documento con capas.
