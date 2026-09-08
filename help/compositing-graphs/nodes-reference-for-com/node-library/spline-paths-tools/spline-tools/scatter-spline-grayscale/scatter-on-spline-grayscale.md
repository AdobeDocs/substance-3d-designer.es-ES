---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-on-spline-grayscale.html"
breadcrumb-title: ''
description: Utilice la Dispersión del nodo Escala de grises polinomiales para distribuir elementos de escala de grises a lo largo de trazados polinomiales para patrones de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter on Spline Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersión en escala de grises polinomiales
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '2853'
ht-degree: 0%

---


# Dispersión en escala de grises polinomiales

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/scatter-on-spline-grayscale-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dibuja el patrón o patrones especificados a lo largo de las splines de entrada en el fondo de entrada.

</td>
</tr>
</table>

El nodo ofrece opciones de personalización profundas para controlar cómo se dispersan los patrones.

Algunos aspectos de la dispersión se pueden controlar utilizando imágenes de otros nodos en el gráfico para avanzar en el aspecto dinámico del resultado.

>[!NOTE]
>
> Vea también [Dispersión en Spline Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Fondo</b> <i>Escala de grises</i> (principal) | Imagen de escala de grises sobre la que se deben dibujar las splines. |
| <b>Códigos polinómicos</b> <i>Color</i> | Las coordenadas de los puntos de las splines de entrada codificados en los canales RGBA de una imagen de color:<br><b>R</b> - Posición X<br><b>G</b> - Posición Y<br><b>B</b> - Height<br><b>A</b> - Datos empaquetados:<br>- Firmar: La spline está cerrada (negativa) o abierta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Datos de spline</b> <i>Color</i> | Datos adicionales de las splines de entrada codificadas en los canales RGBA de una imagen en color.<br><b>R</b> - Tangents X<br><b>G</b> - Tangents Y<br><b>B</b> - Sin usar<br><b>A</b> - Sin usar |
| <b>Cantidad de spline</b> <i>Entero</i> | Número de splines de entrada. |
| <b>Entrada de patrón #</b> <i>Escala de grises</i> | Patrón(s) que se debe(n) dispersar a lo largo de las splines. |
| <b>Mapa de escala</b> <i>Escala de grises</i> | Mapa que controla la escala de los patrones dispersos. El efecto de este mapa se controla mediante el parámetro &#39;Escalar multiplicador de entrada de mapa&#39; y se combina con los demás parámetros del grupo &#39;Tamaño&#39;. |
| <b>Mapa de Height</b> <i>Escala de grises</i> | Mapa que controla el height de los motivos dispersos. El efecto de este mapa se controla mediante el parámetro &#39;Multiplicador de entrada de Height&#39; y se combina con los demás parámetros &#39;Color&#39; del grupo &#39;Color&#39;. |
| <b>Mapa de máscara</b> <i>Escala de grises</i> | Mapa que controla el enmascaramiento de los motivos dispersos. El efecto de este mapa se controla mediante el parámetro &quot;Umbral de mapa de máscara&quot; y se combina con los demás parámetros &quot;Máscara&quot; del grupo &quot;Color&quot;. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | Imagen que representa los motivos dispersos a lo largo de la spline o splines de entrada sobre el fondo de entrada. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Entrada spline</b> <i>Entero</i> | Método para seleccionar las splines que se deben usar para los patrones de dispersión:<br><br>- <i>Todas las splines</i>: Usar todas las splines en la lista de entrada;<br>- <i>Single Spline</i>: Utilice sólo la spline especificada de la lista de entrada;<br>- <i>Rango de spline</i>: Utilice sólo las splines del rango especificado de la lista de entrada. |
| <b>Índice spline</b> <i>Entero</i> (disponible cuando &#39;Spline Input&#39; está establecido en &#39;Single Spline&#39;) | Índice de lista de la spline que se debe utilizar para patrones de dispersión. |
| <b>Rango de spline</b> <i>Integer2</i> (disponible cuando &#39;Spline Input&#39; está establecido en &#39;Spline Range&#39;) | El rango de índices de lista, incluidas las splines que deben utilizarse para patrones de dispersión. |
| <b>Modo de Dispersión</b> <i>Entero</i> | El método de dispersión de los patrones a lo largo de las splines, que afecta a la cantidad de patrones en cada spline:<br><br>- Cantidad de forma: La cantidad especificada de patrones espaciados uniformemente está dispersa;<br>- Espaciado entre formas: El número de patrones se ajusta automáticamente para ajustarse al espaciado par especificado.<br><br>En ambos casos, el primer y el último motivo aparecen exactamente al principio y al final de cada spline, respectivamente. |
| <b>Cantidad de forma</b> <i>Entero</i> (disponible cuando &#39;Modo de Dispersión&#39; está establecido en &#39;Cantidad de formas&#39;) | Cantidad de patrones espaciados uniformemente dispersos a lo largo de cada spline. |
| <b>Distribución de formas a lo largo de la spline</b> <i>Entero</i> (disponible cuando &#39;Modo de Dispersión&#39; está establecido en &#39;Cantidad de formas&#39;) | Método de distribución de los patrones a lo largo de una spline:<br><br>- <i>Desde origen</i>: El espaciado de los patrones se ve influenciado por las tangentes del punto de spline, donde las formas están más separadas cerca de los puntos con tangentes largas;<br>- <i>Uniforme</i>: Los patrones se espacian uniformemente a lo largo de la spline independientemente de sus tangentes y trayectoria. |
| <b>Espaciado entre formas</b> <i>Flotante</i> (disponible cuando &#39;Modo de Dispersión&#39; está establecido en &#39;Espaciado de formas&#39;) | Distancia mínima a lo largo de una spline por la que se deben espaciar los motivos, mientras que el primer y el último motivo se sitúan en el inicio y el final de cada spline, respectivamente. |
| <b>Inicio</b> <i>Flotador</i> | <span id="_Hlk135680521"></span>Desplaza el punto desde el inicio de una spline donde comienza la dispersión. El valor es la longitud normalizada de cada spline. |
| <b>Fin</b> <i>Flotador</i> | Desplaza el punto desde el inicio de una spline donde termina la dispersión. El valor es la longitud normalizada de cada spline. |
| <b>Tabla dinámica de formas</b> <i>Float2</i> | Desplaza el pivote del patrón X e Y en el espacio de tangente de spline.<br>Teniendo en cuenta que el giro es lo que se coloca en la spline, esto compensa eficazmente los patrones a lo largo de la spline o perpendicularmente a ella.<br>Nota: Las posiciones de las tablas dinámicas afectan al efecto de los parámetros &quot;Escala&quot; y &quot;Rotación (Tabla dinámica)&quot;. |
| <b>Patrón</b> |  |
| <b>Patrón</b> <i>Entero</i> | Trama que debe estar dispersa a lo largo de las splines:<br><br>- <i>Entrada de patrón</i>: Use los patrones suministrados a las entradas de &#39;Entrada de patrón #&#39;;<br>- Cuadrado;<br>- Disco;<br>- Paraboloide;<br>- Campana;<br>- Gaussiano;<br>- Espina;<br>- Pirámide;<br>- Ladrillo;<br>- Gradación;<br>- Ondas;<br>- Media campana;<br>- Campana con bordes;<br>- Media luna;<br>- Cápsula;<br>- Cono<br>- Gradación w. offset;<br>- Hemisphere. |
| <b>Número de entrada de patrón</b> <i>Entero</i> (disponible cuando &#39;Patrón&#39; está establecido en &#39;Entrada de patrón&#39;) | Selecciona el índice del patrón de entrada que se debe dispersar. |
| <b>Distribución de entrada de patrón</b> <i>Entero</i> (disponible cuando &#39;Patrón&#39; está establecido en &#39;Entrada de patrón&#39;) | Método utilizado para seleccionar los patrones de entrada que se deben dispersar en una spline determinada:<br><br>- <i>Random</i>: se selecciona aleatoriamente un patrón;<br>- <i>A lo largo de la spline</i>: El índice de patrón aumenta gradualmente a lo largo de la spline;<br>- <i>Índice de patrón</i>: Realiza un bucle sobre el índice de patrones de entrada a lo largo de cada spline;<br>- <i>Índice de spline</i>: Realiza un bucle sobre el índice de patrones de entrada de una spline a la siguiente en la lista de splines de entrada. |
| <b>Variación de la distribución</b> <i>Flotante</i> (disponible cuando &#39;Distribución de entrada de patrón&#39; está establecido en &#39;A lo largo de la spline&#39;) | Aumenta o disminuye aleatoriamente el índice de motivos seleccionado en la spline. |
| <b>Anular primer patrón</b> <i>Booleano</i> | Seleccione manualmente el índice del patrón que debe colocarse al principio de cada spline. |
| <b>Índice de entrada de primer patrón</b> <i>Entero</i> (disponible cuando &#39;Anular primer patrón&#39; está establecido en &#39;Verdadero&#39;) | Índice del motivo que debe colocarse al principio de cada spline. |
| <b>Anular último patrón</b> <i>Booleano</i> | Seleccione manualmente el índice del patrón que debe colocarse al final de cada spline. |
| <b>Índice de entrada de último patrón</b> <i>Entero</i> (disponible cuando &#39;Omitir último patrón&#39; está establecido en &#39;Verdadero&#39;) | Índice del motivo que debe colocarse al final de cada spline. |
| <b>Duplicados</b> |  |
| <b>Modo de distribución</b> <i>Entero</i> | Método utilizado para colocar los patrones duplicados:<br><br>- <i>Lineal</i>: los duplicados se espacian uniformemente a lo largo de la normal de la spline desde la ubicación original del patrón;<br>- <i>Circular</i>: los duplicados se organizan a lo largo de un círculo virtual centrado en la spline en la ubicación original del patrón. |
| <b>Cantidad de duplicados</b> <i>Entero</i> | El número de patrones duplicados. |
| <b>Desplazamiento</b> <i>Flotante2</i> (disponible cuando &#39;Distribution Mode&#39; está establecido en &#39;Linear&#39;) | Aplica un desplazamiento a las posiciones de los duplicados a lo largo de la tangente (paralela) y normal (perpendicular) de la spline.<br>Los duplicados de los lados opuestos de la spline se mueven en direcciones opuestas. |
| <b>Centro de desplazamiento</b> <i>Flotante2</i> (disponible cuando &#39;Distribution Mode&#39; está establecido en &#39;Linear&#39;) | Aplica un desplazamiento a los duplicados a lo largo de la spline en X (paralelo) e Y (perpendicular). |
| <b>Ángulo de pliego</b> <i>Flotante</i> (disponible cuando &#39;Distribution Mode&#39; está establecido en &#39;Circular&#39;) | El arco del círculo virtual a lo largo del cual se distribuyen los duplicados, como el ángulo de ese arco donde 1 es el círculo completo. |
| <b>Distancia de desplazamiento</b> <i>Flotante</i> (disponible cuando &#39;Distribution Mode&#39; está establecido en &#39;Circular&#39;) | Radio del círculo virtual a lo largo del cual se distribuyen los duplicados. |
| <b>Rotación</b> <i>Flotador</i> | Rota el círculo virtual a lo largo del cual se distribuyen los duplicados. |
| <b>Desviar atenuación de inicio/fin</b> <i>Float2</i> | Factores en la distancia desde el punto medio de la spline hasta su inicio y fin, al aplicar desplazamientos a duplicados.<br>Esto significa que los desplazamientos se reducen para duplicados más cercanos a las extremidades de una spline. |
| <b>Atenuación de desplazamiento por Thickness</b> <i>Flotador</i> | Factores en el thickness de la spline al aplicar desvíos a duplicados.<br>Esto significa que los desplazamientos se reducen para los duplicados en una parte de una spline con un thickness inferior. |
| <b>Tamaño</b> |  |
| <b>Modo de tamaño</b> <i>Entero</i> | Método para establecer el tamaño de los patrones dispersos:<br><br>- <i>Normal</i>: El tamaño se controla uniformemente mediante un parámetro global &#39;Scale&#39;;<br>- <i>Usar Thickness desde spline</i>: El tamaño depende del thickness de la spline. |
| <b>El Thickness Afecta A</b> <i>Entero</i> (disponible cuando &#39;Modo de tamaño&#39; está establecido en &#39;Usar Thickness desde spline&#39;) | Especifica qué eje de la escala de un patrón debe gobernarse mediante el thickness de la spline:<br><br>- X e Y: El thickness se multiplica por el tamaño en los ejes X e Y;<br>- <span id="_Hlk135741125"></span>X: El thickness se multiplica sólo por el tamaño del eje X;<br>- Y: El thickness se multiplica sólo por el tamaño del eje Y.<br><br>Cuando no se multiplica, la escala original del motivo es la extensión completa de la imagen.<br>Esto significa que en el modo &#39;X&#39;, el tamaño del eje Y es el tamaño completo de la imagen y debe modificarse mediante el parámetro Size. Lo mismo se aplica al tamaño en el eje X cuando se utiliza el modo &#39;Y&#39;. |
| <b>Tamaño</b> <i>Float2</i> | El tamaño original de los patrones en X e Y antes de que otros ajustes se realicen mediante otros parámetros. |
| <b>Aleatorio de tamaño</b> <i>Float2</i> | Aplica un multiplicador aleatorio hasta el valor especificado para reducir el tamaño de los patrones en X e Y. |
| <b>Escala de Thickness</b> <i>Flotante</i> (disponible cuando &#39;Modo de tamaño&#39; está establecido en &#39;Usar Thickness desde spline&#39;) | Un multiplicador adicional para la escala de los patrones cuando se acciona por el thickness de la spline. |
| <b>Escala</b> <i>Flotante</i> (disponible cuando &#39;Modo de tamaño&#39; está establecido en &#39;Normal&#39;) | Un control global para el tamaño de todos los patrones, donde 1 es la extensión completa de la imagen.<br>El escalado se aplica en relación con el pivote de un patrón. La posición de pivote se puede desplazar mediante el parámetro &#39;Shape Pivot&#39;. |
| <b>Escala aleatoria</b> <i>Flotante</i> | Aplica un multiplicador aleatorio hasta el valor especificado para reducir el tamaño de los patrones. |
| <b>Multiplicador de entrada de mapa de escala</b> <i>Flotante</i> | Controla la intensidad de la entrada del mapa de escala. Este mapa actúa como un multiplicador para el tamaño actual de los patrones.<br>El efecto de este mapa se combina con los demás parámetros del grupo &#39;Tamaño&#39;. |
| <b>Modo de muestreo de entrada de escala</b> <i>Espacio de Textura</i> | Método de asignación de los valores de la asignación de escala a las splines:<br><br>- <i>espacio de Textura</i>: Los valores se aplican a las splines donde se colocarían si se colocaran en una textura utilizando las coordenadas UV de la textura. Esto aplica el valor a las splines &#39;in place&#39;;<br>- <i>Horizontal along spline</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), donde cada fila se aplica a una spline diferente de arriba a abajo;<br>- <i>Hora. a lo largo de la spline (rand. desplazamiento X)</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento horizontal aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline);<br>- <i>Hora. a lo largo de la spline (rand. desplazamiento Y)</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento vertical aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline). |
| <b>Iniciar o finalizar atenuación</b> <i>Flotante2</i> | Factores en la distancia desde el punto medio de la spline hasta su inicio y fin al escalar los patrones.<br>Esto significa que el tamaño se reduce para patrones más cercanos a las extremidades de una spline. |
| <b>Posición</b> |  |
| <b>Desplazamiento local</b> <i>Float2</i> | Aplica un desvío a las posiciones de los patrones a lo largo de la tangente (paralela) y normal (perpendicular) de la spline. |
| <b>Desplazamiento local aleatorio</b> <i>Float2</i> | Aplica un desvío aleatorio adicional a las posiciones de los patrones a lo largo de la tangente (paralela) y normal (perpendicular) de la spline. |
| <b>Centro aleatorio de desplazamiento local</b> <i>Float2</i> | Desplaza el centro del desvío aleatorio aplicado por el parámetro Aleatorio de desvío local a lo largo de la tangente (paralela) y normal (perpendicular) de la spline. |
| <b>Atenuación de inicio/fin del desplazamiento local</b> <i>Float2</i> | Factores en la distancia desde el punto medio de la spline hasta su inicio y fin al aplicar desplazamientos de posición a los patrones.<br>Esto significa que los desplazamientos se reducen para patrones más cercanos a las extremidades de una spline. |
| <b>Atenuación de desplazamiento local por Thickness</b> <i>Flotador</i> | Factores en el thickness de la spline al aplicar desvíos a patrones.<br>Esto significa que los desplazamientos se reducen para los duplicados en una parte de una spline con un thickness inferior. |
| <b>Desplazamiento en spline</b> <i>Flotador</i> | Aplica un desplazamiento de posición a los motivos a lo largo de las splines. |
| <b>Desplazamiento aleatorio en spline</b> <i>Flotador</i> | Aplica un desplazamiento de posición adicional a los motivos a lo largo de las splines. |
| <b>Rotación</b> |  |
| <b>Alinear con tangente</b> <i>Booleano</i> | Gira los motivos para que coincidan con la dirección de la spline en su posición. |
| <b>Giro (tabla dinámica)</b> <i>Flotador</i> | Rota los motivos alrededor de sus puntos de giro.<br>La posición de pivote se puede desplazar mediante el parámetro &#39;Shape Pivot&#39;. |
| <b>Rotación aleatoria (dinámica)</b> <i>Flotador</i> | Aplica una rotación aleatoria adicional a los patrones alrededor de sus puntos de giro.<br>La posición de pivote se puede desplazar mediante el parámetro &#39;Shape Pivot&#39;. |
| <b>Centro aleatorio de rotación (tabla dinámica)</b> <i>Flotador</i> | Rota alrededor del patrón y pivota el centro de las rotaciones aleatorias aplicadas mediante el parámetro Rotación aleatoria. |
| <b>Rotación (centro)</b> <i>Flotador</i> | Gira los motivos alrededor de su centro. |
| <b>Rotación aleatoria (central)</b> <i>Flotador</i> | Aplica una rotación aleatoria adicional a los patrones alrededor de su centro. |
| <b>Centro aleatorio de rotación (centro)</b> <i>Flotador</i> | Rota alrededor del centro del motivo el centro de las rotaciones aleatorias aplicadas por el parámetro Rotación aleatoria. |
| <b>Color</b> |  |
| <b>Modo de fusión</b> <i>Entero</i> | El método para fusionar los colores de los patrones con el fondo y otros patrones superpuestos:<br><br>- <i>Máx.</i>: Usar el color más brillante;<br>- <i>Agregar</i>: Añade los colores juntos. |
| <b>Color base de la forma</b> <i>Flotador</i> | El color base de los patrones. |
| <b>Multiplicador de color base de forma</b> <i>Flotador</i> | Intensidad del Color base de forma de los patrones.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de Thickness spline</b> <i>Flotador</i> | Intensidad por la que se multiplica el color de cada motivo respecto al thickness de la spline en su ubicación.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de índice de forma</b> <i>Flotador</i> | Intensidad por la que se multiplica el color de cada motivo respecto a su índice normalizado.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Modo de Height hemisférico</b> <i>Entero</i> (disponible cuando &#39;Patrón&#39; está establecido en &#39;Hemisferio&#39;) | Efecto del height de la spline en un patrón de hemisferio disperso en él:<br><br>- <i>Desplazamiento</i>: el height de spline se agrega al height del hemisferio;<br>- <i>Escala</i>: el height spline se multiplica contra el height del Hemisferio. |
| <b>Multiplicador de Height spline</b> <i>Flotador</i> | Intensidad por la que se multiplica el color de cada motivo respecto al height de la spline en su ubicación.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de escala de forma</b> <i>Flotador</i> | Intensidad por la que se multiplica el color de cada motivo en función de su escala.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Luminancia aleatoria</b> <i>Flotador</i> | Aplica un multiplicador aleatorio hasta el valor especificado para reducir la luminancia de los patrones.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Multiplicador de entrada de Height</b> <i>Flotador</i> | Controla la intensidad de la entrada del mapa de altura. Este mapa actúa como un multiplicador de la luminancia actual de los patrones.<br>El efecto de este mapa se combina con los demás parámetros del grupo &#39;Color&#39;.<br>Nota: El color de salida es el resultado ponderado de todos los multiplicadores de color. |
| <b>Modo de muestreo de entrada de mapa de Height</b> <i>Entero</i> | Método de asignación de los valores de la asignación de altura a las splines:<br><br>- <i>espacio de Textura</i>: Los valores se aplican a las splines donde se colocarían si se colocaran en una textura utilizando las coordenadas UV de la textura. Esto aplica el valor a las splines &#39;in place&#39;;<br>- <i>Horizontal along spline</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), donde cada fila se aplica a una spline diferente de arriba a abajo;<br>- <i>Hora. a lo largo de la spline (rand. desplazamiento X)</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento horizontal aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline);<br>- <i>Hora. a lo largo de la spline (rand. desplazamiento Y)</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento vertical aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline). |
| <b>Aleatorio de máscara</b> <i>Flotador</i> | Ajusta el rango de la máscara aleatoria de patrones, donde 0 significa que no hay patrones enmascarados y 1 significa que todos los patrones sí. |
| <b>Umbral de asignación de máscara</b> <i>Flotador</i> | Los valores del Mapa de máscara por debajo de este valor de umbral se procesan como negros, mientras que los valores por encima del umbral se procesan como blancos.<br>Esto significa que se enmascararán todos los patrones de las áreas del mapa de máscara por debajo de este valor. |
| <b>Modo de muestreo de entrada de mapa de máscara</b> <i>Entero</i> | Método de asignación de los valores de la asignación de máscara a las splines:<br><br>- <i>espacio de Textura</i>: Los valores se aplican a las splines donde se colocarían si se colocaran en una textura utilizando las coordenadas UV de la textura. Esto aplica el valor a las splines &#39;in place&#39;;<br>- <i>Horizontal along spline</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), donde cada fila se aplica a una spline diferente de arriba a abajo;<br>- <i>Hora. a lo largo de la spline (rand. desplazamiento X)</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento horizontal aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline);<br>- <i>Hora. a lo largo de la spline (rand. desplazamiento Y)</i>: Los valores se aplican directamente a las coordenadas de las splines codificadas (consulte Entrada de códigos de spline), con un desplazamiento vertical aleatorio en el mapa de escala para cada spline (es decir, cada fila en códigos de spline). |
| <b>Invertir mapa de máscara</b> <i>Booleano</i> | Invierte los valores del Mapa de máscara con la operación &quot;Un signo menos&quot; (1 - x). |
| <b>Invertir máscara</b> <i>Booleano</i> | Invierte la máscara de los motivos. |
| <b>Corrección no cuadrada</b> <i>Booleano</i> | Ajuste la posición de los puntos para conservar la forma de la spline en resoluciones no cuadradas. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant1-Before.jpg" alt="ScatterOnSplineGrayscale-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant1-After.jpg" alt="ScatterOnSplineGrayscale-Variant1-After">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant2-Before.jpg" alt="ScatterOnSplineGrayscale-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant2-After.jpg" alt="ScatterOnSplineGrayscale-Variant2-After">
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

![Ejemplo de nodo 2](../../../../../../assets/ScatterOnSplineGrayscale-Demo.gif "Ejemplo de nodo 2")

</td>
<td style="border: 0;" valign="top">

![Demostración de nodo 2](../../../../../../assets/ScatterOnSplineGrayscale-Demo2.gif "Demostración de nodo 2")

</td>
</tr>
</table>
