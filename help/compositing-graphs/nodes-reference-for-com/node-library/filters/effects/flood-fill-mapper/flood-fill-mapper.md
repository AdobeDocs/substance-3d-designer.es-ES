---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Utilice el nodo Asignador de Flood Fill para asignar valores entre regiones conectadas mediante algoritmos de relleno de área para el procesamiento de texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Asignador de Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---


# Asignador de Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-mapper-gray.png)![](../../../../../../assets/floodfill-mapper-color.png)

## Asignador de Flood Fill (escala de grises)

**En:** *Filtros/Efectos*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

El Asignador de Flood Fill permite reasignar un patrón o textura existente en cada celda desde un [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). Se diferencia de otras conversiones de Flood Fill como [Random Grayscale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) o [Gradient](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md) en que no genera colores o valores sólidos, pero te permite usar tus propios mapas de entrada. Se puede ver como una especie de combinación de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) y [Sampler de mosaico](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) o [Asignador de formas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md), ya que proporciona bastantes controles e interfaces similares.

La versión Color tiene controles adicionales para trabajar con Mapas normales, donde puede [compensar las rotaciones de mapa normal de espacio tangente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md).

## Parámetros

### Entradas

* **Flood Fill Box**: *Entrada de color* Entrada de Flood Fill estándar, necesaria.
* **Entrada de patrón 1-8**: *Entrada de escala de grises/color*\
  Entrada de imagen de patrón personalizado.
* **Mapa de distribución de patrones**: *Entrada en escala de grises* Asignación de ID para determinar qué patrón va a cada celda. Puede proceder de otro Mapa del Flood Fill, como Flood Fill a índice.
* **Mapa de escala**: *Entrada en escala de grises* Asignar para determinar la escala por celda.
* **Mapa de rotación**: *Entrada en escala de grises* Asignar para determinar la rotación por celda.
* **Mapa de desplazamiento de luminancia**: *Entrada en escala de grises* Asignar para establecer la luminancia por celda

### Parámetros

* **Modo de segmentación**: *Sin Mosaico, H+V* Establezca si desea utilizar Mosaico o no. Solo es visible si Tamaño o Escala están establecidos por debajo de 1.
* **Patrón**
  * **Número de entrada de patrón**: *1 - 8* Establecer la cantidad de entradas de patrones personalizados que se deben usar.
  * **Modo De Distribución De Patrones**: *Aleatorio, tamaño de forma, entrada de mapa de distribución* Establezca el método para determinar qué patrón se muestra en una celda.
  * **Variación De Distribución De Patrones**: *0.0 - 1.0* Permite una ligera variación o Desplazamiento en la distribución del Patrón sin cambiar todo a través de la Raíz aleatoria.
* **Tamaño**
  * **Modo de tamaño**: *Relativo a la textura, Relativo a la forma BSphere, Relativo a la forma más grande, Relativo a la forma más pequeña, Ajustar forma Box* Establezca cómo se determina el tamaño del motivo en cada celda.
  * **Tamaño**: *0.0 - 1.0* Permite la escala no uniforme del Patrón.
  * **Escala**: *0.0 - 1.0*\
    Establezca la escala global (uniforme) del efecto.
  * **Multiplicador de mapa de escala**: *0.0 - 1.0* Establecer la influencia del mapa de escala opcional.
  * **Escala aleatoria**: *-1.0 - 1.0* Establece la cantidad de variación aleatoria dentro de la escala de patrón.
* **Rotación**
  * **Rotación**: *0.0 - 1.0* Establecer una rotación uniforme y global para cada celda.
  * **Multiplicador de Mapa de rotación**: *0.0 - 1.0* Establecer la influencia del Mapa de rotación opcional.
  * **Aleatorio de rotación**: *0.0 - 1.0* Establezca la cantidad de rotación aleatoria para cada celda.
  * **Escala automática de rotación**: *Falso/Verdadero* Establece si un patrón debe ajustar su escala para que encaje dentro de una celda cuando se gira.
* **Posición**
  * **Desplazamiento de posición**: *0.0 - 1.0* Establecer desplazamiento de posición global para cada celda.
  * **Alineación de desplazamiento de posición**: *Textura, motivo* Establezca esta opción para alinear el punto de desplazamiento 0 con la celda de motivo o con la textura.
  * **Aleatorio de desplazamiento de posición**: *0,0 - 1,0* Establezca la cantidad de aleatorización de desplazamiento de posición por celda.
* **Color** (solo para la versión en escala de grises)
  * **Rango de luminancia**: *0.0 - 1.0* Establece el contraste global en la textura, donde 0 se convierte en gris medio.
  * **Rango de luminancia aleatorio**: *0.0 - 1.0* Establece la cantidad de aleatoriedad para el rango de luminancia.
  * **Desplazamiento de luminancia**: *-1.0 - 1.0* Establece el desplazamiento de la luminancia, que funciona como un control de brillo.
  * **Aleación de desplazamiento de luminancia**: *0.0 - 1.0* Establece la cantidad de aleatoriedad para el desplazamiento de luminancia.
  * **Multiplicador de mapa de desplazamiento de luminancia**: *0.0 - 1.0* Establece la influencia del mapa de desplazamiento de luminancia opcional.
  * **Color de fondo**: *(Valor de escala de grises)*Define el color de fondo en el que se fusionan las texturas.
* **Color** (solo para la versión Color)
  * **Es un mapa normal**: *Falso/Verdadero* Establecer para interpretar la entrada de patrón como un mapa normal. Compensará y corregirá la rotación del espacio de Tangente normal.
  * **Formato normal**: *DirectX, OpenGL*\
    Cambia entre diferentes Formatos de mapa de normales (invierte el canal verde). Sólo está activo cuando Is Normal Map es True.
  * **Ajuste de HSL**: *-1.0 - 1.0* Ajuste global del HSL.
  * **Aleatorio de HSL**: *-1.0 - 1.0* Establecer aleatoriedad de HSL por celda.
  * **Ajuste de Alpha**: *-1.0 - 1.0* Establecer el ajuste global del Alpha reduce el contraste del Alpha.
  * **Alpha aleatorio**: *-1.0 - 1.0* Establecer aleatoriedad de ajuste de Alpha por celda.
  * **Color de fondo**: *(Valor de color)*Define el color de fondo en el que se fusionan las texturas.

.

## Imágenes de ejemplo

![](../../../../../../assets/floodfill-mapper-ex01.png)

![](../../../../../../assets/floodfill-mapper-ex02.jpg)

</td>
</tr>
</table>
