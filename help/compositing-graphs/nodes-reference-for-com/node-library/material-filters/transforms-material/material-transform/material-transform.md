---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Utilice el nodo Transformación de material para aplicar transformaciones a las salidas de material, incluidas la rotación, la escala y el desplazamiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformación de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# Transformación de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-transforms.png){width="128px"}

## Transformación de material

**En:** *Filtros/Transformaciones De Materiales*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Transformación de material es simplemente la versión de materiales &quot;multicanal&quot; de [el nodo 2D de transformación atómica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Transforma todos los canales de un material de entrada al mismo tiempo, con la misma interfaz que Transformar 2D.

Solo asegúrese de configurar los canales correctamente! De forma predeterminada, se habilitan tanto Metálico/Rugosidad como Specular/Brillo, lo que podría provocar cierta confusión.

## Parámetros

* **Transformación**: *(Matriz de transformación)*\
  Rota y escala el resultado. El desplazamiento/desplazamiento se realiza mediante el parámetro Desplazamiento
* **Desplazamiento**: *-0,5 - 0,5*\
  Mueve o traduce el resultado. Cuando el control Transformación está presente, el resultado se puede modificar interactuando directamente con el lienzo.
* **Formato normal**\
  Elija entre los formatos DirectX y OpenGL (verde inverso).
* **Canales**\
  Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
