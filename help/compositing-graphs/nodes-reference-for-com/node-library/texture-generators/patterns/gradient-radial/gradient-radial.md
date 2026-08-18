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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# Degradado radial

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/gradient-radial.png){width="128px"}

## Degradado radial

**En:** *Generadores De Texturas**/Patrones*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

De forma similar a [Gradient Circular](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md), crea una transición de degradado en escala de grises definida por dos puntos personalizados de forma radial. La transición va de a a b, definida por el punto central y el radio. Ten en cuenta que los resultados no siempre se segmentarán.

## Parámetros

* **Forma: *Cono, Hemisferio***Determina el perfil de transición. El cono es una transición lineal nítida, el hemisferio es suave y redondeado en el centro.
* **Punto 1**:\
  Punto central del degradado. Empieza en blanco.
* **Punto 2**:\
  Punto de radio para determinar la extensión del degradado. Termina en negro.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Active la compensación de aplastamiento y estiramiento con proporciones que no sean de cuadrados.

</td>
</tr>
</table>
