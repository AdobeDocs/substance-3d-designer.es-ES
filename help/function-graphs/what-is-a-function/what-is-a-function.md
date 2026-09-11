---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: Conozca qué funciones hay en Substance 3D Designer y cómo usarlas para crear redes de nodos reutilizables.
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Qué es una función '
user-guide-description: ''
user-guide-title: ''
source-git-commit: baf36ab85717512cc9e52d67d00293eabb5ebcf6
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# ¿Qué es una función?

Las funciones de Substance 3D Designer permiten al usuario generar resultados utilizando la lógica que, de otro modo, se encontraría en un lenguaje de programación.

Sin embargo, en lugar de utilizar líneas de códigos, las funciones de Designer mantienen el mismo enfoque nodal. A primera vista, un gráfico de funciones se parece mucho a un gráfico normal.

![](what-is-a-function.resources/image2015-12-17-18-19-37.png)

Puede encontrar funciones en 2 casos principales:

* para controlar el resultado de un parámetro
* si edita un procesador de píxeles

## Controlar el resultado de un parámetro

En Substance 3D Designer, cualquier parámetro se puede controlar mediante una función.

![](what-is-a-function.resources/image2015-12-17-21-3-46.png)

Por lo tanto, puedes imaginar reglas y dependencias entre las partes de tu gráfico, para obtener resultados únicos.

Por ejemplo, puede decidir que la opacidad de un nodo de fusión sea la mitad de la intensidad de un nodo de deformación :

![](what-is-a-function.resources/warpblend.gif)

De hecho, es posible que ya haya creado funciones sin darse cuenta de ellas:

si ha expuesto un parámetro, ha creado automáticamente una función y una variable: la función contiene un nodo float get que detecta el valor de la variable recién creada:

![](what-is-a-function.resources/expose.gif)
