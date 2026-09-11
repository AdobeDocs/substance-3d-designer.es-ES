---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs.html"
breadcrumb-title: ''
description: Aprenda a crear y utilizar gráficas de funciones de Substance en Designer para crear funciones personalizadas y redes de nodos reutilizables.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gráficas de funciones de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Gráficas de funciones de Substance

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![](function-graphs.resources/function-1.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td style="border: 0;" valign="top">

[Gráficos de funciones de Substance](https://substance3d.adobe.com/) <b>procesar valores individuales</b> (enteros, flotantes, vectores) en lugar de datos de imagen (conjuntos completos de píxeles). Las funciones también son gráficos con redes de nodos, pero se utilizan [nodos](../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md) y la interfaz es diferente de los [gráficos de Substance normales](../compositing-graphs/substance-compositing-graphs.md). El flujo de trabajo se basa completamente en <b>operaciones matemáticas</b> y no muestra miniaturas de vista previa de imágenes, lo que lo convierte en una forma <b>mucho más avanzada de trabajar</b> con Substance 3D Designer.

Las funciones se pueden usar en muchos contextos diferentes, los principales son para modificar el comportamiento de [un parámetro expuesto](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), para crear el comportamiento de [procesadores de píxeles](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) o [FX-Maps](../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) y para usar [valores en Substance](../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

## Ejemplos

A continuación se muestran algunos ejemplos de casos de uso comunes de Functions.

### Función simple

![](function-graphs.resources/lerpfunction_1.png)

Una función simple en el contexto de un parámetro expuesto. Obtiene un valor flotante de entrada denominado &quot;Intensity&quot; (Intensidad) que se determina para ir de 0 a 1 (un rango fácil de entender) y lo reasigna a un rango establecido de 0,1 a 0,8. Eso significa que si el usuario establece Intensity en 0, internamente se utilizará 0.1, si la interfaz de usuario se establece en 1, se utilizará 0.8 y cualquier valor intermedio se interpolará linealmente. Este tipo de función se suele usar cuando se [exponen parámetros](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), pero se usan funciones personalizadas.

Esta función también se puede escribir como *lerp(0.1, 0.8, Intensity)* en un pseudocódigo similar a HLSL o GLSL.

### Función avanzada

![](function-graphs.resources/pixel-function_1.png){width="545px"}

Esta función avanzada muestra el funcionamiento interno de un [procesador de píxeles](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) destinado a ajustar el tono de una entrada de mapa de color en función de la intensidad de una segunda entrada de máscara de escala de grises.

Muestrea ambas entradas con la variable del sistema &quot;$pos&quot; y, a continuación, despoja al Alpha, convierte el valor de color en HSL y modifica el componente Hue multiplicándolo por el valor de escala de grises muestreado. A continuación, vuelve a montar el vector, convierte el HSL de nuevo en el RGB y vuelve a incorporar el Alpha para la salida final.

en pseudo-código esta sería una función mucho más complicada que no cabría en una sola línea.
