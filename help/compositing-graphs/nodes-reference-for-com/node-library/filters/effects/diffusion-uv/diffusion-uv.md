---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: Utilice el nodo UV de difusión para aplicar efectos de difusión en el espacio UV para crear transiciones y fusiones de color suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Difusión UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---


# Difusión UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-uv.resources/diffusion-uv-01.png){width="200px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aplique un proceso de difusión a las coordenadas UV en la entrada de imagen **Source** de acuerdo con la entrada de imagen **Mask** proporcionada, interpolando las coordenadas entre los valores de **Source**.

Solo se difuminan los UV de los píxeles que coinciden con la máscara; otros píxeles no participan en el resultado.

Tenga en cuenta que el mosaico se maneja de una manera especial: Cuando el mosaico está *habilitado* (que es el caso de forma predeterminada), se puede obtener un promedio de las coordenadas vecinas a través del límite 0/1.

Por ejemplo, si el valor de la coordenada U es 0,1 en un píxel y 0,8 en otro, el valor promedio será 0,95 en lugar de 0,45 porque se supone *el mosaico de las coordenadas*. Esto es independiente de la posición real del píxel: los valores de coordenadas se controlan de la misma manera en toda la imagen.

Esto puede producir resultados no deseados al usar este filtro para *deformación de textura*. Si eso sucede, asegúrate de que la máscara define &quot;curvas/puntos de control&quot; con una separación no superior a *media textura*.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Origen</b> <i>Color</i> | Los UV para difundir. Tenga en cuenta que el mosaico se administra de una manera especial en este filtro (consulte <i>Descripción</i>). |
| <b>Máscara</b> <i>Escala de grises</i> | La máscara de difusión: Los píxeles blancos se muestrean en <i>Source</i> y se difuminan en píxeles negros. La imagen debe ser en blanco y negro. Si la máscara incluye degradados, el valor de límite es 0,5. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Iteraciones</b> <i>0.0 - 64.0</i> | El número de iteraciones de difusión que se deben realizar (más alto es mejor, pero más lento). Los valores útiles se encuentran en el intervalo [8, 48].<br>Tenga en cuenta que si no está buscando corrección matemática, los valores bajos son correctos o incluso mejores. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-03.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-05.jpg" />
        </td>
    </tr>
</table>
