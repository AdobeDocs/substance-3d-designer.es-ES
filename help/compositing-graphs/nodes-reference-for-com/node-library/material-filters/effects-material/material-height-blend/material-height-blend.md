---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de Height de material para fusionar varios materiales en función de los mapas de height para crear efectos de material en capas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión de Height de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# Fusión de Height de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

<b>En:</b> Filtros de material > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo es una versión más avanzada de [Height Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md) que combina dos materiales en función de sus mapas de altura. No hay una máscara definida por el usuario, por lo que debe tener dos mapas de altura, uno para cada material, de los cuales al menos uno no es un valor uniforme.

Esto puede ser útil para combinar dos materiales diferentes de alta calidad sin una máscara de mezcla de alta calidad.

Si deseas mezclar agua o nieve, los nodos [Snow Cover](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) y [Water Level](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md) están disponibles en su lugar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Desplazamiento de Height</b> <i>0.0 - 1.0</i> | Desplaza los mapas de altura de forma que el nivel de fusión se mueva a lo largo del eje del height. Este es el control principal de la fusión. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste de la fusión y perfecciona las transiciones. |
| <b>Modo</b> <i>height equilibrado, prioridad de height inferior</i> |  |
| <b>Opacidad</b> <i>0.0 - 1.0</i> | Opacidad de fusión del height en primer plano, lo funde hacia dentro o hacia fuera. |
| <b>Coincidencia de Albedo</b> <i>0.0 - 1.0</i> | Cantidad de coincidencia de color interna que se debe realizar entre los colores de Albedo. |
