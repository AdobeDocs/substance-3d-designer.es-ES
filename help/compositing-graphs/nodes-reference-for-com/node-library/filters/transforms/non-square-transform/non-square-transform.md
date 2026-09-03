---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformo no cuadrado para aplicar transformaciones a texturas no cuadradas con escalado independiente X e Y.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación no cuadrada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# Transformación no cuadrada

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-square-transform.resources/non-square-transform-01.png)

![](non-square-transform.resources/non-square-transform-02.png)

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Versión no cuadrada segura de [Transformar 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Detecta automáticamente proporciones no cuadradas y puede transformar imágenes de entrada cuadradas en un lienzo no cuadrado.

Asegúrate de que entiendes perfectamente los [Parámetros de gráficos](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md) para hacer el mejor uso de este nodo, ya que necesitarás establecer algunos valores correctamente:

* El tamaño del **gráfico** no debe ser cuadrado; de lo contrario, no es necesario este nodo.
* Establezca el tamaño de salida de **node** Transformar no cuadrado en &quot;*Relativo al primario*&quot;.
* Establezca el modo de mosaico **node** en &quot;*No Tiling*&quot; si solo desea transformar la entrada a una única posición.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de mosaico</b> <i>Automático, Manual</i> | Active o no las compensaciones automáticas no cuadradas. |
| <b>Mosaico</b> <i>1 - 16</i> | Solo se puede acceder a él cuando el modo Mosaico está establecido en Manual. Permite cambiar la escala de forma segura para mosaicos. |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Mueve o traduce el resultado. Haga doble clic en el regulador para introducir valores negativos. |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Rota la imagen de entrada. |
| <b>Giro seguro (solo cuadrado)</b> <i>Falso/Verdadero</i> | Ajusta a valores seguros para mantener el enfoque de los píxeles. |
| <b>Color de fondo</b> <i>(Valor de color)</i> | Color de fondo con el que rellenar la imagen. Solo es visible cuando [Modo de mosaico en Parámetros base está establecido en &quot;*Sin mosaico*&quot;](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md). |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-square-transform.resources/non-square-transform-03.png" />
        </td>
    </tr>
</table>
