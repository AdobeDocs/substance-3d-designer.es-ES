---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/adding-actions-to-the-explorer-toolbar.html"
breadcrumb-title: ''
description: Aprenda a agregar acciones personalizadas a la barra de herramientas del Explorador en Substance 3D Designer mediante scripts de Python.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Adding actions to the Explorer toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Agregar acciones a la barra de herramientas del Explorador
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---


# Agregar acciones a la barra de herramientas del Explorador

Los complementos pueden agregar *acciones personalizadas* a la barra de herramientas <b>Explorer</b> mediante las devoluciones de llamada y los métodos disponibles en la clase <b>SDUIMgr</b>.

## Ejemplo de complemento Acciones de barra de herramientas Explorador

```
import sd 

 

import os 

from functools import partial 

 

from PySide2 import QtWidgets 

 

explorerCreatedCallbackID = None 

explorerSelectionChangedCallbackIDs = [] 

 

def onActionTriggered(explorerID, uiMgr): 

    '''Called when the user clicks on the toolbar icon.''' 

 

    print("Selected items:") 

    print("---------------") 

    for item in uiMgr.getExplorerSelection(explorerID): 

        print(item) 

    print("n") 

 

def explorerSelectionChanged(explorerID, uiMgr, action, originalExplorerID): 

    '''Called when the selection in the explorer panel changes.''' 

 

## Ignore callbacks for other explorer panels.

    if explorerID != originalExplorerID: 

        return 

 

    print("Explorer selection changed, id = %s" % explorerID) 

 

## Enable or disable the action depending on the explorer selection.

    selection = uiMgr.getExplorerSelection(explorerID) 

    action.setEnabled(len(selection) != 0) 

 

def explorerCreated(explorerID, uiMgr): 

    '''Called when a new explorer panel is created.''' 

 

    print("Explorer created, id = %s" % explorerID) 

 

## Warning: It is important to parent the action to some Qt object.

## If the action is not parented, Python will garbage collect it.

    act = QtWidgets.QAction("P", parent=uiMgr.getMainWindow()) 

    uiMgr.addActionToExplorerToolbar(explorerID, act) 

    act.setToolTip("Print explorer selection to the console") 

    act.triggered.connect(partial(onActionTriggered, explorerID=explorerID, uiMgr=uiMgr)) 

 

## Register a selection changed callback to update the action enabled state.

    global explorerSelectionChangedCallbackIDs 

    explorerSelectionChangedCallbackIDs.append(uiMgr.registerExplorerSelectionChangedCallback( 

        partial(explorerSelectionChanged, uiMgr=uiMgr, action=act, originalExplorerID=explorerID))) 

 

## Set initial enabled / disabled state.

    explorerSelectionChanged(explorerID, uiMgr, act, explorerID) 

 

def initializeSDPlugin(): 

    ctx = sd.getContext() 

    app = ctx.getSDApplication() 

    uiMgr = app.getQtForPythonUIMgr() 

 

## Register an explorer created callback to add actions to newly created explorer toolbars.

    global explorerCreatedCallbackID 

    explorerCreatedCallbackID = uiMgr.registerExplorerCreatedCallback(partial(explorerCreated, uiMgr=uiMgr)) 

 

def uninitializeSDPlugin(): 

    ctx = sd.getContext() 

    app = ctx.getSDApplication() 

    uiMgr = app.getQtForPythonUIMgr() 

 

## Unregister all callbacks.

    global explorerCreatedCallbackID 

    uiMgr.unregisterCallback(explorerCreatedCallbackID) 

 

    global explorerSelectionChangedCallbackIDs 

    for callbackID in explorerSelectionChangedCallbackIDs: 

        uiMgr.unregisterCallback(callbackID)
```
