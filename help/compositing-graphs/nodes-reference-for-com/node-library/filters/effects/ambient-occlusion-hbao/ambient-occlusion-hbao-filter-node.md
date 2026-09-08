---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo de filtro HBAO de Oclusión ambiental para generar mapas de oclusión ambiental mediante algoritmos basados en horizonte para un sombreado realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oclusión ambiental (HBAO) (nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# Oclusión ambiental (HBAO) (nodo de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Toma un mapa de altura como entrada y genera un mapa de Oclusión ambiente a partir de él. Utiliza la Oclusión Ambiental Basada en Horizonte, un algoritmo originalmente destinado a la generación de AO en tiempo real de espacio de pantalla. Muy útil para crear mapas de procedimientos AO a partir de mapas de altura de procedimientos.

Para obtener una versión alternativa más avanzada pero más lenta del AO, consulte [Oclusión ambiental (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Usar unidades de mundo</b> <i>Falso/Verdadero</i> | Cambia el uso de las unidades de espacio de pantalla o de mundo. Activa parámetros adicionales que permiten un control más preciso. |
| <b>Profundidad de Height</b> <i>0.0 - 1.0</i> | Sólo se utiliza cuando Unidades del mundo está establecido en False. Controla la escala global. |
| <b>Tamaño de superficie</b> <i>0.0 - 1000.0</i> | Sólo se utiliza cuando Unidades del mundo está establecido en Verdadero. Controla la escala global. |
| <b>Escala de Height (cm)</b> <i>0.0 - 1000.0</i> | Sólo se utiliza cuando Unidades del mundo está establecido en Verdadero. Controla la escala global. |
| <b>Radio</b> <i>0.0 - 1.0</i> | Controla la propagación del AO. |
| <b>Calidad</b> <i>4 muestras, 8 muestras, 16 muestras</i> | Establece el nivel de calidad determinando la cantidad de muestras utilizadas para el cálculo. |
| <b>Optimización de GPU</b> <i>Falso/Verdadero</i> | Permite la optimización interna de la GPU y acelera el procesamiento. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2021-6-18-11-11-11-1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2021-6-18-11-11-22.png" />
        </td>
    </tr>
</table>
