---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación no cuadrada para aplicar transformaciones a texturas no cuadradas con escalado independiente X e Y.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación no cuadrada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Transformación no cuadrada

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Transformación no cuadrada (escala de grises)

**En:** *Filtros/Transformaciones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Versión no cuadrada segura de [Transformar 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Detecta automáticamente proporciones no cuadradas y puede transformar imágenes de entrada cuadradas en lienzos no cuadrados.

Asegúrate de que entiendes perfectamente los [Parámetros de gráficos](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md) para hacer el mejor uso de este nodo, ya que necesitarás establecer algunos valores correctamente:

* El tamaño del **gráfico** no debe ser cuadrado; de lo contrario, no es necesario este nodo.
* Establezca el tamaño de salida de transformación no cuadrada **node** en &quot;*Relativo al primario*&quot;.
* Establezca el modo de mosaico **node** en &quot;*No Tiling*&quot; si solo desea transformar la entrada en una única posición.

## Parámetros

* **Modo de mosaico**: *Automático, Manual* Habilita compensaciones automáticas no cuadradas o no.
* **Mosaico**: *1 - 16* Solo se puede acceder cuando el modo de mosaico está establecido en Manual. Permite cambiar la escala de forma segura para mosaicos.
* **Desplazamiento**: *0.0 - 1.0*\
  Mueve o traduce el resultado. Haga doble clic en el regulador para introducir valores negativos.
* **Rotación**: *0.0 - 1.0* Rota la imagen de entrada.
* **Giro seguro (solo cuadrado)**: *Falso/Verdadero* Ajusta a valores seguros para mantener el enfoque de los píxeles.
* **Color de fondo**: *(Valor de color)*Color de fondo con el que rellenar la imagen. Solo es visible cuando el modo de segmentación [en Parámetros base está establecido en &quot;*Sin segmentación*&quot;](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md).

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
