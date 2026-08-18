---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: Utilice el nodo Generador de ladrillos para crear patrones de ladrillos de procedimiento con propiedades de mortero, desplazamiento y tamaño personalizables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generador de ladrillos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# Generador de ladrillos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

## Generador de ladrillos

**En:** *Generadores De Texturas**/Patrones*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Generador avanzado de patrones de ladrillo. Tiene muchas opciones para generar patrones de ladrillo hechos por el hombre específicamente

Para obtener más opciones, consulte [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

## Parámetros

* **Ladrillos**: *1 - 64* Establece la cantidad de ladrillos en los ejes X e Y.
* **Bisel**: *0.0 - 1.0* Cambia el perfil de bisel de los ladrillos, permite cambiar en dos direcciones, así como establecer el perfil de difuminación y el redondeo de las esquinas.
* **Mantener proporción**: *Falso/Verdadero* El perfil de bisel está vinculado al tamaño de ladrillo o no.
* **Hueco**: *0.0 - 1.0* Separación entre ladrillos. Tenga en cuenta que el bisel también introduce un hueco, por lo que la configuración de biseles también significa que debe compensar con este parámetro.
* **Tamaño medio**: *0.0 - 1.0* Desplazamiento de patrón de ladrillo, cambia el tamaño de cada otra columna o fila.
* **Height**: *-1.0 - 1.0* Modifica los perfiles de height. Permite introducir variaciones de luminancia y todo tipo de aleatorización.
* **Pendiente**: *-1.0 - 1.0* Presenta una pendiente por ladrillo, como si ciertos ladrillos estuvieran en ángulo.
* **Desplazamiento**: *0.0 - 1.0*\
  Desplaza los ladrillos en función de la fila y afecta al espaciado por fila.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas.

## Imágenes de ejemplo

![](../../../../../../assets/brick-generator-ex-01.gif)

![](../../../../../../assets/brick-generator-ex-02.gif)

</td>
</tr>
</table>
