---
title: Forma salpicaduras v2
description: Designer > Gráficos de composición de Substance > Referencia de nodos para gráficos de composición de Substance > Biblioteca de nodos > Generador > Patrón > Forma salpicadura v2
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '4234'
ht-degree: 0%

---


# Forma salpicaduras v2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de salpicadura de formas v2](shape-splatter-v2.resources/shape-splatter-v2.png "Salpicadura de formas v2")

<b>En:</b> Generador > Patrón

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Dispersión formas en una superficie de height de fondo con funciones avanzadas para su dispersión en un <b>espacio 3D</b> virtual, con controles de posición, rotación, escala y aleatoriedad.<br><br>El nodo ofrece formas 3D primitivas básicas y admite formas personalizadas proporcionadas como <b>imagen de patrón</b>, <b>atlas</b> o como función de <b>campo de distancia firmada (SDF)</b> para formas 3D personalizadas complejas.<br><br>Hay disponibles varios <b>métodos de distribución de formas</b>, incluida la creación de una función personalizada para un control completo.<br><br>Las formas se pueden desplazar hacia áreas específicas mediante un <b>mapa de densidad</b> personalizado.<br><br><i>Nota:</i> Este nodo no está diseñado para usarse con las versiones de CPU del motor del Substance, es decir, SSE2 (Windows, Linux) y NEON (macOS).

</td>
</tr>
</table>

>[!INFO]
>
> Los datos generados por este nodo se pueden utilizar con los demás nodos de la familia Shape splatter v2:
> * [Color del asignador de salpicaduras de formas v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)
> * [Asignador de salpicaduras de formas v2 en escala de grises](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)
> * [Salpicadura de forma v2 para enmascarar](../shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md)
> 
> Los nodos [color de Atlas de cuadrícula](../grid-atlas-color/grid-atlas-color.md) te permiten empaquetar imágenes en un atlas de tamaño personalizado, hasta 16 patrones en celdas de 4*4.

