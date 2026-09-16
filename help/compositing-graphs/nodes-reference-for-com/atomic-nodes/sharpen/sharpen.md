---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ""
description: Utilice el nodo Perfilar (Sharpen) para mejorar los detalles de textura y las aristas para crear detalles de superficie definidos y nítidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Enfocar
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 4%
---

# Enfocar

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Icono Perfilar nodo](sharpen.resources/sharpen-4.png "Icono Perfilar nodo")

<b>En:</b> nodos atómicos

</td>
<td style="border: 0;" valign="top">

## Descripción

Enfocar nodo realiza una operación de enfoque en una entrada. Es un nodo útil para aplicar ese toque final de nitidez a una imagen.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="sharpen.resources/sharpen-tooltip.gif" alt="información sobre herramientas de enfoque" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

Es matemáticamente muy similar a Máscara de enfoque de Photoshop, a pesar de que el nombre es diferente. Funciona bien para cosas como un mapa Basecolor, pero debe evitarse en mapas como Mapas de normales y mapas metálicos.

## Entradas

<b>Entrada</b> *Color/Escala de grises* (Principal)\
La imagen que debe ser afilada.

## Parámetros

<b>Intensidad</b> *Flotante*\
Define la intensidad del efecto de enfoque.

<b>Alpha Punchthrough</b> *Booleano* (disponible cuando una imagen de color está conectada a <b>Input</b>)\
Determina si el canal alfa de la imagen se debe enfocar o dejar intacto.

## Ejemplos

![Enfocar nodo - Ejemplo 1](sharpen.resources/sharpen-ex.png "Enfocar nodo - Ejemplo 1")
