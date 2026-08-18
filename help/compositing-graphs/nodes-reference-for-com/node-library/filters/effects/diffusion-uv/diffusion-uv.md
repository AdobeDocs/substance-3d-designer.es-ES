---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: Utilice el nodo UV de difusión para aplicar efectos de difusión en el espacio UV para crear transiciones y fusiones de color suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Difusión UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# Difusión UV

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

**En:** *Filtros/Efectos*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

Aplique un proceso de difusión a las coordenadas UV en la entrada de imagen **Source** de acuerdo con la entrada de imagen **Mask** proporcionada, interpolando las coordenadas entre los valores de **Source**.

Solo se difuminan los UV de los píxeles que coinciden con la máscara; otros píxeles no participan en el resultado.

Tenga en cuenta que el mosaico se maneja de una manera especial: Cuando el mosaico está *habilitado* (que es el caso de forma predeterminada), se puede obtener un promedio de las coordenadas vecinas a través del límite 0/1.

Por ejemplo, si el valor de la coordenada U es 0,1 en un píxel y 0,8 en otro, el valor promedio será 0,95 en lugar de 0,45 porque se supone *el mosaico de las coordenadas*. Esto es independiente de la posición real del píxel: los valores de coordenadas se controlan de la misma manera en toda la imagen.

Esto puede producir resultados no deseados al usar este filtro para *deformación de textura*. Si eso sucede, asegúrate de que la máscara define &quot;curvas/puntos de control&quot; con una separación no superior a *media textura*.

</td>
</tr>
</table>

## Parámetros

* **Iteraciones**: *0.0 - 64.0* El número de iteraciones de difusión que se van a realizar (más alto es mejor pero más lento). Los valores útiles se encuentran en el intervalo [8, 48].\
  Tenga en cuenta que si no está buscando corrección matemática, los valores bajos están bien o incluso mejor.

## Entradas

* **Origen** *Color*\
  Los UV para difundir. Tenga en cuenta que el mosaico se administra de una manera especial en este filtro (consulte *Descripción*).
* **Máscara** *Escala de grises* Máscara de difusión: Los píxeles blancos se muestrean en *Source* y se difuminan en píxeles negros. La imagen debe ser en blanco y negro. Si la máscara incluye degradados, el valor de límite es 0,5.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-after.jpg){width="256px"}

</td>
</tr>
</table>
