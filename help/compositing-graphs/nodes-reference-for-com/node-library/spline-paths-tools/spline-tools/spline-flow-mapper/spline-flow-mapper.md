---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: Utilice el nodo Mapeado de flujo de spline para crear patrones de textura fluida a lo largo de trazados de spline para obtener efectos orgánicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Flow Mapper
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---


# Spline Flow Mapper

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-flow-mapper.resources/spline-flow-mapper-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja un mapa de flujo donde se dibujan los datos vectoriales de flujo a lo largo de las splines de entrada.

Esto permite utilizar splines para controlar la dirección, trayectoria, intensidad y thickness del flujo, así como la pendiente de degradado utilizada para atenuar los datos dibujados en el fondo neutro.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> El resultado puede incluir artefactos no deseados fuera del envolvente de la spline cuando se utilizan valores de thickness muy bajos. Se trata de un problema conocido.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen de color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |
| <b>Curva de perfiles de atenuación</b> <i>Escala de grises</i> | <span id="_Hlk135812146"></span>Imagen que describe una curva utilizando los valores de su primera fila de píxeles. Cuando el parámetro Perfil de atenuación se define en Curva de perfil de entrada, esta entrada se utiliza para controlar la pendiente de degradado para la atenuación de los datos del vector de flujo dibujados a lo largo de la spline.<br>Puede usar un nodo [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para crear la curva. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Color</i> | Mapa de flujo de salida codificado en una imagen en color. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad de segmentos</b> <i>Entero</i> | Las splines se simplifican en segmentos antes de que los datos de flujo vectorial los atraviesen. Una mayor cantidad de segmentos produce una asignación de flujo más fluida a lo largo de las curvas. |
| <b>Modo</b> <i>Entero</i> | Método de selección de las splines a lo largo de las cuales se deben dibujar los datos de flujo vectorial:<br><br>- <i>Dibujar lista de splines</i>: Se utilizan todas las splines de la lista de entrada;<br>- <i>Dibujar spline única</i>: Solo se usa la spline con el índice especificado;<br>- <i>Dibujar rango de spline</i>: Sólo se utilizan las splines cuyo índice se incluye en el rango especificado. |
| <b>Dibujar índice de spline</b> <i>Entero</i> (disponible cuando &#39;Mode&#39; está establecido en &#39;Draw Single Spline&#39;) | Índice de la spline a lo largo de la cual se deben dibujar los datos de flujo vectorial. |
| <b>Dibujar rango de spline</b> <i>Integer2</i> (disponible cuando &#39;Mode&#39; está establecido en &#39;Draw Spline Range&#39;) | Rango de índices de las splines a lo largo de las cuales se deben dibujar los datos de flujo vectorial. |
| <b>Modo de Thickness</b> <i>Entero</i> | El método para establecer el thickness de los datos de flujo vectorial dibujados <br><br>- <i>Manual</i>: Establezca el thickness explícitamente con un valor arbitrario;<br>- <i>Desde spline</i>: Utilice el thickness de la spline. |
| <b>Thickness</b> <i>Flotante</i> (disponible cuando &#39;Modo Thickness&#39; está establecido en &#39;Manual&#39;) | Valor arbitrario para el thickness de los datos de flujo vectorial dibujados a lo largo de las splines. |
| <b>Multiplicador de Thickness</b> <i>Flotante</i> (disponible cuando &#39;Modo de Thickness&#39; está establecido en &#39;Desde spline&#39;) | Un multiplicador global para el thickness de los datos de flujo vectorial dibujados a lo largo de las splines, cuando ese thickness está gobernado por el de las splines. |
| <b>Dirección</b> <i>Entero</i> | Dirección del flujo vectorial en relación con la spline.<br><br>- <i>Tangent</i>: Utilice el vector tangente de la spline;<br>- <i>Normal</i>: Usar el vector normal de la spline;<br>- <i>reflejo normal</i>: Utilice la versión simétrica del vector normal de la spline. |
| <b>Voltear dirección</b> <i>Booleano</i> | Invierte la dirección de las splines, lo que también afecta a la dirección del vector de flujo. |
| <b>Perfil de atenuación</b> <i>Entero</i> | Rampa de degradado utilizada para dibujar la atenuación de los datos del vector de flujo dibujados a lo largo de la spline:<br><br>- <i>Lineal</i>: Utilice una rampa de degradado lineal;<br>- <i>Gaussiano</i>: Use una pendiente de degradado gaussiano<br>- <i>Curva de perfiles de entrada</i>: Utilice la curva proporcionada en la entrada Curva de perfil de atenuación como rampa de degradado. |
| <b>Iniciar atenuación</b> <i>Booleano</i> | <span id="_Hlk135769398"></span>Agrega un semicírculo al comienzo de la spline. El semicírculo utiliza la misma atenuación que la spline. |
| <b>Finalizar atenuación</b> <i>Booleano</i> | Añade un semicírculo al final de la spline. El semicírculo utiliza la misma atenuación que la spline. |
| <b>Atenuación de Height spline</b> <i>Flotador</i> | La intensidad de los datos del vector de flujo dibujados a lo largo de la spline se multiplica por el height de la spline, donde los datos dibujados se desvanecen hasta el color neutro del fondo (0,5, 0,5, 0) a medida que el height se acerca a 0. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas. Esto también afecta a la distribución uniforme. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-flow-mapper.resources/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-flow-mapper.resources/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](spline-flow-mapper.resources/SplineFlowMapper-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
