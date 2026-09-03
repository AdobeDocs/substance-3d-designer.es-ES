---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: Usa el nodo Color seguro para Albedos PBR para asegurarte de que los colores de los albedos se encuentran dentro de rangos físicamente plausibles para los materiales PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color seguro para el Albedo PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Color seguro para el Albedo PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-albedo-safe-color.resources/pbr-albedo-safe-color-01.png){width="128px"}

<b>En:</b> Filtros de material > Utilidades de PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este es un nodo de utilidad que realiza correcciones si los valores de Basecolor o Diffuse están fuera de un rango aceptable y correcto de PBR. Cuando se establece en Metálico, el nodo también intenta corregir los valores de Color base en función de la intensidad Metálica.

Consulta también [PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) para obtener información visual sobre qué áreas podrían estar equivocadas.

Esto es útil como una herramienta de corrección rápida, especialmente cuando todavía se está aprendiendo PBR, pero no está pensada como una medida absoluta que siempre se supone que es correcta.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Flujo de trabajo de PBR</b> <i>Color base - Metálico, Difuso - Specular</i> | Cambia entre dos flujos de trabajo PBR diferentes. |
| <b>Tolerancia</b> <i>0.0 - 1.0</i> | Nivel de tolerancia para valores que están fuera del intervalo. |
