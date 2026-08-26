---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: Utilice el nodo Cúbica polinomial para crear splines cúbicas suaves con cuatro puntos de control para trazados curvos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (cúbico)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---


# Spline (cúbico)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-cubic-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una única spline entre dos puntos <b>p1 </b> y <b>p2</b> en ubicaciones arbitrarias.

La trayectoria de la spline está controlada por la tangente ‘out’ de <b>p1</b> y la tangente ‘in’ de <b>p2</b>.

</td>
</tr>
</table>

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

<b>Voltear dirección</b> *Booleano*\
Invierte la dirección de la spline.

<b>Anexar spline de entrada</b> *Booleano*\
Agrega la spline generada al final de la lista de splines conectadas a las entradas <b>Spline</b>.

<b>Corrección no cuadrada </b>*Booleano* Ajusta la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones no cuadradas.\
Esto también afecta a la distribución uniforme.

+++Altura
<b>Iniciar Height</b> *Flotante* Ajusta el height del punto p1 donde un valor más bajo significa una ubicación más baja o más profunda.\
Esto afecta al height de la spline en p1.

<b>Finalizar Height</b> *Flotante* Ajusta el height del punto p2 donde un valor más bajo significa una ubicación más baja o más profunda.\
Esto afecta al thickness de la spline en p2.

<b>Height de tangente automática</b> *Boolean* Establece automáticamente el height de las tangentes polinomiales para que se interpolen linealmente desde el Height Inicio hasta el Height Final.

<b>Height de tangentes p1</b> *Float* (disponible cuando &quot;Height de tangente automática&quot; es True)\
Ajusta el height de la tangente p1 point ‘out’ donde un valor inferior significa una ubicación más baja o más profunda.\
Esto afecta al height a lo largo de la spline a medida que se aleja de p1.

<b>p2 Height Tangent</b> *Float* (disponible cuando &quot;Height de tangente automática&quot; es True)\
Ajusta el height de la tangente p2 point ‘in’ donde un valor inferior significa una ubicación más baja o más profunda.\
Esto afecta al height a lo largo de la spline a medida que se aleja de p2.

+++

+++Grosor
<b>Iniciar Thickness</b> *Flotante* Ajusta el thickness del punto p1.\
Esto afecta al thickness de la spline en p1.\
Nota: El thickness se utiliza en nodos Spline específicos.

<b>Finalizar Thickness</b> *Flotante* Ajusta el thickness del punto p2.\
Esto afecta al thickness de la spline en p2.\
Nota: El thickness se utiliza en nodos Spline específicos.

<b>Thickness de tangente automática</b> *Boolean* Establece automáticamente el thickness de las tangentes polinomiales para que se interpolen linealmente desde el Thickness Inicio hasta el Thickness Final.\
Nota: El thickness se utiliza en nodos Spline específicos.

<b>Thickness de tangentes p1</b> *Float* (disponible cuando &quot;Thickness de tangente automática&quot; es True)\
Ajusta el thickness de la tangente de salida del punto p1.\
Esto afecta al thickness a lo largo de la spline a medida que se aleja de p1.\
Nota: El thickness se utiliza en nodos Spline específicos.

<b>p2 Thickness Tangent</b> *Float* (disponible cuando &quot;Thickness de tangente automática&quot; es True)\
Ajusta el thickness de la tangente del punto p2 &quot;in&quot;.\
Esto afecta al thickness a lo largo de la spline a medida que se aleja de p2.\
Nota: El thickness se utiliza en nodos Spline específicos.

+++

+++Puntos y coordenadas
<b>p1</b> *Float2* Establece la posición del punto p1 en el espacio de textura.

<b>p1 Tangente</b> *Float2* Establece la posición del control de tangente de salida del punto p1 en el espacio de textura.

<b>p2</b> *Float2* Establece la posición del punto p2 en el espacio de textura.

<b>p2 Tangente</b> *Float2* Establece la posición del control de tangente de entrada de punto p2 en el espacio de textura.

+++

+++Vista previa
<b>Mostrar tangentes</b> *Booleano* Muestra la tangente p1 point ‘out’ y el punto p2 point ‘in’ en la salida de la vista previa.

<b>Mostrar ayuda de dirección</b> *Booleano* Muestra un punto al principio de la spline y una punta de flecha al final en la salida de vista previa.

<b>Cantidad de segmentos</b> *Entero* Ajusta el número de segmentos utilizados para dibujar la visualización de la spline en la salida de la vista previa.\
Un valor más alto produce una línea más suave.

<b>Thickness (px)</b> *Flotante* Ajusta el thickness en píxeles de la visualización de la spline en la salida de la vista previa.

+++

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](../../../../../../assets/SplineCubic-Variant1.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineCubic-Variant2.jpg "Ejemplo de nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 3](../../../../../../assets/SplineCubic-Demo.gif "Ejemplo de nodo 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
