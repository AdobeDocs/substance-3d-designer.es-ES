---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/apply-color-palette.html"
breadcrumb-title: ''
description: Utilice el nodo Aplicar paleta de colores para reasignar texturas mediante una paleta de colores para efectos de color estilizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Apply Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aplicar paleta de colores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Aplicar paleta de colores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Cuantificar color](apply-color-palette.resources/ApplyColorPalette.png "Icono Cuantificar color"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aplica los colores de una paleta ordenada a una imagen mediante un mapa de ID.

Los colores se distribuyen haciendo coincidir los índices del mapa de ID con los índices de colores de la paleta.

Por ejemplo, el color #2 de la paleta se aplicará a todos los píxeles del mapa de ID con un valor de ID de 2.

Este nodo se puede utilizar en combinación con los siguientes nodos: [Cuantificar color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Crear paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Modificar paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Ver paleta de colores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>ID</b> <i>Escala de grises</i> PRINCIPAL | Mapa de ID de entrada utilizado para distribuir los colores en la paleta de entrada.   Un mapa de ID es una imagen en la que los píxeles que forman parte de un todo (por ejemplo, una forma) tienen el mismo valor de identificación único. En este caso, el valor es un entero.   Se puede generar una asignación de ID usando un nodo [Quantize Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md). |
| <b>Paleta</b> <i>Color</i> | Una lista ordenada de colores de RGB codificados como una fila de píxeles. La paleta puede contener un máximo de 256 colores. Esta es la paleta que el nodo asigna a los índices de la asignación de ID.   Las paletas se pueden producir con un nodo [Quantize Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) y modificarse con un nodo [Modify Color Palette](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md). |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Color</i> | El resultado de asignar los colores de la paleta a los índices del mapa de ID. |

## Ejemplos

![Aplicar paleta de colores: Ejemplo 1](apply-color-palette.resources/apply_color_palette_example_2.png "Aplicar paleta de colores: Ejemplo 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="apply-color-palette.resources/apply_color_palette_example_1_before.jpg" alt="apply_color_palette_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="apply-color-palette.resources/apply_color_palette_example_1_after.jpg" alt="apply_color_palette_example_1_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

![Aplicar paleta de colores: Ejemplo 3](apply-color-palette.resources/apply_color_palette_example_4.png "Aplicar paleta de colores: Ejemplo 3"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="apply-color-palette.resources/apply_color_palette_example_3_before.jpg" alt="apply_color_palette_example_3_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="apply-color-palette.resources/apply_color_palette_example_3_after.jpg" alt="apply_color_palette_example_3_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>
