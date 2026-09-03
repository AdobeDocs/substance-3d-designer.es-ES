---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Utilice el nodo Dispersión de formas para crear formas y dispersiones entre texturas para crear patrones y detalles de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Salpicadura de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# Salpicadura de forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter.resources/shape-splatter-01.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Un nodo muy complejo, diseñado para usarse junto con los nodos adjuntos [Shape Splatter Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Shape Splatter to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) y [Shape Splatter Data Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md). Se usa para salpicar formas de una manera similar a [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) o [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), pero con un proceso dinámico y no destructivo que permite el control sobre cada paso, a través de un sistema de varios niveles similar a [Flood Fill.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) Mientras que Flood Fill toma un mapa de entrada base de un origen externo, Shape Splatter genera el mapa y los datos posteriores en un solo paso, como una especie de versión más avanzada de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Su propósito principal es permitir la colocación de formas en un mapa de height y guiado por él, y luego generar varios mapas a partir de los datos de salpicaduras. Por ejemplo, colocar rocas, ramas y hojas en un paisaje, orientado y gobernado por varios mapas. Diferentes mapas pueden ser utilizados para el height, normal, base, color, rugosidad y cualquier otro canal, mientras que todos se basan en los mismos datos compartidos Splatter.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height de fondo</b> <i>Entrada en escala de grises</i> | Height de fondo para colocar los azulejos y aplicar diversos efectos. |
| <b>Patrón 1-8</b> <i>Entrada en escala de grises</i> | Patrón opcional |
| <b>Distribución De Patrones</b> <i>Entrada en escala de grises</i> | Asignación en escala de grises a |
| <b>Escala de forma</b> <i>Entrada en escala de grises</i> | Mapa de escala de grises para aplicar escala al azulejo. |
| <b>Rotación de forma</b> <i>Entrada en escala de grises</i> | Mapa de escala de grises para controlar la rotación del azulejo. |
| <b>Desplazamiento de Height</b> <i>Entrada en escala de grises</i> | Mapa de escala de grises que se va a utilizar como desplazamiento para el height de mosaico. |
| <b>Escala de Height</b> <i>Entrada en escala de grises</i> | Mapa de escala de grises que se va a utilizar como desplazamiento para el height de mosaico. |
| <b>Aleatorio de máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |
| <b>Mapa de vectores</b> <i>Entrada de color</i> | Mapa vectorial de color para controlar el posicionamiento y la rotación del azulejo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad X</b> <i>1 - 64</i> | Cantidad de X repeticiones del patrón. |
| <b>Importe Y</b> <i>1 - 64</i> | Cantidad de repeticiones Y del patrón. |
| <b>Patrón</b> |  |
| <b>Número de entrada de patrón</b> <i>1 - 8</i> | Define la cantidad de patrones diferentes que quieres usar. Desbloquea nuevas ranuras de entrada de motivo. |
| <b>Modo de distribución de patrones</b> <i>Aleatorio, Índice de motivo, Índice de línea, Índice de columna</i> | Establezca cómo determinar qué patrón usar. Aleatoriamente o por patrón, línea o columna. |
| <b>Multiplicador de mapa de distribución de patrones</b> <i>0.0 - 1.0</i> | Defina la influencia del mapa de distribución opcional para la colocación de los motivos. |
| <b>Rotación de motivo</b> <i>0, 90, 180, 270</i> | Ajuste preestablecido, rotación de 90 grados de los patrones. |
| <b>Aleatorio de rotación de motivo</b> <i>0.0 - 1.0</i> | Establezca la cantidad de rotación de pasos aleatoria de 90 grados para los patrones. |
| <b>Tamaño</b> |  |
| <b>Escala</b> <i>0.0 - 5.0</i> | Establece la escala uniforme para cada mosaico. |
| <b>Escala aleatoria</b> <i>0.0 - 1.0</i> | Aleatorizar escala uniforme para cada azulejo. |
| <b>Escalar sin superposición</b> <i>0.0 - 1.0</i> | Escale aleatoriamente de manera uniforme, pero solo hacia abajo, para evitar la superposición de mosaicos. No debe utilizarse junto con los dos parámetros anteriores. |
| <b>Multiplicador de mapa de escala</b> <i>0.0 - 1.0</i> | Definir la influencia del mapa de escala. |
| <b>Tamaño</b> <i>0.0 - 1.0</i> | Permite el escalado no uniforme de los azulejos. |
| <b>Proporción de tamaño de la Pendiente grande</b> <i>0.0 - 1.0</i> | Utiliza la pendiente de mapa de fondo (normal calculado) para escalar mosaicos de manera no uniforme. Simula la deformación de perspectiva. |
| <b>Proporción de tamaño por X/Y</b> <i>0.0 - 1.0</i> | Escala no uniforme para compensar una proporción diferente en los importes X e Y. |
| <b>Posición</b> |  |
| <b>Posición aleatoria</b> <i>0.0 - 2.0</i> | Posición de desplazamiento aleatorio para cada azulejo. |
| <b>Distribución aleatoria</b> <i>Gaussiano, uniforme</i> | Establece el cálculo que se va a utilizar para el parámetro anterior. No hace una gran diferencia, más notable con números altos. El gaussiano tiende a dar una difusión más uniforme. |
| <b>Multiplicador de mapa vectorial</b> <i>0.0 - 1.0</i> | Influencia del mapa de entrada del vector en los desplazamientos. |
| <b>Desplazamiento horizontal</b> <i>-2.0 - 2.0</i> | Desplazamiento horizontal global. |
| <b>Desplazamiento vertical</b> <i>-2.0 - 2.0</i> | Desplazamiento vertical global. |
| <b>Opción Fuera de los límites</b> <i>Escalar forma, Restringir posición</i> | Acción que se realiza cuando un mosaico aparece Fuera de los límites. |
| <b>Rotación</b> |  |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Gira globalmente todos los mosaicos. |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Rota aleatoriamente por azulejo. |
| <b>Rotación desde Pendiente grande</b> <i>0.0 - 1.0</i> | Utiliza la pendiente de mapa de fondo (normal calculado) para rotar los mosaicos. Se puede utilizar para que las formas apunten hacia arriba o hacia abajo en las pendientes. |
| <b>Multiplicador de Mapa de rotación</b> <i>0.0 - 1.0</i> | Fusiones en el efecto del Mapa de rotación en la rotación por azulejo. |
| <b>Multiplicador de mapa vectorial</b> <i>0.0 - 1.0</i> | Fusiones en el efecto del Mapa de rotación en la rotación por azulejo. |
| <b>Height</b> |  |
| Ajuste automático de la escala de Height <b>Scale</b> <i>Falso/Verdadero</i> | Ajuste automáticamente el rango de height en relación con el fondo, en lugar de definir un rango absoluto. Permite menos o más control. |
| <b>Desplazamiento de Height</b> <i>-1.0 - 1.0</i> | Modificador para desplazar o mover todos los mosaicos uniformemente por el rango de height. |
| <b>Aleatorio de desplazamiento de Height</b> <i>0.0 - 1.0</i> | Cambia aleatoriamente el desplazamiento de height por mosaico. |
| <b>Multiplicador de mapa de desplazamiento de Height</b> <i>0.0 - 1.0</i> | Modificador para definir la influencia del mapa de desvío. |
| <b>Escala de Height</b> <i>0.0 - 1.0</i> | Modificador para escalar o expandir todos los mosaicos de manera uniforme en el rango de height. Si se opone este desplazamiento, los valores se separan aún más, como el contraste. |
| <b>Escala aleatoria de Height</b> <i>0.0 - 1.0</i> | Cambia aleatoriamente la escala de height por mosaico. |
| <b>Multiplicador de mapa de escala de Height</b> <i>0.0 - 1.0</i> | Modificador para definir la influencia del mapa de escala. |
| <b>Ajustar al fondo</b> <i>0.0 - 1.0</i> | Afecta a la mezcla de azulejos con el fondo. No conformar significa que los mapas de altura permanecen rígidos, conformar significa seguir la forma del fondo. Bueno para hojas vs palos, por ejemplo. |
| <b>Fondo conformado suave</b> <i>0.0 - 2.0</i> | Valor de suavizado del efecto anterior para evitar variaciones incorrectas o extremas. |
| <b>Sesgar desde Pendiente grande</b> <i>0.0 - 1.0</i> | Ajuste/ pendiente del height del azulejo controlado por la pendiente de fondo (normal calculado). |
| <b>Smoothness de Pendiente de fondo</b> <i>0.0 - 2.0</i> | Valor de suavizado del efecto anterior para evitar variaciones incorrectas o extremas. |
| <b>Píxeles negros recortados</b> <i>Falso/Verdadero</i> | Active esta opción para ignorar los píxeles negros completos (0) de las formas de base de mosaico. |
| <b>Acoplar base de patrones</b> <i>Falso/Verdadero</i> | Ajusta el comportamiento de fusión de azulejos con el fondo: los mosaicos se cruzarán con el fondo (False) o anularán el fondo cuando estén más bajos. |
| <b>Enmascaramiento</b> |  |
| <b>Aleatorio de máscara</b> <i>0.0 - 1.0</i> | Oculta los azulejos al azar. Cuanto más alto sea este valor, más mosaicos desaparecerán. |
| <b>Multiplicador de mapa aleatorio de máscara</b> <i>0.0 - 1.0</i> | Umbral para el mapa de máscara cuando se empiezan a ocultar los azulejos. |
| <b>Máscara de la Pendiente Big</b> <i>-1.0 - 1.0</i> | Utiliza la pendiente de mapa de fondo (normal calculado) para ocultar los mosaicos. |
