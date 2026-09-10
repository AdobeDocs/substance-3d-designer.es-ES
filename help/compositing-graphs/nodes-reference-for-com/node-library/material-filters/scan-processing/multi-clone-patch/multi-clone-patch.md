---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Utilice el nodo Parche para varios Clonar para clonar y parchear varios canales de textura para reparar artefactos de material digitalizado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parche para varios Clonar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---


# Parche para varios Clonar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-clone-patch.resources/clone-patch-multi.png){width="128px"}

![](multi-clone-patch.resources/clone-patch-multi-grayscale.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo es la versión de entrada múltiple de [parche de Clonar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Se vincula entre sí hasta ocho entradas y realiza exactamente la misma operación de parche de Clonar en todas ellas. Está pensado principalmente para fotos de varios ángulos, que luego se combinan con [Multi-Ángulo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Multi-Ángulo a Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulte [Parche del Clonar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) para obtener más información. Consulte [Parche del Clonar de materiales](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) para obtener la versión del material.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Recuento de entradas</b> <i>1 - 8</i> | Define la cantidad de entradas que recibirán la misma operación de parche. |
| <b>Es normal (solo para Color)</b> <i>Falso/Verdadero</i> | Establece si la entrada es un mapa normal y si la fusión debe tratarse como tal. |
| <b>Forma</b> <i>Cuadrado, disco</i> | Establece la forma del sello. Sólo se usa como base. |
| <b>Edge</b> |  |
| <b>Umbral</b> <i>0.0 - 1.0</i> | Define hasta dónde debe llegar el área mezclada. Esto aumenta en pasos a lo largo de las formas en el área de destino; tiene muy poco efecto con fondos uniformes. |
| <b>Desenfocar</b> <i>0.0 - 2.0</i> | Desenfoca los bordes del área de sello, en caso de que sea necesaria una transición más suave. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Redondea los bordes de la forma de sello para que los contornos fluyan más suavemente. |
| <b>Resolución de cuadrícula</b> <i>1 - 11</i> | Define la resolución de calidad del análisis de fusión. Un valor más alto significa una fusión más precisa. |
| <b>Transformaciones</b> |  |
| <b>Matriz de origen</b> <i>(Matriz de transformación)</i> | Transforma el origen (Escala y rotación). No se puede realizar en el lienzo; cambie solo mediante estos parámetros. |
| <b>Desplazamiento de origen</b> <i>-0.5 - 0.5</i> | Traduce la ubicación de origen. No se puede realizar en el lienzo; cambie solo mediante estos parámetros. *Este parámetro es probablemente el principal que desea cambiar.* |
| <b>Matriz de destino</b> <i>(Matriz de transformación)</i> | Transforma la ubicación de destino (Escala y rotación). También se puede hacer a través de Gizmo en lienzo. |
| <b>Desplazamiento de destino</b> <i>-0.5 - 0.5</i> | Traduce la ubicación de destino. También se puede hacer a través de Gizmo en lienzo. |
