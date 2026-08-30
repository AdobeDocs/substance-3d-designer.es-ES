---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Utilice el nodo Atlas scatter para realizar dispersiones de texturas en un atlas y así crear patrones en mosaico a partir de materiales escaneados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 7%

---


# Atlas scatter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](atlas-scatter.resources/atlas-scatter.png){width="200px"}

<b>En:</b> Filtros de material > Procesamiento de escaneo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Extrae elementos de un atlas y dispersión sobre un fondo. Las entradas de Atlas son materiales completos, compuestos de elementos individuales dispuestos y empacados en una sola hoja de textura. Este nodo los divide (mediante un proceso [Atlas splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md) interno) y los dispersión, de forma similar a [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md). Atlas scatter requiere como mínimo una entrada de mapa de opacidad y una entrada de mapa de Height para que funcione el sistema Atlas.

</td>
</tr>
</table>

>[!NOTE]
>
> Cientos de [Atlas](https://source.substance3d.com/allassets?assetType=substanceAtlas), listos para su uso en el nodo de Atlas scatter, están disponibles en [Substance Source](https://source.substance3d.com/).

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Resolución de entrada de Atlas</b> <i>Resolución, 1 a 12</i> | Establezca manualmente la resolución del atlas de entrada completo para garantizar una buena relación rendimiento/calidad. |
| <b>Cantidad X</b> <i>1 - 64</i> | Cantidad de X repeticiones del patrón. |
| <b>Importe Y</b> <i>1 - 64</i> | Cantidad de repeticiones Y del patrón. |
| <b>Patrón</b> |  |
| <b>Intervalo de patrones</b> <i>0 - 10</i> | Define el rango de patrones que se van a dispersar. Si se establece en 0, se utilizarán todos los patrones. |
| <b>Modo de distribución de patrones</b> <i>Aleatorio, Índice de motivo, Índice de línea, Índice de columna</i> | Define el orden en el que se utilizan los elementos del atlas. |
| <b>Multiplicador de mapa de distribución de patrones</b> <i>0.0 - 1.0</i> | Seleccione el patrón de forma en función del valor de escala de grises de la imagen de entrada. |
| <b>Rotación de motivo</b> <i>0, 90, 180, 270</i> | Aplica una rotación fija a cada elemento del atlas en función de la cantidad de grados seleccionada. |
| <b>Aleatorio de rotación de motivo</b> <i>0.0 - 1.0</i> | Aplica una rotación aleatoria a la parte definida de los elementos del atlas. |
| <b>Precisión de detección de formas en Atlas</b> <i>Formas simples o pequeñas, Formas complejas o grandes, Modo sin errores</i> | Establece la precisión con la que se detectan las formas. Cuanto mayor sea la precisión, mayor será el impacto en el rendimiento. |
| <b>Opacidad de Atlas de escala baja (detección más rápida)</b> <i>-4 - 0</i> | Permite controlar la proporción de disminución de escala del mapa de opacidad del atlas de entrada, que se utiliza para la detección de formas. Una resolución más baja mejora el rendimiento a costa de la precisión. |
| <b>Omitir forma menor que</b> <i>0.0 - 1.0</i> | Define el tamaño mínimo que debe detectarse una forma, expresado como proporción de la imagen global |
| <b>Tamaño</b> |  |
| <b>Escala</b> <i>0.0 - 5.0</i> | Establece la escala relativa de las formas dispersas. |
| <b>Escala aleatoria</b> <i>0.0 - 1.0</i> | Define el multiplicador para aplicar una escala aleatoria a cada forma dispersada. |
| <b>Escalar sin superposición</b> <i>0.0 - 1.0</i> | Reduce la escala de la forma para que no se superpongan. |
| <b>Multiplicador de mapa de escala</b> <i>0.0 - 1.0</i> | Multiplica la escala de la forma en función del valor de escala de grises de la imagen de entrada. |
| <b>Tamaño</b> <i>0.0 - 1.0</i> | Establece la escala relativa de las formas dispersas por longitud (X) y anchura (Y). |
| <b>Proporción de tamaño de la Pendiente grande</b> <i>0.0 - 1.0</i> | Modifica la proporción de tamaño de la forma en función de la pendiente de height de fondo. |
| <b>Conservar proporción</b> <i>0.0 - 1.0</i> | Determina en qué medida se deben conservar las proporciones originales de las formas dispersas, en lugar de utilizar la proporción de celdas de cuadrícula, es decir, la proporción de los valores Cantidad X e Cantidad Y. |
| <b>Posición</b> |  |
| <b>Posición aleatoria</b> <i>0.0 - 2.0</i> | Un multiplicador para mover cada forma en una dirección aleatoria desde su punto inicial de cuadrícula. |
| <b>Distribución aleatoria</b> <i>Gaussiano, uniforme</i> | Cambia de una distribución gaussiana a una distribución uniforme para la posición aleatoria. La distribución gaussiana producirá un resultado más orgánico en comparación con la distribución Uniforme. |
| <b>Multiplicador de mapa vectorial</b> <i>0.0 - 1.0</i> | Controla la influencia de la entrada del mapa vectorial para mover las formas en la dirección del vector especificado por los canales rojo (X) y verde (Y) del mapa. |
| <b>Desplazamiento horizontal</b> <i>-2.0 - 2.0</i> | Un multiplicador para el desplazamiento de posición a lo largo del eje X. |
| <b>Desplazamiento vertical</b> <i>-2.0 - 2.0</i> | Un multiplicador para el desplazamiento de posición a lo largo del eje Y. |
| <b>Opción Fuera de los límites</b> <i>Escalar forma, Restringir posición</i> | Debido a la naturaleza técnica de la salpicadura, las formas no pueden dibujarse a más de 2 celdas de su tamaño original. Si una forma se vuelve demasiado grande o se mueve demasiado lejos, tiene dos opciones: - Escalar forma reducirá el tamaño de la forma cuando llegue a un límite - Restringir posición moverá la forma de nuevo a su posición original |
| <b>Rotación</b> |  |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Permite controlar la rotación local de todas las formas. |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Un multiplicador para una cantidad aleatoria de rotación aplicada por forma. |
| <b>Rotación desde Pendiente grande</b> <i>0.0 - 1.0</i> | Modifica el giro de la forma en función de la pendiente de height de fondo. Normalmente se utiliza en combinación con el parámetro &quot;Proporción de tamaño de la Pendiente Bg&quot; |
| <b>Multiplicador de Mapa de rotación</b> <i>0.0 - 1.0</i> | Multiplica el giro de la forma en función del valor de escala de grises de la imagen de entrada. |
| <b>Multiplicador de mapa vectorial</b> <i>0.0 - 1.0</i> | Establece el giro de la forma en función de la entrada de imagen vectorial. |
| <b>Height</b> |  |
| Ajuste automático de la escala de Height <b>Scale</b> <i>Falso/Verdadero</i> | Ajusta automáticamente el height en función de la escala del motivo para mantener el height de la forma proporcional al height del fondo. |
| <b>Modo de fusión</b> <i>Fusión de Height, prueba de Alpha</i> | Establece el método para resolver superposiciones de formas. |
| <b>Desplazamiento de Height</b> <i>-1.0 - 1.0</i> | Aplica un desplazamiento global al height de formas |
| <b>Aleatorio de desplazamiento de Height</b> <i>0.0 - 1.0</i> | Un multiplicador para un desplazamiento de height aleatorio aplicado por forma |
| <b>Multiplicador de mapa de desplazamiento de Height</b> <i>0.0 - 1.0</i> | Multiplica el desplazamiento del height de forma en función del valor de escala de grises de la imagen de entrada. |
| <b>Escala de Height</b> <i>0.0 - 1.0</i> | Permite controlar la escala de height global de las formas dispersas |
| <b>Escala aleatoria de Height</b> <i>0.0 - 1.0</i> | Un multiplicador para una escala de height aleatoria aplicada por forma |
| <b>Multiplicador de mapa de escala de Height</b> <i>0.0 - 1.0</i> | Multiplica la escala de height de la forma en función del valor de escala de grises de la imagen de entrada. |
| <b>Ajustar al fondo</b> <i>0.0 - 1.0</i> | En 0, el height de forma permanece intacto, en 1 el height de forma se deformará por el fondo del height subyacente. |
| <b>Fondo conformado suave</b> <i>0.0 - 2.0</i> | Permite controlar la cantidad de suavizado aplicado a la deformación de height de la forma cuando se ajusta a su fondo. |
| <b>Sesgar desde Pendiente grande</b> <i>0.0 - 1.0</i> | Deforma el height de forma en función de la pendiente de height de fondo local: se agrega al height de forma un degradado lineal correspondiente a la pendiente de fondo. |
| <b>Smoothness de Pendiente de fondo</b> <i>0.0 - 2.0</i> | Controla la cantidad de suavizado aplicado a la pendiente de fondo cuando la forma se sesga en función de esa pendiente. |
| <b>Píxeles negros recortados</b> <i>Falso/Verdadero</i> | Ignora el valor negro de las entradas de patrón. |
| <b>Acoplar base de patrones</b> <i>Falso/Verdadero</i> | Permite acoplar el height de fondo debajo de una forma para que coincida con su height inicial. |
| <b>Enmascaramiento</b> |  |
| <b>Aleatorio de máscara</b> <i>0.0 - 1.0</i> | Enmascara una cantidad aleatoria de formas, expresada como proporción de la cantidad total. |
| <b>Multiplicador de mapa aleatorio de máscara</b> <i>0.0 - 1.0</i> | Define la máscara de forma aleatoria en función de la entrada de imagen de escala de grises. |
| <b>Máscara de la Pendiente Big</b> <i>-1.0 - 1.0</i> | Controla el enmascaramiento de las formas en función de la pendiente del fondo en su ubicación. |
| <b>Color</b> |  |
| <b>Ajuste de color</b> <i>-1.0 - 1.0</i> | Permite ajustar los colores de los elementos dispersos de forma global. |
| <b>Aleatorio de color</b> <i>0.0 - 1.0</i> | Un multiplicador para cambiar los valores de color en una cantidad aleatoria por forma. |
| <b>Color de fondo</b> <i>0.0 - 1.0</i> | Cambia los colores de la forma al color del fondo en su ubicación. |
| <b>Normal</b> |  |
| <b>Sesgar desde Pendiente grande</b> <i>0.0 - 1.0</i> | Sesgar la forma normal de acuerdo con el fondo normal. |
| <b>Aleatorio normal</b> <i>0.0 - 1.0</i> | Un multiplicador para sesgar la forma normal en una cantidad aleatoria por forma. |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambiar entre diferentes Formatos de mapa de normales (invierte el canal verde) |
| <b>Rugosidad</b> |  |
| <b>Ajuste de rugosidad</b> <i>-1.0 - 1.0</i> | Permite desplazar la rugosidad de la forma global. |
| <b>Rugosidad del fondo</b> <i>0.0 - 1.0</i> | Desplaza la rugosidad de las formas a la rugosidad del fondo en su ubicación. |
| <b>Aleación de rugosidad</b> <i>0.0 - 1.0</i> | Un multiplicador para compensar la rugosidad en una cantidad aleatoria por forma. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="atlas-scatter.resources/atlas-scatter-11.png" />
        </td>
    </tr>
</table>
