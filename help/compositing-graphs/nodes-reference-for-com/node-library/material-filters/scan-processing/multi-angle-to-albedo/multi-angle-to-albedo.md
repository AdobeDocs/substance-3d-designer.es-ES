---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: Utilice el nodo Multicángulo a Albedo para extraer mapas de albedo de imágenes digitalizadas multiángulo para obtener colores de material limpios.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: De múltiples ángulos a Albedo
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# De múltiples ángulos a Albedo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-albedo.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo intenta eliminar toda la información de iluminación de un conjunto de fotografías/digitalizaciones de entrada tomadas con diferentes ángulos de iluminación. Combina todas las muestras en una sola imagen que debería ser lo más neutra en cuanto a iluminación y, por lo tanto, correcta en cuanto a PBR, posible.

Ten en cuenta que cuantas más muestras tengas y cuanto mayor sea la diferencia en el ángulo de iluminación, mayor será el éxito que consigas. A partir de cuatro muestras, debe ser posible lograr resultados casi perfectos, dependiendo de las imágenes de entrada. Las imágenes de entrada deben tomarse con un trípode y no tienen diferencias mínimas o, idealmente, ninguna, excepto por la iluminación desde un ángulo diferente.

>[!NOTE]
>
> Vea [Multi-Angle to Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) para obtener la versión de mapa normal de este nodo. Si quieres preprocesar tus entradas, [Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) y [Multi Clonar Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) pueden ser útiles, ya que están pensados para combinarse con estos nodos.
> 
> [La entrada del blog &quot;Tu Smartphone es un escáner de materiales&quot; ilustra este proceso un poco mejor.](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-8</b> <i>Entrada de color</i> | El número de entradas se determina mediante el parámetro Cantidad de muestras. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad de muestras</b> <i>2 - 8</i> | Define el número de muestras (entradas) que se utilizarán en el procesamiento. |
