---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Utilice el nodo Pincel de superficie para generar máscaras basadas en la orientación de la superficie para crear efectos de desgaste y meteorización direccional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pincel de superficie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# Pincel de superficie

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## Pincel de superficie

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa un efecto interesante del cepillado de metal en una superficie de objeto, ocluida por la geometría de objeto y el AO.

## Parámetros

### Entradas

* **Normal del Espacio Mundial**: *Entrada de color*
* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Posición**: *Entrada en escala de grises*
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define el nivel de efecto global y lo revela gradualmente.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Longitud de los Scratches**: *0.0 - 8.0* Establece la longitud de los arañazos. Los valores más pequeños son más parecidos a los puntos, los valores más altos son rayas largas.
* **Ocluir Eje**: *X, Y, Z, none* Eje del objeto que debe recibir rasguños. No altera la dirección de los arañazos.
* **Intensidad del eje de oclusión**: *0,0 - 1,0* Intensidad del efecto de oclusión de ejes.
* **Oclusión**: *0.0 - 1.0* Resistencia del AO en arañazos oclusivos.
* **Intensidad de enfoque**: *0.0 - 1.0* Establezca la cantidad de enfoque posterior que se aplicará a los arañazos.

## Imágenes de ejemplo

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>
