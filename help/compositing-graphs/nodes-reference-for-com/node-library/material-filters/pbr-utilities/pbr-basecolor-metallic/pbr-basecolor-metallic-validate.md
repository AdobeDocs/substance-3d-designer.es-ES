---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: Use el nodo Validación metálica de PBR BaseColor para validar y corregir los valores de color base y metálico de los materiales PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Validación Metálica de BaseColor de PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# PBR BaseColor / Validación metálica

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

<b>En:</b> Filtros de material > Utilidades de PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de utilidad que genera un &quot;mapa de calor&quot; entre bueno y malo en el que los valores son correctos o incorrectos según los estándares de PBR.

Es muy útil como herramienta de aprendizaje para la PBR, ya que proporciona una retroalimentación visual muy clara de cuáles son los errores y dónde se pueden encontrar.

No uses esto como herramienta para todo, pero asegúrate de tener siempre una comprensión clara de por qué estás rompiendo cualquier regla que esta herramienta pueda destacar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de validación</b> <i>Albedo, Metal, Combinado</i> | Establece si se debe comprobar sólo el Albedo, el metal o ambos combinados como modo de descripción general. |
| <b>Umbral de rango oscuro de Albedo</b> <i>50 sRGB, 30 sRGB</i> | Establece el límite de Albedo inferior en 50 o 30 sRGB. Puede disminuir o aumentar la tolerancia de las áreas rojas. |
| <b>Rango de reflejo de metal</b> <i>70-100% Reflectante, 60-100% Reflectante</i> | Cambia el rango metálico para que se considere correcto. Puede disminuir o aumentar la tolerancia de las áreas rojas. |
| <b>Mapa de superposición</b> <i>Falso/Verdadero</i> | El modo de depuración rápida para superponer los mapas de entrada permite un seguimiento más rápido de las áreas problemáticas. |
