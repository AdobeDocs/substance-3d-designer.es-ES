---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# Sampler en mosaico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

## Sampler en mosaico (color)

**En:** *Generadores De Texturas**/Patrones*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Tile Sampler es el nodo de generación de patrones de mosaico definitivo. Es una versión evolucionada y más compleja de [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). A partir de 2017 2.1, las diferencias son mucho menores entre Tile Sampler y [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Las principales diferencias están ahora solo en las siete ranuras de mapas diferentes que están disponibles para la escala de conducción, posición, rotación, tamaño, color y máscara. Su efecto se puede fusionar por separado.

El Sampler de mosaico es útil para crear patrones de procedimientos creados por el hombre, con un control adicional sobre ciertos parámetros controlados por mapas de entrada externos.

Asegúrate de estar familiarizado con [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) antes de pasar al Sampler de mosaico. En la mayoría de los casos, encontrarás [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) suficiente y no necesitarás la complejidad añadida de Tile Sampler.

## Parámetros

### Entradas

* **Entrada de patrón 1-6**: *Entrada de escala de grises/entrada de color*\
  Imagen de motivo personalizado, utilizada cuando el parámetro &quot;Motivo&quot; se define en &quot;Entrada de imagen&quot;.\
  La cantidad de entradas disponibles viene determinada por el parámetro **Número de entrada de patrón**.
* **Entrada de mapa de escala**: *Entrada de escala de grises* Mapa de escala de grises para escalar los azulejos de la unidad.
* **Entrada de mapa de Desplazamiento**: *Entrada de escala de grises* Mapa de escala de grises para controlar el desplazamiento del azulejo.
* **Entrada de Mapa de rotación**: *Entrada en escala de grises*\
  Mapa de escala de grises para controlar la rotación del azulejo.
* **Entrada de mapa vectorial**: *Entrada de color*\
  Mapa vectorial de color para controlar la escala no uniforme.
* **Entrada de mapa de color**: *Entrada de escala de grises / Entrada de color* Asignar a matiz por mosaico de unidad.
* **Entrada de mapa de máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para ocultar ciertos azulejos.
* **Entrada de mapa de distribución de patrones**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para controlar varias entradas de patrón personalizadas.
* **Entrada en segundo plano**: *Entrada de escala de grises/entrada de color* Imagen de fondo opcional.

### Parámetros

* **Cantidad X**: *0 - 64*\
  Cantidad de repeticiones X del patrón.
* **Importe Y**: *0 - 64*\
  Cantidad de repeticiones Y del patrón.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas.
* **Patrón**
  * **Patrón**: *Entrada De Patrón, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media Campana, Campana Cortada, Media Luna, Cápsula, Cono*\
    Selecciona la forma de motivo que se va a utilizar.
  * **Número de entrada de patrón**: *1 - 6* Cantidad de patrones personalizados entre los que elegir al azar.
  * **Distribución De Entrada De Patrón**: *Aleatorio, Número de patrón, Mapa de distribución* Establece cómo se eligen las múltiples entradas de patrón. Aleatorio significa que se ha elegido uno aleatorio, Número de patrón significa que se han colocado en una secuencia en bucle. El mapa de distribución utiliza una entrada de mapa en escala de grises para controlar la posición.
  * **Filtrado de entrada de patrón (Motor > v4)**: *Bilineal + Mipmaps, Bilineal, Más Cercano*
  * **Específico del patrón**: *0.0 - 1.0*\
    Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado.
  * **Aleatorio específico de patrón**: *0.0 - 1.0* El efecto de aleatorización depende del patrón seleccionado.
  * **Rotación**: *0, 90, 180, 270* Rotación escalonada (90 grados).
  * **Aleatorio de rotación**: *0.0 - 1.0* Rotación libre aleatoria por mosaico.
  * **Aleatorio de simetría**: *0.0 - 1.0* Establece el número de mosaicos que se deben voltear o reflejar aleatoriamente de acuerdo con el comportamiento siguiente.
  * **Modo aleatorio de simetría**: *Horizontal + Vertical, Horizontal, Vertical* Determina el comportamiento de reflejo de la simetría.
* **Tamaño**
  * **Modo de tamaño**: *Normal, Mantener proporción, Absoluto, Píxel* Establece el comportamiento general del tamaño del patrón.\
    Normal permite definir el tamaño de los elementos de patrón. Se ve afectada por la cantidad X e Y.\
    Mantener proporción le permite establecer un tamaño afectado por la cantidad de X e Y, pero la proporción de X e Y entre los dos se deja intacta.\
    Absoluto le permite establecer un tamaño absoluto que no se vea afectado por la cantidad X e Y.\
    El píxel le permite establecer un tamaño absoluto en píxeles, sin que se vea afectado por la cantidad de X e Y. El cambio de la resolución afectará al tamaño de los elementos.
  * **Tamaño (absoluto/píxel)**: *0.0 - 1.0* Cambia las proporciones no uniformes de los mosaicos. El comportamiento exacto depende del modo Tamaño.
  * **Aleatorio de tamaño**: *0.0 - 1.0* Aleatoriza las proporciones por mosaico.
  * **Escala**: *0.0 - 10.0* Establece la escala de mosaico global.
  * **Escala aleatoria**: *0.0 - 1.0* Aleatoriza la escala por mosaico
  * **Multiplicador de mapa de escala**: *0.0 - 1.0* Mezcla el efecto del mapa de escala.
  * **Multiplicador de mapa de vectores de escala**: *0.0 - 1.0* Fusiona el efecto del mapa vectorial de escala para generar una escala no uniforme.
  * **Efecto de parametrización de escala**: *X e Y, X, Y* Establece los ejes a los que afecta la parametrización de escala. Se puede utilizar para que el mapa de escala solo afecte a X o Y de los elementos.
* **Posición**
  * **Posición aleatoria**: *0.0 - 10.0* Aleatoriza la posición del azulejo sobre ambos ejes.
  * **Desplazamiento**: *0.0 - 1.0*\
    Cambia los azulejos en función del tipo de desplazamiento.
  * **Tipo de desplazamiento**: *quincux horizontal, quincux vertical, global horizontal, global vertical* Cambia la dirección en la que funciona el desplazamiento.
  * **Desplazamiento global**: *0.0 - 1.0* Desfasa globalmente todos los mosaicos de los ejes X o Y.
  * **Intensidad del mapa de Desplazamiento**: *0.0 - 1.0* Se mezcla en la intensidad del mapa de Desplazamiento en el desplazamiento.
  * **Ángulo de Desplazamiento**: *0.0 - 1.0* Establece el ángulo en el que se va a desplazar.
  * **Desplazamiento de mapa vectorial**: *0.0 - 1.0* Usa mapa vectorial para controlar el desplazamiento y el ángulo.
* **Rotación**
  * **Rotación**: *0.0 - 1.0* Gira globalmente todos los mosaicos.
  * **Aleatorio de rotación**: *0.0 - 1.0* Rota aleatoriamente por mosaico.
  * **Multiplicador de Mapa de rotación**: *0.0 - 1.0* Mezclas en el efecto del Mapa de rotación en la rotación por azulejo.
  * **Multiplicador de mapa vectorial**: *0.0 - 1.0* Usa Mapa de vectores para controlar la rotación por mosaico.
* **Color**
  * **Umbral de asignación de máscara**: *0.0 - 1.0* Umbral para el mapa de máscara cuando se empiezan a ocultar los mosaicos.
  * **Invertir mapa de máscara**: *Falso/Verdadero* Efecto de mapa de máscara invertida.
  * **Técnica de muestreo del mapa de máscara**: *Centro de motivo, Cuadro delimitador de motivo (más lento)*Si la ocultación debe estar determinada por un solo punto o por un cuadro delimitador. Evita que los píxeles aislados produzcan efectos extraños.
  * **Aleatorio de máscara**: *0.0 - 1.0* Enmascaramiento aleatorio, funciona en paralelo al mapa de máscara.
  * **Invertir máscara**: *Falso/Verdadero* Invierte las máscaras aleatorias.
  * **Modo De Fusión**: *Agregar/Inferior, Máx. (Sampler de mosaico) /* Agregar/Inferior, Fusión de Alpha* (Color de Sampler de mosaico)*Modo de fusión para mosaicos en fondo y entre sí.
  * **Color**: *(Valor de escala de grises) / (Valor de color)*Color de azulejo global sólido.
  * **Aleatorio de color/luminancia**: *0.0 - 1.0* Aleatorización del color, por mosaico.
  * **Modo de parametrización de color**: *Entrada de color, escala, índice de línea, índice de fila, índice de motivo (Sampler de mosaico)*\
    */*Mapa de color, Escala, Índice de línea, Índice de fila, Índice de motivo, Posición central del motivo, Posición central del motivo (RG) Tamaño de esfera (B) (Color de Sampler de azulejo)**Define cómo se parametriza exactamente la aleatorización del color.
  * **Multiplicador de parametrización de color**: *0.0 - 1.0* Fusiones en el efecto de parametrización anterior.
  * **Efecto de parametrización de color (solo color):** **RGB+Alpha, solo RGB, solo Alpha** Establece cómo afecta la parametrización al color.
  * **Opacidad global (solo escala de grises)**: *0.0 - 1.0* Establece la opacidad del mosaico global.
  * **Color de fondo**: *(Valor de escala de grises) / (Valor de color)*Define el color de fondo sólido.
  * **Orden de procesamiento inverso**: *Falso/Verdadero* Invierte el orden de procesamiento para ir de atrás hacia adelante.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tilesampler-ex2.png" width="256px"/></div> |
| --- |
|  |

*El ejemplo muestra cómo se controlan los parámetros mediante mapas de entrada (distribución de patrones, escala, rotación).*

</td>
</tr>
</table>
