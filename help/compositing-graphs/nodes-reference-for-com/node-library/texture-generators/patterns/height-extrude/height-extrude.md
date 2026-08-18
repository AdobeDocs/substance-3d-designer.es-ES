---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: Utilice el nodo Extrusión de altura para extruir formas basadas en mapas de height para crear efectos de profundidad similares a 3D en texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrusión de altura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Extrusión de altura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-extrude.png){width="200px"}

## Extrusión de altura

**En:** *Generadores De Texturas**/Patrones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

La Extrusión de altura representa la Profundidad Z en 3D a partir de un mapa de Height de entrada. Al igual que [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) y [Cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), te permite girar una cámara en la vista 2D. Su objetivo principal es servir como generador para crear formas rotadas en 3D a partir de un mapa de altura plano. Estas formas se pueden usar con [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md).

La principal diferencia con [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) es que el mapa de entrada no tiene que ser un tipo de mapa binario &quot;alfa&quot;, sino un mapa de escala de grises de rango completo. Esto significa que tiene más control sobre el height de extrusión (formas orgánicas y complejas), pero no sobre nada como los perfiles biselados (superficies duras, formas más simples).

## Parámetros

* **Ángulo de cámara**:\
  Ángulos de Euler de la cámara, en media vuelta. Tenga en cuenta que la rotación horizontal y la escala se aplican directamente a la entrada.
* **Escala de cámara**: *0,001 - 3,0*\
  Escala global aplicada al resultado.
* **Escala de Height**: *0.0 - 2.0*\
  Aplica un factor global a los valores del height de entrada.
* **Desplazamiento vertical**: *-1.0 - 1.0*\
  Mueve el resultado final hacia arriba o hacia abajo.
* **Tierra**: *Apagado/Encendido*\
  Si Masa está desactivada, se muestra un fondo negro donde la entrada es 0 en lugar de un plano similar a tierra.
* **Formato normal**: *DirectX/OpenGL*\
  El parámetro **Formato normal** invierte la coordenada y del mapa normal.
* **Intensidad normal**: *0.0 - 256.0*\
  Igual que el parámetro **Intensity** del nodo **Normal**. Establézcalo en 256 para obtener una normal sin fragmentos mientras gira.

## Imágenes de ejemplo

</td>
</tr>
</table>
