---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/working-with-3d-scenes.html"
breadcrumb-title: ""
description: Aprenda a importar, editar y trabajar con escenas 3D en Substance 3D Designer para previsualizar y probar sus materiales.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trabajo con escenas 3D
user-guide-description: ""
user-guide-title: ""
source-git-commit: b1404a9f03e3156f5fba0e499bbe41dbc79b7308
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 0%
---

# Trabajo con escenas 3D

![Trabajo con escenas 3D](working-with-3d-scenes.resources/workingWith3DScenes.png "Trabajo con escenas 3D"){zoomable="yes"}

Designer te permite cargar [escenas 3D](../glossary/glossary.md) para trabajar con materiales en contexto. Puede encontrar una lista de formatos de archivo compatibles con escenas 3D aquí, incluida una lista de funciones compatibles con cada formato. <b>&lt;vínculo necesario></b>

Trabajar en contexto implica [reemplazar](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) uno de los [materiales](../glossary/glossary.md) de la escena para reemplazarlo por un material creado en Designer.\
Puedes empezar desde cero utilizando cualquiera de las plantillas de gráficos de Substance disponibles en Designer o [extraer valores y texturas](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md) del material de la escena 3D como punto de partida.

Cuando hayas terminado con la escena 3D, puedes [exportarla](../working-with-3d-scenes/exporting-scenes/exporting-scenes.md) a un nuevo archivo para que se incorpore a otra aplicación.

Al exportar a formatos USD, este flujo de trabajo puede ser completamente <b>no destructivo</b>, lo que significa que solo se exportan las ediciones y adiciones.

En primer lugar, debe cargar una escena 3D para trabajar en ella y poder conservar su estado en Designer en todas las sesiones.

## Contenido de las escenas 3D

Al cargar una escena 3D, Designer creó su propia escena para alojarla.

Puede interactuar con el siguiente contenido de la escena:

* <b>Materiales:</b> todos los materiales utilizados en la escena se pueden [reemplazar](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) con una copia creada por Designer. Puedes editar las [propiedades de material](../interface/3d-view/material-properties/material-properties.md) de esa copia, con valores o texturas sin procesar de un gráfico de Substance.
* <b>Mallas:</b> la geometría se puede seleccionar directamente en la ventana gráfica o desde el [explorador de escenas](../interface/3d-view/scene-browser/scene-browser.md), para acceder a sus acciones materiales ([override](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), [reset](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), [extract to Substance graph](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md))
* <b>Luces:</b> todas las luces de la escena se pueden deshabilitar en el [Explorador de escenas](../interface/3d-view/scene-browser/scene-browser.md).
* <b>Cámaras:</b> cualquier cámara detectada en la escena se agrega como ajuste preestablecido a la cámara agregada por Designer.

![Contenido de una escena 3D](working-with-3d-scenes.resources/loaded3DScene.png "Contenido de una escena 3D"){zoomable="yes"}

Designer utiliza una descripción en USD para su escena 3D. Su diseño se puede navegar en el explorador de escenas, donde cada tipo [USD prim](https://openusd.org/release/glossary.html#usdglossary-prim) tiene su propio icono (geometría, material, sombreador, cámara, transformación, etc.).

El [explorador de escenas](../interface/3d-view/scene-browser/scene-browser.md) se puede usar para seleccionar, habilitar y deshabilitar el contenido de la escena. Por lo tanto, le recomendamos que la mantenga visible cuando trabaje con escenas 3D personalizadas.

## Carga de una escena

Hay varias rutas para cargar una escena 3D en la vista 3D:

1. Haga doble clic o arrastre un [recurso de escena 3D](../resources/3d-scene-resource/3d-scene-resource.md) de un [paquete](../glossary/glossary.md) a la vista 3D
1. Arrastra un elemento de escena 3D de la [biblioteca](../interface/the-library/the-library.md) a la vista 3D (siempre que hayas [agregado tu propio contenido a la biblioteca](../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md))
1. Arrastre un archivo de escena 3D desde el explorador de archivos del sistema a la vista 3D
1. Cargar un archivo de estado de escena 3D (SBSSCN) junto con su malla de referencia

Tenga en cuenta que solo los métodos 1 y 4 le permiten volver a cargar la escena exactamente como estaba la última vez que trabajó en ella, ya que el estado de la escena se escribe en el recurso de escena 3D y en el archivo de estado de escena y se guarda en el paquete. Los métodos 2 y 3 cargan la escena como cualquier otro.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cargando una escena 3D - Desde un recurso de escena 3D](working-with-3d-scenes.resources/load3DScene-3DSceneResource.gif "Cargando una escena 3D - Desde un recurso de escena 3D"){zoomable="yes"}

