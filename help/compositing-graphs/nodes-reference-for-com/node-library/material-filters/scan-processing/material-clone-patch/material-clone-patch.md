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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# Parche de Clonación de Material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## Parche de Clonación de Material

**En:** *Procesamiento De Escaneo/Filtros De Materiales*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Esta es la versión de material completo multicanal de [Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Realiza un parche de clonación en todos los canales de un material. [Consulte la versión original para obtener más información.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Esto resulta muy útil si desea quitar un detalle de todos los canales de un material. Emite imágenes de depuración para varios canales para ver exactamente el aspecto del área de revisión inteligente.

## Parámetros

### Entradas

* **Máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;.

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Forma**: *Cuadrado, disco* Establece la forma del sello. Sólo se usa como base.
* **Edge**
  * **Umbral (para varios canales)**: *0.0 - 1.0* Establece hasta dónde debe llegar el área mezclada. Esto crece en pasos, a lo largo de las formas en el área de destino, por lo que tiene muy poco efecto con fondos uniformes*.*Tenga cuidado con cambiar esto demasiado entre canales, ya que podría conducir a discrepancias visuales!
  * **Desenfocar**: *0.0 - 2.0* Desenfoca los bordes del área de sello en caso de que se necesite una transición más suave.
  * **Smoothness**: *0.0 - 2.0* Redondea los bordes de la forma de sello para que los contornos fluyan más suavemente.
  * **Resolución de cuadrícula**: *1 - 11* Establece la resolución de calidad del análisis de fusión. Un valor más alto significa una fusión más precisa.
* **Transformaciones**
  * **Matriz de origen**: *(Matriz de transformación)*Transforma el origen (Escala y rotación). No se puede realizar en el lienzo; cambie solo mediante estos parámetros.
  * **Desplazamiento de origen**: *-0.5 - 0.5* Traduce la ubicación de origen. No se puede realizar en el lienzo; cambie solo mediante estos parámetros. *Este parámetro es probablemente el principal que desea cambiar.*
  * **Matriz de destino**: *(Matriz de transformación)*Transforma la ubicación de destino (Escala y rotación). También se puede hacer a través de Gizmo en lienzo.
  * **Desplazamiento de destino**: *-0.5 - 0.5* Traduce la ubicación de destino. También se puede hacer a través de Gizmo en lienzo.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
