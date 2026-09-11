---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/overview.html"
breadcrumb-title: ''
description: Obtén una visión general de Substance 3D Designer y descubre sus funciones para crear texturas y materiales de procedimientos.
helpx_creative_field: ""
helpx_description: Designer > Getting started > Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Información general
user-guide-description: ''
user-guide-title: ''
source-git-commit: baf36ab85717512cc9e52d67d00293eabb5ebcf6
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 2%

---


# Información general

[Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) es una aplicación diseñada para crear texturas, materiales y filtros 2D en una interfaz basada en nodos, con especial atención en la generación de procedimientos, la parametrización y los flujos de trabajo no destructivos. Se trata de la aplicación de mayor duración del ecosistema de Substance 3D y los recursos creados con ella son los más versátiles y dinámicos posibles.

Así es como se compara con otras aplicaciones:

|  | <div><img alt="Icono de Substance 3D Sampler" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c1_position_position-par_image_713298714" src="overview.resources/sa-appicon-noshadow-256.png" title="Icono de Substance 3D Sampler" width="64px"/></div>  Substance 3D Sampler | <div><img alt="Icono de Substance 3D Painter" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c2_position_position-par_image" src="overview.resources/pt-appicon-noshadow-256.png" width="64px"/></div>  Substance 3D Painter | <div><img alt="Icono de Substance 3D Designer" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c3_position_position-par_image" src="overview.resources/ds-appicon-noshadow-256.png" title="Icono de Substance 3D Designer" width="64px"/></div>  Substance 3D Designer |
| --- | --- | --- | --- |
| <b>Curva de aprendizaje</b> | Bajo | Medio | Alto |
| <b>Materiales de autor</b> | Sí | Sí | Sí |
| <b>Crear modelos 3D</b> | No | Limitada\* | Limitada\* |
| <b>Crea filtros, patrones y efectos</b> | No | Limitado | Sí |
| <b>Exportar contenido paramétrico</b> | No | No | Sí |

\*: Solo para desplazamiento, consulte la función <b>Exportación de escenas</b> en la sección [Vista 3D](../../interface/3d-view/3d-view.md).

En resumen, Substance 3D Designer debe considerarse la aplicación de texturizado más técnica y avanzada disponible.

Permite crear contenido para casi cualquier caso de uso o escenario. Esto significa que no está limitado a un solo tipo de salida, como un material único/conjunto de texturas para una malla mapeada por UV, sino que puede crear contenido para un conjunto mucho más amplio de usos.

Por ejemplo, la mayor parte del contenido inteligente y de procedimiento de Painter y Sampler se creó y exportó desde Designer. Cosas como Alpha de pinceles, generadores, filtros y Materiales base se pueden crear en Designer.

## Flujo de trabajo

Substance 3D Designer es un editor basado en nodos que le permite crear contenido de muchas maneras diferentes con diferentes complejidades. [El flujo de trabajo se explica con más detalle en páginas dedicadas](../../getting-started/workflow-overview/workflow-overview.md), pero las siguientes son las ventajas de trabajar con el software:

<b>[No lineal](../../compositing-graphs/substance-compositing-graphs.md) </b>: puede crear multitud de salidas de textura a la vez. Edite una máscara o un regulador y se volverá a calcular automáticamente cualquier salida conectada. Ya no es necesario crear por separado mapas como Color base, Rugosidad, Normal, etc.

<b>[No destructivo](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) </b>: puedes revertir cualquier acción *sin que* pierda tu trabajo. Se vuelve mucho más rápido iterar y experimentar, y encontrar flujos de trabajo aún más eficientes.

<b>[Horneado integrado](../../bakers/bakers.md) </b>: accede a herramientas avanzadas de cocción de malla de alta velocidad directamente dentro del software. Ya no es necesario realizar el procesamiento en un software independiente y realizar largos procesos de importación y exportación.

<b>[Paramétrico](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) </b>: puedes configurarlo para que controle casi cualquier aspecto de una textura con un solo regulador o menú desplegable. Esto te permite añadir un control y una variación interminables a un solo activo.

## Tipos de archivo

La aplicación y su ecosistema utilizan 4 tipos de archivo diferentes. Para ser claros: estos son tipos de archivo <b>exportados desde Substance 3D Designer</b> que se pueden importar en algunas o en todas las demás aplicaciones de Substance 3D.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](overview.resources/ds-sbs-48.png)

