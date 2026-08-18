---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Utilice el nodo Dirt para generar máscaras de acumulación de dirt basadas en la curvatura, posición y oclusión de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tierra
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# Tierra

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dirt.png){width="128px"}

## Tierra

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa los dirtes en bordes y esquinas ocluidos y hundidos, en función del AO horneado y la curvatura.

## Parámetros

### Entradas

* **Curvatura**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras. ¡Obligatorio!
* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras. ¡Obligatorio!
* **Entrada de Suciedad**: *Entrada en escala de grises*\
  Entrada de mapa de suciedad personalizada, opcional, activada por parámetro.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Normal del Espacio Mundial**: *Entrada de color*\
  Solo se usa para triplanar.
* **Posición**: *Entrada de color*\
  Solo se usa para triplanar.

### Parámetros

* **Nivel de Dirt**: *0.0 - 1.0* Control principal de la cantidad de dirt.
* **Contraste de Dirt**: *0.0 - 1.0* Controla el contraste principal del dirt de la máscara.
* **Cantidad de Suciedades**: *0.0 - 1.0* Establece qué grado de suciedad tiene el dirt. Ajuste a 0 para obtener un dirt perfectamente suave.
* **Enmascaramiento de bordes**: *0.0 - 1.0* Cantidad de dirt que se debe quitar de los bordes elevados (según el mapa de curvatura).
* **Usar Suciedad personalizada**: *Falso/Verdadero* Permite el uso de la entrada de mapa de suciedad personalizado en lugar de la Suciedad integrada.
* **Escala de Suciedad**: *1 - 16* Define la escala de mosaico de los detalles de la Suciedad.
* **Usar triplanar**: *Falso/Verdadero* Usa la [proyección triplanar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) para la asignación de Suciedades y elimina las costuras.
* **Contraste de fusión triplanar**: *0.001 - 1.0* Establece el contraste de la proyección triplanar.

## Imágenes de ejemplo

![](../../../../../../assets/dirt-ex.gif)

</td>
</tr>
</table>
