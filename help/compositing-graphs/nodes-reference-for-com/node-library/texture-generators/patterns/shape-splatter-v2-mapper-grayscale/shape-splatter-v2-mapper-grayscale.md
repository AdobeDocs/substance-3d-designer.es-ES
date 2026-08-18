---
title: Escala de grises del asignador de salpicaduras de formas v2
description: Designer > Gráficos de composición de Substance > Referencia de nodos para gráficos de composición de Substance > Biblioteca de nodos > Generador > Patrón > Escala de grises del asignador de salpicaduras de formas v2
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '1766'
ht-degree: 0%

---


# Escala de grises del asignador de salpicaduras de formas v2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de escala de grises del asignador de salpicaduras de formas v2](./shape-splatter-v2-mapper-grayscale.resources/shape-splatter-v2-mapper-grayscale.png "Asignador de salpicaduras de formas v2 de escala de grises")

<b>En:</b> Generador > Patrón

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Asigna imágenes en escala de grises en formas generadas y dispersas mediante el nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) , utilizando los datos adicionales proporcionados por el nodo.<br><br>Las imágenes se proporcionan como entradas de patrones independientes o se empaquetan en un atlas de cuadrícula, y se pueden aplicar a las formas mediante la asignación UV, la proyección triplanar o la asignación personalizada.<br><br>Las formas se pueden teñir y su luminancia se puede ajustar de manera uniforme o aleatoria por forma.

Consulte también [Color del asignador de salpicaduras de formas v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md).

</td>
</tr>
</table>

>[!INFO]
>
> Este nodo requiere datos de entrada generados por el nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).
> 
> Otros nodos de la familia Shape splatter v2:
> * [Salpicadura de forma v2 para enmascarar](../shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md)
>
> Los nodos [Atlas de cuadrícula grayscale](../grid-atlas-grayscale/grid-atlas-grayscale.md) te permiten empaquetar imágenes en un atlas de tamaño personalizado, hasta 16 patrones en celdas 4*4.

