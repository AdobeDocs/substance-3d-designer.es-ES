---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Transformación segura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Transformación segura (escala de grises)

**En:** *Filtros/Transformaciones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Versión de [Transformar 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) a prueba de mosaicos. Permite escalar, rotar y desplazar sin romper el mosaico y sin perder detalles de píxeles (pérdida de nitidez/nitidez) debido a pequeños desplazamientos y rotaciones.

Resulta útil para transformar el ruido cuando se requiere el máximo control o una nitidez perfecta.

## Parámetros

* **Mosaico**: *1 - 16* Reduce la entrada segmentándola.
* **Modo de desplazamiento**: *Manual, aleatorio* Cambia a un desplazamiento aleatorio en lugar de uno definido manualmente.
* **Desplazamiento**: *0.0 - 1.0*\
  Mueve o traduce el resultado. Garantiza que los píxeles estén ajustados y no interpolados.
* **Rotación**: *0.0 - 1.0* Rota la entrada a lo largo del ángulo.
* **Rotación segura del azulejo**: *Falso/Verdadero* Determina el comportamiento de la rotación, si debe ajustarse a valores seguros que no desenfoquen ningún píxel.
* **Simetría**: *ninguno, X, Y, X+Y*
* **Color de fondo**: *(valor de color) (solo versión de color)*
* **Modo Mipmap**: *Automático, Manual* Determina el modo de mipmapping. Si se establece en Manual, se obtienen resultados más nítidos.
* **Nivel de mapa MIP**: *0 - 10* Cuando el modo Mipmap está establecido en Manual, esto le permite elegir un Mipmap diferente.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
