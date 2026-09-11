---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color.html"
breadcrumb-title: ''
description: Utilice el nodo Dispersión en color de spline para distribuir elementos de color a lo largo de trazados de spline para patrones de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter on Spline Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersión en color polinomial
user-guide-description: ''
user-guide-title: ''
source-git-commit: 29dd2e6adc826f63ee26defc0032b0e52d4e30fb
workflow-type: tm+mt
source-wordcount: '3092'
ht-degree: 0%

---


# Dispersión en color polinomial

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](scatter-on-spline-color.resources/scatter-on-spline-color-icon.png "Icono de nodo")

En: Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja el patrón o patrones especificados a lo largo de las splines de entrada en el fondo de entrada.

</td>
</tr>
</table>

El nodo ofrece opciones de personalización profundas para controlar cómo se dispersan los patrones

Algunos aspectos de la dispersión se pueden controlar utilizando imágenes de otros nodos en el gráfico para avanzar en el aspecto dinámico del resultado.

>[!NOTE]
>
> Vea también [Dispersión en escala de grises polinomiales](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-spline-grayscale/scatter-on-spline-grayscale.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Fondo</b> <i>Escala de grises</i> (principal) | Imagen de escala de grises sobre la que se deben dibujar las splines. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificadas en los canales RGBA de una imagen en color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br> * Firmar: La spline está cerrada (negativa) o abierta (positiva);<br> * Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |
| <b>Entrada de patrón #</b> <i>Escala de grises</i> | Patrón(s) que se debe(n) dispersar a lo largo de las splines. |
| <b>Mapa de escala</b> <i>Escala de grises</i> | Mapa que controla la escala de los patrones dispersos. El efecto de este mapa se controla mediante el parámetro &quot;Scale Map Input Multiplier&quot; y se combina con los demás parámetros del grupo &quot;Size&quot;. |
| <b>Mapa de Height</b> <i>Escala de grises</i> | Mapa que controla el height de los motivos dispersos. El efecto de este mapa se controla mediante el parámetro &quot;Height Input Multiplier&quot; y se combina con los demás parámetros &quot;Color&quot; del grupo &quot;Color&quot;. |
| <b>Mapa de máscara</b> <i>Escala de grises</i> | Mapa que controla el enmascaramiento de los motivos dispersos. El efecto de este mapa se controla mediante el parámetro &quot;Umbral del mapa de máscara&quot; y se combina con los demás parámetros &quot;Máscara&quot; del grupo &quot;Color&quot;. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | Imagen que representa los motivos dispersos a lo largo de la spline o splines de entrada sobre el fondo de entrada. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Entrada spline</b> <i>Entero</i> | Método para seleccionar las splines que se deben usar para los patrones de dispersión:<br>** Todas las splines *: Usar todas las splines en la lista de entrada;<br>* *Single Spline*: Utilice sólo la spline especificada de la lista de entrada;<br>* *Rango de spline*: Utilice sólo las splines del rango especificado de la lista de entrada. |
| <b>Índice spline</b> <i>Entero</i> (disponible cuando &quot;Spline Input&quot; está establecido en &quot;Single Spline&quot;) | Índice de lista de la spline que se debe utilizar para patrones de dispersión. |
| <b>Rango de spline</b> <i>Integer2</i> (disponible cuando &quot;Spline Input&quot; está establecido en &quot;Spline Range&quot;) | El rango de índices de lista, incluidas las splines que deben utilizarse para patrones de dispersión. |
| <b>Modo de Dispersión</b> <i>Entero</i> | El método de dispersión de los patrones a lo largo de las splines, que afecta a la cantidad de patrones en cada spline:<br>* Cantidad de forma: La cantidad especificada de patrones espaciados uniformemente está dispersa;<br>* Espaciado de formas: El número de patrones se ajusta automáticamente para ajustarse al espaciado par especificado.<br>En ambos casos, el primer y el último motivo aparecen exactamente al principio y al final de cada spline, respectivamente. |
| <b>Cantidad de forma</b> <i>Entero</i> (disponible cuando &quot;Modo de Dispersión&quot; está establecido en &quot;Cantidad de forma&quot;) | Cantidad de patrones espaciados uniformemente dispersos a lo largo de cada spline. |
| <b>Distribución de formas a lo largo de la spline</b> <i>Entero</i> (disponible cuando &quot;Modo de Dispersión&quot; está establecido en &quot;Cantidad de forma&quot;) | Método de distribución de los patrones a lo largo de una spline:<br>** Desde origen *: El espaciado de los patrones se ve influenciado por las tangentes del punto de spline, donde las formas están más separadas cerca de los puntos con tangentes largas;<br>* *Uniforme*: Los patrones se espacian uniformemente a lo largo de la spline independientemente de sus tangentes y trayectoria. |
| <b>Espaciado entre formas</b> <i>Flotante</i> (disponible cuando &quot;Modo de Dispersión&quot; está establecido en &quot;Espaciado de formas&quot;) | Distancia mínima a lo largo de una spline por la que se deben espaciar los motivos, mientras que el primer y el último motivo se sitúan en el inicio y el final de cada spline, respectivamente. |
| <b>Inicio</b> <i>Flotante</i> | Desplaza el punto desde el inicio de una spline donde comienza la dispersión. El valor es la longitud normalizada de cada spline. |
| <b>Fin</b> <i>Flotante</i> | Desplaza el punto desde el inicio de una spline donde termina la dispersión. El valor es la longitud normalizada de cada spline. |
| <b>Tabla dinámica de formas</b> <i>Flotante2</i> | Desplaza el pivote del patrón X e Y en el espacio de tangente de spline.<br>Teniendo en cuenta que el giro es lo que se coloca en la spline, esto compensa eficazmente los patrones a lo largo de la spline o perpendicularmente a ella.<br>Nota: Las posiciones de los puntos de giro afectan al efecto de los parámetros &quot;Escala&quot; y &quot;Rotación (Pivotar)&quot;. |
| <b>Patrón</b> |  |
| <b>Patrón</b> <i>Entero</i> | El patrón que debe estar disperso a lo largo de las splines:<br>*- Entrada de patrón*: Use los patrones suministrados a las entradas de &quot;Entrada de patrón #&quot;;<br>*- Cuadrado;<br>* Disco;<br>* Paraboloide;<br>* Campana;<br>* Gaussiano;<br>* Espina;<br>* Pirámide;<br>* Ladrillo;<br>* Gradación;<br>* Ondas;<br>* Media campana;<br>* Campana con bordes;<br>* Media luna;<br>* Cápsula;<br>* Cono 7&rbrace;* Gradación w. <br>offset;<br>* Hemisphere.* |
| <b>Número de entrada de patrón</b> <i>Entero</i> (disponible cuando ‘Patrón’ está establecido en ‘Entrada de patrón’) | Selecciona el índice del patrón de entrada que se debe dispersar. |
| <b>Distribución de entrada de patrón</b> <i>Entero</i> (disponible cuando ‘Patrón’ está establecido en ‘Entrada de patrón’) | Método utilizado para seleccionar los patrones de entrada que se deben dispersar en una spline determinada:<br>*- Aleatorio*: se selecciona aleatoriamente un patrón;<br>*- En la spline*: El índice de patrón aumenta gradualmente a lo largo de la spline;<br>*- Índice de patrón*: Realiza un bucle sobre el índice de patrones de entrada en cada spline;<br>*- Índice de spline*: Realiza un bucle sobre el índice de patrones de entrada de una spline a la siguiente en la lista de splines de entrada. |
| <b>Variación de la distribución</b> <i>Flotante</i> (disponible cuando &quot;Distribución de entrada de patrón&quot; está establecido en &quot;A lo largo de la spline&quot;) | Aumenta o disminuye aleatoriamente el índice de motivos seleccionado en la spline. |
| <b>Anular primer patrón</b> <i>Booleano</i> | Seleccione manualmente el índice del patrón que debe colocarse al principio de cada spline. |
| <b>Índice de entrada de primer patrón</b> <i>Entero</i> (disponible cuando &quot;Anular primer motivo&quot; está establecido en &quot;Verdadero&quot;) | Índice del motivo que debe colocarse al principio de cada spline. |
| <b>Anular último patrón</b> <i>Booleano</i> | Seleccione manualmente el índice del patrón que debe colocarse al final de cada spline. |
| <b>Índice de entrada de último patrón</b> <i>Entero</i> (disponible cuando &#39;Omitir último patrón&#39; está establecido en &#39;Verdadero&#39;) | Índice del motivo que debe colocarse al final de cada spline. |
| <b>Duplicados</b> |  |
| <b>Modo de distribución</b> <i>Entero</i> | Método utilizado para colocar los patrones duplicados:<br>*- Lineal*: los duplicados se espacian uniformemente a lo largo de la spline normal desde la ubicación original del patrón;<br>*- Circular*: los duplicados se organizan a lo largo de un círculo virtual centrado en la spline en la ubicación original del patrón. |
| <b>Cantidad de duplicados</b> <i>Entero</i> | El número de patrones duplicados. |
| <b>Desplazamiento</b> <i>Flotante2</i> (disponible cuando &quot;Modo de distribución&quot; está establecido en &quot;Lineal&quot;) | Aplica un desplazamiento a las posiciones de los duplicados a lo largo de la tangente (paralela) y normal (perpendicular) de la spline.<br>Los duplicados de los lados opuestos de la spline se mueven en direcciones opuestas. |
| <b>Centro de desplazamiento</b> <i>Flotante2</i> (disponible cuando &quot;Modo de distribución&quot; está establecido en &quot;Lineal&quot;) | Aplica un desplazamiento a los duplicados a lo largo de la spline en X (paralelo) e Y (perpendicular). |
| <b>Ángulo de pliego</b> <i>Flotante</i> (disponible cuando &quot;Modo de distribución&quot; está establecido en &quot;Circular&quot;) | El arco del círculo virtual a lo largo del cual se distribuyen los duplicados, como el ángulo de ese arco donde 1 es el círculo completo. |
| <b>Distancia de desplazamiento</b> <i>Flotante</i> (disponible cuando &quot;Modo de distribución&quot; está establecido en &quot;Circular&quot;) | Radio del círculo virtual a lo largo del cual se distribuyen los duplicados. |
| <b>Rotación</b> <i>Flotador</i> | Rota el círculo virtual a lo largo del cual se distribuyen los duplicados. |
| <b>Desviar atenuación de inicio/fin</b> <i>Float2</i> | Factores en la distancia desde el punto medio de la spline hasta su inicio y fin, al aplicar desplazamientos a duplicados.<br>Esto significa que los desplazamientos se reducen para duplicados más cercanos a las extremidades de una spline. |
| <b>Atenuación de desplazamiento por Thickness</b> <i>Flotante</i> | Factores en el thickness de la spline al aplicar desvíos a duplicados.<br>Esto significa que los desplazamientos se reducen para los duplicados en una parte de una spline con un thickness inferior. |
| <b>Tamaño</b> |  |
| <b>Modo de tamaño</b> <i>Entero</i> | El método para establecer el tamaño de los patrones dispersos:<br>*- Normal*: El tamaño se controla uniformemente mediante un parámetro global de escala;<br>*- Usar Thickness de spline*: El tamaño depende del thickness de la spline. |
| <b>El Thickness Afecta A</b> <i>Entero</i> (disponible cuando &quot;Modo de tamaño&quot; está establecido en &quot;Usar Thickness desde spline&quot;) | Especifica qué eje de la escala de un patrón debe gobernarse mediante el thickness de la spline:<br>* X e Y: El thickness se multiplica por el tamaño en los ejes X e Y;<br>* X: El thickness se multiplica sólo por el tamaño del eje X;<br>* Y: El thickness se multiplica sólo por el tamaño del eje Y.<br>Cuando no se multiplica, la escala original del motivo es la extensión completa de la imagen.<br>Esto significa que en el modo &quot;X&quot;, el tamaño del eje Y es el tamaño completo de la imagen y debe modificarse mediante el parámetro Size. Lo mismo se aplica al tamaño en el eje X cuando se utiliza el modo &quot;Y&quot;. |
| <b>Tamaño</b> <i>Flotante2</i> | El tamaño original de los patrones en X e Y antes de que otros ajustes se realicen mediante otros parámetros. |
| <b>Aleatorio de tamaño</b> <i>Flotante2</i> | Aplica un multiplicador aleatorio hasta el valor especificado para reducir el tamaño de los patrones en X e Y. |
| <b>Escala de Thickness</b> <i>Flotante</i> (disponible cuando &quot;Modo de tamaño&quot; está establecido en &quot;Usar Thickness desde spline&quot;) | Un multiplicador adicional para la escala de los patrones cuando se acciona mediante el thickness de la spline. |
| <b>Escala</b> <i>Flotante</i> (disponible cuando &quot;Modo de tamaño&quot; está establecido en &quot;Normal&quot;) | Un control global para el tamaño de todos los patrones, donde 1 es la extensión completa de la imagen.<br>El escalado se aplica en relación con el giro de un motivo. La posición de pivote se puede desplazar mediante el parámetro &quot;Shape Pivot&quot;. |
| <b>Escala aleatoria</b> <i>Flotador</i> | Aplica un multiplicador aleatorio hasta el valor especificado para reducir el tamaño de los patrones. |
| <b>Multiplicador de entrada de mapa de escala</b> <i>Flotador</i> | Controla la intensidad de la entrada del mapa de escala. Este mapa actúa como un multiplicador para el tamaño actual de los patrones.<br>El efecto de este mapa se combina con los demás parámetros del grupo &quot;Tamaño&quot;. |
| <b>Modo de muestreo de entrada de escala</b> <i>Espacio de Textura</i> | Método de asignación de los valores de la asignación de escala a las splines:<br>*- espacio de Textura*: Los valores se aplican a las splines donde se colocarían si se colocan en una textura utilizando las coordenadas UV de la textura. Esto aplica efectivamente el valor a las splines &quot;in place&quot;;<br>*- Horizontal along spline*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), donde cada fila se aplica a una spline diferente de arriba a abajo;<br>*- Hor. a lo largo de la spline (rand. desplazamiento X)*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento horizontal aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline);<br>*- Hor. a lo largo de la spline (rand. desplazamiento Y)*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento vertical aleatorio en el mapa de escala para cada spline (es decir, cada fila de códigos de spline). |
| <b>Iniciar o finalizar atenuación</b> <i>Float2</i> | Factores en la distancia desde el punto medio de la spline hasta su inicio y fin al escalar los patrones.<br>Esto significa que el tamaño se reduce para patrones más cercanos a las extremidades de una spline. |
| <b>Posición</b> |  |
| <b>Desplazamiento local</b> <i>Flotante2</i> | Aplica un desvío a las posiciones de los patrones a lo largo de la tangente (paralela) y normal (perpendicular) de la spline. |
| <b>Desplazamiento local aleatorio</b> <i>Float2</i> | Aplica un desvío aleatorio adicional a las posiciones de los patrones a lo largo de la tangente (paralela) y normal (perpendicular) de la spline. |
| <b>Centro aleatorio de desplazamiento local</b> <i>Flotante2</i> | Desplaza el centro del desvío aleatorio aplicado por el parámetro Aleatorio de desvío local a lo largo de la tangente (paralela) y normal (perpendicular) de la spline. |
| <b>Atenuación de inicio/fin del desplazamiento local</b> <i>Float2</i> | Factores en la distancia desde el punto medio de la spline hasta su inicio y fin al aplicar desplazamientos de posición a los patrones.<br>Esto significa que los desplazamientos se reducen para patrones más cercanos a las extremidades de una spline. |
| <b>Atenuación de desplazamiento local por Thickness</b> <i>Flotante</i> | Factores en el thickness de la spline al aplicar desvíos a patrones.<br>Esto significa que los desplazamientos se reducen para los duplicados en una parte de una spline con un thickness inferior. |
| <b>Desplazamiento en spline</b> <i>Flotante</i> | Aplica un desplazamiento de posición a los motivos a lo largo de las splines. |
| <b>Desplazamiento aleatorio en spline</b> <i>Flotador</i> | Aplica un desplazamiento de posición adicional a los motivos a lo largo de las splines. |
| <b>Rotación</b> |  |
| <b>Alinear con tangente</b> <i>Booleano</i> | Gira los motivos para que coincidan con la dirección de la spline en su posición. |
| <b>Giro (tabla dinámica)</b> <i>Flotante</i> | Rota los motivos alrededor de sus puntos de giro.<br>La posición de pivote se puede desplazar mediante el parámetro ‘Shape Pivot’. |
| <b>Rotación aleatoria (dinámica)</b> <i>Flotante</i> | Aplica una rotación aleatoria adicional a los patrones alrededor de sus puntos de giro.<br>La posición de pivote se puede desplazar mediante el parámetro ‘Shape Pivot’. |
| <b>Centro aleatorio de rotación (tabla dinámica)</b> <i>Flotante</i> | Rota alrededor del patrón y pivota el centro de las rotaciones aleatorias aplicadas mediante el parámetro Rotación aleatoria. |
| <b>Rotación (centro)</b> <i>Flotante</i> | Gira los motivos alrededor de su centro. |
| <b>Rotación aleatoria (central)</b> <i>Flotante</i> | Aplica una rotación aleatoria adicional a los patrones alrededor de su centro. |
| <b>Centro aleatorio de rotación (centro)</b> <i>Flotante</i> | Rota alrededor del centro del motivo el centro de las rotaciones aleatorias aplicadas por el parámetro Aleatorio de rotación (Rotation Random). |
| <b>Color</b> |  |
| <b>Color de fondo</b> <i>Flotante4</i> | El color del fondo en la imagen de salida. |
| <b>Modo de fusión</b> <i>Entero</i> | El método para fusionar los colores de los patrones con el fondo y otros patrones superpuestos:<br>*- Add*: Agregue los colores juntos;<br>** Fusión del Alpha*: Aplica una fusión de transparencia simple utilizando el canal alfa del motivo. Los patrones dibujados en último lugar están delante. |
| <b>Modo de color</b> <i>Entero</i> | Método de fusión para seleccionar el color de cada patrón:<br>*- Color base*: El Color base se aplica a todos los patrones;<br>** Posición*: La posición del patrón en el espacio de textura se utiliza para dirigir su color de modo que las coordenadas X e Y se asignen a los canales rojo y verde respectivamente. |
| <b>Color base de la forma</b> <i>Float4</i> | El color base de los patrones. |
| <b>Multiplicador de entrada de color</b> <i>Flotador</i> | Controla la intensidad de la entrada del mapa de color. Este mapa actúa como un multiplicador para el color actual de los patrones.<br>El efecto de este mapa se combina con los demás parámetros del grupo &quot;Color&quot;.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Modo de muestreo de entrada de mapa de color</b> <i>Entero</i> | Método de asignación de los valores de la asignación de color a las splines:<br>*- espacio de Textura*: Los valores se aplican a las splines donde se colocarían si se colocan en una textura utilizando las coordenadas UV de la textura. Esto aplica efectivamente el valor a las splines &quot;in place&quot;;<br>*- Horizontal along spline*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), donde cada fila se aplica a una spline diferente de arriba a abajo;<br>*- Hor. a lo largo de la spline (rand. desplazamiento X)*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento horizontal aleatorio en el mapa de color para cada spline (es decir, cada fila en códigos de spline);<br>*- Hor. a lo largo de la spline (rand. desplazamiento Y)*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento vertical aleatorio en el mapa de color de cada spline (es decir, cada fila de códigos de spline). |
| <b>Color aleatorio</b> <i>Float4</i> | Aplica un desplazamiento aleatorio hasta los valores especificados a los colores de los patrones en el espacio HSV, así como a su alfa.<br>*Nota:* El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Centro de color aleatorio</b> <i>Flotador</i> | Aplica un desplazamiento al rango del desplazamiento aleatorio aplicado en Color aleatorio<br>Un valor de -1 significa que todos los valores aleatorios son más altos y un valor de 1 significa que todos los valores aleatorios son más bajos. |
| <b>Multiplicador de Thickness spline</b> <i>Flotador</i> | Intensidad por la que se multiplica el color de cada motivo respecto al thickness de la spline en su ubicación.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de escala de forma</b> <i>Flotador</i> | Intensidad por la que se multiplica el color de cada motivo en función de su escala.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de índice de forma</b> <i>Flotador</i> | Intensidad por la que se multiplica el color de cada motivo respecto a su índice normalizado.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de Height spline</b> <i>Flotador</i> | Intensidad por la que se multiplica el color de cada motivo respecto al height de la spline en su ubicación.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Luminancia aleatoria</b> <i>Flotador</i> | Aplica un multiplicador aleatorio hasta el valor especificado para reducir la luminancia de los patrones.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de Thickness spline</b> <i>Flotador</i> | Intensidad por la que se multiplica el alfa de cada motivo respecto al thickness de la spline en su ubicación.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de escala de forma</b> <i>Flotador</i> | Intensidad por la que se multiplica el alfa de cada patrón en relación con su escala.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de índice de forma</b> <i>Flotador</i> | Intensidad por la que se multiplica el alfa de cada patrón respecto a su índice normalizado.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de Height spline</b> <i>Flotador</i> | Intensidad por la que se multiplica el alfa de cada motivo respecto al height de la spline en su ubicación.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Luminancia aleatoria</b> <i>Flotador</i> | Aplica un multiplicador aleatorio hasta el valor especificado para reducir el alfa de los patrones.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Aleatorio de máscara</b> <i>Flotador</i> | Ajusta el rango de la máscara aleatoria de patrones, donde 0 significa que no hay patrones enmascarados y 1 significa que todos los patrones sí. |
| <b>Umbral de asignación de máscara</b> <i>Flotador</i> | Los valores del Mapa de máscara por debajo de este valor de umbral se procesan como negros, mientras que los valores por encima del umbral se procesan como blancos.<br>Esto significa que se enmascararán todos los patrones de las áreas del mapa de máscara por debajo de este valor. |
| <b>Modo de muestreo de entrada de mapa de máscara</b> <i>Entero</i> | Método de asignación de los valores de la asignación de máscara a las splines:<br>*- espacio de Textura*: Los valores se aplican a las splines donde se colocarían si se colocan en una textura utilizando las coordenadas UV de la textura. Esto aplica efectivamente el valor a las splines &quot;in place&quot;;<br>*- Horizontal along spline*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), donde cada fila se aplica a una spline diferente de arriba a abajo;<br>*- Hor. a lo largo de la spline (rand. desplazamiento X)*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento horizontal aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline);<br>*- Hor. a lo largo de la spline (rand. desplazamiento Y)*: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento vertical aleatorio en el mapa de escala para cada spline (es decir, cada fila de códigos de spline). |
| <b>Invertir mapa de máscara</b> <i>Booleano</i> | Invierte los valores del Mapa de máscara con la operación &quot;Un signo menos&quot; (1 - x). |
| <b>Invertir máscara</b> <i>Booleano</i> | Invierte la máscara de los motivos. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste las posiciones de los puntos para conservar la forma de la spline en resoluciones que no sean cuadradas. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="scatter-on-spline-color.resources/ScatterOnSplineGrayscale-Variant1-Before.jpg" alt="ScatterOnSplineGrayscale-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="scatter-on-spline-color.resources/ScatterOnSplineColor-Variant1-After.jpg" alt="ScatterOnSplineColor-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="scatter-on-spline-color.resources/ScatterOnSplineGrayscale-Variant2-Before.jpg" alt="ScatterOnSplineGrayscale-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="scatter-on-spline-color.resources/ScatterOnSplineColor-Variant2-After.jpg" alt="ScatterOnSplineColor-Variant2-After">
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

![Ejemplo de nodo 1](scatter-on-spline-color.resources/ScatterOnSplineGrayscale-Demo.gif "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](scatter-on-spline-color.resources/ScatterOnSplineColor-Demo.gif "Ejemplo de nodo 2")

</td>
</tr>
</table>
