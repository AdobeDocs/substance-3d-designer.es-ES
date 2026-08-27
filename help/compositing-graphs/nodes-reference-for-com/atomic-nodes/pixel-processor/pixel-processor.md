---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: Utilice el nodo Procesador de píxeles para procesar píxeles individuales mediante expresiones personalizadas para la manipulación avanzada de texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Procesador de píxeles
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# Procesador de píxeles

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Procesador de píxeles](../../../../assets/comp_pixelprocessor_1.png "Nodo atómico: Procesador de píxeles"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Genera una imagen en la que el valor de cada píxel es el resultado del [gráfico de funciones de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) especificado.

El procesador de píxeles le permite ejecutar una función personalizada para cada píxel que se devuelve como salida, en una entrada opcional.

Es, con mucho, el nodo más versátil, ya que permite ejecutar cualquier operación matemática y devolver resultados dentro del gráfico.

</td>
</tr>
</table>

De forma similar a [FX-Map](../../../../function-graphs/fxmaps/fxmaps.md), es necesario configurar la funcionalidad interna para realizar cualquier cosa. Donde el procesador de píxeles se diferencia de FX-Map es que no se centra en colocar patrones, con múltiples funciones que controlan la forma y la colocación del patrón. En su lugar, se ejecuta una sola función en paralelo para cada píxel, donde cada píxel desconoce los resultados de cálculo de sus vecinos.

El procesador de píxeles es similar al [procesador de valores](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), que se ejecuta en valores únicos y puede proporcionar una optimización agradable en comparación con el procesador de píxeles.

Para cualquiera que esté acostumbrado a crear funciones de [sombreador](../../../../glossary/glossary.md) en editores basados en nodos, el procesador Pixel debería ofrecer un entorno familiar.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> En la sección [Gráficos de Substance de muestra](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) de esta documentación hay disponible un archivo de proyecto anotado que muestra los usos simples del nodo Procesador de píxeles.
> 
> El nodo [Value processor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) es un buen punto de partida para obtener información acerca de los [gráficos de funciones de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Asimismo, tenga en cuenta que trabajar con este tipo de gráfico y realizar operaciones matemáticas es obligatorio para obtener cualquier elemento de este nodo.
> 
> También recomendamos estar familiarizados con el concepto de [UV](../../../../glossary/glossary.md), [muestreo de texturas](../../../../glossary/glossary.md) y vectores.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Conectores de salida

</td>
<td style="border: 0;" valign="top">

### Ejemplos

</td>
</tr>
</table>

## Parámetros

|  |  |
| --- | --- |
| <b>Modo de color</b> *Booleano* | Alterna entre una imagen de salida en escala de grises y en color. |
| <b>Función por píxel</b> *Float/Float4* | [Gráfico de funciones de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) por píxel en la imagen de salida.   Use el nodo [Get Float2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) establecido en la variable <b>$pos</b> para acceder a la posición [normalizada](../../../../glossary/glossary.md) del píxel actual. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Imagen de entrada #</b> *Escala de grises/Color* | Use un nodo [Sample color](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) o [Sample grayscale](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) para obtener acceso a los valores de la entrada del índice especificado. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises/Color* |  |

## Ejemplos

*Próximamente.*
