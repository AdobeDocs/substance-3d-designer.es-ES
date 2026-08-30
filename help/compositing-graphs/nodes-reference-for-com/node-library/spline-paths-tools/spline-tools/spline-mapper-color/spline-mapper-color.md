---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-color.html"
breadcrumb-title: ''
description: Utilice el nodo Color del asignador de spline para asignar texturas de color a lo largo de trazados de spline con parámetros personalizables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color del asignador de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 0%

---


# Color del asignador de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-mapper-color.resources/spline-mapper-color-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Asigna una imagen de color de entrada a una forma simple estirada a lo largo de las splines de entrada.

La forma primitiva puede ser un plano, medio cilindro o cilindro. Los cilindros se pueden girar a lo largo de la spline para deformar la imagen asignada en consecuencia.

</td>
</tr>
</table>

El nodo emite la imagen asignada como una imagen en color, así como otra información como el height, UV (es decir, coordenadas de imagen) y una máscara de ID para seleccionar cada spline asignada de forma independiente.

>[!IMPORTANT]
>
> El resultado puede incluir artefactos no deseados fuera del envolvente de la spline cuando se utilizan valores de thickness muy bajos. Se trata de un problema conocido.

>[!NOTE]
>
> Consulte también [Escala de grises del asignador de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> - Firma: La spline está cerrada (negativa) o abierta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |
| <b>Mapa de color</b> <i>Color</i> | Imagen de color de entrada que se debe asignar a lo largo de las splines de entrada. |
| <b>Mapa de Height</b> <i>Escala de grises</i> | Mapa de altura de escala de grises de entrada que se debe asignar a lo largo de las splines de entrada. |
| <b>Twist curve</b> <i>Escala de grises</i> | Imagen que describe una curva utilizando los valores de su primera fila de píxeles.<br>Cuando el parámetro <b>Shape</b> está establecido en <i>Half-Cylinder</i> o <i>Cylinder</i>, esta entrada se utiliza para controlar la torsión de las coordenadas UV alrededor de la forma. Su impacto se controla mediante el parámetro <b>Twist UVs Curve Multiplier</b>.<br>La curva proporciona un perfil para la cantidad de rotación a lo largo de la spline, donde el primer píxel de la fila es la rotación al principio de la spline y el último es la rotación al final. El valor de escala de grises representa un número de vueltas.<br>Puede usar un nodo [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para crear la curva. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Color</b> <i>Color</i> | El resultado de asignar la imagen de color de entrada a través de las splines de entrada, como una imagen de color. |
| <b>Height</b> <i>Escala de grises</i> | El resultado de asignar la imagen del Height de entrada a través de las splines de entrada, como una imagen en escala de grises. |
| <b>UV</b> <i>Color</i> | Los UV (es decir, las coordenadas) de la asignación entre las splines de entrada, codificados en una imagen en color. |
| <b>ID</b> <i>Escala de grises</i> | Máscara de las imágenes asignadas a lo largo de las splines de entrada, donde los valores blancos se incrementan en 1 de una spline a la siguiente para que cada forma se pueda seleccionar de forma independiente. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad de segmentos</b> <i>Entero</i> | Las splines se simplifican en segmentos antes de que las coordenadas de la imagen los atraviesen.<br>Una cantidad mayor de segmentos genera una asignación más fluida a lo largo de las curvas. |
| <b>UV de escala automática</b> <i>Booleano</i> | Ajusta la escala de las coordenadas automáticamente para conservar una imagen cuadrada al asignarla a lo largo de las splines. |
| <b>Escala de UV</b> <i>Float2</i> | Ajusta la escala de las coordenadas asignadas en X (horizontalmente) e Y (verticalmente).<br>Los valores más altos dan como resultado una imagen en mosaico más densa. |
| <b>Modo</b> <i>Entero</i> | Método de selección de las splines a lo largo de las cuales se debe asignar la imagen:<br>- <i>Dibujar lista de splines</i>: Se utilizan todas las splines de la lista de entrada;<br>- <i>Dibujar spline única</i>: Solo se usa la spline con el índice especificado;<br>- <i>Dibujar rango de spline</i>: Sólo se utilizan las splines cuyo índice se incluye en el rango especificado. |
| <b>Dibujar índice de spline</b> <i>Entero</i> | (Disponible cuando &quot;Mode&quot; se establece en &quot;Draw Single Spline&quot;) Índice de la spline a lo largo de la cual se debe asignar la imagen. |
| <b>Dibujar rango de spline</b> <i>Entero2</i> | (Disponible cuando &quot;Mode&quot; se establece en &quot;Draw Spline Range&quot;) Intervalo de índices de las splines a lo largo de las cuales se debe asignar la imagen. |
| <b>Inicio</b> <i>Flotador</i> | Desplaza el inicio de la parte de la spline que se debe asignar.<br>El valor representa la longitud normalizada de la spline. |
| <b>Fin</b> <i>Flotador</i> | Desplaza el extremo de la parte de la spline que se debe asignar.<br>El valor representa la longitud normalizada de la spline. |
| <b>Modo de Thickness</b> <i>Entero</i> | El método para establecer el thickness de la imagen asignada:<br>- <i>Manual</i>: Establezca el thickness explícitamente con un valor arbitrario;<br>- <i>Desde spline</i>: Utilice el thickness de la spline. |
| <b>Thickness</b> <i>Flotador</i> | (Disponible cuando &quot;Modo Thickness&quot; se establece en &quot;Manual&quot;) Valor arbitrario para el thickness de la imagen asignada a lo largo de las splines. |
| <b>Multiplicador de Thickness</b> <i>Flotador</i> | (Disponible cuando &quot;Modo de Thickness&quot; se establece en &quot;Desde spline&quot;) Un multiplicador global para el thickness de la imagen asignada a lo largo de las splines, cuando ese thickness está gobernado por el de las splines. |
| <b>Forma</b> <i>Entero</i> | Forma primitiva utilizada para asignar coordenadas de imagen a lo largo de las splines:<br>- <i>Plano</i>: Las coordenadas se asignan a un plano plano plano;<br>- <i>Medio cilindro</i>: Las coordenadas se asignan a un medio cilindro cuyo eje del círculo base sigue la dirección de la spline;<br>- <i>Cilindro</i>: Las coordenadas se asignan a un cilindro en el que el eje del círculo base sigue la dirección de la spline. |
| <b>Multiplicador de Height del cilindro</b> <i>Flotador</i> | (Disponible cuando &quot;Shape&quot; se define en &quot;Half Cylinder&quot; o &quot;Cylinder&quot;) Un multiplicador para la intensidad de la aportación de height del cilindro en la salida de Height.<br>Los ajustes de Height son acumulativos. |
| <b>Desplazamiento del Height del cilindro</b> <i>Flotador</i> | (Disponible cuando &quot;Shape&quot; está definido como &quot;Half Cylinder&quot; o &quot;Cylinder&quot;) Desplaza el centro del perfil de forma de cilindro o semicírculo desde la superficie de la spline hasta un diámetro debajo de la superficie. |
| <b>Intensidad de giro UV</b> <i>Flotador</i> | (Disponible cuando &quot;Shape&quot; está establecido en &quot;Half Cylinder&quot; o &quot;Cylinder&quot;) La torsión de las coordenadas de imagen alrededor del cilindro, en número de vueltas.<br>La torsión implica girar el cilindro solo al final de la spline. A continuación, la rotación se interpola a lo largo de la spline. |
| <b>Multiplicador de curvas UV de giro</b> <i>Flotador</i> | (Disponible cuando &quot;Shape&quot; se define en &quot;Half Cylinder&quot; o &quot;Cylinder&quot;) Un multiplicador para la intensidad de la contribución de la entrada de Twist curve al torcido del cilindro.<br>La curva proporciona un perfil para la cantidad de rotación a lo largo de la spline, donde el primer píxel de la fila es la rotación al principio de la spline y el último es la rotación al final. El valor de escala de grises representa un número de vueltas. |
| <b>Desplazamiento de curva de giro UV</b> <i>Flotador</i> | (Disponible cuando &quot;Shape&quot; se define en &quot;Half Cylinder&quot; o &quot;Cylinder&quot;) Aplica un desplazamiento global a los valores de rotación proporcionados por el Twist curve, en número de vueltas. |
| <b>Multiplicador de Height spline</b> <i>Flotador</i> | Ajusta la intensidad de la aportación del Height polinómico a la salida del Height.<br>Los ajustes de Height son acumulativos. |
| <b>Multiplicador de Height de entrada</b> <i>Flotador</i> | Ajusta la intensidad de la contribución de la entrada del mapa de altura a la salida del Height.<br>Los ajustes de Height son acumulativos. |
| <b>Color de fondo</b> <i>Float4</i> | El color del fondo en la salida de color. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas.<br>Esto también afecta a la distribución uniforme. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-mapper-color.resources/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-mapper-color.resources/SplineMapperColor-Variant1-After.jpg" alt="SplineMapperColor-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](spline-mapper-color.resources/SplineMapperColor-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 3](spline-mapper-color.resources/SplineMapperColor-Variant1-After1.jpg "Ejemplo de nodo 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
