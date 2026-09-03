---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: Utilice el nodo Lista de puentes polinómicos para enlazar texturas entre varias splines de una lista para patrones complejos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Puente polinomial (lista)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Puente polinomial (lista)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](spline-bridge-list.resources/spline-bridge-list-01.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera splines que atraviesan todas las splines de la lista de entrada, a lo largo de estas splines.

Las splines generadas pueden ser lineales (rectas) o curvadas (curvadas).

</td>
</tr>
</table>

>[!TIP]
>
> Las splines generadas van desde la primera spline de la lista hasta la última y atraviesan las splines intermedias siguiendo estrictamente el orden de estas splines en la lista.
> 
> Por lo tanto, debe tener en cuenta el orden en el que se añaden las splines de antemano.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de entrada como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen de color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Vista previa</b> <i>Escala de grises</i> | Vista previa de las splines de salida como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de salida codificados en los canales RGBA de una imagen en color.<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de salida codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de salida. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad de spline de puente</b> <i>Entero</i> | Número de splines generadas a través de las splines de entrada. |
| <b>Tipo de splines de puente</b> <i>Entero</i> | Tipo de spline que se genera:<br><br>- Lineal: una spline nítida conectando splines intermedias con trayectorias rectas de principio a fin;<br>- Curva cuadrática: una spline curva conectando splines intermedias con trayectorias suaves de principio a fin.<br><br>Nota: Se requieren al menos 3 splines de entrada para calcular una spline de curva cuadrática. |
| <b>Las splines de entrada están cerradas</b> <i>Booleano</i> | Controla si el primer y el último punto de las splines de entrada deben procesarse como un único punto. Esto evita la duplicación de la primera y la última spline de recorrido. |
| <b>Voltear dirección</b> <i>Booleano</i> | Invierte la dirección de la spline. |
| <b>Cerrar división de puente</b> <i>Booleano</i> | Extiende las splines de recorrido para volver a conectarse a la primera spline de la lista de entrada. |
| <b>Desplazamiento de spline de primer puente</b> <i>Float2</i> | Aplica un desvío al inicio de todas las splines recorridas. El valor es la longitud normalizada de las splines de entrada.<br>Las splines generadas que coinciden con el principio o el final de las splines recorridas se dejan allí. |
| <b>Desplazamiento de la última spline de puente</b> <i>Float2</i> | Aplica un desvío al final de todas las splines recorridas. El valor es la longitud normalizada de las splines de entrada.<br>Las splines generadas que coinciden con el principio o el final de las splines recorridas se dejan allí. |
| <b>Rango de desplazamiento aleatorio</b> <i>Entero</i> | Distancia máxima utilizada para el desplazamiento aleatorio aplicado en las splines.<br><br>- <i>spline principal:</i> Se utiliza la longitud completa de las splines principales. Puede provocar superposiciones.<br>- <i>Intervalo:</i> Se usa el intervalo entre las splines del puente. Esto mitiga las superposiciones. Esta distancia disminuye a medida que aumenta la cantidad de splines del puente. |
| <b>Iniciar desplazamiento aleatorio</b> <i>Flotador</i> | Un multiplicador para el desplazamiento aleatorio aplicado en la posición inicial de las splines de puente, donde la distancia máxima se especifica mediante el parámetro <b>Rango de desplazamiento aleatorio</b>. |
| <b>Finalizar desplazamiento aleatorio</b> <i>Flotador</i> | Un multiplicador para el desplazamiento aleatorio aplicado en la posición final de las splines de puente, donde la distancia máxima se especifica mediante el parámetro <b>Rango de desplazamiento aleatorio</b>. |
| <b>Desplazamiento aleatorio global</b> <i>Flotador</i> | Un multiplicador para la *cantidad igual* de desplazamiento aleatorio aplicado en *both* la posición inicial y final de las splines de puente, donde la distancia máxima se especifica mediante el parámetro <b>intervalo de desplazamiento aleatorio</b>. |
| <b>Distribución uniforme</b> <i>Booleano</i> | Si es True, los puntos de las splines generadas se espacian uniformemente de principio a fin. |
| <b>Thickness</b> |  |
| <b>Modo de Thickness</b> <i>Entero</i> | Método para adquirir el valor de thickness para las splines de bridge.<br><br>- <i>Heredar de splines primarias:</i> Se usa el thickness de las splines principales en las posiciones inicial y final de las splines de bridge<br>- <i>Reemplazar:</i> Se usa el valor arbitrario que especifique en el parámetro <b>Thickness</b> |
| <b>Thickness</b> <i>Flotador</i> | Valor de thickness absoluto aplicado a las splines de puente. |
| <b>Aleatorio de Thickness</b> <i>Flotador</i> | Un multiplicador aleatorio para el thickness de las splines de bridge, donde el parámetro <b>modo de Thickness</b> especifica el thickness inicial al que se aplica este multiplicador. |
| <b>Height</b> |  |
| <b>Modo de Height</b> <i>Entero</i> | Método para adquirir el valor de height para las splines de bridge.<br><br>- <i>Heredar de splines primarias:</i> Se usa el height de las splines principales en las posiciones inicial y final de las splines de bridge<br>- <i>Reemplazar:</i> Se usa el valor arbitrario que especifique en el parámetro <b>Height</b> |
| <b>Desplazamiento de Height</b> <i>Flotante</i> | Cantidad de desvío aplicado al height heredado de las splines padre, antes de que ese height se aplique a las splines de puente. |
| <b>Height</b> <i>Flotante</i> | Valor de height absoluto aplicado a las splines de puente. |
| <b>Aleatorio de Height</b> <i>Flotante</i> | Una cantidad aleatoria de ajuste en el height de las splines de bridge, donde ese ajuste depende del parámetro <b>modo de Height</b> seleccionado:<br><br>- <i>Heredar de splines principales:</i> El valor es un multiplicador para el height heredado.<br>- <i>Anular:</i> El valor es un desplazamiento agregado al height. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas. Esto también afecta a la distribución uniforme. |
| <b>Vista previa</b> |  |
| <b>Mostrar ayuda de dirección</b> <i>Booleano</i> | Muestra un punto al principio de la spline y una punta de flecha al final en la salida de previsualización. |
| <b>Mostrar sobre de Thickness</b> <i>Booleano</i> | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Cantidad de segmentos</b> <i>Entero</i> | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de previsualización. Un valor más alto produce una línea más suave. |
| <b>Thickness (px)</b> <i>Flotador</i> | Ajusta el thickness de la visualización de la spline en píxeles en la salida de previsualización. |
| <b>Intensidad de vista previa en segundo plano</b> <i>Flotador</i> | Intensidad de la visualización de previsualización. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-02.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-03.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](spline-bridge-list.resources/spline-bridge-list-04.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>

![Nodo en el gráfico](spline-bridge-list.resources/spline-bridge-list-05.jpg "Nodo en el gráfico")
