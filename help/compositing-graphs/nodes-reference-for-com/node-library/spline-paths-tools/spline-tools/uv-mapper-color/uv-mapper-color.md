---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Utilice el nodo Color del asignador UV para asignar texturas de color a lo largo de las splines para la generación procedimienta de texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color del asignador UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# Color del asignador UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](uv-mapper-color.resources/uv-mapper-color-icon.png "Icono de nodo")

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

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>UV</b> <i>Color</i> | Coordenadas de imagen codificadas en los canales rojo (U) y verde (V) de una imagen en color. |
| <b>Entrada</b> <i>Color</i> | La imagen en color que debe asignarse a las coordenadas proporcionadas en la entrada UV. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Color</i> | El resultado de asignar la imagen de entrada utilizando las coordenadas UV de entrada, como una imagen en color. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Color de fondo</b> <i>Float4</i> | El color de fondo de la imagen de salida.<br>El fondo es visible en las áreas de la imagen donde no se han definido UV (es decir, el valor es (0, 0, 0, 0)). |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Nodo en el gráfico](uv-mapper-color.resources/UVMapperColor-Graph.jpg "Nodo en el gráfico")
