---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: Aprenda a acceder y manipular gráficos y selecciones de nodos en scripts de Substance 3D Designer Python.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Acceso a gráficos y selecciones
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Acceso a gráficos y selecciones

La clase <b>SDApplication</b> contiene algunos métodos útiles que le permiten obtener acceso al gráfico *actualmente activo* y a la *selección actual* que contiene.

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


Se puede obtener acceso a un gráfico mostrado en una vista de gráfico *específica* mediante <b>graphViewID</b>.

Este método resulta útil al crear barras de herramientas de vista de gráfico personalizadas. El ejemplo de <b>Creación de barras de herramientas en vistas de gráficos</b> del capítulo [Creación de elementos de interfaz de usuario](../../scripting/creating-user-interface/creating-user-interface-elements.md) proporciona más detalles.
