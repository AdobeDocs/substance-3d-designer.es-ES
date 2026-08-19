---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Utilice el nodo Óxido de goteo para generar patrones de goteo de óxido basados en la geometría de malla y la dirección de la gravedad.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Óxido goteo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# Óxido goteo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

## Óxido goteo

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa los copos de óxido y las motas, con las fugas que corren hacia abajo.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa horneado o generado para ayudar con la colocación del óxido.
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa horneado o generado para ayudar con la colocación del óxido.
* **Posición**: *Entrada en escala de grises*\
  Mapa horneado o generado para direcciones de goteo.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Difusión de Óxido**: *0.0 - 1.0* Control principal de la cantidad de óxido.
* **Contraste de Óxido**: *0.0 - 1.0* Define la cantidad de contraste en las motas de óxido generadas (no afecta a los goteos).
* **Smoothness de propagación**: *0.0 - 1.0* Efecto difuminado/manchado que se aplica a las motas de óxido.
* **Intensidad de goteo**: *0.0 - 1.0* Establece la fuerza y la longitud de los goteos de los flecos.
* **Smoothness de goteos**: *0.0 - 1.0* Cantidad de desenfoque y suavizado que se aplica a los goteos.
* **Cantidad de muestras de goteo**: *0 - 32* Define el nivel de calidad (pasos) para el efecto de goteo. Tiene un ligero efecto en la velocidad.

## Imágenes de ejemplo

![](../../../../../../assets/dripping-rust-ex3.gif)

</td>
</tr>
</table>
