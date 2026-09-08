---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de Height para fusionar texturas basadas en mapas de altura para crear transiciones de materiales realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de height
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Fusión de height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

<b>En:</b> Filtros de material > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Combina dos mapas de altura en función de la información de height. Genera un mapa de altura fusionado, pero también una máscara de blanco y negro que se puede utilizar en otros lugares.

Esto resulta útil cuando tiene que combinar dos mapas de altura de alta calidad, pero no necesariamente un material completo, como se requiere para la [Fusión de Height de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height superior</b> <i>Entrada en escala de grises</i> |  |
| <b>Height inferior</b> <i>Entrada en escala de grises</i> |  |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Desplazamiento de Height</b> <i>0.0 - 1.0</i> | Desplaza los mapas de altura de forma que el nivel de fusión se mueva a lo largo del eje del height. Este es el control principal de la fusión. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste de la fusión y perfecciona las transiciones. |
| <b>Modo</b> <i>height equilibrado, prioridad de height inferior</i> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Opacidad de fusión del height en primer plano, lo funde hacia dentro o hacia fuera. |
