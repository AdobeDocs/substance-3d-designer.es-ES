---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: Utilice el nodo Deformación polinomial para deformar texturas a lo largo de trazados polinomiales con el fin de crear motivos curvos y orgánicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deformación polinomial
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---


# Deformación polinomial

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-warp.resources/spline-warp-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Desplaza las splines de entrada en función del mapa de intensidad de entrada o del mapa vectorial.

La intensidad del efecto de deformación se puede ajustar a lo largo de la spline mediante los controles de atenuación.

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
| <b>Mapa de intensidad</b> <i>Escala de grises</i> | (Disponible cuando &quot;Usar mapa vectorial&quot; se establece en &quot;Falso&quot;) Imagen de escala de grises de entrada utilizada para controlar la dirección y la intensidad del efecto de deformación en las splines de entrada.<br>El color de cada píxel de la imagen especifica un multiplicador para desplazar los puntos de la spline a lo largo de su dirección normal (es decir, la dirección perpendicular a la spline), hasta el grupo completo de la imagen.<br>El [0; 1] los valores de la imagen se reasignan al [-1; 1] rango cuando se lee como multiplicador: 0 y 1 desplazan la spline en la misma distancia pero en direcciones opuestas. 0,5 deja la spline en su lugar. |
| <b>Mapa de vectores</b> <i>Escala de grises</i> | (Disponible cuando &quot;Usar mapa vectorial&quot; se establece en &quot;Verdadero&quot;) Imagen de color de entrada utilizada para controlar la dirección y la intensidad del efecto de deformación en las splines de entrada.<br>El color de cada píxel de la imagen especifica un vector (X, Y) cuyas coordenadas están codificadas en los canales rojo (X) y verde (Y). +X es la derecha y +Y es abajo.<br>El [0; 1] los valores de la imagen se reasignan al [-1; 1] rango cuando se lee como coordenadas vectoriales: 0 rojo desplaza puntos hacia la izquierda y 0 verde desplaza puntos hacia arriba. El color rojo y verde de 0,5 deja la spline en su lugar. |
| <b>Curva de atenuación</b> <i>Escala de grises</i> | Imagen que describe una curva utilizando los valores de su primera fila de píxeles.<br>Cuando el parámetro Usar curva de atenuación está establecido en True, esta entrada se utiliza para controlar la atenuación del efecto de deformación cerca del principio y el final de la spline.<br>La curva proporciona un perfil para la atenuación, donde el primer píxel de la fila es la intensidad del efecto de deformación al principio de la spline y el último es la intensidad al final. El valor de escala de grises es la intensidad.<br>Puede usar un nodo Curva para crear la curva. |

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
| <b>Intensidad de deformación</b> <i>Flotador</i> | Intensidad por la que se desplazan las splines. |
| <b>Centro de deformación</b> <i>Flotador</i> | Especifica el valor de mapa de intensidad que corresponde a dejar las splines en su lugar.<br>Un valor de 0 o 1 significa que las splines solo se pueden desplazar en un lado. |
| <b>Modo de muestreo</b> <i>Entero</i> | Método de asignación de los valores del mapa de intensidad o del mapa vectorial a las splines:<br>- <i>espacio de Textura</i>: Los valores se aplican a las splines donde se colocarían si se colocan en una textura utilizando las coordenadas UV de la textura. Esto aplica el valor a las splines &quot;in place&quot;;<br>- <i>Horizontal along spline</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), donde cada fila se aplica a una spline diferente de arriba a abajo;<br>- <i>Hora. a lo largo de la spline (rand. desplazamiento X)</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento horizontal aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline);<br>- <i>Hora. a lo largo de la spline (rand. desplazamiento Y)</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento vertical aleatorio en el mapa de escala para cada spline (es decir, cada fila de códigos de spline). |
| <b>Usar mapa vectorial</b> <i>Booleano</i> | Cambia el método de desplazamiento de las splines al uso de una entrada de mapa vectorial para especificar la dirección del desplazamiento.<br>El color de cada píxel de la imagen especifica un vector (X, Y) cuyas coordenadas están codificadas en los canales rojo (X) y verde (Y). +X es la derecha y +Y es abajo.<br>El [0; 1] los valores de la imagen se reasignan al [-1; 1] rango cuando se lee como coordenadas vectoriales: 0 rojo desplaza puntos hacia la izquierda y 0 verde desplaza puntos hacia arriba. El color rojo y verde de 0,5 deja la spline en su lugar. |
| <b>Usar curva de atenuación</b> <i>Booleano</i> | Permite controlar la intensidad del efecto de deformación a lo largo de una spline mediante una curva codificada en la imagen de entrada Curva de atenuación. |
| <b>Mosaico de mapa de intensidad</b> <i>Flotador</i> | (Disponible cuando &quot;Modo de muestreo&quot; no está definido como &quot;Espacio de Textura&quot;) Ajusta el mosaico del mapa de intensidad cuando se asigna directamente a las coordenadas de spline (consulte Entrada de códigos de spline). |
| <b>Iniciar atenuación</b> <i>Flotador</i> | (Disponible cuando &quot;Usar curva de atenuación&quot; está establecido en &quot;Falso&quot;) Un multiplicador para la atenuación del efecto de deformación cerca del inicio de la spline.<br>Un valor de 1 significa que no se aplica deformación al inicio de la spline. |
| <b>Finalizar atenuación</b> <i>Flotador</i> | (Disponible cuando &quot;Usar curva de atenuación&quot; está establecido en &quot;Falso&quot;) Un multiplicador para la atenuación del efecto de deformación cerca del final de la spline.<br>Un valor de 1 significa que no se aplica deformación al final de la spline. |
| <b>Recalcular tangentes</b> <i>Booleano</i> | Si es True, las tangentes de una spline se vuelven a calcular después de aplicar el efecto de deformación.<br>Esto garantiza que las tangentes de la spline sean coherentes con su trayectoria cuando se utilizan en nodos como Dispersión en spline o Asignador de flujo de spline. |
| <b>Vista previa</b> |  |
| <b>Cantidad de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de vista previa.<br>Un valor más alto produce una línea más suave. |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Muestra un punto al principio de la spline y una punta de flecha al final en la salida de previsualización. |
| <b>Mostrar sobre de Thickness</b> <i>Booleano</i> | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Thickness (px)</b> <i>Flotador</i> | Ajusta el thickness de la visualización de la spline en píxeles en la salida de previsualización. |
| <b>Intensidad de vista previa en segundo plano</b> <i>Flotador</i> | El valor se multiplica por la imagen de entrada de vista previa de fondo. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-warp.resources/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![Ejemplo de nodo 1](spline-warp.resources/SplineWarp-Demo.gif "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
