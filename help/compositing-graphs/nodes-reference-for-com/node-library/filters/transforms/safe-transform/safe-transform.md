---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación segura para aplicar transformaciones a la vez que conserva los límites de la textura y evita artefactos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación segura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# Transformación segura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Versión de [Transformar 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) a prueba de mosaicos. Permite escalar, rotar y desplazar sin romper el mosaico y sin perder detalles de píxeles (pérdida de nitidez/nitidez) debido a pequeños desplazamientos y rotaciones.

Resulta útil para transformar el ruido cuando se requiere el máximo control o una nitidez perfecta.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Mosaico</b> <i>1 - 16</i> | Reduce la entrada segmentándola. |
| <b>Modo de desplazamiento</b> <i>Manual, aleatorio</i> | Cambia a un desplazamiento aleatorio en lugar de uno definido manualmente. |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Mueve o traduce el resultado. Garantiza que los píxeles estén ajustados y no interpolados. |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Rota la entrada a lo largo del ángulo. |
| <b>Rotación segura del azulejo</b> <i>Falso/Verdadero</i> | Determina el comportamiento de Rotación, si debe ajustarse a valores seguros que no desenfoquen ningún píxel. |
| <b>Simetría</b> <i>ninguno, X, Y, X+Y</i> |  |
| <b>Color de fondo</b> <i>(valor de color) (solo versión de color)</i> |  |
| <b>Modo Mipmap</b> <i>Automático, Manual</i> | Determina el modo de asignación. Si se establece en Manual, se obtienen resultados más nítidos. |
| <b>Nivel de mapa MIP</b> <i>0 - 10</i> | Cuando el modo Mipmap se establece en Manual, esto le permite elegir un Mipmap diferente. |
