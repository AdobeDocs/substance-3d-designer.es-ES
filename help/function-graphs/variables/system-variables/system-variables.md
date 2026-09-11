---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: Obtenga más información sobre las variables del sistema integradas disponibles en los gráficos de funciones de Substance 3D Designer para flujos de trabajo avanzados.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variables incorporadas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 3%

---


# Variables incorporadas

Puede utilizar variables integradas en [gráficos de funciones de Substance](../../../function-graphs/function-graphs.md) para tener acceso a valores específicos. Siempre comienzan con un símbolo `$` (dólar).

Algunas variables solo están disponibles en contextos específicos.

<b>Todos los nodos</b>

Variables del sistema

| Nombre | Tipo | Propósito |
| --- | --- | --- |
| $size | Flotante 2 | Devuelve el tamaño del nodo actual en píxeles.   Si se usa en el parámetro [Tamaño de salida](../../../compositing-graphs/output-size/output-size.md) establecido en *Relativo a...* [método de herencia](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), devuelve el *valor heredado*. |
| $sizelog2 | Flotante 2 | Como se ha indicado anteriormente, pero devuelve el tamaño como valores de potencia de 2 (por ejemplo: para la imagen 2048\*2048, `$sizelog2` devuelve 11).   Si se usa en el parámetro [Tamaño de salida](../../../compositing-graphs/output-size/output-size.md) establecido en *Relativo a...* [método de herencia](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), devuelve el *valor heredado*. |
| $pixelratio | Entero | Devuelve un valor entero correspondiente a la proporción de píxeles del nodo actual (heredada o absoluta):   0: Estirar 1: Cuadrado |
| $mosaico | Entero | Devuelve un valor entero correspondiente al modo de segmentación de nodos actual (heredado o absoluto):   0: Sin mosaico 1: Mosaico horizontal 2: Mosaico vertical 3: Mosaico en H y V |
| $fisiccalsize | Flotante 3 | Devuelve el valor de la propiedad [graph](../../../compositing-graphs/graph-parameters/graph-parameters.md) <b>Tamaño físico</b>. |
| $uvitil | Entero 2 | Cuando se utilizan flujos de trabajo UDIM, esta variable devuelve el índice de la vista actual en U y V.   Por ejemplo, (2, 0) para el azulejo 1003, (7, 11) para el azulejo 1118, ... |

<b>FX-Map</b>

Variables del sistema

| Nombre | Tipo | Propósito |
| --- | --- | --- |
| $pos | Flotante 2 | Devuelve la posición de nacimiento del motivo. El origen (0, 0) se encuentra en la esquina superior izquierda de la imagen. |
| $profundidad | Flotante | Devuelve el número de octava (nivel) del nodo [FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md). Esto permite a un nodo modificar su comportamiento según el nivel del cuádruple árbol que representa. |
| $depthpow2 | Flotante | Como se ha indicado anteriormente, pero devuelve el inverso multiplicativo de 2 elevado a la potencia del número de octava (nivel), es decir, 1/(2^octava). Se trata de un valor auxiliar que resulta útil para algunos cálculos comunes. |
| $number | Flotante | Devuelve el número del motivo dibujado. Se puede acceder a esto mediante gráficos de funciones dinámicas que controlan un nodo [Iterate](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md) para modificar su comportamiento en cada paso de iteración.   Tenga en cuenta que `$number` empieza a contar desde 0, no desde 1.   Cuando se utiliza una cadena de nodos de iteración, la variable `$number` devolverá el número de iteración del último nodo de iteración conectado antes del parámetro de función que se utiliza. Si desea recuperar el número de iteración de varios nodos iterados, debe utilizar &quot;variables personalizadas&quot; a través de [nodos Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md). |

<b>Procesador de píxeles</b>

Variables del sistema

| Nombre | Tipo | Propósito |
| --- | --- | --- |
| $pos | Flotante 2 | Devuelve la posición del píxel que se está evaluando. |

<b>Global</b>

Variables del sistema

| Nombre | Tipo | Propósito |
| --- | --- | --- |
| $time | Flotante | Esta variable devuelve el tiempo en segundos desde que se inició el Substance Engine. Se puede utilizar en gráficos cuyo resultado debe cambiar según el tiempo transcurrido.  **Nota:** Aunque actualmente no hay forma de hacer este cambio de valor en Designer, las aplicaciones que integran el Substance Engine pueden aprovecharlo, como [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) para animación o [Substance 3D Painter](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/home) para [trazos dinámicos](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes). |
| $normalformat | Entero | El formato normal (es decir, DirectX u OpenGL) que se utiliza en el entorno actual.  **Nota:** Esta variable no tiene efecto en Designer y pueden utilizarla otras aplicaciones que integran el Substance Engine. |
