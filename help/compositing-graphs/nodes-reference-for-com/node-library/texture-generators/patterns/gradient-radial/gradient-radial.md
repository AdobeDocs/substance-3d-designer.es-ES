---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
breadcrumb-title: ''
description: Utilice el nodo Degradado radial para crear degradados radiales que irradian desde un punto central para transiciones circulares de color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Gradient Radial
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Degradado radial
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# Degradado radial

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-radial.resources/gradient-radial-01.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

De forma similar a [Gradient Circular](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md), crea una transición de degradado en escala de grises definida por dos puntos personalizados de forma radial. La transición va de a a b, definida por el punto central y el radio. Ten en cuenta que los resultados no siempre se segmentarán.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Forma</b> <i>Cono, Hemisferio</i> | Determina el perfil de transición. El cono es una transición lineal nítida, el hemisferio es suave y redondeado en el centro. |
| <b>Punto 1</b> | Punto central del degradado. Empieza en blanco. |
| <b>Punto 2</b> | Punto de radio para determinar la extensión del degradado. Termina en negro. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Active la compensación de aplastamiento y estiramiento con proporciones que no sean de cuadrados. |
