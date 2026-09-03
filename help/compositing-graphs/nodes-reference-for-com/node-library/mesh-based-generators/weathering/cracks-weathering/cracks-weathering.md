---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo Grietas de intemperismo para añadir patrones de grietas a los materiales en función de la curvatura de la malla y los puntos de tensión.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grietas Desgaste
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Grietas Desgaste

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cracks-weathering.resources/cracks-weathering-01.png){width="128px"}

<b>En:</b> Generadores Basados En Malla > Meteorización

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Se trata de un efecto de material completo que funciona en varios canales a la vez. Añade un patrón de grietas aleatorio, con control sobre la propagación y la profundidad.

Asegúrate de entender correctamente los [Modos de creación de vínculos](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) al trabajar con materiales completos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa horneado o generado utilizado para efectos internos y enmascaramiento. |
| <b>Height</b> <i>Entrada en escala de grises</i> | Mapa horneado o generado utilizado para efectos internos y enmascaramiento. |
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Avanzado</b> |  |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Máscara</b> <i>Falso/Verdadero</i> | Activa o desactiva el uso del mapa de máscara. |
| <b>Efecto</b> |  |
| <b>Propagación de Grietas</b> <i>0.0 - 1.0</i> | Hasta dónde deben extenderse las grietas. Este es el control principal de este efecto. |
| <b>Profundidad de Grietas</b> <i>0.0 - 1.0</i> | Profundidad del efecto crack. Esto afecta principalmente al height y afecta ligeramente al thickness visual. |
| <b>Fusión</b> | Controla la intensidad con la que el efecto se fusiona en cada canal resultante. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cracks-weathering.resources/cracks-weathering-02.gif" />
        </td>
    </tr>
</table>
