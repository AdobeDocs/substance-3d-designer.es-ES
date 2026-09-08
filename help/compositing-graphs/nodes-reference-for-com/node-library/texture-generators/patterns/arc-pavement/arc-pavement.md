---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Utilice el nodo Pavimento de arco para generar patrones de pavimento en forma de arco para crear texturas curvas de carretera y trazado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pavimento de arco
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 11%

---


# Pavimento de arco

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera un patrón de pavimento de arco parisino. Este efecto no se puede lograr con [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) estándar o [Sampler en mosaico](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md), de ahí este nodo dedicado.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>1 - 8</i> | Establece la escala o el mosaico global. |
| <b>Cantidad de patrón</b> <i>1 - 32</i> | Define la cantidad de ladrillos utilizados en cada arco. |
| <b>Aleatorio de cantidad de patrón</b> <i>0.0 - 1.0</i> | Aleatoriza la cantidad de ladrillos en cada arco. Tiene el efecto añadido de dar a los ladrillos diferentes escalas. |
| <b>Cantidad mínima del patrón</b> <i>1 - 10</i> | Controla la cantidad mínima de ladrillos al aleatorizar arcos. |
| <b>Cantidad De Arcos</b> <i>0 - 20</i> | Define la cantidad de arcos apilados verticalmente. Cambia el height del ladrillo. |
| <b>Patrón</b> <i>Imagen De Entrada, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradaciones, Ondas, Media campana, Campana Cortada, Media Luna, Cápsula, Cono</i> | Selecciona la forma de motivo que se va a utilizar. |
| <b>Filtrado de imágenes de entrada</b> <i>Bilineal + Mipmaps, Bilineal, Más Cercano</i> |  |
| <b>Escala de patrón</b> <i>0.0 - 1.0</i> | Define la escala de cada mosaico. |
| <b>Ancho de motivo</b> <i>0.0 - 1.0</i> | Define la anchura de cada azulejo. |
| <b>Height de motivo</b> <i>0.0 - 1.0</i> | Define el height de cada mosaico. |
| <b>Anchura aleatoria del patrón</b> <i>0.0 - 1.0</i> | Aleatoriza la anchura del azulejo. |
| <b>Aleatorio de Height de motivo</b> <i>0.0 - 1.0</i> | Aleatoriza el height del azulejo. |
| <b>Anchura de patrón global aleatoria</b> <i>0.0 - 1.0</i> | Aleatoriza la anchura del azulejo, sin crear espacios más grandes entre ellos. |
| <b>Disminución de Height de motivo</b> <i>0.0 - 1.0</i> | Controla el aplastamiento del height de azulejo en los extremos de cada arco. |
| <b>Aleatorio de color</b> <i>0.0 - 1.0</i> | Aleatoriza los colores del azulejo. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/arcpavement-ex.png" />
        </td>
    </tr>
</table>
