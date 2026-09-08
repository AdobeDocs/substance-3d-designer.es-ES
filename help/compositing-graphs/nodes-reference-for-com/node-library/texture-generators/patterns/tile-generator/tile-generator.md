---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-generator.html"
breadcrumb-title: ''
description: Utilice el nodo Tile Generator para crear patrones de mosaico de procedimientos con controles de tamaño, desplazamiento y variación personalizables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generador de mosaicos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 6%

---


# Generador de mosaicos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/tile-generator.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Tile Generator es uno de los nodos más avanzados de la biblioteca. Si aprendes a dominarlo, puedes crear cualquier tipo de patrón (dentro de algunas limitaciones). A partir de la versión 2017 2.1, ha habido algunas actualizaciones importantes, lo que pone a este nodo más en línea con lo que [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) puede hacer.

Este nodo es muy útil para una variedad de escenarios, pero tenga en cuenta que la simple lectura de parámetros no le enseñará completamente a usarlos. ¡Te sugerimos que experimentes también!

Para el 99% de todos los casos, la versión de color NO es necesaria!

Algunas sugerencias de uso general:

* Puedes empezar con una forma básica, pero si tienes una entrada personalizada (establece **Tipo de patrón** en *Entrada de imagen*), créala primero. Determina gran parte de la apariencia.
* Empieza por establecer correctamente tus cantidades X e Y.
* Encuentra el modo **Size** adecuado: Los modos relativos como **Intersticio** se comportan de manera muy diferente a los modos **Absoluto**.
* A continuación, ajuste la **escala** global y el **tamaño** no uniforme.
* Por último, modifique cualquier parámetro **&quot;Variation&quot;** hasta que cumpla sus necesidades. ¡La sutileza es clave con la variación!

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de patrón 1-6</b> <i>Entrada en escala de grises</i> | Imagen de motivo personalizado, utilizada cuando el parámetro &quot;Motivo&quot; se define en &quot;Entrada de imagen&quot;. |
| <b>Fondo</b> <i>Entrada en escala de grises</i> | Fondo que se va a utilizar en lugar de color sólido. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad X</b> <i>1 - 64</i> | Cantidad de repeticiones X del patrón. |
| <b>Importe Y</b> <i>1 - 64</i> | Cantidad de repeticiones Y del patrón. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |
| <b>Patrón</b> |  |
| <b>Patrón</b> <i>Entrada de imagen, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media campana, Campana con bordes, Media luna, Cápsula, Cono</i> | Selecciona la forma de motivo que se va a utilizar. |
| <b>Número de entrada de patrón</b> <i>1 - 6</i> | Número de entradas de imagen distintas que se van a utilizar. Solo está disponible cuando <i>Image Input</i> está seleccionado arriba. |
| <b>Distribución de entrada de patrón</b> <i>Aleatorio, Por Número De Motivo</i> | Cómo elegir entre las diferentes entradas de imagen, si hay más de 1 seleccionado. |
| <b>Específico del patrón</b> <i>0.0 - 1.0</i> | Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado. |
| <b>Filtrado de entrada de imágenes (motor > v4 únicamente)</b> <i>Bilineal + Mipmaps, Bilineal, Más Cercano</i> |  |
| <b>Rotación</b> <i>0, 90, 180, 270</i> | Gira todos los azulejos globalmente por un ángulo definido en pasos de 90 grados. |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Aleatoriamente gira un azulejo en uno de los cuatro pasos de 90 grados. |
| <b>Volteado de Quincunx</b> <i>Falso/Verdadero</i> | Rota cada dos mosaicos 90 grados. |
| <b>Aleatorio de Simetría</b> <i>0.0 - 1.0</i> | Refleja aleatoriamente determinados patrones en el modo aleatorio de Simetría seleccionado. Cuanto más alto sea este valor, más patrones se reflejarán. |
| <b>Modo aleatorio de Simetría</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Determina el comportamiento del reflejo cuando el valor aleatorio de Simetría es superior a 0. |
| <b>Tamaño</b> |  |
| <b>Modo de tamaño</b> <i>Normal - Intersticio, Normal - Tamaño, Mantener Proporción, Absoluto, Píxel</i> | Define el comportamiento general del tamaño del patrón.<br><br>Normal - Intersticio permite definir el espacio entre los elementos de patrón. Se ve afectada por la cantidad X e Y.<br><br>Normal - Tamaño permite definir el tamaño de los elementos de patrón, independientemente del espacio. Se ve afectada por la cantidad X e Y.<br><br>Mantener proporción te permite establecer un tamaño afectado por la cantidad de X e Y, pero la proporción de X e Y entre los dos se deja intacta.<br><br>Absoluto te permite establecer un tamaño absoluto que no se vea afectado por la cantidad de X e Y.<br><br>Píxel te permite establecer un tamaño absoluto en píxeles, sin que la cantidad de X e Y te afecte. El cambio de la resolución afectará al tamaño de los elementos. |
| <b>Tamaño medio</b> <i>0.0 - 1.0</i> | Cambia el tamaño alternando columna y fila. |
| <b>Intersticio X/Y</b> <i>0.0 - 1.0</i> | Solo disponible en el modo Normal - Tamaño intersticial. Cambia la brecha intersticial. Afecta a la unión entre las formas, permite un control no uniforme a diferencia de <b>Scale</b>. |
| <b>Tamaño (Absoluto/Píxel)</b> <i>0.0 - 1.0</i> | Solo disponible fuera del modo de tamaño normal - intersticio. Establece un tamaño no uniforme, a diferencia de <b>Scale</b>. |
| <b>Escala</b> <i>0.0 - 2.0</i> | Define la escala global. |
| <b>Escala aleatoria</b> <i>0.0 - 1.0</i> | Establece la variación de escala global por mosaico. |
| <b>Velocidad aleatoria de escala</b> <i>0 - 1000</i> | Desvíos de la variación de escala |
| <b>Posición</b> |  |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Desplaza todo el patrón de forma incremental en cada fila o columna consecutiva (el comportamiento depende del parámetro Desplazamiento vertical ). |
| <b>Desplazamiento aleatorio</b> <i>0.0 - 1.0</i> | Aleatoriza el desplazamiento de línea. |
| <b>Desplazar semilla aleatoria</b> <i>0 - 1000</i> | Cambia la velocidad relativa del efecto de compensación aleatoria. |
| <b>Desplazamiento vertical</b> <i>Falso/Verdadero</i> | Establece si el efecto Desplazamiento se produce sobre filas o líneas; Horizontal o Vertical. |
| <b>Posición aleatoria</b> <i>0.0 - 1.0</i> | Aleatoriza la posición de forma no uniforme, con control separado para X e Y. |
| <b>Desplazamiento global</b> <i>0.0 - 1.0</i> | Desplaza el resultado completo en los ejes X e Y. |
| <b>Rotación</b> |  |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Hace una rotación libre uniforme de todos los azulejos del patrón. |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Aleatoriza la rotación libre de todos los azulejos. Cuanto más alto sea este valor, más mosaicos se pueden girar. |
| <b>Color</b> |  |
| <b>Color</b> <i>(valor de escala de grises)</i> | Establece el color sólido del azulejo. |
| <b>Aleatorio de luminancia/color</b> <i>0.0 - 1.0</i> | Introduce la variación de color o luminancia por azulejo. |
| <b>Luminancia por número</b> <i>Falso/Verdadero</i> | Atenua la luminancia en todo el motivo. |
| <b>Luminancia Por Escala</b> <i>Falso/Verdadero</i> | La variación de luminancia depende de la escala del azulejo. |
| <b>Máscara de verificador</b> <i>Falso/Verdadero</i> | Oculta los demás azulejos. |
| <b>Máscara horizontal</b> <i>Falso/Verdadero</i> | Oculta todas las demás columnas. |
| <b>Máscara vertical</b> <i>Falso/Verdadero</i> | Oculta las filas alternas. |
| <b>Máscara aleatoria</b> <i>0.0 - 1.0</i> | Oculta los azulejos al azar. Cuanto más alto sea este valor, más mosaicos desaparecerán. |
| <b>Invertir máscara</b> <i>Falso/Verdadero</i> | Invierte el resultado de cualquier efecto de máscara de esta sección. |
| <b>Modo De Fusión</b> <i>Agregar, Máx., Agregar Sub</i> | Define el modo de fusión que se va a utilizar. |
| <b>Color de fondo</b> <i>(valor de escala de grises)</i> | Define el color de fondo sólido. |
| <b>Opacidad global</b> <i>0.0 - 1.0</i> | Establece la opacidad de los mosaicos globales. |
| <b>Orden de procesamiento inverso</b> <i>Falso/Verdadero</i> | Procesa los mosaicos de vuelta al frente o viceversa. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilesampler-ex.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2020-9-17-14-50-18.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2020-9-17-14-52-4.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2020-9-17-14-53-47.png" />
        </td>
    </tr>
</table>
