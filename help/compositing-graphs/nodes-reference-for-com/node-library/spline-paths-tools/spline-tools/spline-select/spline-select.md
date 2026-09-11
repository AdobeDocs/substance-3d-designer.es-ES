---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-select.html"
breadcrumb-title: ''
description: Utilice el nodo Selección de spline para seleccionar y enmascarar regiones específicas en función de los trazados de spline de los gráficos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selección de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Selección de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-select.resources/spline-select-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Selecciona splines en la lista de entrada según los criterios especificados y genera una nueva lista que incluye sólo las splines seleccionadas.

Las splines seleccionadas también se pueden recortar.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de entrada como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Firma: La spline está cerrada (negativa) o abierta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de salida como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de salida codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Firma: La spline está cerrada (negativa) o abierta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de salida codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de salida. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de selección</b> <i>Entero</i> | Método de selección de las splines en la lista de entrada:<br>- <i>Primero</i>: Selecciona la primera spline de la lista;<br>- <i>Last</i>: Selecciona la última spline de la lista;<br>- <i>Index</i>: Selecciona la spline con el índice especificado;<br>- <i>Range</i>: Selecciona las splines cuyos índices se incluyen en el rango especificado. |
| <b>Índice spline</b> <i>Entero</i> | (Disponible cuando &quot;Modo de selección&quot; se define en &quot;Índice&quot;) El índice de la spline que debe seleccionarse. |
| <b>Inicio del intervalo</b> <i>Entero</i> | (Disponible cuando &quot;Modo de selección&quot; se define en &quot;Rango&quot;) El índice más bajo del rango de splines seleccionadas. |
| <b>Fin de intervalo</b> <i>Entero</i> | (Disponible cuando &quot;Modo de selección&quot; se define en &quot;Rango&quot;) El índice más alto del rango de splines seleccionadas. |
| <b>Inicio</b> <i>Flotador</i> | Desplaza el inicio de la parte de la spline que se debe seleccionar. Esto recorta la spline de manera efectiva.<br>El valor representa la longitud normalizada de la spline. |
| <b>Fin</b> <i>Flotador</i> | Desplaza el extremo de la parte de la spline que se debe seleccionar. Esto recorta la spline de manera efectiva.<br>El valor representa la longitud normalizada de la spline. |
| <b>Vista previa</b> |  |
| <b>Cantidad de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de vista previa.<br>Un valor más alto produce una línea más suave. |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Muestra un punto al principio de la spline y una punta de flecha al final en la salida de previsualización. |
| <b>Mostrar sobre de Thickness</b> <i>Booleano</i> | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Thickness (px)</b> <i>Flotador</i> | Ajusta el thickness de la visualización de la spline en píxeles en la salida de previsualización. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant1-Before.jpg" alt="SplineSelect-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant1-After2.jpg" alt="SplineSelect-Variant1-After2">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant2-Before.jpg" alt="SplineSelect-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant2-After.jpg" alt="SplineSelect-Variant2-After">
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

![Ejemplo de nodo 1](spline-select.resources/SplineSelect-Demo.gif "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
