---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/exporting-bitmaps.html"
breadcrumb-title: ''
description: Aprenda a exportar texturas y mapas de bits desde Substance que componen gráficos para utilizarlos en aplicaciones y flujos de trabajo externos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting Bitmaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportación de mapas de bits
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# Exportación de mapas de bits

Esta página explica cómo Substance 3D Designer puede exportar varios formatos de archivo de mapa de bits y cómo exportar varios mosaicos UV por lotes.Si desea [exportar a archivos de PSD](../exporting-psd-files/exporting-psd-files.md), hay una página dedicada independiente para esto.

![Exportación simplificada](exporting-bitmaps.resources/exportflow.png "Exportación simplificada")

## Exportación de conceptos

Conviene tener en cuenta lo siguiente al exportar un mapa de bits:

* Usted<b> exporta desde un gráfico</b>, no desde un paquete. Un paquete no genera contenido de imagen por sí mismo.
* El número (y la resolución) de mapas de bits exportados viene determinado por las <b>salidas</b> de un gráfico.
* Filetype se establece para todos los mapas de bits/salidas.
* La exportación es diferente de la [publicación](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md), asegúrate de que entiendes bien la diferencia.

## Métodos de exportación

Una vez que esté listo para exportar, hay dos formas de acceder al cuadro de diálogo Exportar:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

En la ventana [Explorador](../../interface/the-explorer-window/the-explorer-window.md), haga clic con el botón derecho en el gráfico que desea exportar y seleccione **&quot;Exportar salidas como mapas de bits&quot;**

![](exporting-bitmaps.resources/export-explorer.gif)

</td>
<td style="border: 0;" valign="top">

En la [vista de gráficos](../../interface/the-graph-view/the-graph-view.md), haciendo clic en el botón Herramientas ![](exporting-bitmaps.resources/image2019-9-17-14-44-17.png) y eligiendo **&quot;Exportar salidas...&quot;**

![](exporting-bitmaps.resources/export-graph.gif)

</td>
</tr>
</table>

## Cuadro de diálogo Exportar

El cuadro de diálogo Exportar le presenta algunas opciones para personalizar su exportación.

La versión que se muestra a la derecha es el cuadro de diálogo estándar; el cambio de resolución se produce en el gráfico, en las salidas o definiendo la resolución principal antes de abrir el cuadro de diálogo.

1. <b>Destino: </b>ubicación para guardar todos los archivos.
1. <b>Formato:</b> tipo de archivo usado para todos los archivos exportados.
1. <b>Patrón</b>: método genérico para generar tipos de archivo basados en palabras clave de metadatos. A continuación, se muestra un ejemplo de nombre de archivo basado en el primer resultado, para su verificación.\
   A continuación se muestran todas las opciones disponibles:
   1. *$(graph)* - nombre del gráfico actual
   1. *$(identificador)*: identificador del resultado actual
   1. *$(description)*: descripción del resultado actual
   1. *$(label)*: etiqueta del resultado actual
   1. *$(user\_data)*: datos de usuario personalizados del resultado actual
   1. *$(group)*: grupo de salida del resultado actual
   1. *$(espacio de color)*: espacio de color de la salida actual (solo disponible para *OCIO* y *Adobe ACE* [administración de color](../../color-management/color-management.md) modos)
1. <b>Salidas:</b> Active o desactive salidas y grupos de salida específicos de su gráfico. Los botones activan o desactivan todo. Resulta útil cuando sólo ha cambiado un mapa de bits.
1. <b>Exportación automática:</b> Botón de alternancia para habilitar la reexportación automática de salidas de gráficos tan pronto como se realice un cambio. Solo para el gráfico actual. Puede ser pesado y lento dependiendo de la configuración.
1. <b>Botón de exportación:</b> Exporta con la configuración actual o cierra el cuadro de diálogo.

![Cuadro de diálogo Exportar salidas](exporting-bitmaps.resources/fromgraph-1.png "Cuadro de diálogo Exportar salidas")

## Cuadro de diálogo Exportar (mosaicos por lotes/UV)

Cuando se trabaja con mallas de mosaico UV en Designer, el cuadro de diálogo Exportar se puede utilizar de una forma ligeramente diferente que permita la exportación por lotes de varios mosaicos UV a la vez. Asegúrate de que entiendes este flujo de trabajo y has asignado correctamente un [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) a uno o más mosaicos UV.\
La ficha por lotes también es una forma más rápida de exportar el gráfico a una resolución diferente a la resolución de trabajo (principal).

Inicie el cuadro de diálogo con los mismos métodos detallados anteriormente, simplemente asegúrese de hacer clic con el botón derecho en *en el gráfico asignado a UV-Tile en el Explorador*, o de que ha *abierto el gráfico asignado a UV-Tile* específico en la vista Gráfico al utilizar el botón Herramientas.

1. <b>Pestaña Lote</b>: Asegúrate de seleccionar esta pestaña en lugar del método estándar <b>Desde el gráfico </b>; de lo contrario, las opciones 2-3 no estarán disponibles.
1. <b>Mosaicos UV:</b> Al igual que con las salidas, le permite activar o desactivar la exportación de mosaicos UV específicos.
1. <b>[Tamaño de salida](../../compositing-graphs/output-size/output-size.md): </b>Anule la resolución de exportación, lo que le permite trabajar de forma más pequeña y eficiente al exportar a tamaño máximo.

![Cuadro de diálogo Resultados de exportación por lotes](exporting-bitmaps.resources/batch.png "Cuadro de diálogo Resultados de exportación por lotes")
