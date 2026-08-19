---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo meteorización de roca para generar patrones de meteorización en superficies de roca basados en la geometría de malla para obtener efectos de erosión realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Meteorización de rocas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# Meteorización de rocas

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rock-weathering.png){width="128px"}

## Meteorización de rocas

**En:** *Generadores Basados En Malla**/Meteorología*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

## Parámetros

### Entradas

* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **WS normal**: *Entrada de color*\
  Baked World Space Normalmap utilizado para efectos internos y enmascaramiento.
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
  * **Dust**: *0.0 - 1.0*
  * **Suciedad**: *0.0 - 1.0*
  * **Bordes Con**: *0.0 - 1.0*
  * **Roca usada**: *0.0 - 1.0*
  * Escala de **Grietas**: *1.0 - 60.0*
  * **Intensidad de Grietas**: *0.0 - 1.0*
  * **Edad**: *0.0 - 1.0*
  * **Umbral de edad**: *0.0 - 1.0*
  * **Escala de Scratches de bordes afilados**: *1.0 - 32.0*
  * **Intensidad de deformación de los Scratches de bordes afilados**: *0.0 - 1.0*
  * **Desaturación de roca usada**: *0.0 - 1.0*
  * **Brillo de roca usado**: *0.0 - 1.0*
* **Fusión**
  * **Intensidad de difusión**: *0.0 - 1.0*\
    Intensidad de fusión de la difusión.
  * **Intensidad de color base**: *0.0 - 1.0*\
    Intensidad de fusión del color base.
  * **Intensidad normal**: *0.0 - 64.0*\
    Intensidad de fusión de la Normal.
  * **Intensidad del Specular**: *0.0 - 1.0*\
    Fusión del Specular.
  * **Intensidad de brillo**: *0.0 - 1.0*\
    Fuerza de fusión del Brillo.
  * **Intensidad de rugosidad**: *0.0 - 1.0*\
    Fuerza de fusión de la rugosidad.
  * **Intensidad de Oclusión ambiente**: *0.0 - 1.0*\
    Fuerza de fusión de la Oclusión ambiente.
  * **Intensidad de Height**: *0.0 - 1.0*\
    Fusión del Height.

## Imágenes de ejemplo

![](../../../../../../assets/rock-ex.gif)

</td>
</tr>
</table>