>[!TIP]
> 
> La muestra de material [**&#39;Rusty bolt&#39;**](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) está disponible para comenzar con los nodos Shape splatter v2.
> 
> Para obtener más información sobre conceptos y flujos de trabajo que implican Funciones SDF, vaya a la página dedicada: [Trabajando con Funciones SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entradas

|                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Entrada de Atlas de cuadrícula</b> *Escala de grises* | Imagen en escala de grises de motivos agrupados en un diseño de cuadrícula.<br><br>El tamaño de cuadrícula debe coincidir con el que usa el nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).<br><br>Usa el nodo [Atlas de cuadrícula grayscale](../grid-atlas-grayscale/grid-atlas-grayscale.md) para empaquetar patrones separados en un atlas de cuadrícula. |
| <b>Entrada de patrón 1</b> *Escala de grises* | Imagen en escala de grises para el patrón #1 asignado a las formas.<br><br><i>Sugerencia:</i> Utilice una resolución cercana al tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 2</b> *Escala de grises* | Imagen de escala de grises para el patrón #2 que está asignado a las formas.<br><br><i>Sugerencia:</i> Utilice una resolución cercana al tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 3</b> *Escala de grises* | Imagen de escala de grises para el patrón #3 que está asignado a las formas.<br><br><i>Sugerencia:</i> Utilice una resolución cercana al tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 4</b> *Escala de grises* | Imagen en escala de grises para el patrón #4 que está asignado a las formas.<br><br><i>Sugerencia:</i> Utilice una resolución cercana al tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 5</b> *Escala de grises* | Imagen en escala de grises para el patrón #5 que está asignado a las formas.<br><br><i>Sugerencia:</i> Utilice una resolución cercana al tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 6</b> *Escala de grises* | Imagen en escala de grises para el patrón #6 que está asignado a las formas.<br><br><i>Sugerencia:</i> Utilice una resolución cercana al tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 7</b> *Escala de grises* | Imagen en escala de grises para el patrón #7 que está asignado a las formas.<br><br><i>Sugerencia:</i> Utilice una resolución cercana al tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada de patrón 8</b> *Escala de grises* | Imagen en escala de grises para el patrón #8 que está asignado a las formas.<br><br><i>Sugerencia:</i> Utilice una resolución cercana al tamaño máximo que puede tener el patrón cuando está disperso. |
| <b>Entrada en segundo plano</b> *Escala de grises* | Imagen de escala de grises utilizada como fondo para las formas asignadas. |
| <b>Entrada de color</b> *Escala de grises* | Imagen en escala de grises utilizada para teñir las formas asignadas según su posición de pivote.<br><br>Use el parámetro <b>Opacidad de entrada de color</b> para ajustar la intensidad de la contribución de estos colores al color de las formas. |
| <b>Normal</b> *Color* | Las normales calculadas para las formas dispersas, enmascaradas según la fusión con el height de fondo.<br><br> Si el <b>tipo de forma</b> es &#39;Atlas de cuadrícula&#39;, las normales proporcionadas a la entrada <b>normal de Atlas de cuadrícula</b> se utilizan directamente. |
| <b>Splatter UVW</b> *Color* | <b>R</b> - Componente U de las UV de las formas.<br><b>G</b> - Componente V de las UV de las formas.<br><b>B</b> - height de las formas. (W)<br><b>A</b> - Datos empaquetados:<br> - <i>Parte entera:</i> El identificador único de las formas. (Id.)<br> - <i>Parte fraccional:</i> Depende del <b>tipo de forma</b>: Id. de material si SDF/primitivo, id. de patrón* si entrada/atlas de cuadrícula de patrón.<br><br><b>*:</b> El id. de patrón es el índice de la forma en la lista/atlas. |
| <b>Datos de salpicaduras 1</b> *Color* | <b>R</b> - Componente X de la posición en la superficie de la forma, en el espacio de objetos.<br><b>G</b> - Componente Y de la posición en la superficie de la forma, en el espacio de objetos.<br><b>B</b> - Componente Z de la posición en la superficie de la forma, en el espacio de objetos.<br><b>A</b> - Datos empaquetados:<br> - <i>Componente entero:</i> Componente U de las coordenadas UV para los datos de las formas en las salidas de datos 2/3.<br> - <i>Parte fraccional:</i> componente V de las coordenadas UV para los datos de las formas en las salidas de datos 2/3.<br> - <i>Firmar:</i> Máscara binaria para la fusión de las formas con el height de fondo. |
| <b>Datos de salpicaduras 2</b> *Color* | <b>R</b> - Componente X de la rotación 3D de las formas.<br><b>G</b> - Componente Y de la rotación 3D de las formas.<br><b>B</b> - Componente Z de la rotación 3D de las formas.<br><b>A</b> - Rotación de las formas en torno a su normal.<br><br>Todas las rotaciones se definen en número de vueltas. |
| <b>Datos de salpicaduras 3</b> *Color* | <b>R</b> - Componente X de la posición de las formas.<br><b>G</b> - Componente Y de la posición de las formas.<br><b>B</b> - Desplazamiento de las formas a lo largo de su posición normal.<br><b>A</b> - Datos empaquetados:<br> - <i>Parte entera:</i> El identificador de la forma.<br> - <i>Parte fraccional:</i>El índice del patrón de las formas en su atlas de origen. (Si se utiliza un tipo de patrón de atlas de cuadrícula) |
| <b>Datos de salpicaduras 4</b> *Color* | <i>Píxel 1</i><br><b>R</b> - Tamaño X de las imágenes de salida de datos 2/3.<br><b>G</b> - Tamaño Y de las imágenes de salida de datos 2/3.<br><b>B</b> - Tamaño X de la imagen de salida de datos 4.<br><b>A</b> - Tamaño Y de la imagen de salida de datos 4.<br><br><i>Píxel 2</i><br><b>R</b>: el tipo de forma. (E.g. Cubo, cilindro, ...)<br><b>G</b> - Datos empaquetados:<br> - <i>Valor absoluto:</i> Número de entrada del patrón.<br> - <i>Firmar:</i> Formato normal de la asignación normal de salida. (Positivo: DirectX / Negativo: OpenGL)<br><b>B</b>: tamaño X del atlas de cuadrícula. (Es decir, la cantidad de columnas)<br><b>A</b>: tamaño Y del atlas de cuadrícula. (Es decir, la cantidad de filas) |

<a name="outputs"></a>

## Salidas

|               |                     |
|:--------------|:--------------------|
| <b>Salida</b> | Las formas coloreadas. |

<a name="parameters"></a>

## Parámetros

|                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Modo de proyección</b> *Entero* | Método para proyectar las imágenes de entrada en las formas:<br><br>- <b>UV de salpicaduras:</b> Utilice las UV proporcionadas por el nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).<br>- <b>Triplanar:</b> Utilice la proyección triplanar para asignar las imágenes en los ejes XYZ locales de las formas.<br>- <b>Función personalizada:</b> Cree un gráfico de funciones para definir la asignación de las imágenes a las formas. |
| <b>Función personalizada</b> *Flotador* | Especifica la luminancia por píxel de las formas como flotante.<br><br>Están disponibles las siguientes variables:<br>- <code>shape.position.os</code> (Float3) Posición de la superficie de la forma en el espacio de objetos.<br>- <code>shape.position.ws</code> (Float3) Posición de la superficie de forma en el espacio de entorno*.<br>- <code>shape.normal.os</code> (Float3) Valores normales de la superficie de la forma en el espacio de objetos.<br> - <code>shape.normal.ws</code> (Float3) Valores normales de la superficie de forma en el espacio de entorno*.<br>- <code>shape.id</code> (Float) Identificador único de la forma.<br>- <code>material.id</code> (Float) Id. de material de la superficie de forma, definida por el nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).<br><br>*: El espacio de mundo de la forma se centra en su giro y no tiene en cuenta el height de la forma. Esto significa que la única diferencia con el espacio del objeto es la orientación.<br><br>Si es necesario muestrear las entradas del nodo [Shape splatter v2 mapper grayscale](shape-splatter-v2-mapper-grayscale.md), se pueden usar estas ranuras de entrada de nodo [Sample grayscale](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md):<br>- 0: Atlas de cuadrícula<br>-1-8: Entrada de patrón 1-8 |
| <b>Contraste de fusión</b> *Flotador* | Nitidez de las transiciones entre las proyecciones planas, donde 1 significa que no hay degradado de transición. |
| <b>Proyección de imágenes</b> *Entero* | Cantidad de imágenes <b>Pattern input #</b> distribuidas en las proyecciones planas que contribuyen a la asignación triplanar.<br><br>Para cubrir todos los lados de una forma, se realiza una proyección plana frontal (+) y posterior (-) en cada eje, con un total de 6 proyecciones.<br><br>- <b>1 imagen:</b> La entrada de patrón 1 se usa para todas las proyecciones planas.<br>- <b>3 imágenes:</b> Se usa una entrada de patrón independiente para la proyección +/- de cada eje.<br>- <b>6 imágenes:</b> Cada proyección usa una entrada de patrón independiente.<br>- <b>1 imagen por material ID:</b> entrada de patrón independiente por ID de material, donde cada imagen se utiliza para todas las proyecciones planas. |
| <b>Centro de proyección</b> *Float3* | Desplaza la proyección triplanar por eje, en el espacio del objeto.<br><br>El desplazamiento se aplica a <i>todo el espacio de proyección</i>, por lo que un desplazamiento en un eje afectará la posición de las texturas proyectadas en los <i>otros dos</i> ejes. |
| <b>Escala de proyección</b> *Flotador* | Ajusta la escala de las texturas proyectadas en <i>todos los ejes</i>, según el factor especificado. |
| <b>Modo de selección de entrada</b> *Entero* | El método para seleccionar las imágenes de entrada que se deben asignar a las formas.<br><br>El <b>tipo de forma</b> seleccionado en el nodo de origen [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) cambia la forma de asignar imágenes a las formas:<br><br>- <b>Atlas de cuadrícula</b> significa que las imágenes se obtienen en la &#39;entrada de Atlas de cuadrícula&#39; mediante índices de cuadrícula coincidentes (ambos atlas deben usar el mismo tamaño de cuadrícula)<br>- <b>Entrada de patrón</b> significa que las imágenes se obtienen en las entradas de &#39;Entrada de patrón #&#39; mediante índices coincidentes.<br>- <b>Otros tipos de formas:</b> imágenes se asignan mediante la coincidencia de entradas índices a los identificadores de material de la forma.<br><br>Los métodos disponibles para seleccionar los índices son:<br>- <b>De datos de salpicaduras:</b> Coincidir los índices de las imágenes de &#39;Entrada de patrón #&#39; o &#39;Entrada de Atlas de cuadrícula&#39; con los índices de las formas asignadas por el nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).<br>- <b>Manual:</b> Usar el índice especificado por el parámetro &#39;Índice de imagen&#39;.<br>-<b>Aleatorio: 25} Utilice un índice aleatorio en el rango especificado por el parámetro &#39;Rango aleatorio&#39;.</b> |
| <b>Número de entrada de patrón</b> *Entero* | Cantidad de imágenes de entrada <b>Pattern input #</b> que se deben asignar a las formas. |
| <b>Índice de imagen</b> *Entero* | Índice del patrón de entrada de <b>Patrón de entrada #</b> o <b>entrada de Atlas de cuadrícula</b> que se debe asignar a las formas. |
| <b>Intervalo aleatorio</b> *Entero2* | Intervalo de índices de <b>entrada de patrón #</b> o <b>entrada de Atlas de cuadrícula</b> en los que el patrón se debe seleccionar aleatoriamente para asignarlo a las formas. |
| <b>Ajuste de luminancia</b> *Flotador* | Un desplazamiento aplicado uniformemente a la luminancia de todas las formas. |
| <b>Luminancia aleatoria</b> *Flotador* | Desplazamiento aleatorio positivo o negativo aplicado a la luminancia de las formas, hasta los valores especificados. |
| <b>Opacidad de entrada de color</b> *Flotador* | Intensidad de la contribución de <b>Color input</b> a los colores de las formas, según el <b>modo de fusión de entrada de color</b> seleccionado. |
| <b>Modo de fusión de entrada de color</b> *Entero* | Operación de fusión de color utilizada para combinar las imágenes de primer plano y de fondo.<br><br>Estas operaciones son idénticas a sus equivalentes en el nodo [Blend](../../../../atomic-nodes/blend/blend.md).<br><br>Modos disponibles:<br>- <b>Copiar</b><br>- <b>Agregar (sobreexposición lineal)</b><br>- <b>Restar</b><br>- <b>Multiplicar</b><br>- <b>Superposición</b> |
| <b>Modo de segmentación</b> *Entero* | Ejes a lo largo de los cuales se debe repetir la textura:<br> - <b>Sin mosaico</b><br> - <b>Mosaico horizontal</b><br> - <b>Mosaico vertical</b><br> - <b>Mosaico H y V</b>: Mosaico combinado horizontal y vertical. |
| <b>Mosaico UV</b> *Flotador* | Ajusta el mosaico global de las imágenes asignadas a las formas<br><br>Los valores más altos dan como resultado más repeticiones. |
| <b>Escala de UV</b> *Float2* | Ajusta el mosaico de las imágenes asignadas a las formas según el factor especificado, con controles independientes para la escala U y V. Los valores más altos producen más repeticiones. |
| <b>Desplazamiento de UV</b> *Float2* | Aplica un desplazamiento a la asignación de imágenes entre las formas, lo que permite un ajuste preciso de la posición de las imágenes en las formas.<br><br>Este desplazamiento se agrega al <b>desplazamiento aleatorio</b>, si lo hay. |
| <b>Desplazamiento aleatorio</b> *Flotador* | Aplica una cantidad aleatoria de desplazamiento positivo o negativo <i>por forma</i> a la asignación de imágenes entre las formas, hasta el valor especificado.<br><br>Este desplazamiento se agrega al <b>Desplazamiento de UV</b>, si lo hay. |

