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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# Material Crop

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-material.png){width="128px"}

## Material Crop

**En:** *Procesamiento De Escaneo/Filtros De Materiales*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo es la versión de material completa y multicanal de [Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md). Permite realizar una operación de recorte en todos y cada uno de los canales de material en paralelo.

>[!NOTE]
>
> [Consulta el](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [Recorte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [original para obtener más información.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

## Parámetros

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo cuando utilice mapas de Specular/Brillo en lugar de Metálico/Rugosidad, por ejemplo.
* **Tamaño de entrada**: *0 - 8192* Resolución y proporciones de la imagen de entrada. Muy importante para imágenes no cuadradas.
* **Fondo**: *(Valor de color) / (Valor de escala de grises)*Valor uniforme de fondo para áreas no cubiertas por Recortar.
* **Transformar**: *(Matriz de transformación)*\
  Rota y escala el resultado. El resultado se puede modificar interactuando directamente con el lienzo.
* **Desplazamiento**: *0.0 - 1.0*\
  Mueve o traduce el resultado. El resultado se puede modificar interactuando directamente con el lienzo.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
