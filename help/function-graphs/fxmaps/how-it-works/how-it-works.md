---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: Descubra cómo funciona FXMaps en Substance 3D Designer para aplicar gráficos de funciones a texturas para efectos procedimentales.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cómo funciona
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# Cómo funciona

Comprender cómo funciona un gráfico FX-Map es la clave para dominar esta poderosa característica.

Un gráfico FX-Map puede contener uno o más de los tres tipos de nodos FX-Map: Cuadrante, iterar y conmutar. De estos nodos, el que probablemente utilizará con más frecuencia es el Cuadrante, con el nodo iterado en un segundo cercano.

El nodo Conjunto de parámetros es el principal motor de FX-Maps. Crea la región central en la que se basan los FX-Maps de cuatro árboles, pero no se muestra como uno solo. Visualmente, el gráfico de cuatro árboles se muestra en la forma de una cadena Markov.

Al renderizar el FX-Map, el gráfico FX-Map simplificado se &quot;desenvuelve&quot; para que parezca el gráfico de árbol grande. El motor &quot;camina&quot; todo el cuádruple árbol, trabajando de arriba abajo, luego de izquierda a derecha.

Los nodos FX-Map no copian ni pegan sus imágenes a ciegas. Cuando se procesa cada imagen, se ejecutan todas las funciones dinámicas que tiene. Las funciones afectan a cada imagen representada por el nodo. Por lo tanto, puede dar a cada imagen individual una rotación aleatoria, un factor de escala o varios ajustes más.
