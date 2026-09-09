---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs.html"
breadcrumb-title: ''
description: Obtenga más información sobre la composición gráfica de Substance en Substance 3D Designer para crear texturas de procedimiento y flujos de trabajo de materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gráficos de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---


# Gráficos de Substance

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](substance-compositing-graphs.resources/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

[Los gráficos de Substance](https://substance3d.adobe.com/) son el tipo principal de gráfico creado en Substance 3D Designer. Su propósito es <b>generar y procesar datos de imágenes 2D</b> que no estén restringidos a una resolución, color o forma establecidos. Se han concebido como herramientas de generación y procesamiento de imágenes extremadamente versátiles, no solo como resultados estáticos preconfigurados.

Los resultados pueden ser en forma de un simple patrón en blanco y negro, un filtro que solo se ejecuta en otras imágenes y no genera contenido por sí mismo, o incluso un material procedimental completo con múltiples canales.

Los gráficos de Substance son [el tipo de gráfico más ampliamente admitido](../getting-started/overview/overview.md), y se pueden exportar y usar en una gran variedad de flujos de trabajo diferentes.

</td>
</tr>
</table>

## Ejemplos

A continuación, puede encontrar algunos ejemplos típicos de casos de uso comunes.

+++Forma simple
![Forma simple en el gráfico del Substance](substance-compositing-graphs.resources/simpleshape.png "Forma simple en el gráfico del Substance"){width="512px"}



Se crea una forma de máscara simple para una pegatina generando [un fragmento de texto](../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) y una [forma de disco](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md), [extrayendo el borde](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) del disco y finalmente [fusionándolos](../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) antes de establecerlos como [salida](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) final.

El texto con el número o el thickness del borde se puede exponer externamente para que sea un gráfico más dinámico.

+++

+++Filtro de ajuste
![Filtro de ajuste en el gráfico de Substance](substance-compositing-graphs.resources/simplefilter.png "Filtro de ajuste en el gráfico de Substance"){width="512px"}



Un gráfico de filtro toma un mapa normal como [entrada](../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)(con una vista previa personalizada), [lo convierte en curvatura](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) y, a continuación, [ajusta el contraste](../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) para crear una máscara de bordes convexos como [salida](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) final.

Los valores de contraste establecidos en el histograma pueden ser expuestos, haciendo de este un filtro simple pero útil en combinación con la ranura de entrada dinámica.

+++

+++Material completo
![Material completo en el gráfico del Substance](substance-compositing-graphs.resources/simplematerial.png "Material completo en el gráfico del Substance"){width="512px"}



Un gráfico más complicado[fusiona dos Materiales base](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md). Un [Material base](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) se mantiene simple, el otro usa algunas entradas personalizadas para agregar interés. Se utiliza una máscara para determinar cuál de los dos materiales aparece en qué lugar antes de definirse como [salidas](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finales.

Este ejemplo utiliza [Modos de creación de vínculos](../interface/the-graph-view/link-creation-modes/link-creation-modes.md) para simplificar el uso de varios vínculos.

+++
