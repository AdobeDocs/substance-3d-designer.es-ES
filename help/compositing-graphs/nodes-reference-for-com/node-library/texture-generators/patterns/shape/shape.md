---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Utilice el nodo Forma para generar formas geométricas básicas para crear patrones y texturas en Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## Forma

**En:** *Generadores De Texturas**/Patrones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una variedad de formas de procedimiento, con opciones para modificar formas base. Las formas siempre están perfectamente interpoladas y son de alta precisión.

A pesar de su simplicidad, se trata de un nodo muy útil: es el bloque de construcción de la generación de Heightmap más procedimental! Combinando formas básicas con nodos de transformación, puede crear una forma de mapa de altura con todos los procedimientos que sea mucho más precisa que cualquier mapa de bits.

## Parámetros

* **Mosaico**: *1 - 16*\
  Define la cantidad de veces que el resultado debe aparecer en mosaico.
* **Patrón**: *Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media Campana, Campana Cortada, Crescant, Cápsula, Cono*, Hemisferio**\
  Selecciona la forma de motivo que se va a utilizar.
* **Específico del patrón**: *0.0 - 1.0*\
  Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado.
* **Escala**: *0.0 - 1.0* Ajusta toda la forma.
* **Tamaño**: *0.0 - 1.0* Permite la escala no uniforme en los ejes X o Y.
* **Ángulo**: *0.0 - 1.0* Gira toda la forma.
* **Rotación 45°**: *Falso/Verdadero* Rota a 45 grados preestablecidos.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas.
* **Mosaico no cuadrado****:** *False/True*Cuando se habilita la Expansión no cuadrada, se segmentará la forma sin aplastarla.

## Imágenes de ejemplo

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>
