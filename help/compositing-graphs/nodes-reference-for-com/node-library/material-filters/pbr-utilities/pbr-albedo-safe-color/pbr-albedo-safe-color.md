---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Color seguro para el Albedo PBR

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-albedo-safe-color.png){width="128px"}

## Color seguro para el Albedo PBR

**En:** *Utilidades de filtros de materiales/PBR*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este es un nodo de utilidad que realiza correcciones si los valores de Basecolor o Diffuse están fuera de un rango aceptable y correcto de PBR. Cuando se establece en Metálico, el nodo también intenta corregir los valores de Color base en función de la intensidad Metálica.

Consulta también [PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) para obtener información visual sobre qué áreas podrían estar equivocadas.

Esto es útil como una herramienta de corrección rápida, especialmente cuando todavía se está aprendiendo PBR, pero no está pensada como una medida absoluta que siempre se supone que es correcta.

## Parámetros

* **Flujo de trabajo de PBR**: *Color base - Metálico, Difuso - Specular* Cambia entre dos flujos de trabajo PBR diferentes.
* **Tolerancia**: *0.0 - 1.0* Nivel de tolerancia para valores fuera del intervalo.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
