---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: Utilice el nodo Plano Tri para proyectar texturas de tres planos ortogonales para una asignación de texturas perfecta en geometría compleja.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tri Plano
user-guide-description: ''
user-guide-title: ''
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---


# Tri Plano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

<b>En:</b> Generadores basados en malla > Utilidades

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo avanzado realiza la asignación de proyección triplanar en 2D, en función de los datos de Posición hecha un bake y Normal del Espacio Mundial. Esto significa que básicamente convierte completamente las coordenadas UV en un mapeo (mayormente) sin costuras basado en la malla misma.

Esta es una buena manera de evitar costuras sin tener que volver a hacer cada vez (es posible lograr algo similar con el baker). El inconveniente es que este nodo es bastante pesado y por lo tanto no rápido.

Tenga en cuenta que sus hagas un bake deben ser de alta precisión: Las hagas un bake de 8 bits no darán resultados muy buenos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Posición</b> <i>Entrada de color</i> | Mapa de posición hecho un bake. Lo ideal es una precisión de 16 bits o superior. |
| <b>Normal del Espacio Mundial</b> <i>Entrada de color</i> | Mapa Normal del Espacio Mundial hecho un bake, Idealmente de 16 bits o mayor precisión. |
| <b>Entrada X</b> <i>Entrada de color (entrada en escala de grises)</i> | Mapa de entrada para reasignar desde UV al Espacio Mundial a través de la proyección triplanar. Se utiliza para todos los ejes cuando la entrada de la imagen se establece en 1, para el eje X si se define en 3. |
| <b>Entrada Y</b> <i>Entrada de color (entrada en escala de grises)</i> | Solo si la opción Entradas de imagen está establecida en 3. Mapa de entrada para reasignar de UV a Espacio mundial en el eje Y. |
| <b>Entrada Z</b> <i>Entrada de color (entrada en escala de grises)</i> | Solo si la opción Entradas de imagen está establecida en 3. Mapa de entrada para reasignar de UV a Espacio mundial en el eje Z. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Proyección</b> <i>Todos los ejes, solo X, solo Y, solo Z</i> | Define los ejes con los que se va a fusionar. |
| <b>Entradas De Imagen</b> <i>1 entrada, 3 entradas</i> | Permite definir si se debe utilizar un mapa para todos los ejes o un mapa específico por eje. |
| <b>Modo De Fusión</b> <i>lineal, avanzada</i> | Aumenta la precisión. |
| <b>Contraste de fusión</b> <i>0.001 - 1.0</i> | Contraste de transición, mezcla transiciones suaves o fuertes. |
| <b>Factor de normalización</b> <i>0.0 - 1.0</i> | Mejora la fusión de la proyección restaurando la pérdida de contraste en el área de fusión. |
| <b>Mosaico de Textura</b> <i>0.0 - 10.0</i> | Número de veces que se segmentan las texturas de entrada. |
| <b>Rotación global</b> <i>0.0 - 1.0</i> | Rotación global para todos los ejes. |
| <b>Corregir proyección duplicada</b> <i>Falso/Verdadero</i> | Defina cómo gestionar las proyecciones reflejadas. |
| <b>Rotación X</b> <i>0.0 - 1.0</i> | Rotación individual sobre el eje X de la proyección. |
| <b>Rotación Y</b> <i>0.0 - 1.0</i> | Rotación individual sobre el eje Y de la proyección. |
| <b>Rotación Z</b> <i>0.0 - 1.0</i> | Rotación individual sobre el eje Z de la proyección. |
| <b>Desplazamiento X</b> <i>0.0 - 1.0</i> | Desplazamiento sobre el eje X de la proyección. |
| <b>Desplazamiento Aleatorio X</b> <i>0.0 - 1.0</i> | Permitir la aleatorización del desplazamiento del eje X. |
| <b>Desplazamiento Y</b> <i>0.0 - 1.0</i> | Desplazamiento sobre el eje Y de la proyección. |
| <b>Desplazamiento Aleatorio Y</b> <i>0.0 - 1.0</i> | Permitir la aleatorización del desplazamiento del eje Y. |
| <b>Desplazamiento Z</b> <i>0.0 - 1.0</i> | Desplazamiento sobre el eje Z de la proyección. |
| <b>Desplazamiento aleatorio Z</b> <i>0.0 - 1.0</i> | Permitir la aleatorización del desplazamiento del eje Z. |
