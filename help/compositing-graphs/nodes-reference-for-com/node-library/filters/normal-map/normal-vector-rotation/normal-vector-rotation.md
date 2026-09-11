---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
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
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---


# Rotación de vectores normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation.png){width="128px"}

<b>En:</b> Filtros > Mapa de normales

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo de utilidad normal que gira todos los vectores de un mapa normal de entrada en el espacio Tangente. En realidad no transforma los píxeles, sino que modifica los valores que representan. Puede utilizar un mapa opcional para añadir rotaciones aleatorias a facetas en escala de grises.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Normal</b> <i>Entrada de color</i> | Mapa base sobre el que realizar la rotación. Requerido. |
| <b>Mapa de rotación (opcional)</b> <i>Entrada en escala de grises</i> | Mapa de escala de grises que modula la intensidad de rotación. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ángulo de rotación</b> <i>0.0 - 1.0</i> | Establece el ángulo por el que se gira el mapa normal |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambiar entre diferentes Formatos de mapa de normales (invierte el canal verde) |
