---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: Conozca los conceptos básicos de la creación de complementos de Python para Substance 3D Designer con el fin de ampliar la funcionalidad de la aplicación.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conceptos básicos del complemento
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# Conceptos básicos del complemento

Un complemento es un archivo de Python o un módulo de Python que define una función <b>initializeSDPlugin()</b>.

Se llama a la función <b>initializeSDPlugin()</b> cuando se carga el complemento.\
En esta función, puede crear elementos de interfaz de usuario, registrar devoluciones de llamada y cualquier otra funcionalidad que pueda necesitar.

Opcionalmente, el complemento puede definir una función <b>uninitializeSDPlugin()</b> a la que se llamará cuando se descargue el complemento.\
Puede usar esta función para liberar recursos, cerrar conexiones de red y cosas similares.

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```
