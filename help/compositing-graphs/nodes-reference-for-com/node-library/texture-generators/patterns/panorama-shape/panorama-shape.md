---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/panorama-shape.html"
breadcrumb-title: ''
description: Utilice el nodo Forma de panorama para crear formas asignadas a las coordenadas de panorama para la generación de textura de entorno.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Panorama Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma de panorama
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Forma de panorama

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](panorama-shape.resources/panorama-shape-1.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este es un nodo útil para generar mapas panorámicos de tipo &quot;Studio&quot; procedimientos. Permite colocar y modificar imágenes destacadas, así como establecer sus propiedades HDR. Se puede encadenar para varias formas.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Matriz de formas</b> | Mueve o traduce el resultado; se puede modificar interactuando directamente con el lienzo. |
| <b>Forma</b> <i>square, disk</i> | Establece el tipo de forma. |
| <b>Color de forma</b> <i>(Valor de color)</i> | Establece el color de forma. |
| <b>Intensidad de forma</b> <i>0.0 - 100.0</i> | Establece HDR intensidad de la forma. |
| <b>Borde suave de forma</b> <i>0.0 - 1.0</i> | Cambia la suavidad del borde de la forma. |
| <b>Intensidad del hotspot</b> <i>0.0 - 100.0</i> | Establece HDR.-intensidad de la zona interactiva de la forma. |
| <b>Tamaño de zona interactiva</b> <i>0.0 - 1.0</i> | Cambia el tamaño de la zona interactiva dentro de la forma. |
| <b>Difuminación de zona interactiva</b> <i>0.0 - 1.0</i> | Cambia la difuminación y la fusión de bordes de la zona interactiva. |
| <b>Posición de zona interactiva</b> <i>0.0 - 1.0</i> | Mueve la zona interactiva en relación con la forma. |
| <b>Habilitar fondo</b> <i>Falso/Verdadero</i> | Permite rellenar el fondo con un color sólido. Tenga en cuenta que esto significa que ya no puede encadenarlos mediante la fusión. |
| <b>Color de fondo</b> <i>(Valor de color)</i> | Define el color sólido del fondo. |
| <b>Habilitar entrada de Textura</b> <i>Falso/Verdadero</i> | Permite una entrada personalizada en lugar de un tipo de forma predefinido. |