Carga de un recurso de escena 3D

</td>
<td style="border: 0;" valign="top">

![Cargando una escena 3D - Desde la biblioteca](working-with-3d-scenes.resources/load3DScene-Library.gif "Cargando una escena 3D - Desde la biblioteca"){zoomable="yes"}

Carga de una escena 3D desde la biblioteca

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cargando una escena 3D - Desde un archivo de escena 3D](working-with-3d-scenes.resources/load3DScene-3DSceneFile.gif "Cargando una escena 3D - Desde un archivo de escena 3D"){zoomable="yes"}

Carga de un archivo de escena 3D

</td>
<td style="border: 0;" valign="top">

![Cargando una escena 3D: desde un archivo de estado de escena](working-with-3d-scenes.resources/load3DScene-sceneStateFile.gif "Cargando una escena 3D: desde un archivo de estado de escena"){zoomable="yes"}

Carga de un archivo de estado de escena

</td>
</tr>
</table>

>[!NOTE]
>
> La navegación y la visualización de la escena en la vista 3D se tratan en la [documentación de la vista 3D](../interface/3d-view/3d-view.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Designer siempre crea su propio entorno (DomeLight en USD) y cámara, además de los que puedan existir en la escena.

Todos los elementos creados por Designer se muestran con <b>etiquetas en negrita</b> en el explorador de escenas.

>[!NOTE]
>
> Cuando una escena cargada tiene al menos un entorno (DomeLight), el entorno creado por Designer está *deshabilitado de forma predeterminada*, por lo que no interfiere con la iluminación del entorno de la escena.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Explorador de escenas - Elementos creados por Designer](working-with-3d-scenes.resources/sceneBrowser-createdByDesigner.png "Explorador de escenas - Elementos creados por Designer"){zoomable="yes"}

</td>
</tr>
</table>

## Archivos de estado de escena

Después de configurar un material, una cámara, luces, etc. en la Vista 3D, ese estado se puede guardar en un archivo de estado de escena (.sbsscn) que se puede cargar más adelante para restaurar ese estado. Por ejemplo, puede configurar algunas escenas para previsualizar diferentes tipos de materiales o un entorno de iluminación específico.

![Cargar archivo de estado de escena](working-with-3d-scenes.resources/loadSceneStateFile.gif "Cargar archivo de estado de escena"){zoomable="yes"}

Un estado de escena guardado también se puede utilizar como estado predeterminado para la Vista 3D, de modo que cada vez que se cree una nueva Vista 3D, se utilizará ese estado. Esto resulta útil si desea previsualizar los materiales de forma predeterminada en la malla Esfera 2 - Mosaicos con un valor de mosaico de 2 y un mapa de entorno específico.

Las acciones relacionadas con los archivos de estado de escena se encuentran en el menú Escena de la Vista 3D y se documentan [aquí](../interface/3d-view/3d-view.md).

Los archivos de estado de escena utilizan el formato XML y hacen uso de [alias](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md), si hay alguno definido en la [configuración del proyecto](../interface/preferences-window/project-settings/project-settings.md).

>[!NOTE]
>
> El procesador no se guarda en el archivo de estado de escena.
