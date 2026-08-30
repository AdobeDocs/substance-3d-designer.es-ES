---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: Utilice el nodo Recorte múltiple para recortar varios canales de textura simultáneamente para procesar materiales digitalizados de forma eficaz.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recorte múltiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---


# Recorte múltiple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-crop.resources/crop-multi.png){width="128px"}

![](multi-crop.resources/crop-multi-grayscale.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Esta es la versión multicanal de Crop. Recorta un área a partir de una imagen y está destinado principalmente para su uso con fotos de varios ángulos, que luego se combinan con [Multi-Ángulo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Multi-Ángulo a Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulta el [Recorte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) original para obtener más información.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Recuento de entradas</b> <i>1 - 8</i> | Define el número de entradas que se procesarán en paralelo. |
| <b>Tamaño de entrada</b> <i>0 - 8192</i> | Introduce la resolución y las proporciones de las imágenes. Muy importante para imágenes no cuadradas. |
| <b>Fondo</b> <i>(Valor de color) / (Valor de escala de grises)</i> | Valor uniforme de fondo para áreas no cubiertas por Recorte. |
| <b>Transformar</b> <i>(Matriz de transformación)</i> | Rota y escala el resultado. El resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Mueve o traduce el resultado. El resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Es normal (solo para la versión Color)</b> <i>Falso/Verdadero</i> | Si la entrada debe tratarse o no como un mapa normal. |
