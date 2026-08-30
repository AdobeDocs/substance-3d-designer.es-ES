---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: Utilice el nodo Mosaico automático inteligente para crear automáticamente mosaicos perfectos a partir de materiales digitalizados mediante la detección inteligente de patrones.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaico automático inteligente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# Mosaico automático inteligente

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](smart-auto-tile.resources/smart-auto-tile.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo convierte un conjunto no segmentado de mapas de altura, normales y de color base en una versión segmentada de acuerdo con el análisis inteligente de las entradas. Es similar a [Make It Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), pero mucho más avanzado ya que utiliza información de todos los canales para fusionar las cosas de la manera más inteligente (similar a lo que hace [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)). También tiene una función interna [Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) para determinar qué área se debe usar al aplicar el mosaico. Asegúrese de [leer más acerca del nodo Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) para entender esta función correctamente.

Para utilizar este nodo, comience por definir el área Recortada y, a continuación, utilice la configuración de Borde para determinar cómo se fusionan los bordes en mosaico en el centro. Los parámetros del umbral son de importancia clave para esto. Tenga en cuenta que las áreas grandes y uniformes no funcionan muy bien con este efecto; cuanto más detalles y formas haya, más se necesita para trabajar.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Usar máscara&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Recortar</b> |  |
| <b>Tamaño de entrada</b> <i>0 - 8192</i> | Introduce la resolución y las proporciones de las imágenes. Muy importante para imágenes no cuadradas. |
| <b>Transformar</b> <i>(Matriz de transformación)</i> | Rota y escala el resultado. El resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Mueve o traduce el resultado. El resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Edge</b> |  |
| <b>Detectar bordes</b> <i>Falso/Verdadero</i> | Activa o desactiva la fusión de arista especial detectada. |
| <b>Usar umbral por canal</b> <i>Falso/Verdadero</i> | Cambia entre un valor de umbral global o uno para cada canal. |
| <b>Umbral</b> <i>0.0 - 1.0</i> |  |
| <b>Color base de umbral</b> <i>0.0 - 1.0</i> |  |
| <b>Umbral normal</b> <i>0.0 - 1.0</i> |  |
| <b>Height de umbral</b> <i>0.0 - 1.0</i> |  |
| <b>Desplazamiento de corte</b> <i>0.0 - 0.5</i> | Control principal para mover el corte, los ejes X e Y están separados. |
| <b>Desenfocar</b> <i>0.0 - 2.0</i> | Desenfoca la transición de fusión. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Controla la irregularidad de los resultados del análisis de bordes. |
| <b>Resolución de cuadrícula</b> <i>1 - 11</i> | Resolución de calidad del análisis de bordes. |
| <b>Usar Color base</b> <i>Falso/Verdadero</i> | Alterna el procesamiento del Color base (entrada y salida). |
| <b>Usar normal</b> <i>Falso/Verdadero</i> | Alterna el procesamiento normal (entrada y salida). |
| <b>Usar Height</b> <i>Falso/Verdadero</i> | Alterna el procesamiento normal (entrada y salida). |
| <b>Usar máscara</b> <i>Falso/Verdadero</i> | Activa o desactiva el uso del mapa de máscara para las formas de máscara de sello personalizadas. |
