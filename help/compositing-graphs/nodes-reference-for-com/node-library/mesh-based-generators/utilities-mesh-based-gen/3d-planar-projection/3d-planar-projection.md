---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: Utilice el nodo Proyección plana 3D para proyectar texturas en superficies de malla mediante la proyección plana para la asignación de texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Proyección plana 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# Proyección plana 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

## Proyección plana en 3D (color)

**En:** *Generadores basados en malla**/Utilities*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza una proyección plana basada en datos de malla horneada (Mapas de posición y normales del mundo). Permite proyectar y colocar pegatinas a través de las costuras, independientemente de la asignación UV original.

## Parámetros

### Entradas

* **Mapa de posición**: *Entrada de color* Mapa de posición horneada
* **Normal del Espacio Mundial**: *Entrada de color* Mapa normal del espacio del mundo horneado
* **Textura proyectada**: *Entrada de color* Introduce la textura en el proyecto en el destino.

### Parámetros

* **Colocación**
  * **Entrada de proyecto**: *Posición UV, posición del espacio mundial* Elija si la posición de la proyección está definida en 2D/UV o en el espacio 3D/Mundo.
  * **Posición UV de destino**:\
    Solo con entrada de posición UV, se recomienda utilizar para seleccionar un punto en la vista 2D en el mapa de posición.
  * **Posición de destino**: *(Valor de color)*Solo con Entrada de posición de espacio mundial, permite definir una coordenada 3D exacta.
  * **Objetivo normal**: *(Valor de color)*
  * **Rotación**: *0,0 - 1,0\
    Gira la textura proyectada a lo largo de su eje normal.*
  * **Escala**: *0.0 - 1.0*\
    Establezca la escala global de la textura proyectada.
  * **Tamaño**: *0.0 - 2.0* Realizar escalado no uniforme en la textura proyectada.
* **Enmascaramiento**
  * **Profundidad máxima**: *0.0 - 1.0* Controla la profundidad a la que aparecerá la textura proyectada y el momento en que se cortará.
  * **Desvanecimiento de Profundidad**: *0.0 - 1.0* Establezca la transición para que la profundidad de corte sea repentina o desvanecida.
  * **Umbral normal**: *-1.0 - 1.0* Establezca el umbral para las superficies que no estén exactamente alineadas con la proyección normal.
  * **Transición normal**: *0.0 - 1.0* Establezca la transición para las superficies que no estén alineadas con las zonas repentinas o de transición.

## Imágenes de ejemplo

![](../../../../../../assets/3d-planar-projection-ex.gif)

</td>
</tr>
</table>
