---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Utilice el nodo Recorte automático para recortar automáticamente las texturas, eliminar los bordes vacíos y optimizar las dimensiones de la textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recorte automático
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Recorte automático

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

**En:** Filtros*/Transformaciones*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo **Recorte automático** ajusta la **Entrada** para que su contenido se coloque en el *centro* de la imagen sin que se le cambie el tamaño, o *se cambie de tamaño según el tamaño* de la imagen.

El contenido de la imagen se define mediante un cuadro ajustado a los *primeros y últimos píxeles* de **X** e **Y**, cuyos valores son *superiores a 0* (es decir, no negros). La versión de **Color** te permite elegir entre los canales de RGB y Alpha para definir ese cuadro.

</td>
</tr>
</table>

## Parámetros

* **Modo** *Entero* Establezca el método de recorte que debe aplicarse:
  * *Cuadrado de recorte*: la imagen se recorta de modo que la forma esté en el centro de la imagen más pequeña de *cuadrado* que pueda incluirla por completo
  * *Recortar automáticamente*: La imagen se recorta de modo que la forma esté en el centro de la imagen más pequeña *cuadrada o no cuadrada* que pueda incluirla por completo
  * *Ajustar (Mantener proporción)*: El tamaño de la imagen cambia al *tamaño completo* de la imagen, manteniendo sus *proporciones* (es decir, la relación entre anchura y longitud)
  * *Rellenar (estirar)*: El tamaño de la imagen cambia al *tamaño completo* de la imagen
* **Usar alfa** *booleano* Usa el canal alfa de **Input** para determinar los *límites* del contenido de la imagen para el recorte. Cuando se establece en *False*, se utilizan píxeles negros en su lugar.\
  *Nota*: Este parámetro solo está disponible en la versión **Color** del nodo.
* **Modo de filtrado** *Entero* Define cómo tratar los resultados muestreados al *interpolar* entre píxeles:
  * *Más cercano*: mostrará exactamente el valor *same* (más rápido)
  * *Bilineal*: aplicará un filtro bilineal en el resultado para obtener un aspecto *más suave*
  * *Automático*: Utiliza el más adecuado de los dos modos anteriores, dependiendo del **Modo** seleccionado para el recorte

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-demo-01-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant.jpg){width="128px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant4.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant3.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-node.png){width="420px"}

</td>
</tr>
</table>
