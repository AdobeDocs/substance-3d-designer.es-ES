---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
breadcrumb-title: ''
description: Utilice el nodo Color del asignador de puente de spline para enlazar texturas entre dos splines con asignación de color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color del asignador de puente spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# Color del asignador de puente spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-bridge-mapper-color.resources/spline-bridge-mapper-color-01.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Asigna una imagen en color a una lista de splines de entrada para que la imagen atraviese las splines en orden.

</td>
</tr>
</table>

>[!TIP]
>
> La asignación va desde la primera spline de la lista hasta la última y atraviesa las splines intermedias siguiendo estrictamente el orden de estas splines en la lista.
> 
> Por lo tanto, debe tener en cuenta el orden en el que se añaden las splines de antemano.

>[!NOTE]
>
> Vea también [Spline Bridge Mapper Grayscale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen de color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |
| <b>Mapa de color</b> <i>Color</i> | Imagen de color de entrada que se debe asignar a través de las splines de entrada. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Color</b> <i>Escala de grises</i> | El resultado de asignar la imagen de color de entrada a través de las splines sobre el fondo, como una imagen de color. |
| <b>Height</b> <i>Escala de grises</i> | Height de las splines asignadas a través de las splines, como una imagen en escala de grises. |
| <b>UV</b> <i>Color</i> | Los UV (es decir, las coordenadas) de la imagen mapeada, codificados en los canales rojo (U) y verde (V) de una imagen en color. |
| <b>Máscara</b> <i>Escala de grises</i> | Máscara de la asignación a través de las splines. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad de segmentos</b> <i>Entero</i> | Las splines se simplifican en segmentos antes de que las coordenadas de la imagen los atraviesen. Una mayor cantidad de segmentos produce una asignación más fluida a lo largo de las curvas. |
| <b>Reducir el estiramiento de UV</b> <i>Booleano</i> | Ajusta el método utilizado para interpolar las coordenadas de imagen de una spline a la siguiente para minimizar el estiro cuando la distancia entre las splines es irregular. |
| <b>Escala de UV</b> <i>Float2</i> | Ajusta la escala de las coordenadas de la imagen. Los valores más altos dan como resultado una imagen de mosaico más denso. |
| <b>Rotación UV</b> <i>Flotador</i> | Rota las coordenadas de la imagen alrededor de su centro. |
| <b>Color de fondo</b> <i>Float4</i> | El color del fondo en la imagen de salida. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-mapper-color.resources/spline-bridge-mapper-color-02.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-bridge-mapper-color.resources/spline-bridge-mapper-color-03.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](spline-bridge-mapper-color.resources/spline-bridge-mapper-color-04.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](spline-bridge-mapper-color.resources/spline-bridge-mapper-color-05.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](spline-bridge-mapper-color.resources/spline-bridge-mapper-color-06.jpg "Ejemplo de nodo 2")

</td>
</tr>
</table>
