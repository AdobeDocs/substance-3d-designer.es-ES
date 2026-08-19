---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/fxmaps.html"
breadcrumb-title: ''
description: Aprenda a utilizar FXMaps en Substance 3D Designer para aplicar gráficos de funciones a texturas para la generación de patrones de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FXMaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---


# FXMaps

**El nodo FX-Map permite la creación de imágenes de procedimiento**. Es una de las características más potentes de la tecnología Substance.

Un FX-Map representa un tipo especial de gráfico, conocido como una cadena Markov. Las cadenas de Markov representan un proceso básico simple: replicar y subdividir repetidamente una imagen una y otra vez. En cada paso, una imagen se puede rotar, traducir y mezclar a voluntad. Los resultados pueden consistir en cualquier cosa, desde patrones sencillos hasta ruidos complejos. FX-Maps son la base de muchos de los Substance de muestra instalados con Substance 3D Designer.

## Creación de gráficos de FX-Map

Si quieres ver un gráfico FX-Map, solo tienes que añadir un [nodo FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) a un [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md), hacer clic con el botón derecho en el nodo y pulsar CMD + E (OS X) o CTRL + E (Windows) para abrir el gráfico. Este gráfico FX-Map aparecerá en una nueva pestaña del panel Gráficos; puede cambiar entre este gráfico y el gráfico del Substance haciendo clic en la pestaña.

## ¿Para qué sirven los FX-Maps?

Los usos más comunes de FX-Maps son la creación de patrones repetitivos, como rayas y ladrillos, y ruidos, como Perlin, Browniano y Gaussiano. Los ruidos son especialmente útiles para crear texturas orgánicas de aspecto natural, como dirt, dust, hormigones, superficies pétreas, salpicaduras de líquidos, etc.

Los gráficos FX-Map no funcionan del mismo modo que los gráficos de Substance: En los gráficos de Substance, cada nodo es independiente y no tiene conocimiento de su posición en el gráfico general, ni le importa de dónde provienen los datos de sus imágenes o hacia dónde van.

Veremos cada uno de los tres nodos del gráfico FX-Map con más detalle en el siguiente capítulo, pero brevemente, cada nodo FX-Map ofrece una de tres operaciones:

### Cuadrante

Esto divide la imagen en este paso del gráfico en cuatro cuadrantes. Este es el tipo de nodo más común. Una cadena de nodos Quadrant puede crear imágenes de aspecto muy complejo, así como patrones complejos.

De hecho, los nodos del cuadrante representan un nivel, o **octava**, en un gráfico de cuatro árboles. Los gráficos FX-Map ocultan esta estructura de árbol representando cada nivel del árbol con un único cuadrante: cada vez que se conecta un nodo de Cuadrante a otro, se está creando un nivel de árbol completo.

La razón de esta técnica de &quot;trampas&quot; es eliminar la necesidad de representar cada nodo en cada nivel de un árbol individualmente: después de solo cuatro capas de profundidad, necesitaría utilizar 4 x 4 x 4 x 4 nodos, que son 256 nodos individuales! En su lugar, cada nodo del Cuadrante &quot;sabe&quot; en qué nivel se encuentra en el árbol y genera sus imágenes en consecuencia.

Probablemente esto no tenga mucho sentido para muchos lectores, pero en breve entraremos en esto con mucho más detalle.

### Iterar

Repite la imagen pasada en el conector de la derecha sobre la imagen pasada en el conector de la izquierda por el número establecido de iteraciones.

Este nodo se suele utilizar con uno o varios gráficos de funciones dinámicas para mover o rotar la imagen de entrada de alguna manera en cada iteración.

### Cambiar

Esto toma dos entradas y simplemente cambia entre una u otra, según se define en su configuración de selector. Al igual que con el nodo Iteración, el ajuste del selector lo elige a menudo una función dinámica.

## Variables del sistema FX-Maps

FX-Maps soporta variables del sistema. Estas variables siempre comienzan con un símbolo de dólar (&quot;$&quot;) y son las siguientes:

| Nombre | Particularidad | Tipo de datos | Propósito |
| --- | --- | --- | --- |
| $time | - | float1 | Esta variable devuelve el tiempo en segundos desde que se inició el motor de procesamiento de Substance.Es ideal para Substance que necesitan animar según el tiempo. (E.g. las agujas de un reloj.)En algunas aplicaciones, incluido Substance Player, un Substance que utilice $time hará que aparezca una cronología en la interfaz de usuario. |
| $profundidad | - | float1 | Devuelve el número de octava (nivel) del nodo FX-Map. Esto permite a un nodo modificar su comportamiento según el nivel del cuádruple árbol que representa. |
| $depthpow2 | - | float1 | Como se ha indicado anteriormente, pero devuelve 2 elevado a la potencia del número de octava (nivel). Se trata de un valor auxiliar que resulta útil para algunos cálculos comunes. |
| $number | Solo iterar nodos | float1 | Devuelve el número del motivo dibujado. Se puede acceder a esto mediante gráficos de funciones dinámicas que controlan un nodo iterado para modificar su comportamiento en cada paso de iteración. (Tenga en cuenta que $number comienza a contar desde 0, no desde 1.) |
| $size | - | float2 | Devuelve el tamaño del nodo actual (en píxeles). |
| $sizelog2 | - | float2 | Como se ha indicado anteriormente, pero devuelve el tamaño como valores de potencia de 2 (por ejemplo: para la imagen 2048\*2048, $sizelog2 devuelve 1). |
| $pos | Sólo nodos de cuadrante | float2 | Devuelve la posición de nacimiento del motivo. El resultado siempre es un valor entre 0 y 1. |
