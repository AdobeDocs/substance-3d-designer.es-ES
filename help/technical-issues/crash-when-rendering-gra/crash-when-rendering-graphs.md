---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: Solucione los problemas de bloqueos al procesar gráficos en Substance 3D Designer y busque soluciones para evitarlos.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bloqueo al renderizar los gráficos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# Bloqueo al renderizar los gráficos

En esta página se enumeran los bloqueos que se producen durante el procesamiento de gráficos en Substance 3D Designer y se ofrecen pasos de solución de problemas para cada uno.

## TDR (solo Windows)

<b>[![(error)](../../assets/error.svg)](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) Problema</b>

El temporizador <b>Detección y recuperación de tiempo de espera (TDR)</b> del sistema es *demasiado corto* para permitir que Substance 3D Designer finalice sus cálculos actuales antes de que se *reinicie* el controlador de gráficos.

Los cálculos realizados por Substance 3D Designer pueden ser muy intensivos y utilizar los controladores gráficos en un grado en el que *no responde* al sistema operativo durante un tiempo.\
Como medida de seguridad y estabilidad, el sistema operativo *reinicia el controlador de gráficos*, lo que corta los cálculos y da como resultado el *bloqueo* de Substance 3D Designer.

<b>![(tick)](../../assets/check.svg) Pasos recomendados</b>

Los valores del temporizador de TDR deben *aumentarse* para evitar estos bloqueos. Para ello, sigue las instrucciones de [esta página](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) de la documentación de Substance 3D Painter, que también se aplican a Substance 3D Designer.
