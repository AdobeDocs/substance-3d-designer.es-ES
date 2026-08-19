---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Utilice el nodo Color del asignador UV para asignar texturas de color a lo largo de las splines para la generación de texturas de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color del asignador UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Color del asignador UV

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/uv-mapper-color-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Asigna la imagen de color de entrada utilizando las coordenadas proporcionadas en la entrada UV.

</td>
</tr>
</table>

>[!NOTE]
>
> Consulte también [Escala de grises del asignador UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md).

## Conectores de entrada

<b>UV</b> *Color* Coordenadas de imagen codificadas en los canales rojo (U) y verde (V) de una imagen en color.

<b>Entrada</b> *Color* Imagen de color que debe asignarse a las coordenadas proporcionadas en la entrada UV.

## Conectores de salida

<b>Salida</b> *Color* Resultado de asignar la imagen de entrada utilizando las coordenadas UV de entrada como imagen en color.

## Parámetros

<b>Color de fondo</b> *Float4* Color de fondo de la imagen de salida.\
El fondo es visible en las áreas de la imagen donde no se definen UV (es decir, el valor es (0, 0, 0, 0)).

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Nodo en el gráfico](../../../../../../assets/UVMapperColor-Graph.jpg "Nodo en el gráfico")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
