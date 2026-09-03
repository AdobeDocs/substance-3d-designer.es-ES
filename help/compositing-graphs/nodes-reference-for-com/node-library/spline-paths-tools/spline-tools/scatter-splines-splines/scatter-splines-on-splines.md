---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-splines-on-splines.html"
breadcrumb-title: ''
description: Utilice el nodo Splines en splines de Dispersión para distribuir splines hijo a lo largo de las rutas de spline padre.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter Splines on Splines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Splines de dispersión en Splines
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '2832'
ht-degree: 0%

---


# Splines de dispersión en Splines

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Splines de Dispersión en Splines: Icono](scatter-splines-on-splines.resources/scatter-splines-on-splines-01.png "Splines de Dispersión en Splines: Icono")

<b>En:</b> Herramientas de spline y trazado > Herramientas de spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Permite colocar splines a lo largo de las splines primarias de entrada.

El nodo ofrece opciones de personalización profundas para controlar cómo se dispersan las splines y permite la dispersión de splines rectas simples o de sus propias splines personalizadas.

El nodo permite crear estructuras complejas para asignar colores e imágenes mediante los nodos [Spline Mapper](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md), o se usa como esqueleto para colocar formas mediante la Dispersión [en Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-spline-grayscale/scatter-on-spline-grayscale.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Tutorial

Haz clic en la imagen de la derecha para acceder a nuestro <b>tutorial dedicado</b>, y disfrutar de una visita guiada por las capacidades del nodo y su uso en el contexto de un flujo de trabajo basado en spline.

</td>
<td style="border: 0;" valign="top">

[![Nodos de división de vídeo](scatter-splines-on-splines.resources/scatter-splines-on-splines-02.png)](https://youtu.be/aUUWV1dYQdI)

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Vista previa</b> *Escala de grises* | Vista previa de las splines de entrada como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> *Color* | Las coordenadas de los puntos de las splines padre codificados en los canales RGBA de una imagen en color:  <b>R</b> - Posición X <b>G</b> - Posición Y <b>B</b> - Height <b>A</b> - Datos empaquetados:          - Firma: La spline está cerrada (negativa) o abierta (positiva) - Valor absoluto: THICKNESS + 1 |
| <b>Datos de spline</b> *Color* | Datos adicionales de las splines padre codificadas en los canales RGBA de una imagen en color:  <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Sin Usar |
| <b>Cantidad de spline</b> *Entero* | El número de splines padre. |
| <b>Códigos de spline personalizados</b> *Color* | Las coordenadas de los puntos de las splines personalizadas codificadas en los canales RGBA de una imagen en color:  <b>R</b> - Posición X <b>G</b> - Posición Y <b>B</b> - Height <b>A</b> - Datos empaquetados:          - Firma: La spline está cerrada (negativa) o abierta (positiva) - Valor absoluto: THICKNESS + 1 |
| <b>Datos de spline personalizados</b> *Color* | Datos adicionales de las splines personalizadas codificadas en los canales RGBA de una imagen en color:  <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Sin Usar |
| <b>Cantidad de spline personalizada</b> *Entero* | Número de splines personalizadas. |
| <b>Mapa de escala</b> *Escala de grises* | Mapa de escala de grises que controla la escala de las splines dispersas.  El efecto de este mapa se controla mediante el parámetro <b>Scale Map Input Multiplier</b> y se combina con los demás parámetros del grupo <b>Size</b>. |
| <b>Mapa de rotación</b> *Escala de grises* | Mapa de escala de grises que controla la rotación de las splines dispersas.  El efecto de este mapa se controla mediante el parámetro <b>Multiplicador de entrada de Mapa de rotación</b> y se combina con los demás parámetros del grupo <b>Rotación</b>. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Vista previa</b> *Escala de grises* | Vista previa de las splines dispersas como una imagen en escala de grises. |
| <b>Códigos polinómicos</b> *Color* | Las coordenadas de los puntos de las splines dispersas codificadas en los canales RGBA de una imagen en color:  <b>R</b> - Posición X <b>G</b> - Posición Y <b>B</b> - Height <b>A</b> - Datos empaquetados:          - Firma: La spline está cerrada (negativa) o abierta (positiva) - Valor absoluto: THICKNESS + 1 |
| <b>Datos de spline</b> *Color* | Datos adicionales de las splines dispersas codificadas en los canales RGBA de una imagen en color:  <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Sin usar <b>A</b> - Sin usar |
| <b>Cantidad de spline</b> *Entero* | Número de splines dispersas. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Lado</b> *Entero* | Controla en qué lado o lados de las splines principales se deben dispersar las splines, teniendo en cuenta que &quot;adelante&quot; es la dirección de las *splines principales*:<br><br>- <b>Izquierda</b> Coloque las splines en el lado izquierdo.<br>- <b>Derecha</b> Coloque las splines en el lado derecho.<br>- <b>Izquierda + Derecha</b> Coloque las splines en ambos lados.<br>- <b>Izquierda / Derecha - Alternar</b> Coloque las splines a la izquierda y la derecha de forma alternativa (p. cada otro lado).<br>- <b>Izquierda / Derecha - Aleatorio</b> Elija el lado aleatoriamente para cada spline. |
| <b>Modo de cantidad</b> *Entero* | Método de dispersión de las splines a lo largo de las splines principales, que afecta a la cantidad de splines dispersas en cada spline principal:<br><br>- <b>Cantidad fija por spline</b> La cantidad especificada de splines espaciadas uniformemente se dispersa.<br>- <b>Espaciado</b> La cantidad de splines se ajusta automáticamente para ajustarse al espaciado uniforme especificado.<br><br>En ambos casos, la primera y la última spline dispersa aparecen exactamente al principio y al final de cada spline principal, respectivamente. |
| <b>Cantidad De Spline Por Spline</b> *Entero* | Cantidad de splines espaciadas uniformemente dispersas a lo largo de cada spline principal. |
| <b>Espaciado entre líneas</b> *Flotador* | Distancia mínima a lo largo de las splines padre por la que se deben espaciar las splines, mientras que la primera y la última spline se mantienen en el principio y el final de cada spline padre, respectivamente. |
| <b>Tipo de spline</b> *Entero* | Selecciona el tipo de spline que se debe dispersar en las splines principales:<br><br>- <b>Straight</b> Una spline simple y recta.<br>- <b>spline personalizada</b> La spline o splines proporcionadas a las entradas de <b>Custom Spline</b>. Se admiten varias splines cuando se agregan juntas en una lista. |
| <b>Selección de spline personalizada</b> *Entero* | Cuando se utilizan varias splines personalizadas anexadas a una lista, este parámetro le permite seleccionar cómo deben distribuirse estas splines en la dispersión.<br><br>- <b>Lista completa</b> Todas las splines se dispersan juntas como un grupo.<br>- <b>Secuencial</b> Cada spline individual se distribuye en orden, dando vueltas alrededor de la lista.<br>- <b>Aleatorio</b> Se selecciona una spline aleatoria de la lista para cada spline dispersa. |
| <b>Inicio</b> *Flotador* | Desplaza el punto desde el inicio de las splines padre donde comienza la dispersión. El valor es la longitud normalizada de cada spline padre. |
| <b>Fin</b> *Flotador* | Desplaza el punto desde el inicio de las splines padre donde termina la dispersión. El valor es la longitud normalizada de cada spline padre. |
| <b>Voltear dirección</b> *Booleano* | Invierte la dirección de las splines dispersas. |
| <b>Modo de simetría izquierdo/derecho</b> *Entero* | Método de simetría aplicado a las splines dispersas a cada lado de las splines principales.<br><br>- <b>Deshabilitado</b> No se aplica ninguna simetría, las splines se colocan a cada lado mediante una rotación simple.<br>- <b>simetría izquierda</b> La spline de la izquierda es simétrica a la de la derecha relativa a la spline principal.<br>- <b>simetría derecha</b> La spline de la derecha es simétrica a la de la izquierda relativa a la spline principal. |
| <b>Vínculo aleatorio izquierdo/derecho</b> *Booleano* | Controla si las splines de cada lado de la spline padre deben utilizar los mismos valores cuando se utiliza la rotación aleatoria, la escala aleatoria, etc. En otras palabras:<br><br>- <i>False:</i> cada spline usa valores aleatorios independientes<br>- <i>True:</i> ambas splines comparten los mismos valores aleatorios |
| <b>Modo de giro de spline</b> *Entero* | Define el método de colocación del pivote de las splines dispersas, lo que afecta a la rotación y al escalado.<br>Tenga en cuenta que la tabla dinámica *siempre se coloca en la spline principal* y sus controles afectan a la spline dispersa. En otras palabras: Si la tabla dinámica no se mueve, es la spline dispersada la que se mueve y escala con relación a ella.<br><br>- <b>Posición a lo largo de la spline</b> Mover la tabla dinámica a lo largo de la spline dispersa.<br>- <b>Posición absoluta</b> Establezca una posición arbitraria para la tabla dinámica. |
| <b>Posición de pivote a lo largo de la spline</b> *Flotador* | Posición normalizada del pivote a lo largo de la spline dispersada, donde 0 es su inicio y 1 es su final.<br>Tenga en cuenta que el giro sigue la *dirección* de la spline dispersada y la orientación de la spline puede cambiar para conservar la posición y la rotación de la spline principal con respecto a la spline principal. |
| <b>Posición absoluta de tabla dinámica</b> *Float2* | Posición en el espacio UV del pivote. |
| <b>Corrección no cuadrada</b> *Booleano* | Ajuste la posición y el thickness de las splines para conservar su forma en resoluciones no cuadradas.<br><i>Nota:</i> Al usar splines personalizados, la spline personalizada debe usar la *misma proporción de imagen* que los nodos <b>Splines de Dispersión en splines</b>. |
| <b>Tamaño</b> |  |
| <b>Escala de spline</b> *Flotador* | Un control global para el tamaño de todas las splines, donde 1 es su tamaño original completo.<br>El escalado se aplica en relación con el giro de una spline. La posición de pivote se puede desplazar mediante el parámetro <b>Spline Pivot</b>. |
| <b>Aleatoria de escala de spline</b> *Flotador* | Aplica un multiplicador aleatorio hasta el valor especificado para reducir el tamaño de las splines. |
| <b>Multiplicador de entrada de mapa de escala</b> *Flotador* | Controla la intensidad de la entrada <b>Scale Map</b>. Este mapa actúa como un multiplicador para el tamaño actual de los patrones.<br>El efecto de este mapa se combina con los demás parámetros del grupo <b>Size</b>. |
| <b>Modo de muestreo de entrada de mapa de escala</b> *Entero* | Método para asignar los valores del <b>mapa de escala</b> a las splines:<br><br>- <b>espacio de Textura</b> Los valores se aplican a las splines donde se colocarían si se colocaran en una textura utilizando las coordenadas UV de la textura. Esto aplica el valor a las splines &#39;in place&#39;<br>- <b>Horizontal along spline</b>. Los valores se aplican a las coordenadas de las splines codificadas directamente (consulte la entrada <b>Spline Coords</b>), donde cada fila se aplica a una spline diferente de arriba a abajo<br>- <b>Hor. a lo largo de la spline (rand. desplazamiento X)</b> Los valores se aplican a las coordenadas de las splines codificadas directamente (consulte la entrada <b>Spline Coords</b>), con un desplazamiento horizontal aleatorio en el <b>mapa de escala</b> para cada spline (es decir, cada fila en <b>Spline Coords</b>)<br>- <b>Hor. a lo largo de la spline (rand. desplazamiento Y)</b> Los valores se aplican a las coordenadas de las splines codificadas directamente (consulte la entrada <b>Spline Coords</b>), con un desplazamiento vertical aleatorio en el <b>mapa de escala</b> para cada spline (es decir, cada fila en <b>Spline Coords</b>) |
| <b>Iniciar o finalizar atenuación</b> *Float2* | Factores en la distancia desde el punto medio de la spline hasta sus <b>iniciales</b> y <b>finales</b> al escalar las splines.<br>Esto significa que el tamaño disminuye para las splines más cercanas a las extremidades de una spline. |
| <b>Posición</b> |  |
| <b>Desplazamiento local</b> *Float2* | Aplica un desvío a las posiciones de las splines a lo largo de la tangente (paralela) y normal (perpendicular) de la spline principal. |
| <b>Desplazamiento en rango de spline</b> *Entero* | Establece el intervalo de desplazamiento aplicado a las splines dispersas a lo largo de las splines principales.<br><br>- <b>Intervalo</b> El intervalo abarca el intervalo *entre* cada spline dispersada.<br>- <b>spline principal</b> El intervalo abarca la *longitud completa* de la spline principal. |
| <b>Desplazamiento en spline</b> *Flotador* | Aplica un desvío de posición a las splines a lo largo de las splines padre. |
| <b>Rango de desplazamiento aleatorio</b> *Entero* | Establece el intervalo de desplazamiento aleatorio aplicado a las splines dispersas a lo largo de las splines principales.<br><br>- <b>Intervalo</b> El intervalo abarca el intervalo *entre* cada spline dispersada.<br>- <b>spline principal</b> El intervalo abarca la *longitud completa* de la spline principal. |
| <b>Desplazamiento aleatorio en spline</b> *Flotador* | Aplica un desvío de posición adicional a las splines a lo largo de las splines padre. |
| <b>Desplazamiento por Thickness</b> *Flotador* | Aplica un desplazamiento a las splines dispersas a lo largo de la normal de las splines principales, hasta el thickness de las splines principales.<br>En efecto, un valor de 1 permite colocar las splines dispersas en la *superficie* del envolvente de las splines principales. |
| <b>Rotación</b> |  |
| <b>Alineación de spline personalizada</b> *Entero* | Controla la orientación inicial de las splines personalizadas en las splines principales.<br><br>- <b>Tangente del primer punto</b> Las splines están orientadas según la tangente de su primer punto. En otras palabras, salen de las splines principales en la dirección establecida por su primer punto.<br>- <b>Espacio de imagen</b> Las splines se colocan tal y como aparecen originalmente, sin ningún ajuste adicional de su posición u orientación, como si la imagen que las representa se situara en la spline principal. |
| <b>Modo de rotación</b> *Entero* | Establece la orientación inicial de las splines dispersas.<br><br>- <b>Desde spline</b> Las splines están orientadas para que coincidan con la *normal* de las splines principales en su ubicación.<br>- <b>Absoluta</b> Todas las splines están orientadas de la *misma manera*, independientemente de la dirección de las splines principales. |
| <b>Rotación</b> *Flotante* | Gira las splines alrededor de sus puntos de giro, en número de vueltas. La posición de pivote se puede desplazar mediante el parámetro <b>Spline Pivot</b>. |
| <b>Aleatorio de rotación</b> *Flotante* | Aplica una rotación aleatoria adicional a las splines alrededor de sus puntos de giro, en número de vueltas. La posición de pivote se puede desplazar mediante el parámetro <b>Spline Pivot</b>. |
| <b>Ángulo izquierdo/derecho</b> *Flotante* | Controla el ángulo de rotación simétrica aplicado a las splines a cada lado de las splines padre, en número de vueltas. |
| <b>Ángulo aleatorio izquierdo/derecho</b> *Flotador* | Añade una cantidad aleatoria de rotación simétrica a las splines de cada lado de las splines padre, en número de vueltas. |
| <b>Multiplicador de entrada de Mapa de rotación</b> *Flotante* | Controla la intensidad de la entrada de <b>Mapa de rotación</b>. Este mapa actúa como un multiplicador para la rotación actual de los patrones.<br>El efecto de este mapa se combina con los demás parámetros del grupo <b>Rotation</b>. |
| <b>Modo de muestreo de entrada de Mapa de rotación</b> *Entero* | Método para asignar los valores del <b>Mapa de rotación</b> a las splines:<br><br>- <b>espacio de Textura</b> Los valores se aplican a las splines donde se colocarían si se colocaran en una textura utilizando las coordenadas UV de la textura. Esto aplica el valor a las splines &#39;in place&#39;,<br>- <b>Horizontal along spline</b>. Los valores se aplican a las coordenadas de las splines codificadas directamente (consulte la entrada <b>Spline Coords</b>), donde cada fila se aplica a una spline diferente de arriba abajo,<br>- <b>Hor. a lo largo de la spline (rand. desplazamiento X)</b> Los valores se aplican a las coordenadas de las splines codificadas directamente (consulte la entrada <b>Spline Coords</b>), con un desplazamiento horizontal aleatorio en el <b>Mapa de rotación</b> para cada spline (es decir, cada fila en <b>Spline Coords</b>).<br>- <b>Hora. a lo largo de la spline (rand. desplazamiento Y)</b> Los valores se aplican a las coordenadas de las splines codificadas directamente (consulte la entrada <b>Spline Coords</b>), con un desplazamiento vertical aleatorio en el <b>Mapa de rotación</b> para cada spline (es decir, cada fila en <b>Spline Coords</b>)<b>.</b> |
| <b>La Entrada De Mapa de rotación Afecta A</b> *Entero* | Selecciona el parámetro de rotación que se ve afectado por el <b>Mapa de rotación</b>:<br><br>- <b>Rotación de spline</b> El mapa afecta a la rotación global de las splines en el sentido de las agujas del reloj.<br>- <b>Ángulo izquierdo/derecho</b> El mapa afecta a la rotación simétrica de las splines <b>izquierda/derecha</b>. |
| <b>Height</b> |  |
| <b>Iniciar modo de Height</b> *Entero* | Método para calcular el height de inicio de las splines dispersas.<br><br>- <b>Manual</b> Establezca el mismo valor absoluto para todas las splines dispersas.<br>- <b>Desde la spline principal (+ spline personalizada)</b> Utilice el height de la spline principal y, a continuación, agregue el height de la spline personalizada utilizando el mult de height <b>Inicio de spline personalizada.</b> parámetro.<br>- <b>Desde spline personalizada</b> Utilice el height de la spline personalizada tal como está.<br><br><i>Nota:</i> Establezca <b>Tipo de spline</b> en &#39;Spline personalizada&#39; y conecte las entradas de <b>Spline personalizada</b> para usar el height de splines personalizadas. |
| <b>Mult. de Height de inicio de spline personalizada</b> *Flotador* | Controla la contribución del propio height inicial de la spline personalizada al height inicial de las splines dispersas, donde 1 significa que se utiliza el height completo de la spline personalizada.<br>El height de la spline personalizada se usa de forma diferente según el <b>Modo de Height de inicio</b>:<br>- <i>De la spline principal (+ spline personalizada):</i> El height se agrega a la spline principal<br>- <i>De la spline personalizada:</i> El height se usa directamente |
| <b>Iniciar desplazamiento de Height</b> *Flotador* | Aplica un desvío absoluto al height inicial de la spline dispersada. |
| <b>Iniciar Height</b> *Flotador* | Establece un valor absoluto para el height inicial de la spline dispersada. |
| <b>Finalizar modo de Height</b> *Entero* | Método para calcular el height final de las splines dispersas.<br><br>- <b>Manual</b> Establezca el mismo valor absoluto para todas las splines dispersas.<br>- <b>Desde la spline principal (+ spline personalizada)</b> Utilice el height de la spline principal y, a continuación, agregue el height de la spline personalizada utilizando el <b>Height de extremo de spline personalizado Mult.</b> parámetro.<br>- <b>Desde spline personalizada</b> Utilice el height de la spline personalizada tal como está.<br><br><i>Nota:</i> Establezca <b>Tipo de spline</b> en Spline personalizada y conecte las entradas de <b>Spline personalizada</b> para utilizar el height de las splines personalizadas. |
| <b>Mult. de Height de fin de spline personalizado</b> *Flotador* | Controla la contribución del propio height final de la spline personalizada al height final de las splines dispersas, donde 1 significa que se utiliza el height completo de la spline personalizada.<br>El height de la spline personalizada se usa de forma diferente según el <b>Modo de Height final</b>:<br>- <i>De la spline principal (+ spline personalizada):</i> El height se agrega a la spline principal<br>- <i>De la spline personalizada:</i> El height se usa directamente |
| <b>Finalizar desplazamiento de Height</b> *Flotador* | Aplica un desplazamiento absoluto al height final de la spline dispersada. |
| <b>Finalizar Height</b> *Flotador* | Define un valor absoluto para el height final de la spline dispersada. |
| <b>Thickness</b> |  |
| <b>Iniciar modo de Thickness</b> *Entero* | Método para calcular el thickness inicial de las splines dispersas.<br><br>- <b>Manual</b> Establezca el mismo valor absoluto para todas las splines dispersas.<br>- <b>De spline principal</b> Utilice el thickness de la spline principal.<br>- <b>De spline personalizada</b> Utilice el thickness de la spline personalizada.<br><br><i>Nota:</i> Establezca <b>Tipo de spline</b> en Spline personalizada y conecte las <b>Entradas de spline personalizada</b> para usar la thickness  de las estrías personalizadas. |
| <b>Iniciar multiplicador de Thickness</b> *Flotador* | Ajusta el thickness inicial de las splines dispersas, donde 1 es el thickness completo. |
| <b>Iniciar desplazamiento de Thickness</b> *Flotador* | Aplica un desvío absoluto al thickness inicial de la spline dispersada. |
| <b>Iniciar Thickness</b> *Flotador* | Establece un valor absoluto para el thickness inicial de la spline dispersada. |
| <b>Finalizar modo de Thickness</b> *Entero* | Método para calcular el thickness final de las splines dispersas.<br><br>- <b>Manual</b> Establezca el mismo valor absoluto para todas las splines dispersas.<br>- <b>De spline principal</b> Utilice el thickness de la spline principal.<br>- <b>De spline personalizada</b> Utilice el thickness de la spline personalizada.<br><br><i>Nota:</i> Establezca <b>Tipo de spline</b> en Spline personalizada y conecte las <b>Entradas de spline personalizada</b> para usar la thickness  de las estrías personalizadas. |
| <b>Finalizar multiplicador de Thickness</b> *Flotador* | Ajusta el thickness inicial de las splines dispersas, donde 1 es el thickness completo. |
| <b>Finalizar desplazamiento de Thickness</b> *Flotador* | Aplica un desplazamiento absoluto al thickness final de la spline dispersada. |
| <b>Finalizar Thickness</b> *Flotador* | Define un valor absoluto para el thickness final de la spline dispersada. |
| <b>Vista previa</b> |  |
| <b>Mostrar ayuda de dirección</b> *Booleano* | Muestra un punto al principio de la spline y una punta de flecha al final en la salida <b>Preview</b>. |
| <b>Mostrar sobre de Thickness</b> *Booleano* | Muestra líneas adicionales en los bordes del thickness de la spline. |
| <b>Thickness (px)</b> *Flotador* | Ajusta el thickness de la visualización de la spline en la salida de <b>Preview</b>, en número de píxeles. |
| <b>Cantidad de segmentos</b> *Entero* | Ajusta el número de segmentos utilizados para dibujar la visualización de spline en la salida de <b>Preview</b>. Un valor más alto produce una línea más suave. |
| <b>Intensidad de fondo</b> *Flotador* | Intensidad de la entrada <b>Preview</b> en la visualización de salida de <b>Preview</b>. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Splines de Dispersión en Splines: Ejemplo 1](scatter-splines-on-splines.resources/scatter-splines-on-splines-03.png "Splines de Dispersión en Splines: Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Splines de Dispersión en Splines: Ejemplo 1](scatter-splines-on-splines.resources/scatter-splines-on-splines-04.png "Splines de Dispersión en Splines: Ejemplo 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Splines de Dispersión en Splines: Ejemplo 3](scatter-splines-on-splines.resources/scatter-splines-on-splines-05.png "Splines de Dispersión en Splines: Ejemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Splines de Dispersión en Splines: Ejemplo 4](scatter-splines-on-splines.resources/scatter-splines-on-splines-06.png "Splines de Dispersión en Splines: Ejemplo 4"){zoomable="yes"}

</td>
</tr>
</table>

## Renderizadores

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Splines de Dispersión en Splines: Procesar 1](scatter-splines-on-splines.resources/scatter-splines-on-splines-07.png "splines de Dispersión en splines: Procesar 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Splines de Dispersión en Splines: Procesar 2](scatter-splines-on-splines.resources/scatter-splines-on-splines-08.png "splines de Dispersión en splines: Procesar 2"){zoomable="yes"}

</td>
</tr>
</table>

![Splines de Dispersión en Splines: Procesar 3](scatter-splines-on-splines.resources/scatter-splines-on-splines-09.png "splines de Dispersión en splines: Procesar 3"){zoomable="yes"}
