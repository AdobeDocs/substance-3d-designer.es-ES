---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: Utilice el nodo Reaction Diffusion Fast para generar patrones orgánicos utilizando algoritmos de reacción-difusión rápida para texturas procedimientas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Reacción Difusión Rápida
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---


# Reacción Difusión Rápida

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo de difusión de reacción](reaction-diffusion-fast.resources/reaction-diffusion.png "Icono de nodo de difusión de reacción")

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo realiza un efecto de reacción-difusión en una imagen de entrada en escala de grises.

La reacción-difusión es un proceso en el que la materia se propaga (se difunde) e interactúa (reacciona) con otra materia. Es un modelo matemático que simula lo que ocurre en la naturaleza cuando se forman ciertos patrones en la piel de los animales, por ejemplo.

Este nodo está optimizado para el rendimiento y realiza algunas compensaciones de precisión en cuanto a la velocidad.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Escala de grises</i> | Imagen en escala de grises a la que se debe aplicar el efecto Reacción-difusión. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | Imagen en escala de grises que representa el efecto Reacción-difusión aplicado a la imagen de entrada. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Radio</b> *Flotador* | Hasta dónde debe extenderse el efecto. |
| <b>Contraste</b> *Flotador* | Ajusta el contraste de la entrada y sirve como una especie de umbral. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo 1](reaction-diffusion-fast.resources/reactdiff03.png "Ejemplo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo 2](reaction-diffusion-fast.resources/reactdiff02.png "Ejemplo 2")

</td>
<td style="border: 0;" valign="top">

![Ejemplo 3](reaction-diffusion-fast.resources/reactdiff01.gif "Ejemplo 3")

</td>
</tr>
</table>
