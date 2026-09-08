---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: Utilice el nodo Flood Fill para rellenar regiones conectadas de color similar para crear máscaras y efectos de procesamiento de textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 1%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/floodfill.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Flood Fill forma parte de un conjunto avanzado de efectos que le permiten agregar mucha más variación a una textura básica de mosaicos binarios. No está destinado a ser utilizado por sí mismo: en su lugar, es más bien un punto de partida para los efectos de Otros Flood Fill. Estos datos separados y divididos permiten un flujo de trabajo más dinámico, optimizado y menos destructivo.

Los otros efectos de Flood Fill son [Flood Fill a degradado](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), [Flood Fill a color/escala de grises](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md), [Flood Fill a escala de grises aleatoria](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), [Flood Fill a color aleatorio](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md), [Flood Fill a tamaño de cuadro](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md), [Flood Fill a posición](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md), [Asignador de Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md) y [Flood Fill a índice](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)

>[!WARNING]
>
> El mapa de entrada debe ser adecuado para que el Flood Fill funcione. Idealmente es un mapa binario (solo blanco/negro, sin escala de grises) donde cada mosaico está separado de las otras líneas por un borde que es negro completo (0,0,0) por cada píxel. Un ejemplo de candidato perfecto para esto es [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).
> 
> Se producen problemas si los mosaicos no están separados por píxeles totalmente negros, normalmente cuando se utilizan valores inclinados de escala de grises. Esto se puede identificar por una falta general de valores rojos en el resultado y, posiblemente, líneas de artefactos extraños. En tales casos, ajuste el contraste en el mapa de entrada o cambie el mapa de entrada hacia fuera. Asegúrese de cambiar el ajuste de compensación Seguridad/Velocidad para ver si hay alguna mejora.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Compensación de seguridad/velocidad</b> <i>Formas simples o pequeñas, Formas complejas o grandes, Modo sin errores.</i> | Defina el modo de cálculo para que se adapte mejor a las formas de entrada. Permite obtener resultados mucho más precisos si se elige el modo correcto. |
| <b>Opciones avanzadas</b> <i>Mostrar parámetros avanzados y Generar/Ocultar parámetros y resultados avanzados</i> |  |
| <b>Anular intercambio de seguridad/velocidad</b> <i>-1 - 100</i> | Solo visible con Opciones avanzadas activado. Permite la modificación de funciones internas. Muy avanzado, sirve para crear sus propios efectos o depurar. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/flood-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/flood-ex1.png" />
        </td>
    </tr>
</table>

Buenos y malos ejemplos de resultados de Flood Fill.
