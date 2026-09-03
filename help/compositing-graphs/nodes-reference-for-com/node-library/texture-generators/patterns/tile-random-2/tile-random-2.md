---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random-2.html"
breadcrumb-title: ''
description: Utilice el nodo Mosaico aleatorio 2 para crear patrones de mosaico aleatorios con controles de variación avanzados en Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Azulejo aleatorio 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---


# Azulejo aleatorio 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random-2.resources/tile-random-2-01.jpg){width="200px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo **Tile Random 2** genera mosaicos adyacentes de tamaños aleatorios y proporciones de height a ancho.

La cuadrícula se puede retocar *inclinando* aleatoriamente los lados de las formas para romper los ángulos.

Las formas se pueden ajustar con opciones para *escalar*, *biselar*, *redondear las esquinas* y *rotar*.

Estos ajustes se pueden controlar mediante *mapas de entrada*.

Una salida dedicada le permite introducir los **UV** de la forma en el **Flood Fill a (...)** para aplicar variaciones adicionales.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Asignación de tamaño aleatorio</b> <i>Escala de grises</i> | Imagen de entrada de escala de grises que controla la escala aleatoria de las formas.<br><br>Su impacto se controla mediante el parámetro <b>Multiplicador de mapa de entrada de tamaño aleatorio</b>. |
| <b>Mapa de inclinación aleatoria</b> <i>Escala de grises</i> | Imagen de entrada de escala de grises que controla la inclinación aleatoria de las formas.<br><br>Su impacto se controla mediante el parámetro <b>Multiplicador de mapa de entrada de inclinación aleatoria</b>. |
| <b>Mapa de radio de vértices redondos</b> <i>Escala de grises</i> | Imagen de entrada de escala de grises que controla el radio de las esquinas redondeadas de las formas.<br><br>Su impacto está controlado por la variable <b>Round Corners Radius Input Map Mult.</b> parámetro. |
| <b>Mapa de distancia biselado</b> <i>Escala de grises</i> | Imagen de entrada de escala de grises que controla el biselado de las formas.<br><br>Su impacto se controla mediante la <b>Mult. de mapa de entrada de distancia biselada</b> parámetro. |
| <b>Mapa de máscara</b> <i>Escala de grises</i> | Imagen de entrada de escala de grises que controla el enmascaramiento de las formas.<br><br>Su impacto se controla mediante los parámetros <b>Inicio de entrada de mapa de máscara</b> y <b>Fin de entrada de mapa de máscara</b>. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Importe X</b> <i>Entero</i> | Número de celdas en el eje <b>X</b>. |
| <b>Importe Y</b> <i>Entero</i> | Número de celdas en el eje <b>Y</b>. |
| <b>Tamaño</b> |  |
| <b>Multiplicador de tamaño aleatorio</b> <i>Flotador</i> | Aplica un ajuste <i>global</i> a la intensidad de la escala aleatoria. |
| <b>Multiplicador de mapa de entrada de tamaño aleatorio</b> <i>Flotador</i> | Ajusta la intensidad de la escala aleatoria utilizando los valores <i>muestreados</i> de la entrada <b>Random Size Map</b>. |
| <b>Tamaño aleatorio X</b> <i>Flotador</i> | Ajusta la intensidad de la escala aleatoria en el eje <b>X</b> <i>solo</i>. |
| <b>Tamaño aleatorio Y</b> <i>Flotador</i> | Ajusta la intensidad de la escala aleatoria en el eje <b>Y</b> <i>solo</i>. |
| <b>Distribución de tamaño aleatorio</b> <i>Entero</i> | Controla el método de distribución de valores de escala aleatoria:<br><br>- <i>Uniforme</i>: la escala aleatoria se aplica de la <i>misma manera</i> en todas las celdas<br>- <i>Blue Noise</i>: la escala aleatoria está <i>ajustada</i> con un patrón de ruido azul |
| <b>Aspecto de forma - Transformar</b> |  |
| <b>Thickness intersticial</b> <i>Flotador</i> | Ajusta el thickness del espacio entre las formas. Es <i>igual para todas las formas</i>. |
| <b>Multiplicador de posición aleatoria</b> <i>Flotador</i> | Aplica un desplazamiento de posición aleatorio a la forma hasta que <i>cumpla con el borde de su celda</i>. |
| <b>Radio de vértices redondeados</b> <i>Flotador</i> | Ajusta el <i>radio</i> de las esquinas redondeadas de las formas. Un valor de <b>0</b> significa que no se aplica ningún redondeo.<br><br><i>Nota</i>: Este efecto no se puede aplicar cuando el parámetro <b>Habilitar control de bisel por eje</b> está establecido en <i>True</i>. |
| <b>Mapa de entrada de radio de vértices redondeados múltiple.</b> <i>Flotador</i> | Ajusta la intensidad con la que el mapa de entrada <b>Mapa de radio de vértices redondeados</b> afecta al radio de los vértices redondeados.<br><br>El mapa actúa como un multiplicador <i>por píxel</i> para el parámetro <b>Radio de vértices redondeados</b>.<br><br><i>Nota</i>: Este efecto no se puede aplicar cuando el parámetro <b>Habilitar control de bisel por eje</b> está establecido en <i>True</i>. |
| <b>Multiplicador de escala</b> <i>Flotador</i> | Ajusta el tamaño de cada forma como proporción del área <i>de su celda</i>. |
| <b>Escala aleatoria</b> <i>Flotador</i> | Ajusta la intensidad con la que se aplica una escala aleatoria a <i>cada forma</i>. |
| <b>Rotación</b> <i>Flotador</i> | Rota formas en sus celdas moviendo cada <i>esquina</i> a su <i>vecino</i> a lo largo del borde de la celda.<br><br>Este método hace que se aplique cierta cantidad de <i>distorsión</i> y <i>escala</i> a la forma en la que gira. |
| <b>Aleatorio de rotación</b> <i>Flotador</i> | Ajusta la intensidad con la que se aplica una cantidad aleatoria de rotación a cada forma.<br><br>El método de rotación se describe en el parámetro <b>Rotation</b>. |
| Posición aleatoria de <b>esquinas</b> <i>Flotador</i> | Distorsiona las formas aplicando una cantidad aleatoria de <i>offset</i> a cada una de sus <i>esquinas</i> a lo largo del borde de su celda. |
| <b>Inclinación</b> |  |
| <b>Multiplicador de inclinación aleatoria</b> <i>Flotador</i> | Aplica un ajuste <i>global</i> a la intensidad de la inclinación aleatoria. |
| <b>Multiplicador de mapa de entrada de inclinación aleatoria</b> <i>Flotador</i> | Ajusta la intensidad de la inclinación aleatoria utilizando los valores <i>muestreados</i> de la entrada <b>Mapa de inclinación aleatoria</b>. |
| <b>Inclinación Aleatoria X</b> <i>Flotador</i> | Ajusta la intensidad de la inclinación aleatoria en el eje <b>X</b> <i>solo</i>. |
| <b>Inclinación aleatoria Y</b> <i>Flotador</i> | Ajusta la intensidad de la inclinación aleatoria en el eje <b>Y</b> <i>solo</i>. |
| <b>Distribución de inclinación aleatoria</b> <i>Entero</i> | Controla el método de distribución de valores de inclinación aleatorios:<br><br>- <i>Uniforme</i>: la inclinación aleatoria se aplica de la <i>misma manera</i> en todas las celdas<br>- <i>Blue Noise</i>: la inclinación aleatoria está <i>ajustada</i> mediante un patrón de ruido azul |
| <b>Bisel</b> |  |
| <b>Modo de distancia biselada</b> <i>Entero</i> | Establece el método de <i>obtención de la distancia</i> por la que se deben biselar las formas:<br><br>- <i>Relativo al tamaño de cuadrícula</i>: Las formas están biseladas según la <i>proporción especificada de su tamaño de cuadrícula</i><br>- <i>Respecto al tamaño de forma</i>: Las formas están biseladas según la <i>proporción especificada de su tamaño</i><br>- <i>Respecto al tamaño de la imagen</i>: Las formas están biseladas según la <i>proporción especificada de la imagen</i> |
| <b>Multiplicador de distancia biselada</b> <i>Flotador</i> | Aplica un ajuste <i>global</i> a la distancia del biselado. |
| <b>Mapa de entrada de distancia biselada múltiple.</b> <i>Flotador</i> | Ajusta la distancia del biselado usando el mapa de entrada <b>Mapa de distancia de bisel</b> como multiplicador <i>por píxel</i>. |
| <b>Curva redondeada biselada</b> <i>Flotador</i> | Ajusta la intensidad del redondeo aplicado al ángulo de biselado para que sea más <i>convexo</i>. |
| <b>Habilitar control de bisel por eje</b> <i>Booleano</i> | Cuando <i>True</i>, el biselado se puede aplicar y ajustar <i>por separado</i> en los ejes <b>X</b> e <b>Y</b>.<br><br><i>Nota</i>: Este <i> cancela</i> el efecto <b>Vértices redondeados</b>. |
| <b>Distancia biselada X</b> <i>Flotador</i> | Ajusta la distancia del biselado en el eje <b>X</b> <i>solo</i>. Esta distancia depende del valor del parámetro <b>Modo de distancia biselada</b>.<br><br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Habilitar por control de bisel del eje</b> está establecido en <i>True</i>. |
| <b>Distancia biselada Y</b> <i>Flotador</i> | Ajusta la distancia del biselado en el eje <b>Y</b> <i>solo</i>. Esta distancia depende del valor del parámetro <b>Modo de distancia biselada</b>.<br><br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Habilitar por control de bisel del eje</b> está establecido en <i>True</i>. |
| <b>Máscara</b> |  |
| <b>Inversión aleatoria de máscara</b> <i>Booleano</i> | Invierte la máscara aleatoria de las formas. |
| <b>Inicio aleatorio de máscara</b> <i>Flotador</i> | Para una determinada <b>Raíz aleatoria</b>, se aplica una máscara pseudoaleatoria siguiendo un <i>orden específico</i> de una forma inicial a una forma final. Este parámetro le permite <i>desplazar el índice</i> de la forma <i>start</i>.<br><br><i>Nota</i>: Esto determina un límite de un <i>intervalo de valores</i> para enmascaramiento. Por lo tanto, el valor puede ser <i>mayor</i> que el valor <b>Final aleatorio de máscara</b>. |
| <b>Final aleatorio de máscara</b> <i>Flotador</i> | Para una determinada <b>Raíz aleatoria</b>, se aplica una máscara pseudoaleatoria siguiendo un <i>orden específico</i> de una forma inicial a una forma final. Este parámetro le permite <i>desplazar el índice</i> de la forma <i>end</i>.<br><br><i>Nota</i>: Esto determina un límite de un <i>intervalo de valores</i> para enmascaramiento. Por lo tanto, el valor puede ser <i>mayor</i> que el valor de <b>Inicio aleatorio de máscara</b>. |
| <b>Invertir máscara por área de celda</b> <i>Booleano</i> | Invierte el enmascaramiento de las formas por el área de sus celdas. |
| <b>Inicio de máscara por área de celda</b> <i>Flotador</i> | Ajusta el umbral de área de la celda <i>mínimo</i> para enmascarar formas.<br><br><i>Nota</i>: Esto determina un límite de un <i>intervalo de valores</i> para enmascaramiento. Por lo tanto, el valor puede ser <i>mayor</i> que el valor <b>Máscara por extremo del área de celda</b>. |
| <b>Enmascarar por fin de área de celda</b> <i>Flotador</i> | Ajusta el umbral de área de la celda <i>max</i> para enmascarar formas.<br><br><i>Nota</i>: Esto determina un límite de un <i>intervalo de valores</i> para enmascaramiento. Por lo tanto, el valor puede ser <i>inferior</i> al valor <b>Máscara por inicio del área de celdas</b>. |
| <b>Inversión de entrada de mapa de máscara</b> <i>Booleano</i> | Invierte el enmascaramiento de formas mediante el mapa de entrada <b>Mapa de máscara</b>. |
| <b>Inicio de entrada de mapa de máscara</b> <i>Flotador</i> | Ajusta el umbral de <i>valor mínimo de escala de grises</i> en el mapa de entrada <b>Mapa de máscara</b> para enmascarar formas.<br><br><i>Nota</i>: Esto determina un límite de un <i>intervalo de valores</i> para enmascaramiento. Por lo tanto, el valor puede ser <i>mayor</i> que el valor <b>Final de entrada de mapa de máscara</b>. |
| <b>Fin de entrada de mapa de máscara</b> <i>Flotador</i> | Ajusta el umbral de <i>valor máximo de escala de grises</i> en el mapa de entrada <b>Mapa de máscara</b> para enmascarar formas.<br><br><i>Nota</i>: Esto determina un límite de un <i>intervalo de valores</i> para enmascaramiento. Por lo tanto, el valor puede ser <i>inferior</i> al valor de <b>Inicio de entrada de mapa de máscara</b>. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tile-random-2-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tile-random-2-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tile-random-2-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tile-random-2-05.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tile-random-2-06.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tile-random-2-07.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tile-random-2-08.png" />
        </td>
    </tr>
</table>
