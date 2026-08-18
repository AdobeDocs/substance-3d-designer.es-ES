---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo Meteorización de musgo para añadir patrones de crecimiento de musgo a los materiales en función de la curvatura y posición de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Meteorización del musgo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---


# Meteorización del musgo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/moss-weathering.png){width="128px"}

## Meteorización del musgo

**En:** *Generadores Basados En Malla**/Meteorología*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Se trata de un efecto de material completo que funciona en varios canales a la vez. Genera un efecto de musgo crecido, con un único control de Propagación.

Este efecto funciona mejor con un mapa de posición del espacio mundial al horno y un mapa de altura adicional. Si bien este no es un requisito exacto, que presta el efecto de ubicación más creíble.

Asegúrate de entender correctamente los [Modos de creación de vínculos](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) al trabajar con materiales completos.

## Parámetros

### Entradas

* **Posición**: *Entrada de color*\
  Posición espacial del mundo al horno.
* **Height**: *Entrada en escala de grises*\
  Entrada adicional de Heightmap.
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
  * **Propagación de musgo**: *0.0 - 1.0* Establece la extensión del musgo. Crece en pasos desde una ligera cobertura hasta musgo oscuro grueso y pesado.
* **Fusión**
  * **Intensidad de difusión**: *0.0 - 1.0*\
    Intensidad de fusión de la difusión.
  * **Intensidad de color base**: *0.0 - 1.0*\
    Intensidad de fusión del color base.
  * **Intensidad normal**: *0.0 - 1.0*\
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

![](../../../../../../assets/moss-ex.gif)

</td>
</tr>
</table>
