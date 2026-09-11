---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/creating-user-interface-elements.html"
breadcrumb-title: ''
description: Aprenda a crear elementos de interfaz de usuario en complementos de Substance 3D Designer Python para experiencias de usuario interactivas.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Creating user interface elements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Creación de elementos de interfaz de usuario
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Creación de elementos de interfaz de usuario

Substance 3D Designer incluye <b>Qt Para Python</b>. Los usuarios pueden usar la clase [UI Manager](../../scripting/scripting-api-reference/scripting-api-reference.md)para crear <b>menús</b>, <b>cuadros de diálogo</b>, <b>paneles personalizados</b> y otros elementos de la interfaz de usuario para sus complementos.

En esta página encontrará ejemplos sencillos de cómo utilizar Qt para Python en Designer.

Para obtener más información sobre Qt para Python, consulte la [documentación oficial.](https://doc.qt.io/qtforpython/index.html)

## Creación de cuadros de diálogo

```
import sd 

from PySide2 import QtWidgets 

 

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Create a new dialog. For shortcuts to work correctly

## it is important to parent the new dialog to Designer's main window.

mainWindow = uiMgr.getMainWindow() 

dialog = QtWidgets.QDialog(parent=mainWindow) 

 

## Create a layout and some widgets.

layout = QtWidgets.QVBoxLayout() 

layout.addWidget(QtWidgets.QPushButton("Press Me")) 

dialog.setLayout(layout) 

 

## Show the dialog (non-modal).

dialog.show()
```


### Creación de menús

```
import sd 

from PySide2 import QtWidgets 

 

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Function that will be called when our menu item is selected.

def sayHello(): 

 print("Hello!") 

 

## Create a new menu.

menu = uiMgr.newMenu(menuTitle="MyMenu", objectName="doc.example.my_menu") 

## Create a new action.

act = QtWidgets.QAction("Hello", menu) 

act.triggered.connect(sayHello) 

 

## Add the action to the menu.

menu.addAction(act)
```


### Creación de paneles

```
import sd 

from PySide2 import QtWidgets 

 

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Create a new dock widget.

## The dock identifier is used when saving and restoring dock positions and sizes.

## For this reason, it's important that the identifier is unique.

dock = uiMgr.newDockWidget(identifier="sample.test.dock", title="New Dock") 

 

## Create a layout and add some widgets.

layout = QtWidgets.QVBoxLayout() 

dock.setLayout(layout) 

 

for i in range(0, 5): 

 layout.addWidget(QtWidgets.QPushButton("Button %s" % i))
```


### Creación de barras de herramientas en la ventana de la aplicación

```
import sd 

from PySide2 import QtCore, QtWidgets 

  

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

  

## Get Designer's main window.

mainWindow = uiMgr.getMainWindow() 

 

## Create our toolbar.

toolbar = QtWidgets.QToolBar() 

toolbar.addAction("Tool") 

toolbar.addAction("Bar") 

 

## Add our toolbar to Designer's window.

mainWindow.addToolBar(QtCore.Qt.TopToolBarArea, toolbar) 
```


### Creación de barras de herramientas en la vista de gráfico

```
from functools import partial 

import sd 

 

from PySide2 import QtCore, QtGui, QtWidgets 

 

class MyGraphToolBar(QtWidgets.QToolBar): 

    def __init__(self, graphViewID, uiMgr): 

        super(MyGraphToolBar, self).__init__(parent=uiMgr.getMainWindow()) 

 

## Save the graphViewID and uiMgr for later use.

        self.__graphViewID = graphViewID 

        self.__uiMgr = uiMgr 

 

## Add actions to our toolbar.

        act = self.addAction("P") 

        act.setToolTip("Print the selected nodes to the Python console") 

        act.triggered.connect(self.__onPrintNodes) 

 

    def __onPrintNodes(self): 

        for node in self.__getSelectedNodes(): 

            print(node) 

 

    def __getSelectedNodes(self): 

## Use our saved graphViewID to retrieve the graph selection.

        return self.__uiMgr.getGraphSelectedNodesFromGraphViewID( 

            self.__graphViewID) 

 

def onNewGraphViewCreated(graphViewID, uiMgr): 

## Create our toolbar.

    toolbar = MyGraphToolBar(graphViewID, uiMgr) 

 

## Add our toolbar to the graph widget.

    uiMgr.addToolbarToGraphView( 

        graphViewID, 

        toolbar, 

        icon = None, 

        tooltip = "My Graph Toolbar") 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Register a callback to know when GraphViews are created.

uiMgr.registerGraphViewCreatedCallback( 

    partial(onNewGraphViewCreated, uiMgr=uiMgr))
```


### Creación de acciones en la barra de herramientas Vista de gráfico

```
from functools import partial 

import sd 

  

from PySide2 import QtWidgets 

 

 

class MyGraphAction(QtWidgets.QAction): 

    def __init__(self, graphViewID, uiMgr): 

        super(MyGraphAction, self).__init__(parent=uiMgr.getMainWindow()) 

 

## Save the graphViewID and uiMgr for later use.

        self.__graphViewID = graphViewID 

        self.__uiMgr = uiMgr 

 

## Set up the action.

        self.setText("P") 

        self.setToolTip("Print the selected nodes to the Python console") 

        self.triggered.connect(self.__onPrintNodes) 

 

    def __onPrintNodes(self): 

        for node in self.__getSelectedNodes(): 

            print(node) 

  

    def __getSelectedNodes(self): 

## Use our saved graphViewID to retrieve the graph selection.

        return self.__uiMgr.getGraphSelectedNodesFromGraphViewID( 

            self.__graphViewID 

        ) 

 

 

def onNewGraphViewCreated(graphViewID, uiMgr): 

## Create our action.

    action = MyGraphAction( 

        graphViewID = graphViewID, 

        uiMgr = uiMgr 

    ) 

  

## Add our action to the graph toolbar.

    uiMgr.addActionToGraphViewToolbar( 

        graphViewID, 

        action 

    ) 

  

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

  

## Register a callback to know when GraphViews are created.

uiMgr.registerGraphViewCreatedCallback( 

    partial(onNewGraphViewCreated, uiMgr=uiMgr))
```


### Cargar interfaces de usuario creadas con Qt Designer

>[!NOTE]
>
> Qt Designer *no está incluido* con Substance 3D Designer. Puede obtenerlo instalando la distribución oficial de Qt para su sistema operativo.

```
from PySide2 import QtCore, QtWidgets, QtUiTools 

 

def loadUiFile(filename, parent=None): 

    ''' 

    Loads a Qt Designer .ui file. 

    Returns a widget. 

    ''' 

    loader = QtUiTools.QUiLoader() 

    uifile = QtCore.QFile(filename) 

    uifile.open(QtCore.QFile.ReadOnly) 

    ui = loader.load(uifile, parent) 

    uifile.close() 

    return ui 

 

## Get the application and the UI Manager.

app = sd.getContext().getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Load our Qt Designer ui file.

widget = loadUiFile("MyUI.ui", parent=uiMgr.getMainWindow()) 

 

## Show our user interface. In this case we show it as a non-modal dialog,

## but we could also make it modal or create a new dock for it.

widget.show()
```
