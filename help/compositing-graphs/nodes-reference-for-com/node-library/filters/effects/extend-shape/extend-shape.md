---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Utilice el nodo Extend Shape para extender formas más allá de sus límites y crear efectos de máscara y motivo expandidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo <b>Extend Shape</b> extiende una <i>sección</i> de <b>Input</b> en una dirección y distancia establecidas.

El parámetro <b>Show helper</b> te permite visualizar la sección extendida y la dirección de la extensión.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo</b> <i>Entero</i> | Define los <i>parámetros</i> utilizados para aplicar la extensión:<br><br>- <i>Bidireccional</i>: La sección de <b>Entrada</b> especificada por <b>Posición de extensión</b> y <b>Ángulo de extensión</b> se extiende sobre la <b>Distancia de extensión</b> en <i>direcciones opuestas</i><br>- <i>Unidireccional</i>: La sección de <b>Entrada</b> especificada por <b>Posición de extensión</b> y <b>Ángulo de extensión</b> se extiende sobre la <b>Distancia de extensión</b> en una <i>dirección única</i><br>- <i>Posiciones de inicio/fin</i>: La extensión <i>vector</i> está definida por <b>Posición inicial</b> y <b>Posición final</b>. La sección <i>perpendicular</i> de <b>Input</b> en <b>Start Position</b> se extiende <i>sobre este vector</i> hasta <b>End Position</b> |
| <b>Distancia de extensión</b> <i>Flotador</i> | Distancia a la que se debe extender la sección especificada por <b>Posición de extensión</b> y <b>Ángulo de extensión</b>. La distancia se expresa como <i>proporción</i> del tamaño de la imagen. |
| <b>Posición de extensión</b> <i>Flotador</i> | La posición en la imagen de la sección que debe extenderse. El valor se expresa como un <i>desplazamiento desde el centro</i>. |
| <b>Ángulo de extensión</b> <i>Flotador</i> | El ángulo de la sección que debe extenderse, teniendo en cuenta el punto de partida, es una <i>sección vertical</i>. |
| <b>Posición inicial</b> <i>Float2</i> | Posición inicial del <i>vector de extensión</i>. |
| <b>Posición final</b> <i>Float2</i> | Posición final del <i>vector de extensión</i>. |
| <b>Desplazamiento de luminancia inicial</b> <i>Flotador</i> | Aplica un desplazamiento de luminancia al área de la imagen <i>anterior</i> a la sección extendida. Este desplazamiento de luminancia está <i>interpolado a lo largo de la sección</i> a la luminancia del área de la imagen que sigue a la sección.<br><br><i>Nota</i>: Este parámetro solo está disponible en la versión <b>Grayscale</b> del nodo. |
| <b>Desplazamiento de luminancia final</b> <i>Flotador</i> | Aplica un desplazamiento de luminancia al área de la imagen <i>que sigue</i> a la sección extendida. Este desplazamiento de luminancia está <i>interpolado a lo largo de la sección</i> a la luminancia del área de la imagen que precede a la sección.<br><br><i>Nota</i>: Este parámetro solo está disponible en la versión <b>Grayscale</b> del nodo. |
| <b>Lum. El desplazamiento omite los píxeles negros</b> <i>Booleano</i> | Cuando se establece en <i>True</i>, los desplazamientos de luminancia especificados en <i>both</i> <b>Desplazamiento de luminancia inicial</b> y <b>Desplazamiento de luminancia final</b> solo se aplican a <i>píxeles no negros</i>, es decir, píxeles cuyo valor es superior a 0.<br><br><i>Nota</i>: Este parámetro solo está disponible en la versión <b>Grayscale</b> del nodo. |
| <b>Modo de filtrado</b> <i>Entero</i> | Define cómo tratar los resultados muestreados al <i>interpolar</i> entre píxeles:<br><br>- <i>Más cercano</i>: mostrará exactamente el <i>mismo valor</i> (más rápido)<br>- <i>Bilineal</i>: aplicará un filtro bilineal en el resultado para obtener un aspecto <i>más suave</i> |
| <b>Mostrar ayudante</b> <i>Booleano</i> | Visualice la <i>sección extendida</i> como una superposición con flechas que muestran la <i>dirección</i> de la extensión. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/extendshape.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/extendshape-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/extendshape-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/extendshape-node.png" />
        </td>
    </tr>
</table>
