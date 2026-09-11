---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: Utilice el nodo Generador de ladrillos para crear patrones de ladrillos procedimientos con propiedades de mortero, desplazamiento y tamaño personalizables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generador de ladrillos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 827e738d5db4d64bf366d332a62a7bbd2fa840fc
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 8%

---


# Generador de ladrillos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](brick-generator.resources/brick-generator.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Generador avanzado de patrones de ladrillo. Tiene muchas opciones para generar patrones de ladrillo hechos por el hombre específicamente

Para obtener más opciones, consulte [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ladrillos</b> <i>1 - 64</i> | Define la cantidad de ladrillos en los ejes X e Y. |
| <b>Bisel</b> <i>0.0 - 1.0</i> | Cambia el perfil de bisel de los ladrillos, permite cambiar en dos direcciones, así como configurar el perfil de difuminado y el redondeo de las esquinas. |
| <b>Mantener proporción</b> <i>Falso/Verdadero</i> | Hace que el perfil Bisel esté vinculado al tamaño de ladrillo o no. |
| <b>Hueco</b> <i>0.0 - 1.0</i> | Hueco para dejar entre ladrillos. Tenga en cuenta que el bisel también introduce un hueco, por lo que la configuración de biseles también significa que debe compensar con este parámetro. |
| <b>Tamaño medio</b> <i>0.0 - 1.0</i> | Desplazamiento de patrón de ladrillo, cambia el tamaño de cada otra columna o fila. |
| <b>Height</b> <i>-1.0 - 1.0</i> | Modifica los perfiles de height. Permite introducir variaciones de luminancia y todo tipo de aleatorización. |
| <b>Pendiente</b> <i>-1.0 - 1.0</i> | Introduce una pendiente por ladrillo, como si ciertos ladrillos estuvieran colocados en ángulo. |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Desplaza los ladrillos en función de la fila y afecta al espaciado por fila. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-ex-01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-ex-02.gif" />
        </td>
    </tr>
</table>
