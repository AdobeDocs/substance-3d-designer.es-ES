---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---


# Salpicadura de forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter.png){width="128px"}

## Salpicadura de forma

**En:** *Generadores De Texturas**/Patrones*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Un nodo muy complejo, diseñado para usarse junto con los nodos adjuntos [Shape Splatter Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Shape Splatter to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) y [Shape Splatter Data Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md). Se usa para salpicar formas de una manera similar a [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) o [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), pero con un proceso dinámico y no destructivo que permite el control sobre cada paso, a través de un sistema de varios niveles similar a [Flood Fill.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) Mientras que Flood Fill toma un mapa de entrada base de un origen externo, Shape Splatter genera el mapa y los datos posteriores en un solo paso, como una especie de versión más avanzada de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Su propósito principal es permitir la colocación de formas en un mapa de height y guiado por él, y luego generar varios mapas a partir de los datos de salpicaduras. Por ejemplo, colocar rocas, ramas y hojas en un paisaje, orientado y gobernado por varios mapas. Diferentes mapas pueden ser utilizados para el height, normal, base, color, rugosidad y cualquier otro canal, mientras que todos se basan en los mismos datos compartidos Splatter.

## Parámetros

### Entradas

* **Height de fondo**: *Entrada en escala de grises* height de fondo para colocar los mosaicos y controlar diversos efectos.
* **Patrón 1-8**: *Entrada En Escala De Grises**Patrón Opcional*
* **Distribución De Patrones**: *Entrada en escala de grises* Mapa de escala de grises a
* **Escala de forma**: *Entrada de escala de grises* Mapa de escala de grises para escalar los azulejos de la unidad.
* **Rotación de forma**: *Entrada de escala de grises* Mapa de escala de grises para impulsar la rotación del azulejo.
* **Desplazamiento de Height**: *Entrada de escala de grises* Mapa de escala de grises que se usará como desplazamiento para el height de mosaico.
* **Escala de Height**: *Entrada de escala de grises* Mapa de escala de grises que se usará como desplazamiento para el height de mosaico.
* **Aleatorio de máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Mapa de vectores**: *Entrada de color* Mapa vectorial de color para controlar el posicionamiento y la rotación del azulejo.

### Parámetros

* **Cantidad X**: *1 - 64*\
  Cantidad de X repeticiones del patrón.
* **Importe Y**: *1 - 64*\
  Cantidad de repeticiones Y del patrón.
* **Patrón**
  * **Número de entrada de patrón**: *1 - 8* Define la cantidad de patrones diferentes para usar. Desbloquea nuevas ranuras de entrada de motivo.
  * **Modo De Distribución De Patrones**: *Aleatorio, Índice de motivo, Índice de línea, Índice de columna* Establezca cómo determinar qué modelo usar. Aleatoriamente o por patrón, línea o columna.
  * **Multiplicador de mapa de distribución de patrones**: *0.0 - 1.0* Establece la influencia del mapa de distribución opcional para la colocación de patrones.
  * **Rotación de motivo**: *0, 90, 180, 270* Ajuste preestablecido, rotación de 90 grados de los patrones.
  * **Aleatorio de rotación de motivo**: *0.0 - 1.0* Establezca la cantidad de rotación de pasos aleatoria de 90 grados para los patrones.
* **Tamaño**
  * **Escala**: *0.0 - 5.0*\
    Establece la escala uniforme para cada mosaico.
  * **Escala aleatoria**: *0.0 - 1.0* Aleatorizar escala uniforme para cada mosaico.
  * **Escalar sin superposición**: *0.0 - 1.0* Escala aleatoria uniformemente, pero solo hacia abajo, para evitar superposiciones de azulejos. No debe utilizarse junto con los dos parámetros anteriores.
  * **Multiplicador de mapa de escala**: *0.0 - 1.0* Establecer la influencia del mapa de escala.
  * **Tamaño**: *0.0 - 1.0* Permite el escalado no uniforme de los mosaicos.
  * **Proporción de tamaño de la Pendiente grande**: *0.0 - 1.0* Usa la pendiente de mapa de fondo (normal calculado) para escalar mosaicos de manera no uniforme. Simula la deformación de perspectiva.
  * **Proporción de tamaño por X/Y**: *0.0 - 1.0* Escala no uniforme para compensar una proporción diferente en las cantidades X e Y.
