---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-fill.html"
breadcrumb-title: ''
description: Utilice el nodo Relleno polinómico para rellenar áreas definidas por splines cerradas con texturas o colores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Relleno polinómico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Relleno polinómico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-fill.resources/spline-fill-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Rellena el interior de las splines de entrada con un blanco sólido. El exterior está lleno de negro sólido.

Las splines abiertas se cierran con una línea recta de principio a fin. Las intersecciones en las que la spline se cruza a sí misma se resuelven invirtiendo los lados interior y exterior de las líneas en esos cruces.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> No se recomienda utilizar este nodo en splines que estén fuera del mosaico [0,1]. El proceso de llenado no es fiable en ese caso.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen de color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | La imagen resultante de rellenar las splines de entrada con un blanco plano sobre un fondo negro plano. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-fill.resources/SplineFill-Variant1-Before.jpg" alt="SplineFill-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-fill.resources/SplineFill-Variant1-After.jpg" alt="SplineFill-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](spline-fill.resources/SplineFill-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
