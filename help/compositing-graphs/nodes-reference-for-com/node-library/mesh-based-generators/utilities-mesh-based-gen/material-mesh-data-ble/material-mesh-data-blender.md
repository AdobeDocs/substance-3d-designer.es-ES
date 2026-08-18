---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: Utilice el nodo Mezclador de datos de malla de material para fusionar datos de malla de material para crear transiciones suaves entre diferentes zonas de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mezclador de datos de malla de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# Mezclador de datos de malla de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-mesh-data-blender.png){width="128px"}

## Mezclador de datos de malla de material

**En:** *Generadores basados en malla**/Utilities*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo está diseñado para facilitar la adición de detalles en función de los datos predefinidos. Viene con una gran cantidad de reguladores para modificar una entrada de material completo, basado en cualquier y todos los mapas con bake como entrada. Experimenta con él, ya que hay muchas opciones.

Es útil para hacer cosas como añadir resaltado de bordes basado en curvatura u otros mapas, mezclar en algunos AO con el color difuso/básico, añadir Oclusión de Specular basada en curvatura y/o AO, etc.

## Parámetros

### Entradas

* **Entrada completa de material (grupo &quot;Material&quot;):** conjunto completo de mapas de material.\
  Este nodo los modifica y, a continuación, los devuelve de nuevo como resultados.
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Height**: *Entrada en escala de grises*
* **Normal**: *Entrada de color*
* **Color de vértice**: *Entrada de color*
* **Normal del Espacio Mundial**: *Entrada de color*

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. Afecta a la disponibilidad de los siguientes parámetros.
* **Mapas con bake**
  * Si se deben o no utilizar los mapas con bake enumerados para los cálculos. Afecta a la disponibilidad de los siguientes parámetros.
* **OA difusa**: *0.0 - 1.0* Cantidad de Oclusión ambiental que se debe mezclar en la difusión.
* **Difuminar bordes afilados**: 0,0 - 1,0\
  Cantidad del mapa de curvatura que se va a fusionar en la difusión.
* **Color De Difusión Del Color Del Vértice**: 0,0 - 1,0\
  Cantidad de cocción del color del vértice que se va a fusionar en la difusión.
* **Iluminación previa de difusión**: 0,0 - 1,0\
  Cantidad de preiluminación (falsa), basada en las normas espaciales mundiales.
* **Equilibrio de iluminación de dibujos animados difusos**: 0,0 - 1,0\
  Cambia entre la iluminación realista y caricaturesca para la difusión.
* **Difuminar capas de iluminación previa de dibujos animados**: 0 - 10\
  Controla el aspecto de los cálculos de iluminación de dibujos animados.
* **Contornos De Dibujos Animados Difusos**: 0,0 - 1,0\
  Controla el aspecto de los cálculos de iluminación de dibujos animados.
* **Color base AO**: 0,0 - 1,0\
  Cantidad de Oclusión ambiental que se va a fusionar en el color base.
* **Bordes de color base nítidos**: 0,0 - 1,0\
  Cantidad del mapa de curvatura que se va a fusionar en el color base.
* **Color Base Del Color Del Vértice**: 0,0 - 1,0\
  Cantidad de cocción del color del vértice que se va a fusionar en el color base.
* **Intensidad de material normal**: 0,0 - 1,0\
  Intensidad de fusión del mapa normal (tangente) al horno.
* **SpecularAO**: 0,0 - 1,0\
  Fuerza de fusión del AO en el Specular.
* **Specular Brillante Bordes Afilados**: 0,0 - 1,0\
  Intensidad de fusión de la Curvatura en el Specular.
* **Contornos de dibujos animados de Specular**: 0,0 - 1,0\
  Intensidad de fusión de un efecto de contorno de borde de un Specular de dibujos animados, basado en la curvatura.
* **Bordes nítidos y oscuros brillantes**: 0,0 - 1,0\
  Intensidad de fusión de la curvatura en el brillo.
* **Bordes brillantes y nítidos de rugosidad**: 0,0 - 1,0\
  Intensidad de fusión de la curvatura en la rugosidad.
* **Contornos de dibujos animados de rugosidad**: 0,0 - 1,0\
  Intensidad de fusión de un efecto de contorno de borde de Rugosidad de dibujo animado, basado en la Curvatura.
* **Bordes brillantes y brillantes metálicos**: 0,0 - 1,0\
  Intensidad de fusión de la curvatura en el panel Metálico.
* **Contornos De Dibujos Animados Metálicos**: 0,0 - 1,0\
  Intensidad de fusión de un efecto de contorno de borde metálico de dibujo animado, basado en la curvatura.
* **Intensidad del material AO**: 0,0 - 1,0\
  Fusión de mezcla de mapa con bake AO con material-generado AO, qué grado para combinar ambos mapas AO en.
* **Intensidad del material de Height**: 0,0 - 1,0\
  Fusiona la fuerza del Height de mapa con bake con el Height generado por el material, en qué grado combinar ambos mapas de altura.
* **Tipo De Fusión De Material De Height**: Reforzar, interpolación\
  Modo de fusión para combinar ambos mapas de altura.

## Imágenes de ejemplo

![](../../../../../../assets/blenddata-ex.gif)

</td>
</tr>
</table>