* **Posición**
  * **Posición aleatoria**: *0.0 - 2.0* Posición de desplazamiento aleatorio para cada mosaico.
  * **Distribución aleatoria**: *Gaussiano, uniforme* Establece el cálculo para el parámetro anterior. No hace una gran diferencia, más notable con números altos. El gaussiano tiende a dar una difusión más uniforme.
  * **Multiplicador de mapa vectorial**: *0.0 - 1.0* Influencia del mapa de entrada del vector en los desplazamientos.
  * **Desplazamiento horizontal**: *-2.0 - 2.0* Desplazamiento horizontal global.
  * **Desplazamiento vertical**: *-2.0 - 2.0* Desplazamiento vertical global.
  * **Opción Fuera de los límites**: *Escalar forma, Restringir posición* Acción que se debe realizar cuando un mosaico aparece fuera de los límites.
* **Rotación**
  * **Rotación**: *0.0 - 1.0* Gira globalmente todos los mosaicos.
  * **Aleatorio de rotación**: *0.0 - 1.0* Rota aleatoriamente por mosaico.
  * **Rotación desde Pendiente grande**: *0.0 - 1.0* Usa la pendiente de mapa de fondo (normal calculado) para rotar los mosaicos. Se puede utilizar para que las formas apunten hacia arriba o hacia abajo en las pendientes.
  * **Multiplicador de Mapa de rotación**: *0.0 - 1.0* Mezclas en el efecto del Mapa de rotación en la rotación por azulejo.
  * **Multiplicador de mapa vectorial**: *0.0 - 1.0* Mezclas en el efecto del Mapa de rotación en la rotación por azulejo.
* **Height**
  * **Ajuste automático de escala de Height**: *Falso/Verdadero* Ajusta automáticamente el intervalo de height en relación con el fondo, en lugar de definir un intervalo absoluto. Permite menos o más control.
  * **Desplazamiento de Height**: *-1.0 - 1.0* Modificador para desplazar o mover todos los mosaicos uniformemente a través del intervalo de height.
  * **Aleatorio de desplazamiento de Height**: *0.0 - 1.0* Cambia aleatoriamente el desplazamiento de height por mosaico.
  * **Multiplicador de mapa de desplazamiento de Height**: *0.0 - 1.0* Modificador para establecer la influencia del Mapa de desplazamiento.
  * **Escala de Height**: *0.0 - 1.0* Modificador para escalar o expandir todos los mosaicos uniformemente en el rango de height. Si se opone este desplazamiento, los valores se separan aún más, como el contraste.
  * **Escala aleatoria de Height**: *0.0 - 1.0* Cambia aleatoriamente la escala de height por mosaico.
  * **Multiplicador de mapa de escala de Height**: *0.0 - 1.0* Modificador para establecer la influencia del mapa de escala.
  * **Ajustar al fondo**: *0.0 - 1.0* Afecta a la combinación de mosaicos con el fondo. No conformar significa que los mapas de altura permanecen rígidos, conformar significa seguir la forma del fondo. Bueno para hojas vs palos, por ejemplo.
  * **Fondo conformado suave**: *0.0 - 2.0* Valor de suavizado para el efecto anterior, para evitar variaciones incorrectas o extremas.
  * **Sesgar desde Pendiente grande**: *0.0 - 1.0* height de mosaico de ajuste/pendiente controlado por la pendiente de fondo (normal calculado).
  * **Smoothness de Pendiente de fondo**: *0.0 - 2.0* Valor de suavizado para el efecto anterior, para evitar variaciones incorrectas o extremas.
  * **Píxeles negros recortados**: *False/True* Active esta opción para omitir los píxeles negros completos (0) de las formas base del mosaico.
  * **Acoplar base de patrón**: *Falso/Verdadero* Ajusta el comportamiento de fusión de azulejos con el fondo: los mosaicos se cruzarán con el fondo (False) o anularán el fondo cuando estén más bajos.
* **Enmascaramiento**
  * **Aleatorio de máscara**: *0.0 - 1.0* Oculta los mosaicos de forma aleatoria. Cuanto más alto sea este valor, más mosaicos desaparecerán.
  * **Multiplicador de mapa aleatorio de máscara**: *0.0 - 1.0* Umbral para el mapa de máscara cuando se empiezan a ocultar los mosaicos.
  * **Máscara de la Pendiente Big**: *-1.0 - 1.0* Usa la pendiente de mapa de fondo (normal calculado) para ocultar los mosaicos.

## Imágenes de ejemplo

</td>
</tr>
</table>
