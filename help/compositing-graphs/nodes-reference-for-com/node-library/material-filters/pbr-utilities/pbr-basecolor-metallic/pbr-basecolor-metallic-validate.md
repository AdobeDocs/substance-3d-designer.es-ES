---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# PBR BaseColor / Validación metálica

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

## PBR BaseColor / Validación metálica

**En:** *Utilidades de filtros de materiales/PBR*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo de utilidad que genera un &quot;mapa de calor&quot; entre bueno y malo en el que los valores son correctos o incorrectos según los estándares de PBR.

Es muy útil como herramienta de aprendizaje para la PBR, ya que proporciona una retroalimentación visual muy clara de cuáles son los errores y dónde se pueden encontrar.

No uses esto como herramienta para todo, pero asegúrate de tener siempre una comprensión clara de por qué estás rompiendo cualquier regla que esta herramienta pueda destacar.

## Parámetros

* **Modo de validación**: *Albedo, Metal, Combinado* Establece si se debe comprobar solo Albedo, Metal o ambos combinados como modo de descripción general.
* **Umbral de rango oscuro de Albedo**: *50 sRGB, 30 sRGB* Establece el límite de Albedo inferior en 50 o 30 sRGB. Puede disminuir o aumentar la tolerancia de las áreas rojas.
* **Rango de reflejo de metal**: *70-100% reflectante, 60-100% reflectante* Cambia el rango metálico para que se considere correcto. Puede disminuir o aumentar la tolerancia de las áreas rojas.
* **Mapa de superposición**: *Falso/Verdadero* El modo de depuración rápida para superponer mapas de entrada permite un seguimiento más rápido de las áreas problemáticas.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
