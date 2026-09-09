---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
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
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 6%

---


# Asignador de Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-mapper.resources/floodfill-mapper-gray.png)![](flood-fill-mapper.resources/floodfill-mapper-color.png)

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El Asignador de Flood Fill permite reasignar un patrón o textura existente en cada celda desde un [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). Se diferencia de otras conversiones de Flood Fill como [Random Grayscale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) o [Gradient](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md) en que no genera colores o valores sólidos, pero te permite usar tus propios mapas de entrada. Se puede ver como una especie de combinación de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) y [Sampler de mosaico](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) o [Asignador de formas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md), ya que proporciona bastantes controles e interfaces similares.

La versión Color tiene controles adicionales para trabajar con Mapas normales, donde puede [compensar las rotaciones de mapa normal de espacio tangente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Flood Fill Box</b> <i>Entrada de color</i> | Entrada de Flood Fill estándar, necesaria. |
| <b>Entrada de patrón 1-8</b> <i>Entrada de color/escala de grises</i> | Entrada de imagen de patrón personalizado. |
| <b>Mapa de distribución de patrones</b> <i>Entrada en escala de grises</i> | ID Map para determinar qué patrón va a cada celda. Puede proceder de otro Mapa del Flood Fill, como Flood Fill a índice. |
| <b>Mapa de escala</b> <i>Entrada en escala de grises</i> | Asignar para determinar la escala por celda. |
| <b>Mapa de rotación</b> <i>Entrada en escala de grises</i> | Asigne para determinar la rotación por celda. |
| <b>Mapa de desplazamiento de luminancia</b> <i>Entrada en escala de grises</i> | Asignación para definir la luminancia por celda |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de segmentación</b> <i>Sin Mosaico, H+V</i> | Establezca si desea utilizar Mosaico o no. Solo es visible si Tamaño o Escala están establecidos por debajo de 1. |
| <b>Patrón</b> |  |
| <b>Número de entrada de patrón</b> <i>1 - 8</i> | Defina la cantidad de entradas de motivo personalizadas que desea utilizar. |
| <b>Modo de distribución de patrones</b> <i>Aleatorio, Tamaño de forma, Entrada de mapa de distribución</i> | Establezca el método para determinar qué Patrón se muestra en una Celda. |
| <b>Variación De Distribución De Patrones</b> <i>0.0 - 1.0</i> | Permite una ligera variación o Desplazamiento en la distribución del Patrón sin cambiar todo a través de la Raíz aleatoria. |
| <b>Tamaño</b> |  |
| <b>Modo de tamaño</b> <i>Relativo a la Textura, Relativo a la forma BSphere, Relativo a la forma más grande, Relativo a la forma más pequeña, Ajustar forma Box</i> | Establezca cómo se determina el tamaño del patrón en cada celda. |
| <b>Tamaño</b> <i>0.0 - 1.0</i> | Permite la escala no uniforme del motivo. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Establezca la escala global (uniforme) del efecto. |
| <b>Multiplicador de mapa de escala</b> <i>0.0 - 1.0</i> | Defina la influencia del mapa de escala opcional. |
| <b>Escala aleatoria</b> <i>-1.0 - 1.0</i> | Establezca la cantidad de variación aleatoria dentro de la escala de patrón. |
| <b>Rotación</b> |  |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Establecer una rotación global y uniforme para cada celda. |
| <b>Multiplicador de Mapa de rotación</b> <i>0.0 - 1.0</i> | Definir la influencia del Mapa de rotación opcional. |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Establezca la cantidad de rotación aleatoria para cada celda. |
| <b>Escala automática de rotación</b> <i>Falso/Verdadero</i> | Defina si un motivo debe ajustar su escala para que encaje dentro de una celda cuando se gira. |
| <b>Posición</b> |  |
| <b>Desplazamiento de posición</b> <i>0.0 - 1.0</i> | Establecer desplazamiento de posición global para cada celda. |
| <b>Alineación de desplazamiento de posición</b> <i>Textura, patrón</i> | Se define para alinear el punto de desvío 0 con la celda de patrón o con la textura. |
| <b>Aleatorio de desplazamiento de posición</b> <i>0.0 - 1.0</i> | Establezca la cantidad de aleatoriedad de desplazamiento de posición por celda. |
| <b>Color (solo para la versión en escala de grises)</b> |  |
| <b>Rango de luminancia</b> <i>0.0 - 1.0</i> | Establece el contraste global en la textura, donde 0 se convierte en gris medio. |
| <b>Rango de luminancia aleatorio</b> <i>0.0 - 1.0</i> | Define la cantidad de aleatorización para el rango de luminancia. |
| <b>Desplazamiento de luminancia</b> <i>-1.0 - 1.0</i> | Establece el desplazamiento de la luminancia, que funciona como control de brillo. |
| <b>Desplazamiento de luminancia aleatorio</b> <i>0.0 - 1.0</i> | Define la cantidad de aleatorización para el desplazamiento de luminancia. |
| <b>Multiplicador de mapa de desplazamiento de luminancia</b> <i>0.0 - 1.0</i> | Define la influencia del mapa de desplazamiento de luminancia opcional. |
| <b>Color de fondo</b> <i>(valor de escala de grises)</i> | Define el color de fondo en el que se fusionan las texturas. |
| <b>Color (solo para la versión Color)</b> |  |
| <b>Es Mapa de normales</b> <i>Falso/Verdadero</i> | Defina esta opción para interpretar Entrada de motivo como un Mapa de normales. Compensará y corregirá la rotación del espacio de Tangente normal. |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes Formatos de mapa de normales (invierte el canal verde). Sólo está activo cuando Is Normal Map es True. |
| <b>Ajuste HSL</b> <i>-1.0 - 1.0</i> | Ajusta HSL globalmente. |
| <b>Aleatorio HSL</b> <i>-1.0 - 1.0</i> | Establezca HSL aleatorización por celda. |
| <b>Ajuste de Alpha</b> <i>-1.0 - 1.0</i> | Ajusta el Alpha global y reduce el contraste del Alpha. |
| <b>Alpha aleatorio</b> <i>-1.0 - 1.0</i> | Establecer aleatorización de ajuste de Alpha por celda. |
| <b>Color de fondo</b> <i>(Valor de color)</i> | Define el color de fondo en el que se fusionan las texturas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/floodfill-mapper-ex01.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/floodfill-mapper-ex02.jpg" />
        </td>
    </tr>
</table>