### Archivo de Substance 3D

*(\*.SBS)*

Los archivos de Substance son los **archivos de origen principales** para Designer. Al abrir un archivo de Substance, puede **ver y editar todos los nodos de un gráfico**. Se representan como paquetes, que pueden contener cualquier número de recursos como Gráficos, Funciones, Mapas de bits, Mallas, etc... Son más difíciles de compartir y menos rápidos de calcular. Solo se pueden abrir en Substance 3D Designer y el Substance Player.

</td>
<td style="border: 0;" valign="top">

![](overview.resources/sbsar-48.png)

### Activo de Substance 3D

*(\*.SBSAR)*

Los archivos de Substance son<b> archivos de Substance compilados y optimizados</b>. Son mucho más rápidos de calcular y se pueden compartir fácilmente sin problemas de referencia. Los parámetros aún se pueden modificar, pero la edición del gráfico está <b>bloqueada</b>. Substance Archives se puede usar en todas las aplicaciones de Substance 3D y en cualquier aplicación que tenga [Substance 3D integration](https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/home) (algunas con un plugin externo) como Autodesk 3DS Max &amp; Maya, Unreal Engine o Unity Engine.

</td>
<td style="border: 0;" valign="top">

![](overview.resources/bmp-96.png){width="48px"}

### Archivos estáticos

*(\*.TGA, \*.BMP, \*.PNG, \*.FBX, \*.OBJ, etc...)*

Substance 3D Designer siempre admite la exportación a tipos de archivo estáticos. Una imagen 2D se puede exportar a un archivo de mapa de bits, mientras que un modelo 3D se puede exportar a tipos de archivo 3D comunes. Al exportar a archivos estáticos, **se pierde toda la funcionalidad dinámica**. Las imágenes están bloqueadas en resolución, los modelos 3D están bloqueados en el polirecuento.

</td>
</tr>
</table>

Esto generalmente significa que mantendrá su trabajo en formato SBS cuando trabaje dentro de Designer, exportará a SBSAR si el destino lo admite (Painter por ejemplo) o utilizará archivos de mapa de bits estáticos si no hay necesidad o no hay soporte para SBSAR.

## Tipos de recursos

Los archivos de Substance 3D pueden contener una gran variedad de recursos que sirven para diferentes propósitos. Algunos recursos solo se pueden crear dentro de Designer, algunos provendrán de aplicaciones externas.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](overview.resources/graph-5.png){width="150px"}](../../compositing-graphs/substance-compositing-graphs.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Gráficos de Substance

Los gráficos de Substance permiten generar y procesar *datos de imagen 2D* y, a continuación, generarlos en una o más salidas de textura. En muchos casos de uso, un proyecto girará en torno a uno o varios gráficos de Substance.

[Vaya a la sección dedicada a los gráficos de Substance.](../../compositing-graphs/substance-compositing-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](overview.resources/function-1.png){width="150px"}](../../function-graphs/function-graphs.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Gráficas de funciones de Substance

<b>Las funciones</b> tienen un nivel superior de abstracción y complejidad: en lugar de procesar datos de imagen (conjuntos de valores de píxeles), *procesa valores individuales* (enteros, flotantes, vectores). Las funciones se utilizan cuando se desea realizar operaciones más complicadas o si se desea ajustar comportamientos específicos. Las funciones no suelen funcionar de forma independiente y no se utilizan fuera del contexto de los gráficos de Substance.

[Vaya a la sección dedicada a las gráficas de funciones de Substance.](../../function-graphs/function-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](overview.resources/folder-4.png){width="150px"}](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Recursos que no son gráficos

Los recursos que no son gráficos pueden provenir de aplicaciones externas (como Photoshop o Autodesk Maya), mientras que algunos también se pueden *crear dentro de Designer*. La principal diferencia es que no son gráficos basados en nodos; la mayoría de ellos son elementos que deben utilizarse dentro o junto a los tipos de gráfica mencionados anteriormente.

Existen los siguientes tipos de recursos:

* [Mapa de bits](../../resources/bitmap-resource/bitmap-resource.md)
* [Gráficos vectoriales (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [Escenas 3D](../../resources/3d-scene-resource/3d-scene-resource.md)
* [Fuentes](../../resources/font-resource/font-resource.md)
* [Archivos AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)

</td>
</tr>
</table>
