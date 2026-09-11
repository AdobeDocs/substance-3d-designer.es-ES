---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: Utilice el nodo circular de salpicadura para crear formas circulares de dispersión entre texturas y así crear patrones orgánicos y aleatorios.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Splatter Circular
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 8%

---


# Splatter Circular

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter-circular.resources/splatter-circular.png){width="128px"}

![](splatter-circular.resources/splatter-circular-color.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Splatter Circular genera un patrón basado en anillo con varios controles. Puede utilizar formas predefinidas o entradas personalizadas. Es similar a [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), pero con una ubicación circular en lugar de una cuadrícula.

Esto resulta útil para colocar formas de forma circular con varias opciones de aleatorización.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

Ambas entradas son opcionales.

|  |  |
|:---|:---|
| <b>Entrada de imagen de motivo 1-6</b> <i>Entrada de escala de grises (entrada de color)</i> | Sólo Splatter Circular: Imagen de motivo personalizado, utilizada cuando el parámetro &quot;Motivo&quot; se define en &quot;Entrada de imagen&quot;. |
| <b>Fondo</b> <i>Entrada de escala de grises (entrada de color)</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad de patrón</b> <i>1 - 64</i> | Cantidad de mosaicos de motivo que se deben colocar en un anillo. |
| <b>Aleatorio de cantidad de patrón</b> <i>0.0 - 1.0</i> | Aleatorización de la cantidad de patrones a colocar. Se recomienda utilizarlo con una cantidad de anillo superior a 1. |
| <b>Nivel De Patrón Aleatorio Mínimo</b> <i>1 - 10</i> | Define la cantidad mínima de patrones para la aleatorización. |
| <b>Cantidad de anillo</b> <i>1 - 10</i> | Establece el número de anillos que se van a rellenar. Los anillos siempre se colocan dentro del exterior, y el espacio uniformemente. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |
| <b>Patrón</b> |  |
| <b>Patrón</b> <i>Entrada de imagen, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media campana, Campana con bordes, Media luna, Cápsula, Cono</i> | Selecciona la forma de motivo que se va a utilizar. |
| <b>Número de entrada de patrón</b> <i>1 - 6</i> | Define el número de entradas de imagen diferentes que se utilizarán. Solo está disponible cuando <i>Image Input</i> está seleccionado arriba. |
| <b>Distribución de entrada de patrón</b> <i>Aleatorio, Por Número De Motivo, Por Número De Anillo</i> | Define cómo se eligen varias entradas de patrón. Aleatorio significa que se elige uno aleatorio, Número de patrón significa que se colocan en una secuencia de bucle, Por números de anillo significa que cada anillo tiene uno diferente en la secuencia. |
| <b>Filtrado de entrada de imagen</b> <i>Bilineal + Mipmaps, Bilineal, Más Cercano</i> |  |
| <b>Específico del patrón</b> <i>0.0 - 1.0</i> | Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado. |
| <b>Aleatorio de Simetría</b> <i>0.0 - 1.0</i> | Define el número de mosaicos que se deben voltear o reflejar aleatoriamente según el comportamiento siguiente. |
| <b>Modo aleatorio de Simetría</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Determina el comportamiento de reflejo de la simetría. |
| <b>Posición</b> |  |
| <b>Radio</b> <i>0.0 - 1.0</i> | Define el radio desde el centro en el que se colocan los motivos. |
| <b>Aleatorio de radio</b> <i>0.0 - 1.0</i> | Aleatoriza el radio de cada mosaico de motivo. |
| <b>Multiplicador de radio de anillo</b> <i>0.0 - 1.0</i> | Afecta al espaciado de varios anillos. |
| <b>Ángulo aleatorio</b> <i>0.0 - 1.0</i> | Aleatoriza el ángulo de cada motivo. Una cantidad mayor significa más rotación. |
| <b>Factor de espiral</b> <i>0.0 - 1.0</i> | Convierte los anillos en espirales, donde cada azulejo se coloca en un radio ligeramente creciente. |
| <b>Difusión</b> <i>0.0 - 2.0</i> | Define la cantidad de vueltas que realiza un anillo. Esto puede aumentarse más allá de sus límites. |
| <b>Desplazamiento en la dirección</b> <i>0.0 - 1.0</i> | Desplaza cada motivo fuera del centro a lo largo de su ángulo. El efecto depende en gran medida del ángulo aleatorio, o se parece a un multiplicador para el radio. |
| <b>Desplazamiento global</b> <i>0.0 - 1.0</i> | Traduce toda la forma. |
| <b>Tamaño</b> |  |
| <b>Patrones de conexión</b> <i>Falso/Verdadero</i> | Hace que la longitud de los mosaicos de motivo dependa del radio, lo que significa que cada forma debe tocar la anterior y la siguiente. |
| <b>Tamaño (conectado)</b> <i>0.0 - 1.0</i> | Cambia el tamaño de cada patrón globalmente. Cuando está conectado, es relativo al radio total. |
| <b>Aleatorio de tamaño</b> <i>0.0 - 1.0</i> | Aleatoriza el tamaño de cada motivo de forma individual. |
| <b>Escala</b> <i>0.0 - 2.0</i> | Ajusta uniformemente cada patrón. |
| <b>Escala aleatoria</b> <i>0.0 - 1.0</i> | Aleatoriza la escala uniforme. |
| <b>Escalar por número de patrón</b> <i>0.0 - 1.0</i> | Hace que la escala del patrón dependa de la posición a lo largo del anillo. |
| <b>Invertir número de patrón</b> <i>Falso/Verdadero</i> | Si se utiliza con la opción anterior, se puede invertir la escala de pequeña a grande y viceversa. |
| <b>Escalar por número de anillo</b> <i>0.0 - 1.0</i> | Hace que la escala dependa del número de anillo. |
| <b>Invertir número de anillo</b> <i>Falso/Verdadero</i> | Si se utiliza con la opción anterior, puede invertir la escala de pequeña a grande y viceversa. |
| <b>Rotación</b> |  |
| <b>Rotación de motivo</b> <i>0.0 - 1.0</i> | Rota todos los patrones uniformemente. |
| <b>Aleatorio de rotación de motivo</b> <i>0.0 - 1.0</i> | Aleatoriza la rotación de patrones. |
| <b>Tabla dinámica de rotación de motivo</b> <i>Centro, Mín. X, Máx. X, Mín. Y, Máx. Y</i> | Define la posición del punto de giro alrededor del cual se giran los motivos de forma individual. |
| <b>Orientación central</b> <i>Falso/Verdadero</i> | Gira cada motivo de forma que mire hacia el centro del anillo. Al desactivarla, se les aplica la misma orientación, lo que puede producir efectos no deseados con Desplazamiento en la dirección. |
| <b>Rotación de anillo</b> <i>0.0 - 1.0</i> | Gira todo el anillo alrededor del centro. |
| <b>Rotación aleatoria de anillo</b> <i>0.0 - 1.0</i> | Aleatoriza la rotación por anillo. |
| <b>Desplazamiento de rotación de anillo</b> <i>0.0 - 1.0</i> | Desplaza la rotación por anillo. |
| <b>Color</b> |  |
| <b>Color</b> <i>(valor de escala de grises)</i> | Color que se va a multiplicar por el motivo seleccionado. |
| <b>Aleatorio de luminancia</b> <i>0.0 - 1.0</i> | Aleatoriza el color o la luminancia de cada mosaico de motivo. |
| <b>Luminancia Por Escala</b> <i>0.0 - 1.0</i> | Hace que la luminancia dependa de la escala de motivo individual. |
| <b>Luminancia por número de patrón</b> <i>0.0 - 1.0</i> | Hace que la luminancia dependa de la secuencia del motivo. Se puede utilizar, por ejemplo, con espirales. |
| <b>Invertir número de patrón</b> <i>Falso/Verdadero</i> | Invierte la opción anterior. |
| <b>Luminancia por número de anillo</b> <i>0.0 - 1.0</i> | Hace que la luminancia dependa de la secuencia de anillos. |
| <b>Invertir número de anillo</b> <i>Falso/Verdadero</i> | Invierte la opción anterior. |
| <b>Máscara aleatoria</b> <i>0.0 - 1.0</i> | Oculta patrones al azar. |
| <b>Color de fondo</b> <i>(valor de escala de grises)</i> | Cambia el color de fondo sólido. |
| <b>Modo De Fusión</b> <i>Agregar, Máx., Agregar Sub</i> | Define cómo mezclar patrones superpuestos. |
| <b>Opacidad global</b> <i>0.0 - 1.0</i> | Establece la opacidad global de todo el resultado. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter-circular.resources/circularsplatter-ex.png" />
        </td>
    </tr>
</table>
