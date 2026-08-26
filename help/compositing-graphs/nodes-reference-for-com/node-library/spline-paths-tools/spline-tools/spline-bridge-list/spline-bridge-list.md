---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---


# Puente polinomial (lista)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-bridge-list-icon.png "Icono de nodo")

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

## Conectores de entrada

<b>Vista previa</b> *Escala de grises* Vista previa de las splines de entrada como una imagen en escala de grises.

<b>Códigos polinómicos</b> *Color* Coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen en color:\
Posición <b> R</b> - X\
<b> G</b> - Posición Y\
<b> B</b> - Height\
<b>A</b> - Datos empaquetados:\
* Firmar: La spline está cerrada (negativa) o abierta (positiva);\
* Valor absoluto: Thickness + 1.

<b>Datos de spline</b> *Color* Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - No utilizado\
<b> A</b> - No utilizado

<b>Cantidad de spline</b> *Entero* Número de splines de entrada.

## Conectores de salida

<b>Vista previa</b> *Escala de grises* Vista previa de las splines de salida como una imagen en escala de grises.

<b>Códigos polinómicos</b> *Color* Coordenadas de los puntos de las splines de salida codificados en los canales RGBA de una imagen en color.\
Posición <b>R</b> - X\
<b>G</b> - Posición Y\
<b>B</b> - Height\
<b>A</b> - Datos empaquetados:\
* Firmar: La spline está cerrada (negativa) o abierta (positiva);\
* Valor absoluto: Thickness + 1.

<b>Datos de spline</b> *Color* Datos adicionales de las splines de salida codificadas en los canales RGBA de una imagen en color.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Sin usar\
<b>A</b> - Sin usar

<b>Cantidad de spline</b> *Entero* Número de splines de salida.

## Parámetros

<b>Cantidad de spline de puente</b> *Entero* Número de splines generadas en las splines de entrada.

<b>Tipo de splines de puente</b> *Entero* Tipo de spline que se genera:
* Lineal: una spline nítida que conecte splines intermediarios con trayectorias rectas de principio a fin;
* Curva cuadrática: una spline curva que conecta splines intermedias con trayectorias suaves de principio a fin.\
  Nota: Se requieren al menos 3 splines de entrada para calcular una spline de curva cuadrática.

<b>Las splines de entrada están cerradas</b> *Booleano* Controla si los puntos primero y último de las splines de entrada deben procesarse como un solo punto. Esto evita la duplicación de la primera y la última spline de recorrido.

<b>Voltear dirección</b> *Boolean* Invierte la dirección de la spline.

<b>Cerrar división de puente</b> *Boolean* Extiende las splines de recorrido para volver a conectarse a la primera spline de la lista de entrada.

<b>Desplazamiento de spline de primer puente </b>*Float2* Aplica un desplazamiento al inicio de todas las splines recorridas. El valor es la longitud normalizada de las splines de entrada.\
Las splines generadas que coinciden con el principio o el final de las splines recorridas se dejan allí.

<b>Desplazamiento de spline de último puente </b>*Float2*\
Aplica un desvío al final de todas las splines recorridas. El valor es la longitud normalizada de las splines de entrada.\
Las splines generadas que coinciden con el principio o el final de las splines recorridas se dejan allí.

<b>Rango de desplazamiento aleatorio</b> *Entero* Distancia máxima utilizada para el desplazamiento aleatorio aplicado en las splines.\
*- spline primaria:* Se usa la longitud completa de las splines primarias. Puede provocar solapamientos.\
*- Intervalo:* Se usa el intervalo entre las splines del puente. Esto mitiga las superposiciones. Esta distancia disminuye a medida que aumenta la cantidad de splines del puente.

<b>Iniciar desplazamiento aleatorio</b> *Float* Un multiplicador para el desplazamiento aleatorio aplicado en la posición inicial de las splines de puente, donde la distancia máxima se especifica mediante el parámetro <b>Random offset range</b>.

<b>Finalizar desplazamiento aleatorio</b> *Float* Un multiplicador para el desplazamiento aleatorio aplicado en la posición final de las splines de puente, donde la distancia máxima se especifica mediante el parámetro <b>Random offset range</b>.

<b>Desplazamiento aleatorio global</b> *Float* Un multiplicador para la *cantidad igual* de desplazamiento aleatorio aplicado en *ambas* posiciones de inicio y fin de las splines de puente, donde la distancia máxima se especifica mediante el parámetro <b>intervalo de desplazamiento aleatorio</b>.

<b>Distribución uniforme</b> *Booleano* Si es True, los puntos de las splines generadas se espacian uniformemente de principio a fin.

+++Grosor
<b>Modo de Thickness</b> *Integer* Método para adquirir el valor de thickness para las splines de puente.\
*- Heredar de splines principales:* Se utiliza el thickness de las splines principales en las posiciones inicial y final de las splines puente\
*: invalidar:* Se usa el valor arbitrario especificado en el parámetro <b>Thickness</b>

<b>Thickness</b> *Float* Valor de thickness absoluto aplicado a las splines de puente.

<b>Aleatorio de Thickness</b> *Float* Un multiplicador aleatorio para el thickness de las splines de bridge, donde el thickness inicial al que se aplica este multiplicador se especifica mediante el parámetro <b>modo de Thickness</b>.

+++

+++Altura
<b>Modo de Height</b> *Integer* Método para adquirir el valor de height para las splines de puente.\
*- Heredar de splines principales:* Se utiliza el height de las splines principales en las posiciones inicial y final de las splines puente\
*: invalidar:* Se usa el valor arbitrario especificado en el parámetro <b>Height</b>

<b>Desplazamiento de Height</b> *Float* Cantidad de desplazamiento aplicada al height heredado de las splines principales antes de que ese height se aplique a las splines del puente.

<b>Height</b> *Float* Valor de height absoluto aplicado a las splines de puente.

<b>Aleatorio de Height</b> *Float* Cantidad aleatoria de ajuste en el height de las splines de bridge, donde ese ajuste depende del parámetro <b>modo de Height</b> seleccionado:\
*: heredar de splines primarias:* El valor es un multiplicador para el height heredado.\
*- Reemplazar:* El valor es un desplazamiento agregado al height.

+++

<b>Corrección no cuadrada </b>*Boolean*

Ajuste la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas.\
Esto también afecta a la distribución uniforme.

+++Vista previa
<b>Mostrar ayuda de dirección</b> *Booleano* Muestra un punto al principio de la spline y una punta de flecha al final en la salida de vista previa.

<b>Mostrar sobre de Thickness</b> *Booleano*\
Muestra líneas adicionales en los bordes del thickness de la spline.

<b>Cantidad de segmentos</b> *Entero* Ajusta el número de segmentos utilizados para dibujar la visualización de la spline en la salida de la vista previa.\
Un valor más alto produce una línea más suave.

<b>Thickness (px)</b> *Flotante* Ajusta el thickness de la visualización de la spline en píxeles en la salida de la vista previa.

<b>Intensidad de vista previa en segundo plano</b> *Flotante* Intensidad de la visualización de la vista previa.

+++

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridge-List_Variant1_Before.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridge-List_Variant1_After.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineBridge-List_Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>

![Nodo en el gráfico](../../../../../../assets/SplineBridge-List_Graph.jpg "Nodo en el gráfico")
