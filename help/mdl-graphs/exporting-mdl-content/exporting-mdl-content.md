---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exporting-mdl-content.html"
breadcrumb-title: ''
description: Aprenda a exportar contenido MDL desde Substance 3D Designer para utilizarlo en aplicaciones y procesadores externos.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exporting MDL content
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportación de contenido MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 0%

---


# Exportación de contenido MDL

Esta página describe los procesos de exportación relacionados con [gráficos MDL](../../mdl-graphs/mdl-graphs.md) y materiales en Substance 3D Designer.

## Información general

Una vez creado un material MDL en Designer, debe exportarse a un formato que *pueda incluir la definición del material* y ser leído por los procesadores compatibles con MDL. MDL utiliza formatos patentados para llevar definiciones de materiales, denominados módulos MDL, escritos y empaquetados en diferentes formatos que se pueden exportar desde Designer.

>[!NOTE]
>
> Todos estos formatos se pueden abrir directamente con un *editor de texto*, a veces después de desempaquetarlos con un administrador de archivos, para inspeccionar la definición de material que contienen.

## Módulo MDL (\*.mdl)

Este es el formato de archivo de intercambio fundamental para las definiciones de material. Un módulo MDL define lo siguiente:

* las características y el comportamiento del material
* sus parámetros expuestos y valores predeterminados
* sus anotaciones (es decir, metadatos): autor, etiquetas, categorías, ...

La exportación de un módulo MDL se realiza en el nivel de *paquete*. Para exportar un módulo MDL para un paquete determinado, haz clic en el botón ![](../../assets/mdl-export-module-icon.png) <b>Exportar módulo MDL</b> del [Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html) o selecciona esa misma opción en el *menú contextual del paquete*. Seleccione una ubicación de destino y un nombre para el módulo MDL exportado. Se muestra el cuadro de diálogo <b>Informe de exportación</b> con la lista de mensajes registrados durante el proceso de exportación.

El módulo exportado contendrá las definiciones de *todos* los materiales MDL definidos por un [gráfico MDL](../../mdl-graphs/mdl-graphs.md) en el paquete.

>[!NOTE]
>
> Obtenga más información sobre los módulos MDL en las secciones 4 y 15 de la [especificación MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) de NVIDIA.

>[!NOTE]
>
> Advertencias tras esta plantilla: `x appears to be invalid whereas it was expected to be an mdl::call` se deben a la forma en que los materiales MDL se procesan en gráficos MDL y son *seguros de omitir*.

![Ruta de exportación MDL](../../assets/mdl-export-module.png "Ruta de exportación MDL")

*Las rutas del &quot;Módulo Exportar MDL&quot; en el Explorador y el cuadro de diálogo Exportar informe resultante*

### Ajuste preestablecido MDL (\*.mdl)

