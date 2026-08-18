---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo de erosión de cuero para añadir patrones de desgaste y efectos de envejecimiento a los materiales de cuero en función de la curvatura de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Meteorología de cuero
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Meteorología de cuero

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

## Meteorología de cuero

**En:** *Generadores Basados En Malla**/Meteorología*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Se trata de un efecto de material completo que funciona en varios canales a la vez. Añade un efecto de desgaste aleatorio del cuero, con control de la edad y la suciedad. Es similar a [Fabric Weathering](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md), pero se ha ajustado específicamente para el cuero.\
Este efecto no funciona muy bien a menos que tenga conectado un AO y un World Space Normalmaps adecuados, ya que requiere que estos calculen y generen todo adecuadamente.

Asegúrate de que comprendes perfectamente los [modos de creación de vínculos](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) al trabajar con materiales completos.

## Parámetros

### Entradas

* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Espacio normal**: *Entrada de color*
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
  * **Dust**: *0.0 - 1.0* Se fusiona en un efecto de dust más oscuro, basado en las áreas que se encuentran hacia arriba en el mapa normal del espacio mundial.
  * **Suciedad**: *0.0 - 1.0* Se mezcla en un efecto de dirt/difuminado global, basado principalmente en áreas ocluidas (oscuras) en el AO.
  * **Bordes Con**: *0.0 - 1.0* Agrega un efecto de enfoque/intensificación a los bordes, basado en Material Normal.
  * **Usado**: *0.0 - 1.0* Se combina con un aspecto de cuero desgastado global.
  * **Edad**: *0.0 - 1.0* Se combina con un aspecto de cuero desgastado en pliegues basados en AO. La ubicación está muy influenciada por el umbral de edad.
  * **Umbral de edad**: *0.0 - 1.0* Establece el umbral de apariencia para el efecto Edad.
  * Escala de **Grietas**: *1.0 - 16.0* Establece la profundidad del cuero usado en el efecto Usado y Edad.
  * **Intensidad de deformación de Grietas**: *0.0 - 1.0* Establece la intensidad del cuero usado del efecto Usado y Edad.
  * **Escala de Scratches de bordes afilados**: *1.0 - 32.0*
  * **Intensidad de deformación de los Scratches de bordes afilados**: *0.0 - 1.0*
  * **Desaturación de cuero usado**: *0.0 - 1.0* Establece la saturación del aspecto de cuero usado de los efectos Antigüedad y Usados.
  * **Brillo de cuero usado**: *0.0 - 1.0* Establece el brillo del aspecto de cuero usado de los efectos Antigüedad y Usados.
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

![](../../../../../../assets/leather-ex.gif)

![](../../../../../../assets/leather-ex2.png){width="233px"}

</td>
</tr>
</table>
