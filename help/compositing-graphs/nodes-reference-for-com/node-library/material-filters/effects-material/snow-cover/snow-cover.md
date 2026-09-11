---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: Utilice el nodo Cubierta del Snow para añadir efectos de acumulación de nieve a los materiales en función del ángulo y la posición de la superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cubierta del Snow
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 8%

---


# Cubierta del Snow

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](snow-cover.resources/snow-cover.png){width="128px"}

<b>En:</b> Filtros de material > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Efecto todo en uno para añadir acumulación de nieve en un material completo. Se basa en gran medida en un mapa de altura bueno y de alta calidad, como el de un fotoescaneo. El resultado pretende ser una PBR correcta.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/Brillo en lugar de Metálico/Rugosidad. |
| <b>Snow nuevo</b> <i>0.0 - 1.0</i> | Define la cantidad de nieve en las áreas elevadas. El resultado se asocia al parámetro Snow fundido. |
| <b>Snow derretido</b> <i>0.0 - 1.0</i> | Define la cantidad de nieve derretida en las esquinas inferiores. |
| <b>Compilación</b> <i>0.0 - 1.0</i> | Afecta principalmente a la salida de Height y determina el efecto de acumulación de height. |
| <b>Smoothness</b> <i>0.0 - 1.0</i> | Ajusta el suavizado de los detalles del height mediante la acumulación de nieve. |
| <b>Intensidad de los escamas</b> <i>0.0 - 1.0</i> | Afecta principalmente a Normalmap, intensidad de los detalles de escamas. |
