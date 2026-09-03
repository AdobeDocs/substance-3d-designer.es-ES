---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: Utilice el nodo Material Crop para recortar regiones de textura a partir de materiales escaneados para aislar áreas específicas de interés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material Crop
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Material Crop

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-crop.resources/material-crop-01.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo es la versión de material completa y multicanal de [Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md). Permite realizar una operación de recorte en todos y cada uno de los canales de material en paralelo.

>[!NOTE]
>
> [Consulta el](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [Recorte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [original para obtener más información.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo cuando utilice mapas de Specular/Brillo en lugar de Metálico/Rugosidad, por ejemplo. |
| <b>Tamaño de entrada</b> <i>0 - 8192</i> | Resolución y proporciones de la imagen de entrada. Muy importante para imágenes no cuadradas. |
| <b>Fondo</b> <i>(Valor de color) / (Valor de escala de grises)</i> | Valor uniforme de fondo para áreas no cubiertas por Recorte. |
| <b>Transformar</b> <i>(Matriz de transformación)</i> | Rota y escala el resultado. El resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Mueve o traduce el resultado. El resultado se puede modificar interactuando directamente con el lienzo. |
