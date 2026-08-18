---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Utilice el nodo Edge Speckle para generar patrones de desgaste moteado en bordes de malla para crear efectos de daño de borde realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## Edge Speckle

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa los bordes con una pequeña mota añadida para dividirlos. Consulte también [Dirt Edge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para resaltar bordes. ¡Obligatorio!
* **Máscara de variación**: *Entrada en escala de grises*\
  Ranura de máscara opcional utilizada para enmascarar los efectos del nodo. Activar con &quot;Anular máscara de variación&quot;.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define la cantidad total de resaltado de bordes.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Selección de bordes**: *0.0 - 1.0* Establece la influencia de los bordes convexos.
* **Variación**: *0.0 - 1.0* Establece hasta qué punto la máscara de variación interrumpe el efecto.
* **Omitir máscara de variación**: *Falso/Verdadero* Anula la máscara integrada con una ranura de entrada personalizada.

## Imágenes de ejemplo

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>
