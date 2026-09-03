---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: Utilice el nodo Escala de grises del asignador UV para asignar texturas de escala de grises a lo largo de splines para la generación de texturas de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escala de grises del asignador UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# Escala de grises del asignador UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](uv-mapper-grayscale.resources/uv-mapper-grayscale-01.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Asigna la imagen de escala de grises de entrada mediante las coordenadas proporcionadas en la entrada UV.

</td>
</tr>
</table>

>[!NOTE]
>
> Consulte también [Color del asignador UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>UV</b> <i>Color</i> | Coordenadas de imagen codificadas en los canales rojo (U) y verde (V) de una imagen en color. |
| <b>Entrada</b> <i>Color</i> | La imagen en escala de grises que debe asignarse a las coordenadas proporcionadas en la entrada UV. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Color</i> | El resultado de asignar la imagen de entrada utilizando las coordenadas UV de entrada, como una imagen en escala de grises. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-02.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-03.jpg" alt="UVMapperGrayscale-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-04.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-05.jpg" alt="UVMapper-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Ejemplo de nodo 1](uv-mapper-grayscale.resources/uv-mapper-grayscale-06.jpg "Ejemplo de nodo 1")
