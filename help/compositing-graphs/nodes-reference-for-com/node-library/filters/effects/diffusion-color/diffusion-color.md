---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-color.html"
breadcrumb-title: ''
description: Utilice el nodo Color de difusión para aplicar efectos de difusión de color para crear transiciones y fusiones de color suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color de difusión
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 4%

---


# Color de difusión

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-color.resources/diffusion-color-icon.png){width="200px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aplique un proceso de difusión a los colores en la entrada de imagen **Source** de acuerdo con la entrada de imagen **Mask** proporcionada, lo que crea gradaciones suaves entre los colores al usar [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html).

Solo se difuminan los colores de los píxeles que coinciden con la máscara; otros píxeles no participan en el resultado.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Origen</b> <i>Color</i> | La imagen que se va a difundir. |
| <b>Máscara</b> <i>Escala de grises</i> | Máscara de difusión: los píxeles blancos se muestrean en <i>Source</i> y se difuminan en píxeles negros. La imagen debe ser en blanco y negro. Si la máscara incluye degradados, el valor de límite es 0,5. |
| <b>Intensidad</b> <i>Escala de grises</i> | Define localmente qué tan fuerte se aplica el proceso de difusión. Este mapa debe ser <i>contrastado</i> para lograr un efecto apreciable. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Iteraciones</b> <i>0.0 - 64.0</i> | El número de iteraciones de difusión que se deben realizar (más alto es mejor, pero más lento). Los valores útiles se encuentran en el intervalo [8, 48].<br>Tenga en cuenta que si no está buscando corrección matemática, los valores bajos son correctos o incluso mejores. |
| <b>Distancia</b> <i>0.0 - 1.0</i> | Ajusta la distancia máxima de la difusión. |
| <b>Habilitar tramado</b> <i>Verdadero/Falso</i> | Controla el método de muestreo de cada pasada. El tramado permite la convergencia en menos pasadas, pero introduce ruido.<br>Sin ella, cada pase es más rápido, pero se requieren más pases para lograr un resultado sin problemas sin defectos de bandas. |
| <b>Es Mapa de normales</b> <i>Verdadero/Falso</i> | Agrega una normalización a los valores en cada paso. |
| <b>Usar Alpha como máscara</b> <i>Verdadero/Falso</i> | Use el canal alfa de la entrada <i>Source</i> como máscara de difusión, en lugar de la entrada <i>Mask</i>. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02a-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02b-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-01-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-uv-01b-after-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-uv-01a-after-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-normal.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-normal-render.jpg" />
        </td>
    </tr>
</table>
