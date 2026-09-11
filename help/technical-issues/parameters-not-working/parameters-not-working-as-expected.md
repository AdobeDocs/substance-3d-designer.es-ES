---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: Resuelva problemas por el hecho de que los parámetros del gráfico del Substance no funcionen como se esperaba y busque soluciones.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Los parámetros no funcionan según lo previsto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 5%

---


# Los parámetros no funcionan según lo previsto

En esta página se enumeran las causas comunes por las que los parámetros no funcionan según lo previsto en Substance 3D Designer y se ofrecen pasos de solución de problemas para cada una de ellas.

## El parámetro no funciona en el modo de vista previa y el recurso de Substance 3D publicado (SBSAR)

<b>![(error)](../../assets/error.svg) Problema</b>

Algunos parámetros expuestos de un gráfico son *no se muestran* al usar el [modo de vista previa](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) en Designer, o en la lista de parámetros de recursos de Substance 3D (SBSAR) [publicados](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) de ese gráfico.

<b>![(tick)](../../assets/check.svg)Pasos recomendados</b>

Los parámetros que faltan probablemente sean [parámetros estáticos](../../glossary/glossary.md), que *no se pueden editar sobre la marcha* después de que el gráfico se haya *preparado*, es decir, procesado para ejecutar su algoritmo de forma rápida y eficaz. La cocción se produce en Designer cada vez que el gráfico se *edita* o *publica*. Los parámetros afectados por estas limitaciones se enumeran en la sección [Limitaciones](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) de la página [Exposición de un parámetro](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) de esta documentación.

Como tal, los parámetros estáticos son visibles y editables en Designer, pero están *ocultos* en un recurso de Substance 3D publicado. Puede usar el [modo de vista previa](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) para ver estas limitaciones en vigor antes de publicar en un recurso de Substance 3D.

A continuación se muestra una lista de parámetros estáticos:

| Nodo | Parámetro |
| --- | --- |
| Todos los nodos | Modo Mosaico Proporción de píxeles |
| [Color uniforme](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | Modo de color |
| [Procesador de píxeles](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | Modo de color |
| [Fusionar](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | Modo de fusión Fusión Alpha fusionar Área de recorte |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | Modo de fusión |
| [Cuadrante](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | Patrón de entrada imagen alfa Entrada imagen filtrado |

## Resultado incorrecto para el gráfico de funciones del Substance aplicado al parámetro

<b>![(error)](../../assets/error.svg) Problema</b>

Un gráfico de funciones de Substance aplicado a un parámetro de nodo no genera el valor esperado cuando se utiliza un entero negativo.

<b>![(tick)](../../assets/check.svg) Pasos recomendados</b>

Los enteros negativos no se admiten correctamente. Como solución alternativa, use el valor entero negativo en un valor [Integer2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) y extráigalo usando un nodo [Referenciar entero](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md).
