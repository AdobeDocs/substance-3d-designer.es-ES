---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión de Ajuste de Material para fusionar ajustes de material entre materiales para ajustar los efectos de composición.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mezcla de ajuste de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# Mezcla de ajuste de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

## Mezcla de ajuste de material

**En:** *Filtros/Fusión De Materiales*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo permite ajustar todos y cada uno de los canales de un material completo, basándose en una máscara. Su objetivo es facilitar y agilizar el flujo de trabajo de materiales.

Resulta útil si desea ajustar algunos canales de un material (por ejemplo, hacer que la difusión sea más brillante y la rugosidad más oscura) basándose en la misma máscara.

## Parámetros

### Entradas

* **Máscara de ID de color**: *Entrada de color*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Máscara de escala de grises**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Canales**\
  Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.\
  Esto también habilita y deshabilita la apariencia de los grupos relevantes del canal.
* **Difusión**\
  Realiza operaciones de ajuste en el canal Difusión, en áreas definidas por la máscara.
* **Color base**\
  Realiza operaciones de ajuste en el canal Color base, en áreas definidas por la máscara.
* **Normal**
  * **Intensidad**: *0.0 - 1.0* Tonos de intensidad normal
* **Specular**\
  Realiza operaciones de ajuste en el canal de Specular, en áreas definidas por la máscara.
* **Emissive**\
  Realiza operaciones de ajuste en el canal Emissive, en áreas definidas por la máscara.
* **Brillo**\
  Realiza operaciones de ajuste en el canal Brillo, en áreas definidas por la máscara.
* **Rugosidad**\
  Realiza operaciones de ajuste en el canal Rugosidad (Roughness), en áreas definidas por la máscara.
* **Metálico**\
  Realiza operaciones de ajuste en el canal Metálico, en áreas definidas por la máscara.
* **Specular level**\
  Realiza operaciones de ajuste en el canal de Specular level, en áreas definidas por la máscara.
* **Oclusión de ambiente**\
  Realiza operaciones de ajuste en el canal Oclusión ambiente, en áreas definidas por la máscara.
* **Height**\
  Realiza operaciones de ajuste en el canal de Height, en áreas definidas por la máscara.
* **Opacidad**\
  Realiza operaciones de ajuste en el canal Opacidad, en áreas definidas por la máscara.
* **Máscara de ID de color**: *False/True* Se establece para usar la Máscara de ID de color en lugar de la máscara de escala de grises.
* **Rugosidad**: *0.01 - 1.0* Si la Máscara de ID de color está habilitada, esto determina la extensión del color de selección de ID de color.
* **Color**: *(Valor de color)*Define el color que se debe seleccionar en el mapa de ID de color y la máscara.
* **Relleno**: *0.0 - 1.0* Determina el contraste o las transiciones de fusión de las máscaras de ID de color.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
