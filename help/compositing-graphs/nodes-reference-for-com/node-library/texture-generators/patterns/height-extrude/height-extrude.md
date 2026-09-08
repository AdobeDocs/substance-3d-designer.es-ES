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
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# Extrusión de altura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/height-extrude.png){width="200px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

La Extrusión de altura representa la Profundidad Z en 3D a partir de un mapa de Height de entrada. Al igual que [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) y [Cube 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), te permite girar una cámara en la vista 2D. Su objetivo principal es servir como generador para crear formas rotadas en 3D a partir de un mapa de altura plano. Estas formas se pueden usar con [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md).

La principal diferencia con [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) es que el mapa de entrada no tiene que ser un tipo de mapa binario &quot;alfa&quot;, sino un mapa de escala de grises de rango completo. Esto significa que tiene más control sobre el height de extrusión (formas orgánicas y complejas), pero no sobre nada como los perfiles biselados (superficies duras, formas más simples).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ángulo de cámara</b> | Ángulos de Euler de la cámara, en media vuelta. Tenga en cuenta que la rotación horizontal y la escala se aplican directamente a la entrada. |
| <b>Escala de cámara</b> <i>0.001 - 3.0</i> | Escala global aplicada al resultado. |
| <b>Escala de Height</b> <i>0.0 - 2.0</i> | Aplica un factor global a los valores del height de entrada. |
| <b>Desplazamiento vertical</b> <i>-1.0 - 1.0</i> | Mueve el resultado final hacia arriba o hacia abajo. |
| <b>Tierra</b> <i>Activado/Desactivado</i> | Si Masa está desactivada, se muestra un fondo negro donde la entrada es 0 en lugar de un plano similar a tierra. |
| <b>Formato normal</b> <i>DirectX/OpenGL</i> | El parámetro <b>Formato normal</b> invierte la coordenada y del mapa normal. |
| <b>Intensidad normal</b> <i>0.0 - 256.0</i> | Igual que el parámetro <b>Intensity</b> del nodo <b>Normal</b>. Establézcalo en 256 para obtener una normal sin fragmentos mientras gira. |
