---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: Utilice el nodo Dispersión para crear dispersiones de formas entre texturas y así crear patrones aleatorios y detalles de textura orgánica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Salpicadura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 9%

---


# Salpicadura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter.resources/splatter-01.png)

![](splatter.resources/splatter-02.png)

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Splatter es un generador de patrones destinado a la colocación aleatoria de una entrada de mapa. Tiene muchos controles para la colocación de patrones geométricos y su uso es más sencillo que [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Este último puede lograr resultados similares, pero es mucho más complejo.

La salpicadura funciona bien para conseguir rápidamente algunas formas estampadas, sin necesidad de demasiadas modificaciones.

Tenga en cuenta que los parámetros predeterminados de Splatter no son aleatorios: es necesario ajustar algunos de ellos para obtener la aleatorización (principalmente parámetros de trastorno). También tenga en cuenta que Splatter requiere una entrada de mapa para funcionar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ancho de tamaño de motivo</b> <i>0.0 - 1000.0</i> | Número de patrones que se utilizarán en el eje X. |
| <b>Height de tamaño de motivo</b> <i>0.0 - 1000.0</i> | Número de patrones que se utilizarán en el eje Y. |
| <b>Rotación</b> <i>-360.0 - 360.0</i> | Rota cada motivo en una cantidad definida. |
| <b>Variación de rotación</b> <i>0.0 - 360.0</i> | Introduce un giro aleatorio para cada forma independiente. |
| <b>Zoom</b> <i>100.0 - 10000.0</i> | Aumenta el resultado final. Tenga en cuenta que esto rompe la baldosa! |
| <b>Ganancia</b> <i>0.0 - 10.0</i> | Ajusta la ganancia de fusión de cada patrón. Hace que destaquen más. |
| <b>Panorámica X</b> <i>-100.0 - 100.0</i> | Muestra el resultado completo en el eje X. |
| <b>Panorámica Y</b> <i>-100.0 - 100.0</i> | Muestra el resultado completo en el eje Y. |
| <b>Desorden</b> <i>0.0 - 100.0</i> | Cambia formas aleatoriamente. |
| <b>Número de cuadrícula</b> <i>0 - 8</i> | Pasa por diferentes tamaños de cuadrícula para ajustar la escala de resultados. Mantiene el azulejo. |
| <b>Ángulo de desorden</b> <i>0.0 - 360.0</i> | Controla el ángulo de desplazamiento del trastorno. |
| <b>Aleatorio de trastorno</b> <i>Falso/Verdadero</i> | Aleatoriza el ángulo del desorden, agregando mucho más caos. |
| <b>Tamaño de patrón</b> <i>5 - 12</i> |  |
| <b>Variación de tamaño</b> <i>0.0 - 100.0</i> | Introduce una escala aleatoria para cada forma. |
| <b>Filtrado de entrada de imagen (Motor > v4 únicamente)</b> <i>Bilineal + Mipmaps, Bilineal, Más Cercano</i> | Filtrado que se aplicará a la imagen de entrada. |
| <b>Nivel De Salida Mínimo</b> <i>0.0 - 1.0</i> | Ajuste del nivel mínimo de salida. |
| <b>Nivel de salida máx.</b> <i>0.0 - 1.0</i> | Ajuste de nivel máximo de salida. |
| <b>Color de fondo</b> <i>(valor de escala de grises)</i> | Define el color de fondo sólido. |
| <b>Variación de luminancia</b> <i>0.0 - 1.0 (solo versión de escala de grises)</i> | Introduce la variación de luminancia. |
| <b>Variación de color</b> <i>0.0 - 1.0 (solo versión de color)</i> | Introduce la variación de color. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter.resources/splatter-03.gif" />
        </td>
    </tr>
</table>
