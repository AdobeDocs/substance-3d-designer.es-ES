---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: Utilice el nodo Dispersión de forma a máscara para convertir patrones de salpicaduras de formas en máscaras para la fusión de materiales y efectos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersión de forma a máscara
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Dispersión de forma a máscara

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

## Dispersión de forma a máscara

**En:** *Generadores De Texturas**/Patrones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Convierte los datos de [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) en una máscara en blanco y negro basada en el identificador de motivo. Permite, por ejemplo, crear una máscara de un solo tipo determinado de patrón. Dispone de opciones adicionales para seleccionar un rango de ID de motivo y ocultar aleatoriamente algunas formas.

## Parámetros

### Parámetros

* **Intervalo de inicio de id. de patrón**: *1 - 8* Establecer el primer Id. de motivo en el intervalo para seleccionarlo.
* **Intervalo de fin de id. de patrón**: *1 - 8* Establecer el último Id. de patrón en el intervalo para seleccionarlo.
* **Máscara aleatoria**: *0.0 - 1.0* Establecer una proporción de patrones para enmascarar aleatoriamente.
* **Salida**: *Máscara binaria, Máscara de enteros, Valores de escala de grises* Determine el tipo de valores de salida. Máscara binaria devuelve solo blanco y negro, valores de 0 o 1, Máscara de enteros codificará valores más altos hasta 8 para cada patrón en formato HDR, Valores de escala de grises se extenderá el rango proporcionalmente entre 0 y 1.

</td>
</tr>
</table>
