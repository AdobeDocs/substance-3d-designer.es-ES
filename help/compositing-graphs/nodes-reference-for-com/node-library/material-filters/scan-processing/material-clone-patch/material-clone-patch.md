---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: Utilice el nodo Parche de clonación de material para clonar y parchear regiones de textura para reparar artefactos en materiales digitalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parche de Clonación de Material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---


# Parche de Clonación de Material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-clone-patch.resources/clone-patch-material.png){width="128px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Esta es la versión de material completo multicanal de [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Realiza un parche de clonación en todos los canales de un material. [Consulte la versión original para obtener más información.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Esto resulta muy útil si desea quitar un detalle de todos los canales de un material. Emite imágenes de depuración para varios canales para ver exactamente el aspecto del área de revisión inteligente.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Forma</b> <i>Cuadrado, disco</i> | Establece la forma del sello. Sólo se usa como base. |
| <b>Edge</b> |  |
| <b>Umbral (para varios canales)</b> <i>0.0 - 1.0</i> | Define hasta dónde debe llegar el área mezclada. Esto crece en pasos, a lo largo de las formas en el área de destino, por lo que tiene muy poco efecto con fondos uniformes. Tenga cuidado con cambiar esto demasiado entre canales, ya que podría conducir a discrepancias visuales! |
| <b>Desenfocar</b> <i>0.0 - 2.0</i> | Desenfoca los bordes del área de sello en caso de que sea necesaria una transición más suave. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Redondea los bordes de la forma de sello para que los contornos fluyan más suavemente. |
| <b>Resolución de cuadrícula</b> <i>1 - 11</i> | Define la resolución de calidad del análisis de fusión. Un valor más alto significa una fusión más precisa. |
| <b>Transformaciones</b> |  |
| <b>Matriz de origen</b> <i>(Matriz de transformación)</i> | Transforma el origen (Escala y rotación). No se puede realizar en el lienzo; cambie solo mediante estos parámetros. |
| <b>Desplazamiento de origen</b> <i>-0.5 - 0.5</i> | Traduce la ubicación de origen. No se puede realizar en el lienzo; cambie solo mediante estos parámetros. *Este parámetro es probablemente el principal que desea cambiar.* |
| <b>Matriz de destino</b> <i>(Matriz de transformación)</i> | Transforma la ubicación de destino (Escala y rotación). También se puede hacer a través de Gizmo en lienzo. |
| <b>Desplazamiento de destino</b> <i>-0.5 - 0.5</i> | Traduce la ubicación de destino. También se puede hacer a través de Gizmo en lienzo. |
