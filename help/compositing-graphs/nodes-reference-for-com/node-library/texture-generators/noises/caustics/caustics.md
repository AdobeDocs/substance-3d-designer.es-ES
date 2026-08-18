---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Utilice el nodo Cáustico para generar patrones de luz cáustica para crear efectos de iluminación subacuática y refractiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cáustico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Cáustico

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**En:** *Generadores De Texturas**/Ruidos*

**Complejo**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

Genera cáusticos proyectados basados en un mapa de height y una dirección de la luz.Tanto en la versión en escala de grises como en la de color, las diferencias son sutiles, pero la versión en color añade efectos de dispersión de color. La luz se proyecta desde un único punto, no se utiliza ningún mapa de entorno.

</td>
</tr>
</table>

## Parámetros

* **Espacio de color de salida**: *Raw, sRGB*\
  Establecer el espacio de color de salida.
* **Tamaño de cuadrícula de fotones**: *Auto, 512, 1024, 2048, 4096*\
  Establece la calidad ajustando el tamaño de la cuadrícula, pero de forma predeterminada la entrada coincidente. Se puede utilizar para acelerar el cálculo.
* **Escala de Height de superficie**: *0.0 - 1.0*\
  Multiplicador para determinar la interpretación del height.
* **Posición del Height de superficie**: *0.0 - 1.0*\
  Ajuste la distancia de la superficie de refracción a la proyección.
* **IOR de superficie**: *1.0 - 2.0*\
  Defina el índice de refracción; en la versión de color, esto añade más dispersión de color.
* **Tamaño del fotón**: *1.0 - 50.0*\
  El tamaño del fotón afecta a la nitidez del efecto.
* **Dispersión**: *0.0 - 0.01 (solo versión de color)*\
  Afecta solo a la dispersión del color. No es visible cuando el IOR es bajo.
* **Vibración**: *0.0 - 1.0*\
  Añada vibraciones irregulares a las partículas de fotones fundidos.
* **Posición de la luz**:\
  Mueve la posición de la luz. También se realiza mediante un gizmo en la vista 2D.
* **Color de fondo**: *(Valor de color) (Solo versión de color)*\
  Cambiar el color de fondo. Limitado al negro en la versión en escala de grises.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Active la compensación de aplastamiento y estiramiento con proporciones que no sean de cuadrados.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |
