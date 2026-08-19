---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo Metal Weathering para añadir efectos realistas de óxido y corrosión a los materiales metálicos basados en la geometría de malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metal Weathering
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 1%

---


# Metal Weathering

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-weathering.png){width="128px"}

## Metal Weathering

**En:** *Generadores Basados En Malla**/Meteorología*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

## Parámetros

### Entradas

* **WS normal**: *Entrada de color*\
  Baked World Space Normalmap utilizado para efectos internos y enmascaramiento.
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Máscara** : *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;.

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Avanzado**
  * **Formato normal**: *Direct X, Open GL*\
    Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).
  * **Máscara**: *Falso/Verdadero*\
    Activa o desactiva el uso del mapa de máscara.
* **Efecto**
  * **Dust**: *0.0 - 1.0*
  * **Suciedad**: *0.0 - 1.0*
  * **Bordes Con**: *0.0 - 1.0*
  * **Pintado descascarillado**: *0.0 - 1.0*
  * **Óxido**: *0.0 - 1.0*
  * **Descascarillado de Óxido**: *0.0 - 1.0*
  * **Óxido Verdigris**: *Óxido, Verdigris*
  * **Escala de Grietas de pintura**: *1.0 - 16.0*
  * **Intensidad de deformación de Grietas de pintura**: *0.0 - 1.0*
  * **Escala de Scratches de bordes afilados**: *1.0 - 32.0*
  * **Intensidad de deformación de los Scratches de bordes afilados**: *0.0 - 1.0*
  * **Color de metal sin procesar**: *(Valor de color)*
  * **Color de Specular de metal crudo**: *(Valor de color)*
  * **Valor De Brillo De Metal Bruto**: *(valor de escala de grises)*
  * **Valor de rugosidad de metal sin procesar**: *(valor de escala de grises)*
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
  * **Intensidad metálica**: *0.0 - 1.0*\
    Intensidad de fusión del metal.
  * **Intensidad de Oclusión ambiente**: *0.0 - 1.0*\
    Fuerza de fusión de la Oclusión ambiente.
  * **Intensidad de Height**: *0.0 - 1.0*\
    Fusión del Height.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
