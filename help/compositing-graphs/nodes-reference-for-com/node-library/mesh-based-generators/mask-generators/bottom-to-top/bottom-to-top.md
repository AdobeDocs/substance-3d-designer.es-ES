---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Utilice el nodo de abajo arriba para generar máscaras de degradado de abajo arriba en función de la posición del mundo de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: De abajo arriba
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# De abajo arriba

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

## De abajo arriba

**En:** *Generadores/Generadores De Máscara Basados En Malla*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks) en [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home).

Esto genera una transición de blanco a negro desde la parte inferior a la superior de un modelo, útil para realizar falloffs y selecciones basadas en geometría.

## Parámetros

### Entradas

* **Posición**: *Entrada de color*\
  Mapa de posición horneada. ¡Obligatorio!
* **Rugosidad:** *Entrada en escala de grises*\
  Esto no tiene nada que ver con la rugosidad de la PBR, pero es un mapa de variación (opcional) para romper la transición. Solo aparece cuando el valor de Rugosidad es superior a 0.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Cambia el nivel medio del resultado entre blanco o negro, como un ajuste de brillo.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste de la transición.
* **Rugosidad\_Variación**: *0.0 - 1.0* Determina la cantidad del mapa de rugosidad que se debe fusionar para variar. Si se aumenta este valor por encima de 0, se muestra la ranura del mapa.

## Imágenes de ejemplo

![](../../../../../../assets/bottom-to-top-ex.gif)

</td>
</tr>
</table>
