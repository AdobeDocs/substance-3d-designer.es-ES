---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/3d-scene-resource.html"
breadcrumb-title: ''
description: Aprenda a importar y utilizar recursos de escenas 3D en Substance 3D Designer para la previsualización de materiales y las pruebas.
helpx_creative_field: ""
helpx_description: Designer > Resources > 3D scene resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recurso de escena 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---


# Recurso de escena 3D

Esta página describe el tipo de recurso **3D scene** en Substance 3D Designer, incluidos los formatos de archivo compatibles y cómo se puede usar.

## Información general

Los recursos de escenas 3D se pueden utilizar en diversos flujos de trabajo:

* [mapas de malla de banca](../../bakers/bakers.md)
* obtener una vista previa de *texturas* de [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) en la [vista 3D](../../interface/3d-view/3d-view.md)

Se admiten los siguientes formatos de archivo de escena 3D:

* [USD](https://graphics.pixar.com/usd/release/index.html) (\*.usd)
* [USDA](https://graphics.pixar.com/usd/release/index.html) (\*.usda)
* [USDZ](https://graphics.pixar.com/usd/release/index.html) (\*.usdz)
* [Autodesk FBX](https://www.autodesk.com/products/fbx/overview) (\*.fbx)
* [Wavefront OBJ](https://www.fileformat.info/format/wavefrontobj/egff.htm) (\*.obj)
* [Malla de Autodesk 3D Studio](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2022/ENU/3DSMax-Data-Exchange/files/GUID-A16ECF7F-70E5-4F9F-8EAD-35F5CFB485A2-htm.html) (\*.3ds)
* [Collada](https://www.khronos.org/collada/) (\*.date)
* [Dibujo AutoCAD de Autodesk](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/AutoCAD-Core/files/GUID-D4242737-58BB-47A5-9B0E-1E3DE7E7D647-htm.html) (\*.dxf)

## Almacenamiento de malla

Las escenas 3D *solo* se pueden vincular, lo que significa que permanecen en su ubicación en el disco y solo se hace referencia a ellas en la aplicación.

Cuando se publica un paquete con un recurso de escena 3D como un recurso de [Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) (SBSAR), la malla es *no incrustada*, pero se descarta.

## Panificación de mapas de malla

La vinculación de una escena 3D en el paquete es la única forma de [eliminar los mapas de malla](../../bakers/bakers.md) de esa geometría de escena. Para empezar, puede realizar los siguientes pasos:

* Haga clic en *RMB* en un paquete y seleccione la opción <b>Vínculo > Malla 3D</b> en el menú contextual
* Elija cualquier archivo de escena 3D compatible
* Si aparece el aviso del cuadro de diálogo <b>Vincular como malla Udim</b>, haz clic en *No* a menos que quieras hornear mosaicos UV
* Con el recurso cargado en [Explorer](../../interface/the-explorer-window/the-explorer-window.md), haz clic en *RMB* y selecciona la opción <b>Bake Model Information</b> en el menú contextual
* Aparece el cuadro de diálogo [Información del modelo de horneado](../../bakers/bakers.md) para que configure y ejecute los horneados de los mapas de malla

![Mapas de malla de cocción](3d-scene-resource.resources/3d-scene-resource-01.gif "Mapas de malla de cocción"){width="512px"}

## UDIM/UV-tile usage

Cuando se vincula un recurso de malla y la aplicación detecta que tiene UV fuera del rango 0-1, se le preguntará si esta malla debe tratarse como una malla UDIM (también conocida como UV Tiles). Esta es una configuración que se puede cambiar posteriormente y, a menos que esté seguro de que está utilizando UV-Tiles, debe responderse como <b>No</b>.

Si el comportamiento de azulejo UV está activo, el horneado se comporta de forma diferente y crea texturas para cada azulejo UV detectado.

## Recurso/escena frente a estado

La aplicación separa lo que se ve en la vista 3D en dos archivos distintos. El modelo o malla 3D real es un recurso visible en el Explorador. La configuración de luces, cámaras y otros ajustes se denomina &quot;<b>Estado</b>&quot;. Los estados se pueden guardar en archivos .sbsscn externos para volver a cargarlos más tarde. Los archivos .sbsscn no son recursos, son archivos de configuración adicionales que solo se pueden cargar a través de [&#x200B; en el menú Escena de la vista 3D.](../../interface/3d-view/3d-view.md)
