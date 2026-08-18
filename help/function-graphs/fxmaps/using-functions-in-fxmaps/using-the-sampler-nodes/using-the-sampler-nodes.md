---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: Aprenda a utilizar nodos de muestra en FXMaps para probar texturas y crear variaciones de materiales procedimentales.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uso de los nodos de Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Uso de los nodos de Sampler

![](../../../../assets/sampler-graph.jpg)

El nodo de muestra se puede utilizar para muestrear valores de píxeles en una entrada de imagen conectada al nodo fx-map. Los valores muestreados se pueden utilizar para controlar cualquier parámetro mediante funciones.

## Ejemplo sencillo

En este ejemplo se ha creado una cadena de nodos de cuadrantes para generar una cuadrícula de patrón. Se crea una función en el parámetro Opacidad/Luminancia del último cuadrante.

![](../../../../assets/sampler-function.jpg){width="300px"}![](../../../../assets/sampler-result-1.jpg){width="300px"}

El nodo Sample toma una entrada float2 como coordenadas de muestreo (x, y). En este ejemplo se utilizó la variable $pos: para cada patrón, el valor de píxel se muestrea en la posición del patrón en la primera entrada de imagen conectada al nodo FxMap.

El nodo Gris de ejemplo devuelve un valor float1 en el intervalo 0, 1.

El nodo Color de muestra devuelve un valor float4 (rgba) en el rango 0, 1.

## Ejemplo avanzado

Aquí, comparamos el valor muestreado con una constante (0,3). Si el valor muestreado es mayor que 0,3, la función devuelve 1; de lo contrario, devuelve 0.

![](../../../../assets/sampler-function-advanced.jpg){width="300px"}![](../../../../assets/sampler-result-advanced.jpg){width="300px"}

## Descargar ejemplo

[![Icono de archivo SBS](../../../../assets/sbs-1_1.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)
