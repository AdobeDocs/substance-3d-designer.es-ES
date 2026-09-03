---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Utilice el nodo Cáustico para generar patrones de luz cáustica para crear efectos de iluminación subacuática y refractiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cáustico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# Cáustico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](caustics.resources/caustics-01.png){width="128px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera cáusticos proyectados en función de un mapa de altura y una dirección de la luz.Tanto en la versión en escala de grises como en la de color, las diferencias son sutiles, pero la versión en color añade efectos de dispersión de color. La luz se proyecta desde un único punto, no se utiliza ningún mapa de entorno.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Espacio de color de salida</b> <i>Raw, sRGB</i> | Establecer el espacio de color de salida. |
| <b>Tamaño de cuadrícula de fotones</b> <i>Auto, 512, 1024, 2048, 4096</i> | Establece la calidad ajustando el tamaño de la cuadrícula, pero de forma predeterminada la entrada coincidente. Se puede utilizar para acelerar el cálculo. |
| <b>Escala de Height de superficie</b> <i>0.0 - 1.0</i> | Multiplicador para determinar la interpretación del height. |
| <b>Posición del Height de superficie</b> <i>0.0 - 1.0</i> | Ajuste la distancia de la superficie de refracción a la proyección. |
| <b>IOR de superficie</b> <i>1.0 - 2.0</i> | Defina el índice de refracción; en la versión de color, esto añade más dispersión de color. |
| <b>Tamaño de fotón</b> <i>1.0 - 50.0</i> | El tamaño del fotón afecta a la nitidez del efecto. |
| <b>Dispersión</b> <i>0.0 - 0.01 (solo versión de color)</i> | Afecta solo a la dispersión del color. No es visible cuando el IOR es bajo. |
| <b>Vibración</b> <i>0.0 - 1.0</i> | Añada vibraciones irregulares a las partículas de fotones fundidos. |
| <b>Posición de luz</b> | Mueve la posición de la luz. También se realiza mediante un gizmo en el Vista 2D. |
| <b>Color de fondo</b> <i>(Valor de color) (Solo versión de color)</i> | Cambiar el color de fondo. Limitado al negro en la versión en escala de grises. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Active la compensación de aplastamiento y estiramiento con proporciones que no sean de cuadrados. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="caustics.resources/caustics-02.png" />
        </td>
    </tr>
</table>
