---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: Utilice el nodo Sampler de mosaico para muestrear y organizar los mosaicos de las texturas de entrada para crear patrones de mosaico en Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sampler en mosaico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 6%

---


# Sampler en mosaico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-sampler.resources/tile-sampler.png){width="128px"}

<b>En:</b> Generadores De Texturas > Motivos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Tile Sampler es el nodo de generación de patrones de mosaico definitivo. Es una versión evolucionada y más compleja de [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). A partir de 2017 2.1, las diferencias son mucho menores entre Tile Sampler y [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Las principales diferencias están ahora solo en las siete ranuras de mapas diferentes que están disponibles para la escala de conducción, posición, rotación, tamaño, color y máscara. Su efecto se puede fusionar por separado.

El Sampler de mosaico es útil para crear patrones procedimientos creados por el hombre, con un control adicional sobre ciertos parámetros controlados por mapas de entrada externos.

Asegúrate de estar familiarizado con [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) antes de pasar al Sampler de mosaico. En la mayoría de los casos, encontrarás [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) suficiente y no necesitarás la complejidad añadida de Tile Sampler.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de patrón 1-6</b> <i>Entrada de escala de grises/entrada de color</i> | Imagen de patrón personalizado, utilizada cuando el parámetro &quot;Pattern&quot; se establece en &quot;Image Input&quot;.<br><br>La cantidad de entradas disponibles viene determinada por el parámetro <b>Pattern Input Number</b>. |
| <b>Entrada de mapa de escala</b> <i>Entrada en escala de grises</i> | Mapa de escala de grises para aplicar escala al azulejo. |
| <b>Entrada de mapa de Desplazamiento</b> <i>Entrada en escala de grises</i> | Mapa de escala de grises para controlar el desplazamiento del azulejo. |
| <b>Entrada de Mapa de rotación</b> <i>Entrada en escala de grises</i> | Mapa de escala de grises para controlar la rotación del azulejo. |
| <b>Entrada de mapa vectorial</b> <i>Entrada de color</i> | Mapa vectorial de color para controlar la escala no uniforme. |
| <b>Entrada de mapa de color</b> <i>Entrada de escala de grises/entrada de color</i> | Mapa para controlar el matiz por azulejo. |
| <b>Entrada de mapa de máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para ocultar ciertos azulejos. |
| <b>Entrada de mapa de distribución de patrones</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para controlar varias entradas de patrón personalizadas. |
| <b>Entrada en segundo plano</b> <i>Entrada de escala de grises/entrada de color</i> | Imagen de fondo opcional. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad X</b> <i>0 - 64</i> | Cantidad de repeticiones X del patrón. |
| <b>Importe Y</b> <i>0 - 64</i> | Cantidad de repeticiones Y del patrón. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |
| <b>Patrón</b> |  |
| <b>Patrón</b> <i>Entrada de patrón, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media campana, Campana con bordes, Media luna, Cápsula, Cono</i> | Selecciona la forma de motivo que se va a utilizar. |
| <b>Número de entrada de patrón</b> <i>1 - 6</i> | Cantidad de patrones personalizados entre los que elegir aleatoriamente. |
| <b>Distribución de entrada de patrón</b> <i>Aleatorio, Número de patrón, Mapa de distribución</i> | Define cómo se eligen varias entradas de patrón. Aleatorio significa que se ha elegido uno aleatorio, Número de patrón significa que se han colocado en una secuencia en bucle. El mapa de distribución utiliza una entrada de mapa en escala de grises para controlar la posición. |
| <b>Filtrado de entrada de patrón (Motor > v4)</b> <i>Bilineal + Mipmaps, Bilineal, Más Cercano</i> |  |
| <b>Específico del patrón</b> <i>0.0 - 1.0</i> | Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado. |
| <b>Aleatorio específico de motivo</b> <i>0.0 - 1.0</i> | El efecto de aleatorización depende del patrón seleccionado. |
| <b>Rotación</b> <i>0, 90, 180, 270</i> | Rotación escalonada (90 grados). |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Rotación libre aleatoria por unidad de medida. |
| <b>Aleatorio de Simetría</b> <i>0.0 - 1.0</i> | Define el número de mosaicos que se deben voltear o reflejar aleatoriamente según el comportamiento siguiente. |
| <b>Modo aleatorio de Simetría</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Determina el comportamiento de reflejo de la simetría. |
| <b>Tamaño</b> |  |
| <b>Modo de tamaño</b> <i>Normal, Mantener Proporción, Absoluta, Píxel</i> | Define el comportamiento general del tamaño del patrón.<br><br>Normal te permite definir el tamaño de los elementos de patrón. Se ve afectada por la cantidad X e Y.<br><br>Mantener proporción te permite establecer un tamaño afectado por la cantidad de X e Y, pero la proporción de X e Y entre los dos se deja intacta.<br><br>Absoluto te permite establecer un tamaño absoluto que no se vea afectado por la cantidad de X e Y.<br><br>Píxel te permite establecer un tamaño absoluto en píxeles, sin que la cantidad de X e Y te afecte. El cambio de la resolución afectará al tamaño de los elementos. |
| <b>Tamaño (Absoluto/Píxel)</b> <i>0.0 - 1.0</i> | Cambia las proporciones no uniformes de los mosaicos. El comportamiento exacto depende del modo Tamaño. |
| <b>Aleatorio de tamaño</b> <i>0.0 - 1.0</i> | Aleatoriza proporciones por azulejo. |
| <b>Escala</b> <i>0.0 - 10.0</i> | Establece la escala de mosaico global. |
| <b>Escala aleatoria</b> <i>0.0 - 1.0</i> | Aleatoriza la escala por azulejo. |
| <b>Multiplicador de mapa de escala</b> <i>0.0 - 1.0</i> | Fusiones en el efecto del mapa de escala. |
| <b>Multiplicador de mapa de vectores de escala</b> <i>0.0 - 1.0</i> | Fusiones en el efecto del mapa vectorial de escala para controlar la escala no uniforme. |
| <b>Efecto de parametrización de escala</b> <i>X e Y, X, Y</i> | Define los ejes a los que afecta la parametrización de escala. Se puede utilizar para que el mapa de escala solo afecte a X o Y de los elementos. |
| <b>Posición</b> |  |
| <b>Posición aleatoria</b> <i>0.0 - 10.0</i> | Aleatoriza la posición del azulejo en ambos ejes. |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Cambia los azulejos en función del tipo de desplazamiento. |
| <b>Tipo de desplazamiento</b> <i>quincux horizontal, quincux vertical, global horizontal, global vertical</i> | Cambia la dirección en la que funciona el desplazamiento. |
| <b>Desplazamiento global</b> <i>0.0 - 1.0</i> | Desplaza globalmente todos los mosaicos en los ejes X o Y. |
| <b>Intensidad del mapa de Desplazamiento</b> <i>0.0 - 1.0</i> | Fusiones en la intensidad del mapa de Desplazamiento en el desplazamiento. |
| <b>Ángulo de Desplazamiento</b> <i>0.0 - 1.0</i> | Define el ángulo en el que se va a desplazar. |
| <b>Desplazamiento de mapa vectorial</b> <i>0.0 - 1.0</i> | Utiliza mapa vectorial para controlar el desplazamiento y el ángulo. |
| <b>Rotación</b> |  |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Gira globalmente todos los mosaicos. |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Rota aleatoriamente por azulejo. |
| <b>Multiplicador de Mapa de rotación</b> <i>0.0 - 1.0</i> | Fusiones en el efecto del Mapa de rotación en la rotación por azulejo. |
| <b>Multiplicador de mapa vectorial</b> <i>0.0 - 1.0</i> | Usa Mapa vectorial para controlar la rotación por mosaico. |
| <b>Color</b> |  |
| <b>Umbral de asignación de máscara</b> <i>0.0 - 1.0</i> | Umbral del mapa de máscara cuando se empiezan a ocultar los mosaicos. |
| <b>Invertir mapa de máscara</b> <i>Falso/Verdadero</i> | Efecto Mapa de máscara invertida. |
| <b>Técnica de muestreo del mapa de máscara</b> <i>Centro de motivo, Cuadro delimitador de motivo (más lento)</i> | Si la ocultación debe estar determinada por un solo punto o por un cuadro delimitador. Evita que los píxeles aislados produzcan efectos extraños. |
| <b>Aleatorio de máscara</b> <i>0.0 - 1.0</i> | Máscara aleatoria, funciona en paralelo al mapa de máscara. |
| <b>Invertir máscara</b> <i>Falso/Verdadero</i> | Invierte la máscara aleatoria. |
| <b>Modo De Fusión</b> <i>Agregar/Inferior, Máx. (Sampler En Mosaico) / Agregar/Inferior, Fusión De Alpha (Color Sampler En Mosaico)</i> | Modo de Fusión para azulejos en el fondo y entre sí. |
| <b>Color</b> <i>(valor de escala de grises) / (valor de color)</i> | Color de azulejo global y sólido. |
| <b>Aleatorio de color/luminancia</b> <i>0.0 - 1.0</i> | Aleatorización del color, por azulejo. |
| <b>Modo de parametrización de color</b> <i>Entrada de color, Escala, Índice de línea, Índice de fila, Índice de motivo (Sampler de mosaico) / Mapa de color, Escala, Índice de línea, Índice de fila, Índice de motivo, Posición central del motivo, Posición central del motivo (RG) Tamaño de esfera (B) (Color de Sampler de mosaico)</i> | Define cómo se parametriza exactamente la aleatorización de color. |
| <b>Multiplicador de parametrización de color</b> <i>0.0 - 1.0</i> | Fusiones en el efecto de parametrización anterior. |
| <b>Efecto de parametrización de color (solo color)</b> <i>RGB+Alpha, solo RGB, solo Alpha</i> | Define cómo afecta la parametrización al color. |
| <b>Opacidad global (solo escala de grises)</b> <i>0.0 - 1.0</i> | Define la opacidad global del azulejo. |
| <b>Color de fondo</b> <i>(valor de escala de grises) / (valor de color)</i> | Define el color de fondo sólido. |
| <b>Orden de procesamiento inverso</b> <i>Falso/Verdadero</i> | Invierte el orden de procesamiento para ir de atrás hacia adelante. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-sampler.resources/tilesampler-ex2.png" /><br><i>El ejemplo muestra cómo se controlan los parámetros mediante mapas de entrada (distribución de patrones, escala, rotación).</i>
        </td>
    </tr>
</table>
