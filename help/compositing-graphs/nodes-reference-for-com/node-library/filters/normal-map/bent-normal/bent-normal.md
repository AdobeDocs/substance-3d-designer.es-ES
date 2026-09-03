---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: Utilice el nodo Normal doblada (Bent Normal) para generar mapas normales doblados que tengan en cuenta la oclusión ambiente y la luz indirecta.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal doblada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# Normal doblada

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo normal doblado](bent-normal.resources/bent-normal-01.png "Icono de nodo normal doblado")

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera un mapa normal doblado basado en una entrada de mapa de height. Un mapa normal doblado es una versión especial de [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) y [Oclusión ambiente (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md), que generan un mapa normal con oclusión ambiente incrustada.\
Esto se puede utilizar en motores en tiempo real para que la Oclusión ambiental se convierta en el mapa normal, por ejemplo para obtener reflejos de oclusión más precisos sobre los metales.

Este nodo no debe utilizarse en combinación con el motor de CPU (SSE) debido al tiempo de cálculo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Usar Tamaño físico</b> <i>Booleano</i> | Active esta opción para usar la configuración de Tamaño físico para determinar la escala de height. |
| <b>Tamaño físico</b> <i>Float3</i> | (Disponible cuando <b>Usar Tamaño físico</b> está establecido en <i>Verdadero</i>) Ajusta la escala de height en función del tamaño físico real de la superficie. |
| <b>Ejemplos</b> <i>Entero</i> | Número de rayos utilizados para calcular la normal doblada.<br>Un valor más alto proporciona un resultado más suave y preciso a costa del rendimiento. |
| <b>Escala de Height</b> <i>Flotador</i> | (Disponible cuando Usar Tamaño físico está establecido en Falso) Multiplicador para la intensidad de la entrada del mapa de altura. |
| <b>Distribución</b> <i>Entero</i> | Establece el método de distribución. Afecta a la difuminación hacia áreas sombreadas. |
| <b>Distancia máxima</b> <i>Flotador</i> | Define la distancia máxima que los rayos pueden recorrer para ser ocluidos. |
| <b>Ángulo de pliego</b> <i>Flotador</i> | Define el ángulo de propagación de los rayos a los que se disparará. Un valor de 1 es un hemisferio completo. |
| <b>Formato normal</b> <i>Entero</i> | Invierte el canal verde de la salida. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bent-normal.resources/bent-normal-02.jpg" />
        </td>
    </tr>
</table>
