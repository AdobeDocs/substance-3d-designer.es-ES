---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo Filtro biselado para crear bordes biselados en formas y motivos para añadir profundidad y dimensión.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bisel (nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 4%

---


# Bisel (nodo de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza un efecto de biselado de bordes en un mapa de altura de escala de grises de entrada. Devuelve tanto el mapa de altos biselado como el mapa de normales en función de dicho mapa de altos.

Este es un nodo útil para aplicar perfiles de curva exactos en un mapa de altura básico y perfectamente binario (blanco y negro de alto contrato).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>entrada</b> <i>Entrada en escala de grises</i> | Mapa de altura para convertir. |
| <b>Curva personalizada</b> <i>Entrada en escala de grises</i> | Degradado que determina la curva/pendiente exacta. Lo ideal es un nodo lineal de degradado, en el que se pueda realizar cualquier tipo de ajuste, como [Niveles](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) o [Curvas](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md). Solo está activo cuando &quot;Usar curva personalizada&quot; es True. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Distancia</b> <i>-1.0 - 1.0</i> | Hasta dónde debe llegar el efecto biselado. |
| <b>Tipo de vértice</b> <i>Ronda, Angular</i> | Si el perfil biselado debe ser redondeado o recto. |
| <b>Suavizado</b> <i>0.0 - 5.0</i> | Cantidad de suavizado adicional (desenfoque) que se debe realizar después del bisel. |
| <b>Usar desenfoque no uniforme</b> <i>Falso/Verdadero</i> | Si el suavizado se debe realizar de forma no uniforme. |
| <b>Usar curva personalizada</b> <i>Falso/Verdadero</i> | Cambia el uso de su propia curva de height personalizada. Consulte más arriba para obtener más información. |
| <b>Intensidad normal</b> <i>0.0 - 50.0</i> | Intensidad del mapa normal generado. |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambiar entre diferentes formatos de Mapa normal (invierte el canal verde). |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/bevel-example.png" />
        </td>
    </tr>
</table>
