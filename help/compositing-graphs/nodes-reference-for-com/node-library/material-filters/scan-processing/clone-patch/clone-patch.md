---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: Utilice el nodo Parche de clonación para clonar y parchear áreas de materiales escaneados para eliminar artefactos e imperfecciones.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parche de clonación
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Parche de clonación

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

## Clonar Parche / Clonar Parche Escala De Grises

**En:** *Procesamiento De Escaneo/Filtros De Materiales*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Clone Patch es un nodo paramétrico de procedimiento llamado &quot;Clone Stamp&quot;. Clona un área de una entrada en otra, ocultando detalles potencialmente no deseados. Si bien no es tan rápido y fácil como usar una herramienta familiar en una aplicación basada en pincel, proporciona la ventaja clave de no ser destructivo y de trabajar dentro de un flujo de trabajo basado en nodos. Además, este nodo realiza un análisis inteligente del área de origen y de destino, e intenta fusionar las cosas lo mejor posible en función del contraste, los valores y las formas.

Esto está destinado principalmente a esos raros momentos en los que desea hacer una corrección manual de un área específica, en caso de que haya un detalle no deseado en algún lugar.

Tenga en cuenta que esto no funciona como un pincel estándar sencillo de &quot;Sello&quot;. La forma del área mezclada se basa en las formas y valores de las áreas con las que está trabajando, lo que significa que se trata de un nodo bastante pesado que requiere paciencia, pero ofrece excelentes resultados.

También es importante comprender el hecho de que puede mover el área de destino con un gizmo, pero el área de origen debe establecerse cambiando los parámetros de &quot;Matriz de origen&quot;.

>[!NOTE]
>
> Si desea esto para un material completo (como suele ser el caso), consulte [Parche de clonación de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md).
> 
> Para aquellos casos en los que desee realizar esta operación en varias entradas al mismo tiempo (sin que sea un material), consulte [Parche de varios clones](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md).

## Parámetros

* **Es normal (solo para Color)**: *Falso/Verdadero*\
  Establece si la entrada es un mapa normal y si la fusión debe tratarse como tal.
* **Forma**: *Cuadrado, disco* Establece la forma del sello. Sólo se usa como base.
* **Edge**
  * **Umbral**: *0.0 - 1.0* Establece hasta dónde debe llegar el área mezclada. Crece en pasos, a lo largo de las formas del área de destino y tiene muy poco efecto con fondos uniformes*.*
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
