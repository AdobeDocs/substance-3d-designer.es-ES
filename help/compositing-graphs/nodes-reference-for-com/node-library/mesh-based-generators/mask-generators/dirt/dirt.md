---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Utilice el nodo Dirt para generar máscaras de acumulación de dirt basadas en la curvatura, posición y oclusión de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tierra
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---


# Tierra

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dirt.resources/dirt.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa dirtes en bordes y esquinas ocluidos y hundidos, en función de la AO y la curvatura hechas un bake.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. ¡Obligatorio! |
| <b>Oclusión ambiental</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. ¡Obligatorio! |
| <b>Entrada de Suciedad</b> <i>Entrada en escala de grises</i> | Entrada de mapa de suciedad personalizada, opcional, activada por parámetro. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |
| <b>Normal del Espacio Mundial</b> <i>Entrada de color</i> | Solo se usa para triplanar. |
| <b>Posición</b> <i>Entrada de color</i> | Solo se usa para triplanar. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel de Dirt</b> <i>0.0 - 1.0</i> | Control principal de la cantidad de dirt. |
| <b>Contraste de Dirt</b> <i>0.0 - 1.0</i> | Controla el contraste principal del dirt de la máscara. |
| <b>Cantidad de Suciedades</b> <i>0.0 - 1.0</i> | Define qué grado de suciedad tiene el dirt. Ajuste a 0 para obtener un dirt perfectamente suave. |
| <b>Enmascaramiento de bordes</b> <i>0.0 - 1.0</i> | Cantidad de dirt que se debe quitar de los bordes elevados (según el mapa de curvatura). |
| <b>Usar Suciedad personalizada</b> <i>Falso/Verdadero</i> | Permite el uso de entradas de mapa de suciedad personalizadas en lugar de Suciedad integrada. |
| <b>Escala de Suciedad</b> <i>1 - 16</i> | Establece la escala de mosaico de los detalles de Suciedad. |
| <b>Usar triplanar</b> <i>Falso/Verdadero</i> | Usa la [proyección triplanar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) para la asignación de Suciedades y elimina las costuras. |
| <b>Contraste de fusión triplanar</b> <i>0.001 - 1.0</i> | Define el contraste de la proyección triplanar. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dirt.resources/dirt-ex.gif" />
        </td>
    </tr>
</table>
