---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: Utilice el nodo Azulejo aleatorio para crear patrones de azulejo aleatorios con variación de procedimiento para los efectos de textura orgánica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Azulejo aleatorio
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---


# Azulejo aleatorio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

## Azulejo aleatorio (color)

**En:** *Generadores/Patrones*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Tile Random genera un patrón de mosaico de procedimiento que tiene un poco más de caos en las formas de mosaico que su contraparte, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Esto lo hace dividiendo aleatoriamente ciertos azulejos en azulejos más pequeños. Le sugerimos que primero encuentre su camino alrededor de Tile Generator antes de abordar Tile Random, ya que muchos conceptos son similares.

Se utiliza Tile Random en lugar de [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) cuando el objetivo es un patrón más antiguo y menos organizado. Sin embargo, tiene sus limitaciones, así que considera [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) para cualquier otra necesidad avanzada.

## Parámetros

### Entradas

* **Entrada de patrón**: *Entrada en escala de grises (entrada de color)*\
  Imagen de motivo personalizado, utilizada cuando el parámetro &quot;Motivo&quot; se define en &quot;Entrada de imagen&quot;.
* **Entrada en segundo plano**: *Entrada en escala de grises (entrada de color)*

### Parámetros

* **Cantidad X**: *1 - 64*\
  Cantidad de repeticiones X del patrón.
* **Importe Y**: *1 - 64*\
  Cantidad de repeticiones Y del patrón.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas.
* **Patrón**
  * **Patrón**: *Entrada De Patrón, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media Campana, Campana Redondeada, Media Luna, Cápsula, Cono*\
    Selecciona la forma de motivo que se va a utilizar.
  * **Filtrado de entrada de imagen (Motor > v4)**: *Bilineal + Mipmaps, Bilineal, Más Cercano*
  * **Específico del patrón**: *0.0 - 1.0*\
    Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado.
  * **Aleatorio específico de patrón**: *0.0 - 1.0* El efecto de aleatorización depende del patrón seleccionado.
  * **Rotación**: *0, 90, 180, 270, horizontal aleatorio, vertical aleatorio* Establece la rotación en pasos de 90 grados, con aleatorización opcional.
  * **Aleatorio de rotación**: *0.0 - 1.0* Agrega rotación libre aleatoria.
  * **Aleatorio de simetría**:  **0.0 - 1.0** Refleja aleatoriamente ciertos patrones según el modo aleatorio de simetría seleccionado. Cuanto más alto sea este valor, más patrones se reflejarán.
  * **Modo aleatorio de simetría**: *Horizontal + Vertical, Horizontal, Vertical* Determina el comportamiento del reflejo cuando el valor aleatorio de simetría es superior a 0.
* **División**
  * **Modo**: *ninguno, automático, horizontal automático, vertical automático, aleatorio h+v* Establece la regla sobre cómo dividir los mosaicos.
  * **Umbral**: *0.0 - 1.0* Umbral de tamaño para dividir un azulejo.
  * **Multiplicador**: *0 - 10* Multiplicador de división. Cuanto mayor sea este valor, más se dividirá.
* **Tamaño**
  * **Aleatorio X**: *0.0 - 1.0* Aleatoriza la escala no uniforme sobre el eje X.
  * **Y aleatorio**: *0.0 - 1.0* Aleatoriza la escala no uniforme sobre el eje Y.
* **Intersticio**
  * **Modo**: *Relativo al ladrillo más pequeño, Relativo al ladrillo más grande* Establece a qué intersticio de tamaño de ladrillo es relativo.
  * **Importe**: *0.0 - 1.0* Establece el tamaño de hueco entre los ladrillos.
* **Forma**
  * **Escala**: *0.0 - 1.0* Escala globalmente cada mosaico.
  * **Escala aleatoria**: *0.0 - 1.0* Escala aleatoria por mosaico.
  * **Rotación**: *0.0 - 1.0* Rotación global por cada mosaico.
  * **Aleatorio de rotación**: *0.0 - 1.0* Rota aleatoriamente por mosaico.
  * **Restricción de rotación**: *Falso/Verdadero* Restringe la escala para que los mosaicos rotados nunca se superpongan.
* **Posición**
  * **Desplazamiento**: *0.0 - 1.0*\
    Mueve o traduce los mosaicos globalmente y sólo se desliza sobre el eje X
  * **Desplazamiento aleatorio**: *0.0 - 1.0* Aleatoriza el desplazamiento por mosaico, se desliza únicamente sobre el eje X
  * **Aleatorio**: *0.0 - 1.0* Aleatoriza la posición, los mosaicos se mueven en los ejes X e Y.
  * **Restricciones aleatorias**: *Falso/Verdadero* Restringe la escala para que los mosaicos se toquen, pero no se superpongan. Reduce significativamente el efecto Posición aleatoria.
* **Color**
  * **Color**: *(Valor de escala de grises) / (Valor de color)*Establece un color sólido para todos los mosaicos.
  * **Aleatorio de color**: *0.0 - 1.0* Aleatoriza el color según el azulejo.
  * **Parametrización de color**: *ninguno, área, tamaño x, tamaño y* Hace que la variación de color dependa de uno de estos valores.
  * **Intensidad de parametrización de color**: *0.0 - 1.0* Multiplicador para el efecto de parametrización anterior.
  * **Efecto de parametrización de color (solo para Color):** **RGB+Alpha, solo RGB, solo Alpha** Determina el efecto de parametrización de solo color.
  * **Color de fondo**: *(Valor de escala de grises) / (Valor de color)*Define el color de fondo sólido.
  * **Modo De Fusión**: *Agregar/Inferior, Máx./* Agregar/Inferior, Fusión de Alpha (Color)**Establece el modo de fusión de los mosaicos en el fondo.
* **Máscara**
  * **Aleatorio**: *0.0 - 1.0* Comienza a enmascarar aleatoriamente los mosaicos. Cuanto mayor sea el valor, más mosaicos desaparecerán.
  * **Invertir**: *Falso/Verdadero*\
    Invierte el resultado de la máscara.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tile-random-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
