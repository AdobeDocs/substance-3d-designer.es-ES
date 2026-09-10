---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transforma de material para aplicar transformaciones a salidas de material, incluidas la rotación, la escala y el desvío.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# Transformación de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transforms.png){width="128px"}

<b>En:</b> Filtros de material > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

La Transforma de materiales es simplemente la versión de materiales &quot;multicanal&quot; de [el nodo de Transformación 2D atómico](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Transforma todos los canales de un material de entrada al mismo tiempo, con la misma interfaz que Transformar 2D.

Solo asegúrese de configurar los canales correctamente! De forma predeterminada, están activadas tanto la opción Metálico/Rugosidad como Specular/Brillo, lo que podría provocar cierta confusión.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Transformación</b> <i>(Matriz de transformación)</i> | Rota y escala el resultado. El desplazamiento/desplazamiento se realiza mediante el parámetro Desplazamiento |
| <b>Desplazamiento</b> <i>-0.5 - 0.5</i> | Mueve o traduce el resultado. Cuando el control Transformación está presente, el resultado se puede modificar interactuando directamente con el lienzo. |
| <b>Formato normal</b> | Elija entre los formatos DirectX y OpenGL (verde inverso). |
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
