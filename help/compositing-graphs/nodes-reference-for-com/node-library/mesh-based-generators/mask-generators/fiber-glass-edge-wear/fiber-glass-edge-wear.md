---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Utilice el nodo Edge Wear de fibra de vidrio para generar máscaras de desgaste en bordes de fibra de vidrio en función de la curvatura de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de fibra de vidrio
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 6%

---


# Edge Wear de fibra de vidrio

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fiber-glass-edge-wear.resources/fiber-glass-edge-wear-01.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Representa una máscara específicamente destinada a un tipo de fibra de vidrio de desgaste, tal vez podría ser utilizado para tela. Debido a la naturaleza muy enlosada y repetitiva de las fibras, la fusión triplanar puede habilitarse opcionalmente.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para el resaltado de bordes. ¡Obligatorio! |
| <b>Oclusión de ambiente</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para enmascarar áreas ocluidas. No es obligatorio, pero definitivamente recomendable. |
| <b>Entrada de Suciedad</b> <i>Entrada en escala de grises</i> | Ranura personalizada opcional para anular el patrón de fibra. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |
| <b>Normal del Espacio Mundial</b> <i>Entrada de color</i> | Solo se usa para triplanar. |
| <b>Posición</b> <i>Entrada de color</i> | Solo se usa para triplanar. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel de desgaste</b> <i>0.0 - 1.0</i> | Como un [Histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), revela progresivamente el desgaste. |
| <b>Contraste de desgaste</b> <i>0.0 - 1.0</i> | Define el contraste total del efecto. |
| <b>Smoothness de bordes</b> <i>0.0 - 16.0</i> | Define el sangrado/desenfoque de aristas resaltadas. |
| <b>Cantidad de Suciedades</b> <i>0.0 - 1.0</i> | Define la cantidad de efecto de fibra que se debe fusionar entre los bordes. Ajusta esto junto con el nivel de desgaste para obtener el máximo control. |
| <b>Enmascaramiento de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Define la cantidad de influencia que tiene el AO para ocultar el efecto. |
| <b>Peso de curvatura</b> <i>0.0 - 1.0</i> | Define la cantidad de influencia que tienen las aristas convexas de la curvatura. |
| <b>Usar Suciedad personalizada</b> <i>Falso/Verdadero</i> | Reemplaza las fibras integradas con el mapa personalizado. |
| <b>Usar triplanar</b> <i>Falso/Verdadero</i> | Permite que [Tri Plana](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) oculte las costuras. |
| <b>Contraste de fusión triplanar</b> <i>0.0 - 1.0</i> | Controla el contraste del efecto Triplanar. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="fiber-glass-edge-wear.resources/fiber-glass-edge-wear-02.gif" />
        </td>
    </tr>
</table>
