---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/fxmaps/the-quadrant-node.html"
breadcrumb-title: ''
description: Utilice el nodo Cuadrante en FXMaps para dividir las texturas en cuatro secciones y crear motivos en mosaico y variaciones.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Quadrant Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: El nodo del cuadrante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---


# El nodo del cuadrante

Muchos FX-Maps consiste enteramente de cadenas de nodos de Cuadrante. Los nodos Quadrant son el nodo más potente y flexible en el grupo FX-Map, por lo que vale la pena entender cómo funciona este nodo.

Lo más importante de los nodos Quadrant es que son el único nodo que puede aumentar la profundidad o *octava* del gráfico FX-Map. Cada nodo Cuadrante se agrega al gráfico de cuatro árboles subyacente; ninguno de los otros nodos lo hace.

El nodo Cuadrante tiene una serie de parámetros:

## Color/Luminosidad

Cuando el nodo está añadiendo una imagen al FX-Map, estos ajustes definen cómo se mezclan los canales con otras imágenes de la cadena. Los parámetros *Color / Luminosidad* se aplican a cualquier imagen representada por este nodo en particular.

### Desplazamiento de rama

Desplaza la imagen del nodo. El desplazamiento se aplica a todas las demás imágenes procesadas por los nodos posteriores del gráfico. El Desplazamiento de rama aplica la conversión al nodo Cuadrante actual y a todos los nodos situados debajo de él en la misma rama del gráfico.

Este parámetro se puede controlar con una función dinámica.

### Patrón

Define la imagen (si la hay) que este nodo agregará al FX-Map.

Los nodos del cuadrante admiten una larga lista de patrones, que se describen más adelante en este tema.

>[!WARNING]
>
> Este parámetro no se puede controlar mediante una función dinámica en un archivo sbsar.

### Desplazamiento de patrón

Desplaza la imagen del nodo en la cantidad especificada, pero no afecta a los nodos posteriores. Este parámetro se puede controlar con una función dinámica.

### Tamaño de patrón

Define el tamaño de la imagen (si corresponde) que se añadirá al mapa FX. Este parámetro se puede controlar con una función dinámica.

### Rotación de patrón

Define la rotación de la imagen (si corresponde) que se añadirá al mapa de efectos. Este parámetro se puede controlar con una función dinámica.

### Variación de patrón

Algunos patrones tienen variantes. Este ajuste le permite elegir qué variante utilizar. Este parámetro se puede controlar con una función dinámica.

### Modo de fusión

Especifica el proceso de fusión que se va a utilizar al mezclar la imagen de este nodo (si procede) con la imagen FX-Map. Este parámetro se puede controlar con una función dinámica.

### Grano aleatorio

Semilla para el generador de números aleatorios.

El generador utiliza esta semilla como punto de partida, creando una secuencia de lo que parecen ser números aleatorios. La ventaja de este enfoque es que, a diferencia del mundo real, puedes asegurarte de que se genera la misma secuencia exacta de números aleatorios cada vez, lo que produce resultados predecibles, repetibles, pero de aspecto aleatorio.

Este parámetro se puede controlar con una función dinámica.

### Heredar aleatorio

Si se establece en &quot;Sí&quot;, la semilla del generador de números aleatorios se hereda del nodo anterior en el gráfico (es decir, el nodo sobre este en el árbol cuádruple). Si este es el primer nodo, toma su semilla aleatoria del gráfico [Substance](../../../compositing-graphs/substance-compositing-graphs.md) que lo contiene.

## Motivos

Cada nodo del Cuadrante puede añadir opcionalmente una imagen al FX-Map final.

De forma predeterminada, la opción Sin motivo está seleccionada, por lo que no se procesa ninguna imagen. El nodo Cuadrante simplemente subdivide la imagen FX-Map, dividiéndola en cuatro para el siguiente nodo de la cadena.

La siguiente opción, *Input image*, es usar una imagen suministrada al nodo FX-Map. El nodo FX-Map acepta imágenes en color o en escala de grises para su uso como fondo o como sustitución de uno de los patrones integrados. Tenga en cuenta que el nodo Cuadrante solo puede procesar una imagen de entrada de escala de grises en un mapa de efectos de escala de grises y, a la inversa, solo puede procesar una imagen de entrada de color en un mapa de efectos de color. Si desea mezclar el tipo de color, debe convertir las entradas antes en el gráfico.

Por último, puede elegir uno de los motivos integrados: Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espinoso, Pirámide, Ladrillo, Gradación, Ondas, Media Campana, Campana Redondeada, Media Luna y Cápsula.

Nota adicional: tiene la posibilidad de crear una función dinámica en este parámetro, pero solo funcionará en Substance 3D Designer. Para tener acceso a la entrada de imagen mediante una función dinámica, deberá utilizar valores de 256 (entrada de imagen 1) a valores superiores (257 para entrada de imagen 2, etc.).

### Tipos de patrones.

Todos los patrones son en escala de grises. Algunas se pueden modificar un poco con el parámetro *Pattern Variation*.

Muchos de los patrones incorporados tienen algún tipo de relleno de degradado radial o similar. Esto los hace muy útiles para muchos tipos de ruidos y patrones. Otros patrones, como Ladrillo, Disco y Cuadrado, son formas simples y planas.

El parámetro Variación de patrón ajusta una función definida del patrón.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/fxmap-quadrants.png){width="80px"}

</td>
<td style="border: 0;" valign="top">

![](../../../assets/quadrant-parameters.jpg)

</td>
</tr>
</table>
