---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Utilice el nodo SDF de textura 3D para generar texturas de campo de distancia firmadas a partir de datos 3D para crear formas y efectos suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Textura 3D SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# Textura 3D SDF

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-sdf.resources/3dtexturesdf.png){width="200px"}

<b>En:</b> Filtro > Efecto

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo **3D Texture SDF** genera el *campo de distancia firmado* de una forma a partir de la máscara *3D Texture* de **Input** que representa los sectores del *volumen* de la forma.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de máscara</b> <i>Escala de grises</i> | La máscara de <i>textura 3D</i> representa los sectores del <i>volumen</i> de una forma. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Umbral</b> <i>Flotador</i> | Cuando el volumen de la forma se describe mediante un <i>degradado</i>, establece el valor de degradado en el que se <i>detecta</i> la <i>superficie</i> de la forma. |
| <b>Salida</b> <i>Entero</i> | El tipo de campo de distancia que debe generarse:<br>- <i>Campo de distancia</i>: muestra un campo de distancia que describe las distancias <i>fuera</i> de la forma.<br>- <i>Campo de distancia con signo</i>: genera un campo de distancia que describe las distancias <i>exterior</i> (positivo) e <i>interior</i> (negativo) de la forma. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-node.png" />
        </td>
    </tr>
</table>
