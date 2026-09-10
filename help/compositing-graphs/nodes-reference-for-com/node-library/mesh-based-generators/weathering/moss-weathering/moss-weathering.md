---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo Meteorización de musgo para añadir patrones de crecimiento de musgo a los materiales en función de la curvatura y posición de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Meteorización del musgo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 7%

---


# Meteorización del musgo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](moss-weathering.resources/moss-weathering.png){width="128px"}

<b>En:</b> Generadores Basados En Malla > Meteorización

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Se trata de un efecto de material completo que funciona en varios canales a la vez. Genera un efecto de musgo crecido, con un único control de Propagación.

Este efecto funciona mejor con un mapa de posición del espacio mundial al horno y un mapa de altura adicional. Si bien este no es un requisito exacto, que presta el efecto de ubicación más creíble.

Asegúrate de entender correctamente los [Modos de creación de vínculos](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) al trabajar con materiales completos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Posición</b> <i>Entrada de color</i> | Posición espacial del mundo al horno. |
| <b>Height</b> <i>Entrada en escala de grises</i> | Entrada adicional de Heightmap. |
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
| <b>Propagación de musgo</b> <i>0.0 - 1.0</i> | Define la extensión del musgo. Crece en pasos desde una ligera cobertura hasta musgo oscuro grueso y pesado. |
| <b>Fusión</b> |  |
| <b>Intensidad de Difuso</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la difusión. |
| <b>Intensidad de Color base</b> <i>0.0 - 1.0</i> | Intensidad de fusión del color base. |
| <b>Intensidad normal</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la Normal. |
| <b>Intensidad del Specular</b> <i>0.0 - 1.0</i> | Fusión del Specular. |
| <b>Intensidad de Brillo</b> <i>0.0 - 1.0</i> | Fuerza de fusión del Brillo. |
| <b>Intensidad de rugosidad</b> <i>0.0 - 1.0</i> | Fuerza de fusión de la rugosidad. |
| <b>Intensidad de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Fuerza de fusión de la Oclusión ambiente. |
| <b>Intensidad de Height</b> <i>0.0 - 1.0</i> | Fusión del Height. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="moss-weathering.resources/moss-ex.gif" />
        </td>
    </tr>
</table>
