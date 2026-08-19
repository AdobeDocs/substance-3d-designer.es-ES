---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: Utilice el nodo Nivel de agua para mezclar materiales basados en el height del nivel de agua para crear efectos realistas sobre el agua.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nivel del agua
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# Nivel del agua

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## Nivel del agua

**En:** *Filtros/Efectos De Materiales*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Efecto todo en uno que añade un nivel de agua a una entrada de material completa. El material de entrada debe tener un buen mapa de altura de alta calidad para que el efecto funcione. El resultado es una PBR correcta.

## Parámetros

### Entradas

* **Máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Canales**\
  Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Nivel de agua**: *0.0 - 1.0* Control principal para subir o bajar el nivel del agua.
* **Oscuridad del agua**: *0.0 - 1.0* Define la &quot;transparencia&quot; general del agua.
* **Humedad de los bordes**: *0.0 - 1.0* Determina el aspecto húmedo que deben tener los bordes del agua.
* Distancia de humedad de **bordes**: *0.0 - 1.0* Establece hasta dónde llegan los bordes húmedos.
* **Cantidad de desenfoque de Profundidad**: *0.0 - 1.0* Define la cantidad de desenfoque en función de la profundidad debajo del agua. Modifica el radio de desenfoque.
* **Opacidad De Desenfoque De Profundidad**: *0.0 - 1.0* Determina en qué cantidad se mezcla el desenfoque de profundidad, que se puede usar para reducir el efecto del desenfoque.
* **Color de lodo**: *(Valor de color)*Define el color del efecto de lodo.
* **Profundidad de lodos**: *0.0 - 1.0* Establece la profundidad a la que comienza a aparecer el lodo, en relación con el nivel del agua.
* **Opacidad del lodo**: *0.0 - 1.0* Define la opacidad global del efecto de lodo.
* **Frost**: *0.0 - 1.0* Establece la cantidad de escarcha. Comienza a aparecer desde los bordes exteriores y se mueve hacia dentro.
* **Intensidad de escarcha**: *0.0 - 1.0* Define la intensidad de la helada y controla la &quot;opacidad&quot; del efecto.
* **Grietas Frost**: *0.0 - 1.0* Establece la cantidad de grietas en las transiciones de congelado a líquido.
* **Formato Normal Frost**: *DirectX/OpenGL* Cambia el canal verde del efecto Frost Normalmap.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
