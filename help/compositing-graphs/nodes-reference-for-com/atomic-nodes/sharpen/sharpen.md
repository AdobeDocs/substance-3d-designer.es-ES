---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ''
description: Utilice el nodo Perfilar para mejorar los detalles de la textura y las aristas para crear detalles de superficie definidos y nítidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Enfocar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# Enfocar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Perfilar nodo](sharpen.resources/sharpen-01.png "Icono Perfilar nodo")

<b>En:</b> nodos atómicos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Enfocar nodo realiza una operación de enfoque en una entrada. Es un nodo útil para aplicar ese toque final de nitidez a una imagen.

</td>
</tr>
</table>

Es matemáticamente muy similar a Máscara de enfoque de Photoshop, a pesar de que el nombre es diferente. Funciona bien para cosas como un mapa Basecolor, pero debe evitarse en mapas como los mapas normales y los mapas metálicos.

## Entradas

<b>Entrada</b> *Color/Escala de grises* (Principal)\
La imagen que debe ser afilada.

## Parámetros

<b>Intensidad</b> *Flotador*\
Define la intensidad del efecto de enfoque.

<b>Alpha Punchthrough</b> *Booleano* (disponible cuando una imagen de color está conectada a <b>Input</b>)\
Determina si el canal alfa de la imagen se debe enfocar o dejar intacto.

## Ejemplos

![Enfocar nodo - Ejemplo 1](sharpen.resources/sharpen-02.png "Enfocar nodo - Ejemplo 1")
