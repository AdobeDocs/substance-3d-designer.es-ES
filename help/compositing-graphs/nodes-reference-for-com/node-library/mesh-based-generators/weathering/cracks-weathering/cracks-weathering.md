---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo Grietas de intemperismo para añadir patrones de grietas a los materiales en función de la curvatura de la malla y los puntos de tensión.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grietas Desgaste
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# Grietas Desgaste

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

## Grietas Desgaste

**En:** *Generadores Basados En Malla**/Meteorología*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Se trata de un efecto de material completo que funciona en varios canales a la vez. Añade un patrón de grietas aleatorio, con control sobre la propagación y la profundidad.

Asegúrate de entender correctamente los [Modos de creación de vínculos](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) al trabajar con materiales completos.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa horneado o generado utilizado para efectos internos y enmascaramiento.
* **Height**: *Entrada en escala de grises*\
  Mapa horneado o generado utilizado para efectos internos y enmascaramiento.
* **Máscara** : *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;.

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Avanzado**
  * **Formato normal**: *DirectX, OpenGL*\
    Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).
  * **Máscara**: *Falso/Verdadero*\
    Activa o desactiva el uso del mapa de máscara.
* **Efecto**
  * **Propagación de Grietas**: *0.0 - 1.0* Hasta dónde deben extenderse las grietas. Este es el control principal de este efecto.
  * **Profundidad de Grietas**: *0.0 - 1.0* Profundidad del efecto de grieta. Esto afecta principalmente al height y afecta ligeramente al thickness visual.
* **Fusión**
  * Controla la intensidad con la que el efecto se fusiona en cada canal resultante.

## Imágenes de ejemplo

![](../../../../../../assets/cracks-ex.gif)

</td>
</tr>
</table>
