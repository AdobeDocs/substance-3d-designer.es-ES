---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: Utilice el nodo Tri Planar para proyectar texturas de tres planos ortogonales para una asignación de texturas perfecta en geometría compleja.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tri Planar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Tri Planar

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

## Tri Planar (escala de grises)

**En:** *Generadores basados en malla**/Utilities*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo avanzado realiza la asignación de proyección triplanar en 2D, en función de los datos de posición horneada y normal del espacio mundial. Esto significa que básicamente convierte completamente las coordenadas UV en un mapeo (mayormente) sin costuras basado en la malla misma.

Esta es una buena manera de evitar costuras sin tener que volver a hacer cada vez (es posible lograr algo similar con el panadero). El inconveniente es que este nodo es bastante pesado y por lo tanto no rápido.

Tenga en cuenta que sus pasteles deben ser de alta precisión: Los pasteles de 8 bits no darán resultados muy buenos.

## Parámetros

### Entradas

* **Posición**: *Entrada de color*\
  Mapa de posición horneada. Lo ideal es una precisión de 16 bits o superior.
* **Normal del Espacio Mundial**: *Entrada de color*\
  Mapa Normal de Espacio Mundial al Horno, Idealmente de 16 bits o más precisión.
* **Entrada X**: *Entrada de color (entrada en escala de grises)*Mapa de entrada para reasignar de UV a espacio mundial mediante proyección triplanar. Se utiliza para todos los ejes cuando la entrada de la imagen se establece en 1, para el eje X si se define en 3.
* **Entrada Y**: *Entrada de color (entrada de escala de grises)*Solo si la entrada de imagen se define en 3. Mapa de entrada para reasignar de UV a Espacio mundial en el eje Y.
* **Entrada Z**: *Entrada de color (entrada de escala de grises)*Solo si la entrada de imagen se define en 3. Mapa de entrada para reasignar de UV a Espacio mundial en el eje Z.

### Parámetros

* **Proyección**: *Todos los ejes, Sólo X, Sólo Y, Sólo Z* Establece los ejes con los que se va a realizar la fusión.
* **Entradas de imagen**: *1 entrada, 3 entradas*\
  Permite definir si se debe utilizar un mapa para todos los ejes o un mapa específico por eje.
* **Modo De Fusión**: *lineal, avanzada* Aumenta la precisión.
* **Contraste de fusión**: *0.001 - 1.0* Contraste de transición, mezcla entre transiciones suaves o fuertes.
* **Factor de normalización**: *0.0 - 1.0*\
  Mejora la fusión de la proyección restaurando la pérdida de contraste en el área de fusión.
* **Mosaico de texturas**: *0.0 - 10.0* Número de veces que se segmentan las texturas de entrada.
* **Rotación global**: *0.0 - 1.0*\
  Rotación global para todos los ejes.
* **Corregir proyección duplicada**: *Falso/Verdadero* Establecer cómo administrar las proyecciones reflejadas.
* **Rotación X**: *0,0 - 1,0* Rotación individual sobre el eje X de la proyección.
* **Rotación Y**: *0,0 - 1,0* Rotación individual sobre el eje Y de la proyección.
* **Rotación Z**: *0,0 - 1,0* Rotación individual sobre el eje Z de la proyección.
* **Desplazamiento X**: *0,0 - 1,0* Desplazamiento sobre el eje X de la proyección.
* **Desplazamiento Aleatorio X**: *0.0 - 1.0*\
  Permitir la aleatorización del desplazamiento del eje X.
* **Desplazamiento Y**: *0,0 - 1,0* Desplazamiento sobre el eje Y de la proyección.
* **Desplazamiento Aleatorio Y**: *0.0 - 1.0*\
  Permitir la aleatorización del desplazamiento del eje Y.
* **Desplazamiento Z**: *0,0 - 1,0* Desplazamiento sobre el eje Z de la proyección.
* **Desplazamiento aleatorio Z**: *0.0 - 1.0*\
  Permitir la aleatorización del desplazamiento del eje Z.

## Imágenes de ejemplo

</td>
</tr>
</table>
