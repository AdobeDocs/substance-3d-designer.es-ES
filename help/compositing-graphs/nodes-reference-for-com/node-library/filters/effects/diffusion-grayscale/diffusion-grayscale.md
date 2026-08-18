---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: Utilice el nodo Escala de grises de difusión para aplicar efectos de difusión de escala de grises para crear transiciones y fusiones de color suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escala de grises de difusión
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# Escala de grises de difusión

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-icon.png){width="200px"}

**En:** *Filtros/Efectos*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

Aplique un proceso de difusión a los valores en la entrada de imagen **Source** según la entrada de imagen **Mask** proporcionada, lo que crea gradaciones suaves entre los valores.

Solo se difunden los valores de los píxeles que coinciden con la máscara; otros píxeles no participan en el resultado.

</td>
</tr>
</table>

## Parámetros

* **Iteraciones**: *0.0 - 64.0* El número de iteraciones de difusión que se van a realizar (más alto es mejor pero más lento). Los valores útiles se encuentran en el intervalo [8, 48].\
  Tenga en cuenta que si no está buscando corrección matemática, los valores bajos están bien o incluso mejor.\
  **Distancia**: **0.0 - 1.0** Ajusta la distancia máxima de la difusión.
* **Habilitar tramado**: *Verdadero/Falso* Controla el método de muestreo de cada pasada. El tramado permite la convergencia en menos pasadas, pero introduce ruido.\
  Sin ella, cada pase es más rápido, pero se requieren más pases para lograr un resultado suave sin defectos de bandas.

## Entradas

* **Origen** *Escala de grises*\
  La imagen que se va a difundir.
* **Máscara** *Escala de grises*\
  Máscara de difusión: los píxeles blancos se muestrean en *Source* y se difuminan en píxeles negros. La imagen debe ser en blanco y negro. Si la máscara incluye degradados, el valor de límite es 0,5.
* **Intensidad** *Escala de grises*\
  Define localmente qué tan fuerte se aplica el proceso de difusión. Este mapa debe ser *contrastado* para lograr un efecto apreciable.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01a-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01b-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-render.jpg){width="512px"}

</td>
</tr>
</table>
