---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-smooth.html"
breadcrumb-title: ''
description: Utilice el nodo Suavizado de bisel para crear bordes biselados suaves en formas y patrones para superficies realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Suavizado de bisel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---


# Suavizado de bisel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de escala de grises Kuwahara anisotrópico](bevel-smooth.resources/bevel_smooth.png "Icono de escala de grises Kuwahara anisotrópico"){width="200px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja un degradado o un color plano desde los bordes de una máscara hacia fuera, hacia dentro o ambos.

Los degradados superpuestos se ordenan por distancia normalizada invertida, de modo que se dibuje la distancia hasta el borde más cercano.

La distancia del degradado se puede ajustar dinámicamente a lo largo del borde mediante un mapa de distancia.

</td>
</tr>
</table>

>[!TIP]
>
> El nodo [Distancia direccional](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/directional-distance/directional-distance.md) ofrece funciones similares, en las que la dilatación se realiza en una dirección específica.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de máscara</b> <i>Escala de grises</i> PRINCIPAL | Imagen de la que se debe extraer la máscara.   Todos los valores por encima del valor &quot;Umbral de máscara&quot; son blancos en esa máscara. |
| <b>Entrada de origen</b> <i>Escala de grises</i> | Una entrada opcional sólo se utiliza cuando el parámetro &quot;Modo de salida&quot; se establece en &quot;Dilación&quot;.   En ese caso, esta imagen se superpone sobre las áreas blancas de la máscara y los valores de escala de grises de los bordes se dilatan. |
| <b>Mapa de distancia</b> <i>Escala de grises</i> | Entrada opcional utilizada cuando el valor del parámetro &#39;Multiplicador de Mapa de distancia&#39; es superior a 0.   Se utiliza para ajustar la distancia de biselado/dilatación a lo largo de los bordes de la máscara, donde un valor más oscuro produce una distancia más corta. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | La imagen resultante, según el &#39;Modo de salida&#39; seleccionado. |
| <b>UV</b> <i>Color</i> | Un mapa UV donde los UV se dilatan a lo largo de los bordes de la máscara.   Se puede conectar a un nodo [UV Mapper](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md) para asignar cualquier otra imagen con estas UV dilatadas. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de salida</b> *Entero* | El método para dilatar los bordes de la máscara:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Bisel:</b> dibuja un degradado del 1 al 0, donde se alcanza 0 en la &#39;Distancia&#39; máxima</li> <li data-preserve-html="true"><b>Dilación:</b> dibuja un color sólido hasta la &#39;Distancia máxima&#39;. Este color es blanco o la imagen de color &quot;Entrada de origen&quot; en el borde de la máscara, si está conectada</li> <li data-preserve-html="true"><b>Distancia:</b> la distancia sin formato desde el borde de máscara más cercano, en el espacio de imagen normalizado donde 1 es la longitud del lado más corto de la imagen</li> </ul> |
| <b>Dirección</b> *Entero* *Disponible cuando &#39;Modo de salida&#39; está establecido en &#39;Bisel&#39; o &#39;Dilación&#39;* | El lado del borde de la máscara que debe dilatarse:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>En:</b> dibuje hacia el interior de la máscara</li> <li data-preserve-html="true"><b>Salida:</b> dibuje hacia el exterior de la máscara</li> <li data-preserve-html="true"><b>Entrada/salida:</b> dibuje hacia el interior y el exterior de la máscara</li> </ul> |
| <b>Distancia máxima</b> *Flotador* | La distancia de dilatación, en el espacio de imagen normalizado donde 1 es la longitud del lado más corto de la imagen de entrada. |
| <b>smoothness de máscara</b> *Flotador* | Intensidad del suavizado aplicado a la máscara.   El valor es el radio del desenfoque y 1 unidad es 1/256 de la imagen. |
| <b>Desplazamiento de máscara</b> *Flotador* | Mueve los bordes de la máscara hacia dentro o hacia fuera. |
| <b>Umbral de máscara</b> *Flotador* | Valor utilizado para detectar los bordes de la máscara en la imagen &quot;Entrada de máscara&quot;.   Los valores por encima de este umbral son el *interior* de las formas de máscara, mientras que los valores por debajo son el *exterior*. |
| <b>Escala</b> *Float2* | Ajusta la distancia horizontal (X) y vertical (Y) de la dilatación.   Estos valores son multiplicadores del valor del parámetro &#39;Distancia máxima&#39;. |
| <b>Multiplicador de Mapa de distancia</b> *Entero* | Ajusta el impacto del Mapa de distancia sobre la distancia máxima. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Suavizado de bisel: Ejemplo 1](bevel-smooth.resources/bevel_smooth_example_1.gif "Suavizado de bisel: Ejemplo 1"){width="1024px" zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Suavizado de bisel: Ejemplo 8](bevel-smooth.resources/bevel_smooth_example_8.jpg "Suavizado de bisel: Ejemplo 8"){width="1024px" zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_4_before.jpg" alt="bevel_smooth_example_4_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_4_after.jpg" alt="bevel_smooth_example_4_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_2_before.jpg" alt="bevel_smooth_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_2_after.jpg" alt="bevel_smooth_example_2_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_3_before.jpg" alt="bevel_smooth_example_3_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_3_after.jpg" alt="bevel_smooth_example_3_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_5_before.jpg" alt="bevel_smooth_example_5_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_5_after.jpg" alt="bevel_smooth_example_5_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_7_before.jpg" alt="bevel_smooth_example_7_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="bevel-smooth.resources/bevel_smooth_example_7_after.jpg" alt="bevel_smooth_example_7_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>
