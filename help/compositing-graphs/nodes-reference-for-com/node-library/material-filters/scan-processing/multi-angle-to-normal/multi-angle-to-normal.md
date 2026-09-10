---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: Utilice el nodo Multicángulo a Normal para generar mapas de normales a partir de imágenes digitalizadas multiángulo para obtener detalles de superficie precisos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: De múltiples ángulos a normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# De múltiples ángulos a normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-normal.resources/multi-angle-to-normal.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo construye un mapa normal a partir de un conjunto de fotografías/digitalizaciones realizadas en diferentes condiciones de iluminación. Permite una conversión de mapa de normas mucho más precisa que cuando se intenta extraer las normales de una sola imagen de albedo.

Es más complicado que [Albedo de varios ángulos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md), ya que requiere que uses ángulos de luz precisos y definidos para tus entradas. El ángulo de iluminación de cada muestra debe espaciarse uniformemente y las muestras deben introducirse en secuencia. Por lo tanto, para tres muestras, los ángulos de iluminación deben tomarse en: 0, 120, 240 - o cualquier compensación uniforme de eso (como 90, 210, 330).

>[!NOTE]
>
> Vea [Multi-Angle to Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) para obtener la versión de albedo de este nodo. Si deseas preprocesar tus entradas, [Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) y [Multi Clonar Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) pueden ser de utilidad, ya que están pensados para combinarse con estos nodos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-8</b> <i>Entrada de color</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Cantidad de muestras</b> <i>2 - 8</i> | Define la cantidad de muestras (entradas) que se procesarán. |
| <b>Intensidad</b> <i>0.0 - 1.0</i> | Establece la intensidad del mapa normal. |
| <b>Primer ángulo de luz de muestra</b> <i>0.0 - 360.0</i> | Establece la dirección del ángulo de iluminación de la primera entrada. |
| <b>Ángulo claro de la siguiente muestra</b> <i>Hacia la izquierda, Hacia la derecha</i> | Establece en qué dirección se mueve la iluminación de la siguiente muestra. |