Un ajuste preestablecido de módulo MDL es prácticamente idéntico al módulo en el que se basa, con la única diferencia de que lleva un conjunto diferente de valores predeterminados: obtenga más información [aquí](https://www.migenius.com/doc/realityserver/latest/resources/general/iray/api_reference/iray/html/classmi_1_1neuraylib_1_1IMdl__factory.html#details).

Un ajuste preestablecido para un material MDL asignado a un material de escena `my_material` se puede exportar desde las siguientes ubicaciones:

* El panel [Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), haciendo clic en <b>RMB</b> en el recurso de gráfico MDL y seleccionando el ajuste preestablecido <b>Exportar...Opción </b> en el menú contextual
* El panel [Vista 3D](../../interface/3d-view/3d-view.md), con el ajuste preestablecido <b>Materiales > mi\_material > Exportar...Opción de menú </b>

La opción de menú abre el cuadro de diálogo <b>Exportar ajuste preestablecido de material MDL</b>, que ofrece las siguientes opciones:

* <b>Directorio</b>: La ubicación de destino a la que se exporta el módulo MDL
* <b>Nombre de archivo MDL</b>: El nombre del módulo MDL.
* <b>Incrustar módulos MDL importados</b>: Si el módulo MDL se basa en módulos importados, es decir, tiene dependencias de módulo, al marcar esta opción, las dependencias de módulo se *incrustan* en el módulo MDL exportado, lo que hace que sea *autosuficiente* a costa del tamaño del archivo y la herencia dinámica

El ajuste preestablecido exportado utilizará los *valores actuales* de los parámetros del material en la vista 3D como los *nuevos valores predeterminados*. Estos valores se pueden modificar mediante la opción <b>Materiales > mi\_material > Editar</b>, que mostrará los parámetros expuestos del material en el panel [Propiedades](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html).

>[!WARNING]
>
> Al exportar un módulo MDL desde el panel [Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), se genera un módulo MDL que contiene *todos* los materiales MDL definidos por un gráfico MDL en el paquete; al exportar un ajuste preestablecido MDL desde [Vista 3D](../../interface/3d-view/3d-view.md), se genera un módulo MDL que contiene *solo* la definición de los materiales MDL aplicados al *material seleccionado* en el menú - `my_material` en este ejemplo.

![Ruta de exportación de ajustes preestablecidos de MDL](../../assets/mdl-export-preset.png "Ruta de exportación de ajustes preestablecidos de MDL")

*La ruta del &quot;ajuste preestablecido de exportación&quot; en la vista 3D y el cuadro de diálogo de ajustes preestablecidos de materiales de exportación MDL resultante*

## Archivo del módulo MDL (\*.mdr)

Un archivo de módulos MDL combina módulos MDL (véase más arriba) con recursos como *texturas* y archivos Léame en un *archivo transportable único*.

La exportación de un archivo de módulo MDL se realiza en el nivel de *paquete*. Para exportar un archivo de módulo MDL para un paquete determinado, haga clic en el botón ![](../../assets/mdl-export-module-icon.png) <b>Exportar archivo de módulo MDL</b> en el [Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html) o seleccione esa misma opción en el *menú contextual del paquete*. Seleccione una ubicación de destino y un nombre para el archivo del módulo MDL exportado y se mostrará el cuadro de diálogo <b>Exportar informe</b> con la lista de mensajes registrados durante el proceso de exportación.

El archivo del módulo exportado contendrá el módulo MDL que contiene las definiciones de *todos* los materiales MDL definidos por un [gráfico MDL](../../mdl-graphs/mdl-graphs.md) en el paquete. Si un [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) se [instala en un gráfico MDL](../../mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md) y se conecta a una secuencia que va al nodo [Root](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md), las texturas que genera se *guardan en el archivo*.

Además de estos elementos, el archivo incluye un archivo <b>MANIFEST</b> que describe los siguientes metadatos para el archivo del módulo MDL:

* `mdl`: la versión de MDL utilizada para exportar el archivo del módulo, por ejemplo, &quot;1.5&quot;
* `version`: la versión del archivo del módulo, por ejemplo, &quot;1.0.0&quot;
* `module`: el nombre del archivo del módulo; por ejemplo, &quot;::pbr\_metallic\_roughness\_basic&quot;
* `exports.material`: el nombre de los materiales definidos en el archivo del módulo, por ejemplo, &quot;::pbr\_metallic\_roughness\_basic::MDL\_graph&quot;

>[!NOTE]
>
> Obtenga más información sobre el formato de archivo de archivo MDL en el Apéndice C de la [Especificación MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) de NVIDIA.

![Ruta de exportación MDR](../../assets/mdl-export-archive.png "Ruta de exportación MDR")

*Las rutas &quot;Exportar archivo del módulo MDL&quot; en el Explorador y el cuadro de diálogo Exportar informe resultante*

## Módulo encapsulado MDL (\*.mdle)

Los gráficos MDL con parámetros expuestos se pueden exportar como materiales MDL encapsulados. La encapsulación *envuelve los datos* en una clase dedicada para que no se pueda tener acceso a los datos *directamente*.

Por ejemplo, aunque puede modificar los valores de los parámetros expuestos para controlar el comportamiento de un material, la *definición* de estos parámetros está *no disponible* en un módulo MDL encapsulado.

La exportación de un módulo MDL encapsulado se realiza en el [Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html) a nivel de gráfico MDL, seleccionando la opción <b>Exportar como .mdle</b> en el menú contextual de un gráfico MDL. Seleccione una ubicación de destino y un nombre para el módulo encapsulado MDL exportado. Se muestra el cuadro de diálogo <b>Informe de exportación</b> con la lista de mensajes registrados durante el proceso de exportación.

*Solo* se incluirá la definición de material para el *gráfico MDL seleccionado* en el módulo MDL encapsulado exportado.

>[!NOTE]
>
> Obtenga más información sobre las definiciones de materiales encapsulados en la sección 13.5 de la [especificación MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) de NVIDIA y la [API SDK MDL](https://raytracing-docs.nvidia.com/mdl/api/mi_neuray_example_mdle.html).

![Ruta de exportación MDLE](../../assets/mdl-export-encapsulated.png "Ruta de exportación MDLE")

*La ruta &quot;Exportar como medio&quot; en el Explorador y el cuadro de diálogo Informe de exportación resultante*
