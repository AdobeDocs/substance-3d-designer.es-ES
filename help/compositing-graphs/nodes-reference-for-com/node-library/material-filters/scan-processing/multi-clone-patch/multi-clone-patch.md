---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Utilice el nodo Parche de clonación múltiple para clonar y parchear varios canales de textura para reparar artefactos de material digitalizado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parche de clonación múltiple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Parche de clonación múltiple

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-multi.png){width="128px"}

![](../../../../../../assets/clone-patch-multi-grayscale.png){width="128px"}

## Parche de clonación múltiple (escala de grises)

**En:** *Procesamiento De Escaneo/Filtros De Materiales*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo es la versión de entrada múltiple de [parche de clonación](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Enlaza hasta ocho entradas y realiza la misma operación de Parche de Clonación en todas ellas. Está pensado principalmente para fotos de varios ángulos, que luego se combinan con [Multi-Ángulo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Multi-Ángulo a Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulte [Parche de clonación](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) para obtener más información. Consulte [Parche de clonación de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) para obtener la versión del material.

## Parámetros

### Parámetros

* **Recuento de entradas**: *1 - 8* Establece la cantidad de entradas que recibirán la misma operación Parche.
* **Es normal (solo para Color)**: **Falso/Verdadero** Establece si la entrada es un mapa normal y si la fusión debe tratarse como tal.
* **Forma**: **Cuadrado, disco** Establece la forma del sello. Sólo se usa como base.
* **Edge**
  * **Umbral**: *0.0 - 1.0* Establece hasta dónde debe llegar el área mezclada. Esto aumenta en pasos a lo largo de las formas en el área de destino; tiene muy poco efecto con fondos uniformes*.*
  * **Desenfocar**: *0.0 - 2.0* Desenfoca los bordes del área de sello, en caso de que sea necesaria una transición más suave.
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
