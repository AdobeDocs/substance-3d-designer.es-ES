---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Utilice el nodo 3D linear gradient para crear degradados lineales basados en la posición de mundo 3D para efectos espaciales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 3D linear gradient

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 3D linear gradient

**En:** *Generadores De Texturas**/Patrones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Crea un degradado volumétrico basado en el mapa de posición de entrada. Genera de forma efectiva una transición de negro a blanco entre 2 puntos en el espacio 3D. Se ha diseñado para su uso únicamente con el motor de GPU.

Consulte también [Máscara de volumen 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) para ver un efecto similar.

## Parámetros

* **Modo de posición de puntos**: *Posiciones UV, Posiciones espaciales mundiales* Elija si los puntos de degradado funcionan en el espacio UV (funciona mejor cuando se establecen en la vista 2D) o en coordenadas 3D, si desea especificar manualmente una posición exacta.
* **Punto 1**:\
  Punto inicial del degradado. Pueden ser coordenadas 2D o 3D basadas en el modo de posición.
* **Punto 2**:\
  Punto final del degradado. Pueden ser coordenadas 2D o 3D basadas en el modo de posición.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.

## Imágenes de ejemplo

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>
