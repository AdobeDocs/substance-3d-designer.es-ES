---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Utilice el nodo Fusión normal para fusionar mapas normales y crear transiciones suaves entre detalles de superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusión normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# Fusión normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

## Fusión normal

**En:** *Filtros/Mapa Normal*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Fusión normal permite fusionar dos mapas normales con una máscara opcional, mientras se garantiza que todos los valores permanecen normalizados. No difiere mucho de un [nodo de fusión atómica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), pero ha agregado cálculos internos para los mapas normales.

Fusión normal no está diseñada para combinar (superponer) mapas normales, donde el mapa superior agrega detalles al mapa inferior. Para ello, usa [Combinación normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md) en su lugar.

## Parámetros

### Entradas

* **NormalFG**: *Entrada de color*\
  Mapa normal frontal/superior.
* **NormalBG**: *Entrada de color*\
  Fondo/Mapa normal inferior.
* **Máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Usar máscara&quot;.

### Parámetros

* **Opacidad**: *0.0 - 1.0*\
  Fusión de opacidad entre primer plano y fondo
* **Usar máscara**: *Falso/Verdadero*\
  Activa o desactiva el uso del mapa de máscara.

## Imágenes de ejemplo

![](../../../../../../assets/normalblend-ex.gif)

*(el formato .gif introduce el tramado en el ejemplo, los resultados en la aplicación son suaves)*

</td>
</tr>
</table>