>[!TIP]
>
> La muestra de material [**&#39;Rusty bolt&#39;**](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) está disponible para comenzar con los nodos Shape splatter v2.
> 
> Para obtener más información sobre conceptos y flujos de trabajo que implican Funciones SDF, vaya a la página dedicada: [Trabajando con Funciones SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entradas

|                                      |                                                                                                                                                                                                                                                                                                                                                                  |
|:-------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>height de fondo</b> *Escala de grises* | Mapa de height base en el que se dispersan las formas. Los heightes de cada uno se combinan usando una &#39;mezcla máxima&#39;, donde se usa la más alta de las dos.<br><br>La contribución del height de fondo al height de salida se controla mediante el parámetro <b>Opacidad de entrada de fondo</b>. |
| <b>Mapa de densidad</b> *Escala de grises* | Un mapa en escala de grises que guía el desplazamiento de las formas según su luminancia, en el que las formas se reúnen en sus áreas más brillantes.<br><br>La intensidad del desplazamiento de las formas se controla mediante el parámetro <b>multiplicador de Mapa de densidad</b>. |
| <b>mapa de desplazamiento de Height</b> *Escala de grises* | Mapa de escala de grises cuyos valores se añaden a las formas de forma uniforme según la ubicación de pivotación de las formas.<br><br>La contribución del mapa se controla mediante el parámetro <b>multiplicador de mapa de desplazamiento de Height</b>. |
| <b>mapa de escala de Height</b> *Escala de grises* | Mapa de escala de grises cuyos valores se utilizan como factor para el height de las formas.<br><br>La contribución del mapa se controla mediante el parámetro <b>multiplicador de mapa de escala de Height</b>. |
| <b>Mapa de escala de formas</b> *Escala de grises* | Mapa de escala de grises cuyos valores se utilizan como factor para la escala de las formas.<br><br>La contribución del mapa se controla mediante el parámetro <b>Multiplicador de mapa de escala</b>. |
| <b>Rotación de forma</b> *Escala de grises* | Un mapa de escala de grises cuyos valores se agregan a la rotación 3D de las formas, ajustados por los factores por eje proporcionados por el parámetro <b>multiplicador de mapa de rotación 3D</b>. |
| <b>Mapa de vectores</b> *Color* | Un mapa que describe los vectores de dirección que se pueden usar para controlar la rotación o la posición de las formas, utilizando los siguientes parámetros:<br><br>- <b>desplazamiento de mapa vectorial</b> ajusta el efecto del mapa para mover las formas.<br>- <b>Entrada de rotación de Pendiente</b> se puede establecer en &#39;Mapa vectorial&#39; para usar este mapa para rotar las formas usando los parámetros relacionados. |
| <b>Mapa de máscaras</b> *Escala de grises* | Imagen utilizada para enmascarar formas según el <b>umbral del mapa de máscaras</b>.<br><br>Es decir. se enmascararán las formas situadas en áreas del mapa donde la luminancia esté por debajo de ese umbral. |
| <b>Entrada de patrón 1</b> *Escala de grises* | El mapa de altura para el patrón #1 que está disperso cuando <b>Tipo de patrón</b> está establecido en &#39;Entrada de patrón&#39;.<br><br><i>Sugerencia:</i> Utilice una resolución que esté cerca del tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 2</b> *Escala de grises* | El mapa de altura para el patrón #2 que está disperso cuando <b>Tipo de patrón</b> está establecido en &#39;Entrada de patrón&#39;.<br><br><i>Sugerencia:</i> Utilice una resolución que esté cerca del tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 3</b> *Escala de grises* | El mapa de altura para el patrón #3 que está disperso cuando <b>Tipo de patrón</b> está establecido en &#39;Entrada de patrón&#39;.<br><br><i>Sugerencia:</i> Utilice una resolución que esté cerca del tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 4</b> *Escala de grises* | El mapa de altura para el patrón #4 que está disperso cuando <b>Tipo de patrón</b> está establecido en &#39;Entrada de patrón&#39;.<br><br><i>Sugerencia:</i> Utilice una resolución que esté cerca del tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 5</b> *Escala de grises* | El mapa de altura para el patrón #5 que está disperso cuando <b>Tipo de patrón</b> está establecido en &#39;Entrada de patrón&#39;.<br><br><i>Sugerencia:</i> Utilice una resolución que esté cerca del tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 6</b> *Escala de grises* | El mapa de altura para el patrón #6 que está disperso cuando <b>Tipo de patrón</b> está establecido en &#39;Entrada de patrón&#39;.<br><br><i>Sugerencia:</i> Utilice una resolución que esté cerca del tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 7</b> *Escala de grises* | El mapa de altura para el patrón #7 que está disperso cuando <b>Tipo de patrón</b> está establecido en &#39;Entrada de patrón&#39;.<br><br><i>Sugerencia:</i> Utilice una resolución que esté cerca del tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 8</b> *Escala de grises* | El mapa de altura para el patrón #8 que está disperso cuando <b>Tipo de patrón</b> está establecido en &#39;Entrada de patrón&#39;.<br><br><i>Sugerencia:</i> Utilice una resolución que esté cerca del tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>height de Atlas de cuadrícula</b> *Escala de grises* | La imagen que describe el height de los patrones empaquetados en un atlas.<br><br>Use el parámetro <b>tamaño de Atlas de cuadrícula</b> para especificar el tamaño de cuadrícula del atlas. |
| <b>Atlas de cuadrícula normal</b> *Color* | Imagen que describe las normales de los patrones empaquetados en un atlas.<br><br>Use el parámetro <b>tamaño de Atlas de cuadrícula</b> para especificar el tamaño de cuadrícula del atlas. |

<a name="outputs"></a>

## Salidas

|                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Height</b> | El mapa de altura calculado para las formas dispersas, incluido el height de fondo, si se utiliza y está visible. |
| <b>Color SDF</b> | Los colores de la forma producidos por la <b>Función SDF</b>.<br><br>Use el nodo <a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-color/set-color.md">Establecer color</a> del gráfico de Funciones SDF para definir un color por componente de la forma. |
| <b>Metalidad SDF</b> | Los colores de la forma producidos por la <b>Función SDF</b>.<br><br>Use el nodo <a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-metalness/set-metalness.md">Set metalness</a> en el gráfico de Función SDF para definir un valor de metalness por componente de la forma. |
| <b>Rugosidad SDF</b> | Los colores de la forma producidos por la <b>Función SDF</b>.<br><br>Use el nodo <a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-roughness/set-roughness.md">Establecer rugosidad</a> del gráfico de Funciones SDF para definir un valor de rugosidad por componente de la forma. |
| <b>Normal</b> | Las normales calculadas para las formas dispersas, enmascaradas según la fusión con el height de fondo.<br><br> Si el <b>tipo de forma</b> es &#39;Atlas de cuadrícula&#39;, las normales proporcionadas a la entrada <b>normal de Atlas de cuadrícula</b> se utilizan directamente. |
| <b>Splatter UVW</b> | <b>R</b> - Componente U de las UV de las formas.<br><b>G</b> - Componente V de las UV de las formas.<br><b>B</b> - height de las formas. (W)<br><b>A</b> - Datos empaquetados:<br> - <i>Parte entera:</i> El identificador único de las formas. (Id.)<br> - <i>Parte fraccional:</i> Depende del <b>tipo de forma</b>: Id. de material si SDF/primitivo, id. de patrón* si entrada/atlas de cuadrícula de patrón.<br><br><b>*:</b> El id. de patrón es el índice de la forma en la lista/atlas. |
| <b>Datos de salpicaduras 1</b> | <b>R</b> - Componente X de la posición en la superficie de la forma, en el espacio de objetos.<br><b>G</b> - Componente Y de la posición en la superficie de la forma, en el espacio de objetos.<br><b>B</b> - Componente Z de la posición en la superficie de la forma, en el espacio de objetos.<br><b>A</b> - Datos empaquetados:<br> - <i>Componente entero:</i> Componente U de las coordenadas UV para los datos de las formas en las salidas de datos 2/3.<br> - <i>Parte fraccional:</i> componente V de las coordenadas UV para los datos de las formas en las salidas de datos 2/3.<br> - <i>Firmar:</i> Máscara binaria para la fusión de las formas con el height de fondo. |
| <b>Datos de salpicaduras 2</b> | <b>R</b> - Componente X de la rotación 3D de las formas.<br><b>G</b> - Componente Y de la rotación 3D de las formas.<br><b>B</b> - Componente Z de la rotación 3D de las formas.<br><b>A</b> - Rotación de las formas en torno a su normal.<br><br>Todas las rotaciones se definen en número de vueltas. |
| <b>Datos de salpicaduras 3</b> | <b>R</b> - Componente X de la posición de las formas.<br><b>G</b> - Componente Y de la posición de las formas.<br><b>B</b> - Desplazamiento de las formas a lo largo de su posición normal.<br><b>A</b> - Datos empaquetados:<br> - <i>Parte entera:</i> El identificador único de la forma.<br> - <i>Parte fraccional:</i>El índice del patrón de las formas en su atlas de origen. (Si se utiliza un tipo de patrón de atlas de cuadrícula) |
| <b>Datos de salpicaduras 4</b> | <i>Píxel 1</i><br><b>R</b> - Tamaño X de las imágenes de salida de datos 2/3.<br><b>G</b> - Tamaño Y de las imágenes de salida de datos 2/3.<br><b>B</b> - Tamaño X de la imagen de salida de datos 4.<br><b>A</b> - Tamaño Y de la imagen de salida de datos 4.<br><br><i>Píxel 2</i><br><b>R</b>: el tipo de forma. (E.g. Cubo, cilindro, ...)<br><b>G</b> - Datos empaquetados:<br> - <i>Valor absoluto:</i> Número de entrada del patrón.<br> - <i>Firmar:</i> Formato normal de la asignación normal de salida. (Positivo: DirectX / Negativo: OpenGL)<br><b>B</b>: tamaño X del atlas de cuadrícula. (Es decir, la cantidad de columnas)<br><b>A</b>: tamaño Y del atlas de cuadrícula. (Es decir, la cantidad de filas) |

<a name="parameters"></a>

## Parámetros

|                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Modo de distribución de posiciones</b> *Entero* | Método de distribución de las formas en el espacio:<br><br>- <b>cuadrícula 2D:</b> Una cuadrícula simple uniforme.<br>- <b>disco Poisson:</b> Una simulación que intenta desplazar aleatoriamente las celdas de una cuadrícula para evitar superposiciones mientras se utiliza el espacio disponible.<br>- <b>Uniforme:</b> Una distribución uniforme de un número especificado de formas. Requiere cálculos más intensivos.<br>- <b>Función personalizada:</b> Cree un gráfico de funciones para definir la distribución de las formas. Las variables disponibles se muestran en la descripción del nodo. |
| <b>Función Position</b> *Float2* | Gráfico de funciones utilizado para definir la distribución de las formas.<br><br>El gráfico genera un valor Flotante2 para la posición normalizada XY de las formas de la imagen.<br><br>Variables disponibles:<br> - <code>shape.id</code> (Flotante) El identificador único de la forma.<br> - <code>shape.amount</code> (Flotante) Cantidad de formas especificadas por el parámetro <b>Amount</b>. |
| <b>Importe X</b> *Entero* | Cantidad de columnas en la cuadrícula de distribución.<br><br>Es decir. la cantidad de formas generadas en el eje X. |
| <b>Importe Y</b> *Entero* | Cantidad de filas en la cuadrícula de distribución.<br><br>Es decir. la cantidad de formas generadas en el eje Y. |
| <b>Importe</b> *Entero* | Cantidad de formas generadas. |
| <b>Formato normal de salida</b> *Entero* | Formato del mapa de normales de salida.<br><br>Invierte de forma efectiva el canal verde.<br><br>- <b>DirectX:</b> El eje Y señala hacia arriba.<br>- <b>OpenGL:</b> El eje Y señala hacia abajo. |
| <b>Expansión no cuadrada</b> *Booleano* | En las imágenes no cuadradas, conserva la proporción de formas y expande su generación a los límites de la imagen. |
| <b>Tipo de forma</b> *Entero* | Hay varios tipos de formas disponibles para ser dispersados, cada uno con características específicas.<br><br>La <b>Función SDF</b> es un gráfico de funciones que genera un campo de distancia firmado (SDF) que describe la superficie de una forma 3D. Esto permite la dispersión 3D de formas procedimientas complejas que pueden variar dinámicamente.<br><br><b>Las formas primitivas</b>, calculadas mediante funciones simples de intersección de rayos y superficies, están listas para usarse: cubo, esfera, cilindro, plano, disco<br><br><b>Los patrones de entrada</b> son imágenes proporcionadas por el gráfico. Estos se asignan a planos y se pueden <i>extruir</i> en formas 3D:<br> - Entrada de imagen: Patrones conectados a los pines de entrada <b>Pattern input #</b>.<br> - Atlas de cuadrícula: Los patrones se empaquetan en una imagen atlas conectada a las entradas de <b>Atlas de cuadrícula</b>. |
| <b>Tamaño de Atlas de cuadrícula</b> *Entero2* | Cantidad de filas y columnas del atlas proporcionadas a las entradas de imagen <b>Atlas de cuadrícula</b>.<br><br><i>Nota:</i> Las celdas vacías del atlas producirán huecos en la distribución de formas. |
| <b>Actualizar atlas de cuadrícula normal</b> *Booleano* | Cuando <i>True</i>, se omite el mapa normal proporcionado a la entrada de imagen <b>Atlas de cuadrícula normal</b> y se calculan desde cero las normales de los patrones proporcionados al <b>height de Atlas de cuadrícula</b>.<br><br>Si <i>False</i>, el mapa normal proporcionado al <b>Atlas de cuadrícula normal</b> se usa tal cual.<br><br><i>Nota:</i> La intensidad de las normales se ajusta según el <b>height de extrusión de forma</b>. |
| <b>Formato normal de Atlas de cuadrícula</b> *Entero* | Formato del mapa normal proporcionado para la entrada de imagen <b>Atlas de cuadrícula normal</b>.<br><br>Invierte de forma efectiva el canal verde.<br><br>- <b>DirectX:</b> El eje Y señala hacia arriba.<br>- <b>OpenGL:</b> El eje Y señala hacia abajo. |
| <b>Número de entrada de patrón</b> *Entero* | Cantidad de patrones proporcionados como imágenes de entrada.<br><br>Agrega tantos pines de entrada <b>Pattern #</b> al nodo. |
| <b>Habilitar extrusión de forma</b> *Booleano* | Alterna la extrusión de patrones de entrada interpretándolos como mapas de height, lo que da como resultado formas 3D de procedimiento complejas. |
| <b>Simetría de extrusión de formas</b> *Booleano* | Permite la extrusión simétrica hacia delante/hacia atrás de los patrones de entrada.<br><br>El eje de simetría es el <i>punto intermedio</i> de la extrusión, lo que significa que su ubicación puede cambiar según la posición de pivote de las formas. |
| <b>height de extrusión de formas</b> *Flotador* | Distancia máxima de extrusión en el espacio de imagen, donde 1 es el lado más largo de la imagen.<br><br>Esta distancia se escala en relación con el valor <b>Escala de forma</b>. |
| <b>Muestras de extrusión de forma</b> *Entero* | Cantidad de muestras realizadas para dibujar la extrusión de los patrones de entrada.<br><br>Una cantidad mayor da como resultado extrusiones más suaves y definidas a costa de cierto rendimiento. |
| <b>Función de patrón</b> *Flotador* | El gráfico de funciones del Substance creado se usa para calcular el patrón asignado a un SDF de plano 3D.<br><br>Estos patrones también se pueden extruir usando <b>Habilitar extrusión de forma</b>. |
| <b>Función SDF de motivo</b> *Flotador* | Gráfico de funciones del Substance que crea el campo de distancia firmada (SDF), que describe la superficie de un objeto 3D en el espacio.<br><br>Examine la colección integrada de [Funciones SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) en la biblioteca para crear un objeto complejo combinando varios SDF <i>primitivos</i> con los <i>operadores</i> y <i>transformaciones</i> disponibles.<br><br>Una forma SDF es completamente procedimental y se puede ajustar dinámicamente, lo que puede permitir que cada forma dispersa sea <i>única</i>.<br><br>Use el nodo [3D viewer](../../../filters/effects/3d-viewer/3d-viewer.md) para visualizar el resultado de una Función SDF.<br><br><i>Nota:</i> Para aplicar aleatoriedad en Funciones SDF, use los nodos [Hash](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#random) en lugar de &#39;Random&#39;. |
| <b>Tamaño de fotograma delimitador de SDF</b> *Float3* | Define el tamaño máximo del cuadro delimitador (cuadro B) de la forma SDF, que a su vez se utiliza para calcular su cuadro 2D.<br><br>Las formas sólo se dibujan dentro de los límites de su cuadro 2D y el resto se recorta. |
| <b>Habilitar recorte</b> *Booleano* | Cambia el recorte de patrones, lo que ignora todos los valores por debajo del <b>umbral de recorte</b>. Esto garantiza que solo se utilice la silueta deseada de los motivos. |
| <b>Umbral de recorte</b> *Flotador* | Valor de escala de grises por debajo del cual se recortan los valores de los patrones. Es decir, el valor utilizado como borde de la silueta para los patrones. |
| <b>Flujo de trabajo normalizado</b> *Booleano* | Cuando está activada, habilita el ajuste automático del height de las formas para que <i>conserven sus proporciones originales</i> a medida que se escalan hacia arriba o hacia abajo.<br><br>Cuando está desactivado, el height de las formas se expresa en el rango completo de height de la imagen, independientemente de sus proporciones originales.<br><br>El height de las formas todavía se puede ajustar manualmente mediante los parámetros <b>escala de Height</b>. |
| <b>La escala de forma afecta a la escala de height</b> *Booleano* | Cuando es <i>True</i>, la escala de height de una forma se ajusta a medida que cambia su escala para conservar sus proporciones.<br><br>Cuando es <i>False</i>, la escala de height es independiente de la escala de la forma, lo que produce deformación. |
| <b>escala de Height</b> *Flotador* | Un multiplicador para el height de la forma, donde 1 es el height completo de la forma expresado en el rango de height completo de la imagen del rango de height normalizado de la forma. (Consulte <b>Flujo de trabajo normalizado</b>) |
| <b>Escala de Height aleatoria</b> *Flotador* | Redimensiona aleatoriamente el height de cada forma hasta la proporción especificada, donde 1 significa que el height de una forma puede reducirse completamente a 0. |
| <b>Multiplicador de mapa de escala de Height</b> *Flotador* | Intensidad del <b>mapa de escala de Height</b> proporcionado, donde 1 significa que el valor completo del mapa se multiplica por el height de la forma. |
| <b>Opacidad de entrada en segundo plano</b> *Flotador* | Intensidad de la entrada de <b>height de fondo</b> proporcionada en el mapa de altura final.<br><br>Los heightes de las formas y el fondo se combinan usando una &#39;fusión máxima&#39;, donde se usa la más alta de las dos. |
| <b>Desplazamiento de Height desde el fondo</b> *Flotador* | La proporción del height de fondo que se debe agregar al height de las formas, donde 1 significa que se agrega el height de fondo completo.<br><br>Se puede usar para que las formas &quot;descansen&quot; sobre el height de fondo. |
| <b>Ajustar al fondo</b> *Flotador* | Intensidad de la deformación aplicada al height de las formas para que coincida con el height de fondo por píxel, donde 1 significa una coincidencia exacta.<br><br><i>Nota:</i> Este parámetro no tiene efecto cuando <b>el desplazamiento del Height desde el fondo</b> = 0. |
| <b>pendiente suave del fondo</b> *Flotador* | Intensidad del suavizado aplicado al height de fondo utilizado para los ajustes <b>Desplazamiento de Height desde fondo</b> y <b>Conformar con fondo</b>.<br><br>Esto suaviza las frecuencias de deformación y desplazamiento de height, que pueden ser más duras de lo deseado. |
| <b>desplazamiento de Height</b> *Flotador* | Valor agregado al height de las formas, que da como resultado un desplazamiento recto.<br><br>El valor se expresa en el intervalo de height completo de la imagen. |
| <b>Aleatorio de desplazamiento de Height</b> *Flotador* | Aplica un desplazamiento aleatorio al height de las formas, hasta el valor especificado.<br><br>El valor se expresa en el intervalo de height completo de la imagen. |
| <b>Desplazamiento de Height desde ID</b> *Flotador* | El desplazamiento aplicado al height de las formas según su índice en la distribución, donde el desplazamiento aumenta linealmente de una forma a la siguiente hasta el valor especificado.<br><br>El valor se puede establecer manualmente más allá de <code>[0, 1]</code> rango. |
| <b>Multiplicador de mapa de desplazamiento de Height</b> *Flotador* | Ajusta la intensidad del desplazamiento aplicado por el <b>mapa de desplazamiento de Height</b> utilizando el factor especificado, donde 1 significa que los valores de intensidad del mapa se aplican tal cual.<br><br>El height de toda la forma se desplaza agregando el valor en el mapa de desplazamiento en su ubicación de tabla dinámica XY.<br><br>El valor del multiplicador se puede establecer manualmente más allá de <code>[0, 1]</code> rango. |
| <b>Modo de tamaño</b> *Entero* | El método para definir el tamaño de las formas dispersas:<br><br>- <b>Automático:</b> El tamaño se expresa como un factor del tamaño de celda de la forma.<br>- <b>Absoluto (espacio de textura):</b> El tamaño se expresa como un factor del lado más largo de la imagen. |
| <b>Mantener proporción de tamaño</b> *Booleano* | Ajusta el tamaño de las formas para conservar sus proporciones originales en cuadrículas no cuadradas y tamaños de imagen. |
| <b>Escala de forma</b> *Flotador* | El tamaño de la forma como factor definido por el <b>modo Tamaño</b>.<br><br><i>Nota:</i> Al utilizar la distribución de <b>disco Poisson</b>, al ajustar el tamaño de las formas se mueven para aprovechar el espacio disponible. Utilice el parámetro <b>Shape scale post Poisson</b> para escalar formas en su lugar. |
| <b>Escala de forma aleatoria</b> *Flotador* | Reduce las formas en un factor aleatorio hasta el valor especificado, donde 1 puede hacer que algunas formas se reduzcan hasta el tamaño cero. |
| <b>Multiplicador de mapa de escala</b> *Flotador* | La intensidad de multiplicar los valores del <b>mapa de escala de forma</b> por el tamaño de las formas. |
| <b>Poste de escala de forma Poisson</b> *Flotador* | Factor de escala aplicado después de la simulación de disco de Poisson. |
| <b>Tamaño de forma</b> *Float3* | Separe los factores de escala por eje para ajustar el tamaño de las formas. |
| <b>Tamaño de forma aleatorio</b> *Float3* | Reduce las formas en un factor aleatorio <i> por eje</i> hasta el valor especificado, donde 1 puede hacer que algunas formas se reduzcan hasta el tamaño cero. |
| <b>Radio del cilindro</b> *Flotador* | El radio de los SDF de los cilindros dispersos. El radio se expresa como un factor definido por el <b>modo Tamaño</b>. |
| <b>Tamaño de forma</b> *Float2* | Separe los factores de escala por eje para ajustar el tamaño de las formas. |
| <b>Tamaño de forma aleatorio</b> *Float2* | Reduce las formas en un factor aleatorio <i> por eje</i> hasta el valor especificado, donde 1 puede hacer que algunas formas se reduzcan hasta el tamaño cero. |
| <b>Posición aleatoria</b> *Flotador* | Aplica un desplazamiento aleatorio en los ejes XY hasta el valor especificado, donde 1 es la longitud del lado más largo de la imagen. |
| <b>Posicionar multiplicador aleatorio</b> *Float2* | Factores independientes por eje para el desplazamiento aleatorio aplicado a las formas en los ejes XY. |
| <b>Secuencia de distribución de posiciones</b> *Entero* | Algoritmo utilizado para distribuir las formas uniformemente en el espacio. <br><br>- <b>R2</b>: Basado en la proporción de oro. Es rápido y ofrece distribuciones más uniformes y aparentemente aleatorias independientemente de la cantidad de formas.<br>- <b>Halton</b>: Basado en números primos. Proporciona excelentes resultados para distribuciones dispersas, pero se ralentiza y puede dar lugar a líneas visibles a medida que aumenta la cantidad de formas.<br><br>Estos algoritmos se conocen como <i>quasirandom</i> y <i>low-discrepancy</i>, en el sentido de que siguen una secuencia determinista (quasirandom) destinada a cubrir un espacio de manera uniforme (poca discrepancia). |
| <b>Multiplicador de Mapa de densidad</b> *Flotador* | Un factor de desplazamiento aplicado a las formas para que se reúnan en las áreas más brillantes del <b>Mapa de densidad</b>. |
| <b>Desplazamiento normal</b> *Flotador* | Desplaza las formas a lo largo de su eje Z normal, es decir, su eje Z local. |
| <b>Desplazamiento aleatorio normal</b> *Flotador* | Añade una cantidad aleatoria de desplazamiento a las formas a lo largo de su forma normal.<br><br>La cantidad aleatoria puede ser positiva o negativa hasta el valor especificado o hasta su valor negativo. |
| <b>desplazamiento de mapa vectorial</b> *Flotador* | Factor del desplazamiento aplicado a las formas agregando los valores de RGB en el <b>mapa vectorial</b> a las coordenadas XYZ de la forma respectivamente.<br><br>El desplazamiento se expresa como un factor del lado más largo de la imagen.<br>P.ej. un valor de RGB de (0,5, 0,5, 0) desplaza las formas a la mitad de su tamaño a lo largo de los ejes X e Y.<br><br>Un valor de parámetro de 1,0 significa que se agrega el valor completo. |
| <b>Multiplicador de desplazamiento vectorial</b> *Float3* | Ajusta el <b>desplazamiento de mapa de vectores</b> por un factor independiente por eje, donde 0.0 significa que no se aplica ningún desplazamiento en ese eje. |
| <b>Desplazamiento global</b> *Float2* | Se aplica un desplazamiento a la posición de cada forma <i>después de</i> cualquier desplazamiento de height, desplazamientos aleatorios y otros desplazamientos.<br><br>Esto significa que al mover las formas con este parámetro no se modificará su posición, orientación ni escala. |
| <b>Desplazamiento de posición de línea</b> *Flotador* | Un desplazamiento aplicado a las líneas de formas de la cuadrícula según el modo de desplazamiento de posición de línea <b>Line position offset mode.</b> |
| <b>Modo de desplazamiento de posición de línea</b> *Entero* | Método para aplicar el <b>desplazamiento de posición de línea</b> a las formas.<br><br>Los métodos <b>All</b> aplican el desplazamiento como factor del lado más largo de la imagen (es decir, en el espacio de textura).<br>- <b>All - Horizontal:</b> Agrega gradualmente el valor de desplazamiento fila por fila horizontalmente, por un factor del índice de fila.<br>- <b>All - Vertical:</b> Agrega gradualmente el valor de desplazamiento columna por columna verticalmente, por un factor del índice de columna.<br><br>Los métodos <b>Quincunx</b> aplican el desplazamiento como un factor del tamaño de celda de las formas.<br>- <b>Quincunx - Horizontal:</b> Agrega el valor de desplazamiento uniformemente cada dos filas.<br>- <b>Quincunx - Vertical:</b> Agrega el valor de desplazamiento uniformemente cada dos columnas. |
| <b>Posición de pivote (local)</b> *Float3* | Ajusta la posición del giro en el espacio local de la forma, lo que afecta al origen de las transformaciones. (Es decir, desplazamiento de posición, rotación y escala)<br><br>Por ejemplo, ajuste la posición de pivote Z para que las formas giren alrededor de su base. |
| <b>Rotación 3D</b> *Float3* | Aplica un giro por eje de manera uniforme a todas las formas, en número de vueltas. |
| <b>rotación 3D aleatoria</b> *Flotador* | Factor de la cantidad aleatoria de rotación aplicada a las formas hasta el valor especificado, en el sentido de las agujas del reloj o en el sentido contrario a las agujas del reloj, en número de vueltas. |
| <b>Multiplicador aleatorio de rotación 3D</b> *Float3* | Ajusta la cantidad de rotación aleatoria aplicada por <b>rotación 3D aleatoria</b> mediante un factor independiente por eje. |
| <b>Multiplicador de mapa de rotación 3D</b> *Float3* | Intensidad con la que los valores del mapa de <b>rotación de forma</b> se agregan al giro por eje de cada forma, donde 1 significa la cantidad total de giro. |
| <b>Rotación alrededor de lo normal</b> *Flotador* | Cantidad de rotación aplicada uniformemente a todas las formas alrededor de su eje Z normal en número de vueltas. |
| <b>Rotación aleatoria normal</b> *Flotador* | Aplica una rotación aleatoria a cada forma alrededor de su eje normal (es decir, su eje Z local) en el sentido de las agujas del reloj o en el sentido contrario a las agujas del reloj, hasta un giro completo. |
| <b>Rotación de Pendiente</b> *Flotador* | Gira las formas para que coincidan con la pendiente del fondo en su ubicación.<br>Es decir, aplica una rotación igual a la del vector Z-up global a la normal del height de fondo.<br><br>Este parámetro es un factor para esta rotación, donde 1 significa que se aplica la rotación completa.<br><br>Este giro se agrega a otras rotaciones que se pueden aplicar a las formas. |
| <b>Entrada de rotación de Pendiente</b> *Entero* | Origen de la pendiente utilizada para controlar la <b>rotación de la Pendiente</b>.<br><br>- <b>Fondo:</b> Se usa la textura del height de fondo, la normal calculada a partir de ese mapa de height es la dirección de destino para la rotación.<br>- <b>Mapa de vectores:</b> Los vectores especificados por la textura del mapa de vectores se usan tal cual para la dirección de destino de la rotación.</b> |
| <b>Multiplicador de mapa vectorial</b> *Flotador* | Gira las formas alrededor del eje especificado por el <b>eje de rotación del mapa vectorial</b> para que coincidan con la dirección de los vectores descritos por la textura del <b>mapa vectorial</b>.<br>Es decir, aplica una rotación igual a la del vector global X-right a los vectores de la textura.<br><br>Este parámetro es un factor para esta rotación, donde 1 significa que se aplica la rotación completa.<br><br>Este giro se agrega a otras rotaciones que se pueden aplicar a las formas. |
| <b>Eje de rotación del mapa vectorial</b> *Entero* | Eje alrededor del cual se debe realizar la rotación especificada por el <b>mapa vectorial</b>.<br><br>- <b>Normal:</b> Rota las formas según su valor normal, de manera similar al uso del parámetro &#39;Rotación según normal&#39;.<br>- <b>Eje Z:</b> Rota las formas alrededor del eje Z global, de forma similar a usar el componente Z del parámetro &#39;Rotación 3D&#39;. |
| <b>Máscara aleatoria</b> *Flotador* | Oculta la proporción especificada de la cantidad total de formas en una secuencia aleatoria, donde 1 significa que todas las formas están ocultas.<br><br>Este parámetro se combina con el mapa de máscara. (Si se utiliza) |
| <b>Umbral de mapa de máscara</b> *Flotador* | Valor de escala de grises en el <b>mapa de máscara</b> debajo del cual están ocultas las formas.<br><br>El mapa se combina con el parámetro <b>Mask random</b>. |
| <b>Escala de UV</b> *Float2* | Un multiplicador por eje para las UV de las formas, donde el mosaico aumenta con los valores. |
| <b>Escala de UV de mayúsculas</b> *Float2* | Un multiplicador por eje para las UV de las tapas del cilindro, donde el mosaico aumenta con los valores. |
| <b>Modo UV de mayúsculas</b> *Entero* | Método para calcular las UV de las tapas del cilindro.<br><br>- <b>Polar:</b> Utilice coordenadas polares en las que U aumente alrededor del eje Z del cilindro y V aumente a medida que se aleja de él.<br>- <b>Planar:</b> Utilice una proyección plana en la que las UV se asignen mediante el cuadro delimitador de las tapas (es decir, un rectángulo ajustado al tamaño de las tapas) |
| <b>Mostrar cuadro 2D de forma</b> *Booleano* | Superpone una visualización del rectángulo delimitador de la forma en la imagen. Esta es el área en la que se dibujan las formas. |
| <b>Mostrar cuadro 3D de forma</b> *Booleano* | Superpone una visualización del volumen delimitador de la forma en el espacio 3D. Esta es la zona en la que se dibujan las formas SDF y los planos extruidos.<br><br>Para formas SDF, esta área coincide con el <b>tamaño de fotograma delimitador SDF</b>.<br><br>Esta visualización ayuda a evaluar el alcance y la orientación de la forma. |
| <b>Mostrar tabla dinámica de formas</b> *Booleano* | Superpone una visualización de la pivotación de formas, como una combinación de sus vectores de eje XYZ locales.<br><br>Esta visualización ayuda a evaluar la orientación de la forma y el origen de sus transformaciones. (Es decir, desplazamiento, rotación, escala) |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-poisson.gif" /><br><i>Distribución de Poisson</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-uniform.gif" /><br><i>Distribución uniforme</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-density-map.gif" /><br><i>Mapa de densidad</i>
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-rotation.gif" /><br><i>Rotación 3D aleatoria</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-background-slope.gif" /><br><i>Rotación de Pendiente</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-shape-extrusion.gif" /><br><i>Extrusión de formas</i>
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-sdf.jpg" /><br><i>Formas 3D SDF</i>
        </td>
        <td style="border: 0; background: transparent">
        </td>
        <td style="border: 0; background: transparent">
        </td>
    </tr>
</table>

