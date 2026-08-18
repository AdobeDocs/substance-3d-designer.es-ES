---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: Utilice el nodo Recorte múltiple para recortar varios canales de textura al mismo tiempo para procesar materiales digitalizados de forma eficaz.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recorte múltiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Recorte múltiple

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

## Recorte múltiple (escala de grises)

**En:** *Procesamiento De Escaneo/Filtros De Materiales*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Esta es la versión multicanal de Crop. Recorta un área a partir de una imagen y está destinado principalmente para su uso con fotos de varios ángulos, que luego se combinan con [Multi-Ángulo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Multi-Ángulo a Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulta el [Recorte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) original para obtener más información.

## Parámetros

### Parámetros

* **Recuento de entradas**: *1 - 8* Establece el número de entradas para procesar en paralelo.
* **Tamaño de entrada**: *0 - 8192* Resolución y proporciones de las imágenes de entrada. Muy importante para imágenes no cuadradas.
* **Fondo**: *(Valor de color) / (Valor de escala de grises)*Valor uniforme de fondo para áreas no cubiertas por Recortar.
* **Transformar**: *(Matriz de transformación)*\
  Rota y escala el resultado. El resultado se puede modificar interactuando directamente con el lienzo.
* **Desplazamiento**: *0.0 - 1.0*\
  Mueve o traduce el resultado. El resultado se puede modificar interactuando directamente con el lienzo.
* **Es normal (solo para la versión Color)**: *Falso/Verdadero* Indica si la entrada debe tratarse o no como un mapa normal.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
