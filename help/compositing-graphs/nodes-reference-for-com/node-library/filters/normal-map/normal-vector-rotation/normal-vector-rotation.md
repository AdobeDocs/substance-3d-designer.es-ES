---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: Utilice el nodo Rotación de vector normal para rotar los vectores de mapa normales para ajustar la iluminación de la superficie y la orientación de los detalles.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotación de vectores normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Rotación de vectores normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## Rotación de vectores normal

**En:** *Filtros/Mapa Normal*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo de utilidad normal que gira todos los vectores de un mapa normal de entrada en el espacio Tangente. En realidad no transforma los píxeles, sino que modifica los valores que representan. Puede utilizar un mapa opcional para añadir rotaciones aleatorias a facetas en escala de grises.

## Entradas

* **Normal**: *Entrada de color*\
  Mapa base sobre el que realizar la rotación. Requerido.
* **Mapa de rotación (opcional)**: *Entrada en escala de grises*\
  Mapa de escala de grises que modula la intensidad de rotación.

## Parámetros

* **Ángulo de rotación**: *0.0 - 1.0*\
  Establece el ángulo por el que se gira el mapa normal
* **Formato normal**: *DirectX, OpenGL*\
  Cambiar entre diferentes Formatos de mapa de normales (invierte el canal verde)

## Ejemplos

</td>
</tr>
</table>
