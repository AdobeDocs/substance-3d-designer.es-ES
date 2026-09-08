---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-map.html"
breadcrumb-title: ''
description: Utilice el nodo Mapa de degradado para asignar valores de escala de grises a colores mediante rampas de degradado para la coloración y los efectos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapa de degradado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# Mapa de degradado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Mapa de degradado](gradient-map.resources/comp_gradient_1.png "Nodo atómico: Mapa de degradado"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Reasigna los valores de escala de grises de una imagen utilizando un degradado personalizado.

Este nodo tiene un doble propósito: Se puede usar simplemente como <b> </b>nodo de conversión de escala de grises a color o para colorear la entrada de escala de grises puede asignarla a una curva de color personalizada.

</td>
</tr>
</table>

El nodo ofrece un editor de degradados avanzado y con muchas funciones para asignar varios colores con precisión: ve a la sección [Editor de degradado](#gradient-editor) de esta página para obtener más información.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

## Ejemplos

## Parámetros

|  |  |
| --- | --- |
| <b>Modo de color</b> *Booleano* | Establece el modo de salida en Color o Escala de grises. |
| <b>Dirección de degradado</b> *Booleano* | Establece el degradado en valores de repetición (mosaico) o de sujeción fuera del rango [0, 1]. |
| <b>Degradado</b> *Matriz de claves de degradado* | Rampa de degradado personalizada utilizada para asignar los valores de escala de grises de entrada.   Puede editarse en contexto o mediante el [editor de degradados](#gradient-editor). |

## Editor de degradado

Esta ventana ofrece controles para editar el degradado de referencia utilizado por el nodo Mapa de degradado para asignar valores de escala de grises a colores.

Se puede abrir desde las <b>propiedades</b> del nodo Mapa de degradado de las siguientes maneras:

* Haga clic en LMB en el botón <b>Editor de degradado</b>;
* Haga doble clic en LMB en un pin de la barra de degradado. La chincheta seleccionada se seleccionará automáticamente en el Editor de degradado para que pueda editar directamente sus valores.

![Editor de degradado](gradient-map.resources/image2017-2-17-16-13-5.png "Editor de degradado")

### Edición de los bordes de degradado

Los colores y sus posiciones a lo largo del degradado se controlan mediante chinchetas situadas a lo largo de la barra de degradado.

Cada borde establece un color en su posición a lo largo del degradado.

Las partes del degradado antes y después de los bordes primero y último se establecen en los colores de esos bordes respectivamente.

![Editor de degradado - Vista de degradado](gradient-map.resources/image2017-2-17-17-27-46.png "Editor de degradado - Vista de degradado")

Los siguientes controles están disponibles para editar ubicaciones:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Agregar pin</b>

Haga clic en LMB en el degradado o justo debajo para agregar una marca en la posición en la que hizo clic en la barra de degradado.

El nuevo punto se establecerá en el color del degradado en esa posición.

</td>
<td style="border: 0;" valign="top">

![Editor de degradado - Agregar borde](gradient-map.resources/move-pin.gif "Editor de degradado - Agregar borde")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Mover pin</b>

Mantenga presionada la tecla LMB y arrastre los bordes seleccionados a lo largo de la barra de degradado para moverlos.

También puede establecer la posición de una chincheta con un valor numérico seleccionándola y usando el parámetro <b>Position</b>. La posición es un valor en el rango [0;1] donde 0 es el inicio del degradado y 1 es su final.

![Editor de degradado: parámetro de posición de borde](gradient-map.resources/image2015-8-27-13-56-2.png "Editor de degradado: parámetro de posición de borde")

</td>
<td style="border: 0;" valign="top">

![Editor de degradado - Mover borde](gradient-map.resources/movepin2.gif "Editor de degradado - Mover borde")

</td>
</tr>
</table>

Cuando se seleccionan varias ubicaciones, todas se pueden mover *simultáneamente*. Cuando uno o más bordes alcanzan y terminan el degradado a medida que se mueven, hay dos comportamientos disponibles en función del botón del ratón utilizado para mover:

* <b>LMB:</b> Los bordes permanecen al final, lo que significa que se apilarán en esa ubicación a medida que lleguen a ella y sus posiciones relativas cambian;
* <b>MMB:</b> Los bordes vuelven al otro extremo del degradado, lo que significa que sus posiciones relativas no cambian.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Eliminar pin</b>

Seleccione los bordes y pulse Supr, o bien arrástrelos fuera de la barra de degradado para eliminarlos.

</td>
<td style="border: 0;" valign="top">

![Editor de degradado - Eliminar pin](gradient-map.resources/removepin.gif "Editor de degradado - Eliminar pin")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Invertir posiciones</b>

Refleja las posiciones de los bordes seleccionados en el degradado.

</td>
<td style="border: 0;" valign="top">

![Editor de degradado: Invertir posiciones](gradient-map.resources/invert.gif "Editor de degradado: Invertir posiciones")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Borrar todo</b>

Quita todos los bordes de la barra de degradado.

</td>
<td style="border: 0;" valign="top">

![Editor de degradado - Borrar todo](gradient-map.resources/remove.gif "Editor de degradado - Borrar todo")

</td>
</tr>
</table>

<b>Invertir colores</b>

Este botón cambia los colores de los bordes seleccionados a su negativo.

<b>Desaturar</b>

Este botón desaturará los colores establecidos en los bordes seleccionados.

### Modos de interpolación

Una vez configurados los bordes, puede controlar la transición de los colores de un borde al siguiente mediante los modos de interpolación disponibles:

+++Lineal
Modo de interpolación predeterminado: aplica una interpolación lineal simple entre cada punto, de modo que el degradado progresa uniformemente.

+++

+++Tangentes planos
Cuando se piensa en la transición entre degradados como curvas Bézier donde los bordes son puntos de la curva, este modo establece que estos puntos tengan tangentes horizontales.

Esto da como resultado una transición que evoca una interpolación de paso suave.

Cuando se selecciona este modo, el parámetro <b>Midpoint</b> está habilitado y le permite desplazar la posición horizontal del punto medio vertical de la curva entre los puntos. De este modo, se ajusta eficazmente la escala entre las tangentes &#39;out&#39; e &#39;in&#39;.

+++

+++Suave
Aplica suavizado a la curva de interpolación entre cada punto.

Cuando se selecciona este modo, el parámetro <b>Smoothness</b> está habilitado y le permite ajustar la intensidad del suavizado, donde un valor de 0 es igual al modo de interpolación <b>Lineal</b>.

+++

+++Sin interpolación
El color solo cambia en la ubicación de los bordes y permanece constante hasta el siguiente borde de la barra de degradado.

Esto da como resultado pasos duros entre colores y solo los colores establecidos por los bordes están presentes en el degradado.

+++

### selector de color

![Editor de degradado - Selector de color](gradient-map.resources/image2017-2-17-18-21-29.png "Editor de degradado - Selector de color")

El Selector de color le permite definir un color de varias maneras:

* <b>Barra de degradado y tono</b>

  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Ajuste las posiciones del gizmo en el degradado y de la entalla en la barra de tono para establecer un color.

  </td>
  <td style="border: 0;" valign="top">

  ![Selector de color: área de degradado y barra de tono](gradient-map.resources/colorpalette.gif "Selector de color: área de degradado y barra de tono")

  </td>
  </tr>
  </table>

* <b>Reguladores de RGB, HSV y Alpha</b>

  <table>
  <tr style="border: 0;">
  <td width="100.00%" style="border: 0;" valign="top">

  Los reguladores RGB, HSV y Alpha le permiten definir un color con precisión, ajustando los reguladores o directamente estableciendo sus valores numéricos.

  Como alternativa, utilice un código hexadecimal en el campo de entrada dedicado situado debajo de los reguladores.

  </td>
  <td width="33.33%" style="border: 0;" valign="top">

  ![Selector de color: reguladores RGB, HSV y Alpha](gradient-map.resources/image2017-2-17-18-31-41.png "Selector de color: reguladores RGB, HSV y Alpha")

  </td>
  </tr>
  </table>

* <b>Elegir en pantalla</b>

  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Usa el botón <b>Elegir</b> y haz clic en LMB en cualquier parte de la pantalla para probar el color en esa ubicación.

  </td>
  <td style="border: 0;" valign="top">

  ![Selector de color: seleccionar en pantalla](gradient-map.resources/pick.gif "Selector de color: seleccionar en pantalla")

  </td>
  </tr>
  </table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

El color seleccionado se previsualiza en la mitad superior de la miniatura de color.\
La mitad inferior muestra el color utilizado anteriormente. Haga doble clic en LMB para revertir el color modificado.

</td>
<td width="16.67%" style="border: 0;" valign="top">

![Selector de color - Revertir color](gradient-map.resources/image2015-8-27-14-40-39.png "Selector de color - Revertir color")

</td>
</tr>
</table>

Cuando se seleccionan varias chinchetas, los reguladores RGB, HSV y Alpha se convierten en reguladores delta (?), lo que significa que se utilizan para desplazar el valor de cada chincheta la misma cantidad.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Además, las siguientes funciones están disponibles debajo de la miniatura de color como botones:

<b>Invertir:</b> Cambia el color a negativo;

<b>Al gris:</b> Desatura el color;

<b>Copiar </b>*:* Copie el color seleccionado actualmente en el portapapeles;

<b>Pegar:</b> Cambiar al color que está actualmente en el portapapeles;

<b>sRGB</b>: Utilice el espacio de color sRGB para mostrar colores. Cuando está desactivado, se utiliza el espacio de color Lineal;

<b>Flotante:</b> Muestra los valores del RGB, HSV y regulador del Alpha en punto flotante.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Selector de color - Botones](gradient-map.resources/invert2.gif "Selector de color - Botones")

</td>
</tr>
</table>

### Cuentagotas de degradado

El Cuentagotas de degradado es una de las características más útiles que ofrece este nodo, ya que puede crear degradados complejos simplemente dibujando una línea en una imagen de referencia.

![Editor de degradado - Selector de degradado](gradient-map.resources/pickgradient.gif "Editor de degradado - Selector de degradado")

El regulador <b>Precisión</b> te ayudará a ajustar el degradado recién creado aumentando o disminuyendo el número de teclas: cuanto más bajos sean sus valores, más preciso será el degradado que coincida con los valores seleccionados.

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises* PRINCIPAL | Imagen en escala de grises que se va a procesar. |

## Conectores de salida

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises* |  |

## Ejemplos

*Próximamente.*
