---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/get-a-variable-value.html"
breadcrumb-title: ''
description: Obtenga información sobre cómo recuperar valores de variables en gráficos de funciones de Substance 3D Designer mediante el nodo Obtener variable.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Get a variable value
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Obtener un valor variable
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Obtener un valor variable

Para utilizar una variable en una función, necesita &quot;llamarla&quot;, lo que significa que necesita importar el valor de la variable en la función.

Para ello, debes usar un nodo *Get*:

![](../../../assets/image2015-12-21-7-29-51.png)

Hay diferentes tipos de nodos Get: elija el correcto según el tipo de valor que desee importar:

![](../../../assets/image2015-12-21-7-31-4.png)

## Asignar una variable a un nodo Get

De forma predeterminada, un nodo get mostrará un signo de advertencia: esto significa que no está vinculado a ninguna variable todavía.

Para vincular una variable, vaya a los parámetros y elija una variable en la lista &quot;Variables/Obtener \*\*\*&quot; (\*\*\* se sustituirá por el tipo de valor al que puede llamar el nodo de obtención).

El nombre de variable se mostrará en el nodo:

![](../../../assets/assign-getfloat.gif)

Tenga en cuenta que sólo aparecerán en la lista las variables que sean del mismo tipo del nodo Get.

>[!WARNING]
>
> Tenga en cuenta que las variables creadas con un nodo *Set* no aparecerán en una lista de nodos *Get*.
> 
> Sin embargo, puede obtener la variable escribiendo manualmente el nombre en la lista.
> 
> No olvide que sólo puede llamar a una variable creada con un nodo Set si:
> 
> * Los nodos Get y Set están en gráficos de funciones que controlan los parámetros de un mismo nodo
> * El parámetro controlado por el gráfico de nodos *Get* es el mismo o se encuentra debajo del parámetro del gráfico de nodos *Set*, en la pila de parámetros.
