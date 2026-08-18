---
title: Dispersión de forma v2 en máscara
description: Designer > Gráficos de composición de Substance > Referencia de nodos para gráficos de composición de Substance > Biblioteca de nodos > Generador > Patrón > Forma de salpicaduras v2 para enmascarar
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---


# Dispersión de forma v2 en máscara

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Salpicadura de forma v2 para enmascarar el icono](shape-splatter-v2-to-mask.png "Salpicadura de forma v2 para enmascarar")

<b>En:</b> Generador > Patrón

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Calcula una máscara a partir de una selección de formas generadas por el nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).<br><br>Las opciones disponibles incluyen la selección aleatoria, así como la selección de rangos de formas mediante un identificador único o un identificador de material/identificador de patrón*.<br><br>El nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) preenmascara las formas a partir de su <i>mezcla de heightes</i> con el height de fondo.<br>Tanto el fondo como las formas no seleccionadas son negro puro. (Es decir, un valor de 0)<br><br><b>*:</b> Uno de los valores recuperados de la entrada Shape splatter UVW es el identificador de material o el identificador de patrón, según el <b>tipo de forma</b> utilizado en el nodo Shape splatter v2:<br>- <i>SDF/primitive</i>: Id. de material<br>- <i>Entrada/Atlas de cuadrícula de patrón:</i> Id. de patrón, es decir, el índice del patrón en la lista/atlas.

</td>
</tr>
</table>

>[!INFO]
>
> Este nodo requiere datos de entrada generados por el nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).
> 
> Otros nodos de la familia Shape splatter v2:
> * [Asignador de salpicaduras de formas v2 en escala de grises](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)
> * [Color del asignador de salpicaduras de formas v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)

>[!TIP]
> 
> La muestra de material [**&#39;Rusty bolt&#39;**](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) está disponible para comenzar con los nodos Shape splatter v2.
> 
> Para obtener más información sobre conceptos y flujos de trabajo que implican Funciones SDF, vaya a la página dedicada: [Trabajando con Funciones SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entradas

|                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:----------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Splatter UVW</b> *Color* | <b>R</b> - Componente U de las UV de las formas.<br><b>G</b> - Componente V de las UV de las formas.<br><b>B</b> - height de las formas. (W)<br><b>A</b> - Datos empaquetados:<br> - <i>Parte entera:</i> El identificador único de las formas. (Id.)<br> - <i>Parte fraccional:</i> Depende del <b>tipo de forma</b>: Id. de material si SDF/primitivo, id. de patrón* si entrada/atlas de cuadrícula de patrón.<br><br><b>*:</b> El id. de patrón es el índice de la forma en la lista/atlas. |

<a name="outputs"></a>

## Salidas

|               |                                           |
|:--------------|:------------------------------------------|
| <b>Salida</b> | La máscara calculada de las formas seleccionadas. |

<a name="parameters"></a>

## Parámetros

|                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Salida</b> *Entero* | Los valores utilizados para las formas seleccionadas en la máscara de salida.<br><br>- <b>Máscara binaria:</b> Todas las formas seleccionadas usan un valor de 1.<br>- <b>Id. de forma (entero):</b> Las formas seleccionadas usan su identificador único. (Id.)<br>- <b>Id. de material (entero):</b> Las formas seleccionadas usan su Id. de material.<br>- <b>Id. de forma (normalizado):</b> Las formas seleccionadas usan su Id. único asignado al intervalo [0, 1] desde el Id. seleccionado más bajo hasta el más alto.<br>- <b>Id. de material (normalizado):</b> Las formas seleccionadas usan su Id. de material asignado al intervalo [0, 1] desde el Id. de material seleccionado más bajo hasta el más alto. |
| <b>Intervalo de inicio del identificador de forma</b> *Entero* | El identificador único de forma (ID) utilizado como inicio del intervalo de selección. (Incluido) |
| <b>Intervalo final de Id. de forma</b> *Entero* | Identificador único de forma (ID) utilizado como final del intervalo de selección. (Incluido) |
| <b>Desplazamiento de Id. de forma</b> *Entero* | Desplaza los identificadores únicos de las formas por el valor especificado, en el contexto del intervalo de selección.<br><br>Esto facilita el desplazamiento de la selección actual por el valor especificado sin tener que ajustar manualmente los límites inicial y final. |
| <b>Combinación de máscara de id. de material/patrón</b> *Entero* | Se ha especificado el operador lógico utilizado para combinar la selección mediante un identificador único (ID) con la selección mediante el identificador de material/identificador de patrón.<br><br>- <b>Ninguno:</b> Omitir el identificador de material/identificador de patrón por completo para la selección.<br>- <b>Y:</b> Las formas seleccionadas deben incluirse en los intervalos de identificador e identificador de material/identificador de patrón. (Incluye menos formas)<br>- <b>O:</b> Las formas seleccionadas deben incluirse en los intervalos ID. o ID. de material/ID. de patrón. (Incluye más formas) |
| <b>Intervalo de inicio de material/ID de patrón</b> *Entero* | El ID de material o el ID de patrón* utilizado como inicio del intervalo de selección. (Incluido)<br><br><b>*:</b> Consulte la descripción del nodo para obtener más información. |
| <b>Intervalo final de material/ID de patrón</b> *Entero* | El ID de material o el ID de patrón* utilizado como final del intervalo de selección. (Incluido)<br><br><b>*:</b> Consulte la descripción del nodo para obtener más información. |
| <b>Máscara aleatoria de formas</b> *Flotador* | Un factor para el enmascaramiento aleatorio de formas, donde 1 significa que todas las formas están enmascaradas. |

