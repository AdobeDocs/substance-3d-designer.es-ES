---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: Acceder a nodos lógicos en gráficos de funciones de Substance 3D Designer para realizar operaciones y comparaciones lógicas booleanas.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lógico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Nodos lógicos

Los nodos lógicos se utilizan para añadir varias condiciones al gráfico:

![](../../../../assets/image2015-12-23-11-23-21.png)

## El nodo *And*

![](../../../../assets/image2015-12-23-11-30-9.png)

El nodo And toma dos nodos booleanos como entrada:

* Si ambas entradas son True, el resultado del nodo *And* será *True*
* En cualquier otro caso, el nodo *And* devolverá *False*

## El nodo *Or*

![](../../../../assets/image2015-12-23-11-30-44.png)

El nodo O toma dos nodos booleanos como entrada:

* Si al menos una de las entradas es True (1), el resultado del nodo *Or* será *True*
* Si ambas entradas son False, el nodo *Or* devolverá *False*

## El nodo *Not*

![](../../../../assets/image2015-12-23-11-31-46.png)

El nodo Not toma un valor booleano como entrada: observará el valor de entrada y devolverá su opuesto:

* La entrada *True* proporciona la salida *False*
* La entrada *False* proporciona la salida *True*
