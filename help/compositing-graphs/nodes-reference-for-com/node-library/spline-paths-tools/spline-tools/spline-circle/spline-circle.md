---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: Utilice el nodo Círculo polinómico para crear splines circulares para generar formas y patrones redondos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Círculo polinómico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# Círculo polinómico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/spline-circle-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una única spline con forma de círculo.

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

<b>Radio del círculo</b> *Flotador*\
Ajusta el radio del círculo en el espacio de textura.

<b>Círculo previo a la rotación</b> *Flotador*\
Aplica una rotación al círculo base antes de aplicar Tamaño.

<b>Tamaño de círculo</b> *Float2*\
Ajusta el tamaño horizontal (X) y el tamaño vertical (Y) del círculo.

<b>Círculo posterior a la rotación</b> *Flotador*\
Aplica una rotación al círculo base después de aplicar Tamaño.

<b>Posición del círculo</b> *Float2*\
Establece la posición del centro del círculo en el espacio de textura.

<b>Iniciar Thickness</b> *Flotante* Ajusta el thickness del punto inicial del círculo.\
Este thickness se interpola a lo largo de la spline hasta el Thickness final.\
Nota: El thickness se utiliza en nodos Spline específicos.

<b>Finalizar Thickness</b> *Flotante* Ajusta el thickness del punto final del círculo.\
Este thickness se interpola a lo largo de la spline hasta el Thickness Inicio.\
Nota: El thickness se utiliza en nodos Spline específicos.

<b>Iniciar Height</b> *Flotante* Ajusta el height del punto inicial del círculo en el que un valor inferior significa una ubicación más baja o más profunda.\
Este height se interpola a lo largo de la spline hasta el Height final.

<b>Finalizar Height</b> *Flotante* Ajusta el height del punto final del círculo donde un valor más bajo significa una ubicación más baja o más profunda.\
Este height se interpola a lo largo de la spline desde el Height Inicio.

<b>Recortar</b> *Flotante2* Desplaza los puntos inicial y final de la spline a lo largo del círculo.\
Estos valores se normalizan.

<b>Espiral</b> *Flotador* Desplaza el punto inicial del círculo desde su radio hasta su centro.\
La distancia desde el centro se interpola a lo largo de la spline hasta el final de la spline.\
Este valor está normalizado.

<b>Giros en espiral</b> *Flotador* Define el número de vueltas que realiza la espiral alrededor de su centro.

<b>Potencia espiral</b> *Flotador* Aplica una curva de potencia a la distancia desde el centro utilizada para dibujar la espiral.\
Un valor superior a uno significa que una porción mayor de la espiral permanece cerca del centro.

<b>Voltear dirección</b> *Booleano*\
Invierte la dirección de la spline.

<b>Distribución uniforme</b> *Booleano*\
Si es True, los puntos de la spline se espacian uniformemente de principio a fin.

<b>Anexar spline de entrada</b> *Booleano*\
Agrega la spline generada al final de la lista de splines conectadas a las entradas <b>Spline</b>.

<b>Corrección no cuadrada </b>*Booleano* Ajusta la posición y el thickness de los puntos para conservar la forma de la spline en resoluciones no cuadradas.\
Esto también afecta a la distribución uniforme.

+++Vista previa
<b>Mostrar ayuda de dirección</b> *Booleano* Muestra un punto al principio de la spline y una punta de flecha al final en la salida de vista previa.

<b>Mostrar sobre de Thickness</b> *Booleano*\
Muestra líneas adicionales en los bordes del thickness de la spline.

<b>Cantidad de segmentos</b> *Entero* Ajusta el número de segmentos utilizados para dibujar la visualización de la spline en la salida de la vista previa.\
Un valor más alto produce una línea más suave.

<b>Thickness (px)</b> *Flotante* Ajusta el thickness en píxeles de la visualización de la spline en la salida de la vista previa.

+++

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](../../../../../../assets/SplineCircle-Variant1.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/SplineCircle-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo 3](../../../../../../assets/SplineCircle-Variant2.jpg "Ejemplo 3")

</td>
<td style="border: 0;" valign="top">

![Ejemplo 4](../../../../../../assets/SplineCircle-Variant3.jpg "Ejemplo 4")

</td>
</tr>
</table>
