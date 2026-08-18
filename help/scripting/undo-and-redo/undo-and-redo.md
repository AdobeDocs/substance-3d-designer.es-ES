---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: Aprenda a implementar la funcionalidad de deshacer y rehacer en scripts de Substance 3D Designer Python para las acciones del usuario.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deshacer y rehacer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# Deshacer y rehacer

Con la clase <b>SDHistoryUtils.UndoGroup</b>, los usuarios pueden *agrupar acciones* para *deshacer o rehacer* todas ellas en un solo comando.

Estos grupos están *nombrados* por los usuarios y aparecerán con ese nombre en la lista de deshacer/rehacer de la interfaz de usuario.  Esto hace que un gran número de acciones sean más manejables.

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```
