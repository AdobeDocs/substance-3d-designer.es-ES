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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

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

**En:** Filtros*/Efectos*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo **Extend Shape** extiende una *sección* de **Input** en una dirección y distancia establecidas.

El parámetro **Show helper** te permite visualizar la sección extendida y la dirección de la extensión.

</td>
</tr>
</table>

## Parámetros

* **Modo** *Entero* Define los *parámetros* utilizados para aplicar la extensión:
  * *Bidireccional*: La sección de **Entrada** especificada por **Posición de extensión** y **Ángulo de extensión** se extiende sobre la **Distancia de extensión** en *direcciones opuestas*
  * *Unidireccional*: La sección de la **Entrada** especificada por la **Posición de extensión** y el **Ángulo de extensión** se extiende sobre la **Distancia de extensión** en una *dirección única*
  * *Posiciones de inicio/finalización*: La extensión *vector* está definida por **Posición inicial** y **Posición final**. La sección *perpendicular* de **Input** en **Start Position** se extiende *sobre este vector* hasta **End Position**
* **Distancia de extensión** *Flotante* Distancia a la que se debe extender la sección especificada por **Posición de extensión** y **Ángulo de extensión**. La distancia se expresa como *proporción* del tamaño de la imagen.
* **Posición de extensión** *Float* Posición en la imagen de la sección que debe extenderse. El valor se expresa como un *desplazamiento desde el centro*.
* **Ángulo de extensión** *Flotante* El ángulo de la sección que debe extenderse, teniendo en cuenta que el punto de partida es una *sección vertical*.
* **Posición inicial** *Float2* Posición inicial del *vector de extensión*.
* **Posición final** *Float2* Posición final del *vector de extensión*.
* **Desplazamiento de luminancia inicial** *Flotante* Aplica un desplazamiento de luminancia al área de la imagen *anterior* a la sección extendida. Este desplazamiento de luminancia se *interpola a lo largo de la sección* a la luminancia del área de la imagen que sigue a la sección.\
  *Nota*: Este parámetro solo está disponible en la versión **Grayscale** del nodo.
* **Desplazamiento de luminancia final** *Flotante* Aplica un desplazamiento de luminancia al área de la imagen *después* de la sección extendida. Este desplazamiento de luminancia se *interpola a lo largo de la sección* a la luminancia del área de la imagen que precede a la sección.\
  *Nota*: Este parámetro solo está disponible en la versión **Grayscale** del nodo.
* **Lum. Desplazamiento omite los píxeles negros** *Boolean* Si se establece en *True*, los desplazamientos de luminancia especificados en *tanto* Desplazamiento de luminancia inicial **como** Desplazamiento de luminancia final **solo se aplican a** píxeles no negros *, es decir, píxeles cuyo valor es superior a 0.*\
  *Nota*: Este parámetro solo está disponible en la versión **Grayscale** del nodo.
* **Modo de filtrado** *Entero* Define cómo tratar los resultados muestreados al *interpolar* entre píxeles:
  * *Más cercano*: mostrará exactamente el valor *same* (más rápido)
  * *Bilineal*: aplicará un filtro bilineal en el resultado para obtener un aspecto *más suave*
* **Mostrar asistente** *Boolean* Visualiza la *sección extendida* como una superposición con flechas que muestran la *dirección* de la extensión.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-node.png){width="360px"}

</td>
</tr>
</table>
