---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: Utilice el nodo Desenfoque no uniforme para aplicar el desenfoque con diferentes intensidades en las direcciones X e Y para los efectos anisotrópicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desenfoque no uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Desenfoque no uniforme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

## Desenfoque no uniforme (escala de grises)

**En:** *Filtros/Desenfoques*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Realiza un desenfoque de alta calidad, en el que la intensidad se controla mediante una máscara de entrada. Las opciones permiten añadir Anisotropía y asimetría.

## Parámetros

### Entradas

* **Mapa de desenfoque**: *Entrada en escala de grises* Mapa de máscara para aumentar la intensidad del efecto.

### Parámetros

* **Intensidad**: *0.0 - 50.0* Intensidad máxima para aplicar el desenfoque. Enmascarado por el mapa de desenfoque, por lo que este ajuste no tendrá efecto en las áreas negras de ese mapa.
* **Anisotropía**: *0.0 - 1.0* Si lo desea, añade direccionalidad al efecto de desenfoque. Se controla mediante el parámetro Ángulo.
* **Asimetría**: *0.0 - 1.0* Opcionalmente agrega un sesgo al muestreo. Se controla mediante el parámetro Ángulo.
* **Ángulo**: *0.0 - 1.0*&#x200B;Ángulo para establecer la direccionalidad y el sesgo de muestreo.
* **Ejemplos**: *1 - 16* La cantidad de muestras determina la calidad. Multiplicado por la cantidad de blades.
* **blades**: *1 -* 9\
  Cantidad de sectores de muestreo, determina la calidad. Multiplicado por la cantidad de muestras.

## Imágenes de ejemplo

*El siguiente ejemplo está gobernado por una pendiente de degradado (a 90 grados) en la ranura Mapa de desenfoque.*

![](../../../../../../assets/nonuniform-example.gif)

</td>
</tr>
</table>
