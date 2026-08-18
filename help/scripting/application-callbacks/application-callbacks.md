---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/application-callbacks.html"
breadcrumb-title: ''
description: Aprenda a utilizar las devoluciones de llamada de aplicación en los complementos de Substance 3D Designer Python para responder a eventos de aplicación.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Application callbacks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Devoluciones de llamada de aplicación
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# Devoluciones de llamada de aplicación

Es posible registrar <b>devoluciones de llamada de Python</b> con el objeto de aplicación al que Designer llamará cuando se produzcan eventos específicos.

Los objetos de interfaz de usuario, como menús y botones, pueden desencadenar devoluciones de llamada mediante la biblioteca <b>Qt para Python</b>. Para obtener más información, consulte [Creación de elementos de interfaz de usuario](../../scripting/creating-user-interface/creating-user-interface-elements.md).

```
import sd 

 

## Our callbacks.

def onBeforeFileLoadedCallback(filePath): 

    print("Before file loaded, file: %s" % filePath) 

 

def onAfterFileLoadedCallback(filePath, succeed, updated): 

    print("After file loaded, file: %s, succeed: %s, updated: %s" % (filePath, succeed, updated)) 

     

def onBeforeFileSavedCallback(filePath, parentPackagePath): 

    print("Before file saved, file: %s, parentPackage: %s" % (filePath, parentPackagePath)) 

 

def onAfterFileSavedCallback(filePath, succeed): 

    print("After file saved, file: %s, succeed: %s" % (filePath, succeed)) 

 

## Get the application.

app = sd.getContext().getSDApplication() 

 

## Register our callbacks.

beforeFileLoadedCallbackID = app.registerBeforeFileLoadedCallback(onBeforeFileLoadedCallback) 

afterFileLoadedCallbackID = app.registerAfterFileLoadedCallback(onAfterFileLoadedCallback) 

beforeFileSavedCallbackID = app.registerBeforeFileSavedCallback(onBeforeFileSavedCallback) 

afterFileSavedCallbackID = app.registerAfterFileSavedCallback(onAfterFileSavedCallback) 

 

## Unregister callbacks when no longer needed.

app.unregisterCallback(beforeFileLoadedCallbackID) 

app.unregisterCallback(afterFileLoadedCallbackID) 

app.unregisterCallback(beforeFileSavedCallbackID) 

app.unregisterCallback(afterFileSavedCallbackID)
```
