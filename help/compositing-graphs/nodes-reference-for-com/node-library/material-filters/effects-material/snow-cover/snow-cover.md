---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Cubierta del Snow

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

## Cubierta del Snow

**En:** *Filtros/Efectos De Materiales*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Efecto todo en uno para añadir acumulación de nieve en un material completo. Se basa en gran medida en un mapa de altura bueno y de alta calidad, como el de un fotoescaneo. El resultado pretende ser una PBR correcta.

## Parámetros

### Entradas

* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Canales**\
  Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Snow nuevo**: *0.0 - 1.0* Establece la cantidad de nieve en áreas elevadas. El resultado se asocia al parámetro Snow fundido.
* **Snow derretido**: *0.0 - 1.0* Establece la cantidad de nieve derretida en las esquinas bajas.
* **Compilación**: *0.0 - 1.0* Afecta principalmente a la salida de Height y determina el efecto de acumulación de height.
* **Smoothness**: *0.0 - 1.0* Ajusta el suavizado de los detalles del height por acumulación de nieve.
* **Intensidad de los escamas**: *0.0 - 1.0* Afecta principalmente a Normalmap, intensidad de los detalles del copo.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
