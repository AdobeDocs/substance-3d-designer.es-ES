---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/inheritance-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Descubra cómo funciona la herencia en Substance que componen gráficos para crear jerarquías y variaciones de gráficos reutilizables.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Inheritance in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Herencia en gráficos de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1681'
ht-degree: 0%

---


# Herencia en gráficos de Substance

En esta página se describe cómo se aplica la herencia en [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) en [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) y el impacto que tiene en la salida del gráfico.

![Métodos de herencia](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-01.jpg "Métodos de herencia"){width="1400px"}

## Información general

Todos los nodos de un gráfico de Substance pueden *heredar* el valor de algunos parámetros de un origen. La herencia significa que al cambiar el valor en el origen *se llevará a cabo ese cambio* en todos los nodos que heredan de él. Este es uno de los conceptos fundamentales que sustentan el poder de Substance 3D Designer para generar activos paramétricos.

>[!NOTE]
>
> Hay disponible un archivo de proyecto anotado que muestra la herencia en la sección [Gráficos de Substance de muestra](../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) de esta documentación.

### Métodos de herencia

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Icono del método de herencia &#39;Absolute&#39;](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-02.png "Icono del método de herencia &#39;Absolute&#39;"){width="128px"}

<b>Absoluto</b>

Sin herencia, el valor se define *arbitrariamente y localmente* para el parámetro

</td>
<td style="border: 0;" valign="top">

![Icono para el método de herencia &#39;Relativo a la entrada&#39;](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-03.png "Icono para el método de herencia &#39;Relativo a la entrada&#39;"){width="128px"}

<b>Relativo a la entrada</b>

El valor se ha heredado de los datos conectados a la *entrada principal* del nodo

</td>
<td style="border: 0;" valign="top">

![Icono para el método de herencia &#39;Relativo al principal&#39;](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-04.png "Icono para el método de herencia &#39;Relativo al principal&#39;"){width="128px"}

<b>Relativo al primario</b>

El valor se ha heredado del *elemento principal* del nodo o gráfico

</td>
</tr>
</table>

![Demostración de métodos de herencia](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-05.gif "Demostración de métodos de herencia")

Los métodos de herencia se aplican para los [parámetros base](../../compositing-graphs/graph-parameters/graph-parameters.md) de un nodo, que es el conjunto de parámetros comunes que tienen todos los nodos que controlan *aspectos fundamentales* de su comportamiento. Estos parámetros incluyen:

* **Tamaño de salida**
* **Formato de salida** (es decir, profundidad de bits)
* **Tamaño de píxel**
* **Proporción de píxeles**
* **Modo de segmentación**
* **Raíz aleatoria**

Esto debería permitirte apreciar cómo los cambios en *un nodo* pueden afectar a la resolución, precisión y comportamiento de mosaico de *todos los nodos aguas abajo* del nodo.

>[!WARNING]
>
> Un recordatorio importante para comprender los conceptos tratados en esta página: un *nodo de instancia* es un [nodo que representa un gráfico en otro gráfico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), con sus *propios valores de parámetros discretos*, de ahí el término *instancia*.\
> Por ejemplo, dos nodos [Ruido Perlin](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/perlin-noise/perlin-noise.md) en un mismo gráfico son representaciones de un gráfico de origen *same* (`perlin_noise` en `noise_perlin_noise.sbs`) con sus *conjuntos propios* de valores de parámetro.

>[!NOTE]
>
> **Tamaño de salida:** Use el botón de bloqueo ![](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-06.jpg) para que el valor de Height *coincida* con el valor de ancho\
> **Raíz aleatoria:** Utilice el botón ![](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-07.jpg) para asignar un nuevo valor aleatorio a la semilla aleatoria.

## Realización de cambios

### Cambio de métodos de herencia

En el panel Propiedades, todos los parámetros enumerados en la sección [Parámetros base](../../compositing-graphs/graph-parameters/graph-parameters.md) de las propiedades de un nodo tienen un botón desplegable (icono) <b>Establecer método de herencia</b> frente a su etiqueta.\
Este botón le permite seleccionar el método de herencia que debe utilizarse para un parámetro.

![Cambiando método de herencia](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-08.gif "Cambiando método de herencia"){width="512px"}

En la mayoría de los casos, los parámetros Base de *node* se establecen en *Relative to input*, para aprovechar el comportamiento procedimental de encadenar nodos juntos, mientras que los parámetros Base de *graph* se establecen en *Relative to parent*, de modo que los parámetros globales se puedan adaptar al contexto en el que se usa el gráfico.

### AJUSTE DE VALORES HEREDADOS

Algunos parámetros base, como [Tamaño de salida](../../compositing-graphs/output-size/output-size.md), Tamaño de píxel o Raíz aleatoria, se pueden cambiar *con relación al valor heredado*.

Por ejemplo, cuando el parámetro Tamaño de salida usa un valor *Relativo a...El método de herencia*, un valor o `(1, -1)` significa una potencia de dos resoluciones *encima* del valor heredado para X y una potencia de dos resoluciones *debajo* del valor heredado para Y como:

* Valor heredado : `(9, 9)` que es `2^9, 2^9 = 512, 512`
* Valor relativo: `(1, -1)` que es `2^(9+1), 2^(9-1) = 256, 1024`

>[!NOTE]
>
> La página [Tamaño de salida](../../compositing-graphs/output-size/output-size.md) profundiza en este parámetro Base crítico y se recomienda leerlo para comprender cómo se calcula la resolución final de un nodo.

Si se aplica una función a un parámetro Base, el resultado de la función también se interpretará utilizando el método de herencia del parámetro.\
Teniendo en cuenta el ejemplo de tamaño de salida, una función cuyo objetivo es aumentar la resolución heredada dos veces en X e Y debe generar el valor de entero `(2, 2)` 2.

## Paternidad para nodos y gráficos

Al utilizar el método de herencia Relativa al padre, debe comprender exactamente qué es ese padre en un contexto específico.

El elemento primario de un nodo es el *gráfico* en el que existe.

El elemento principal de un gráfico es el *contexto* en el que existe:

* Si ese gráfico es un subgráfico instanciado en otro gráfico de host como *nodo de instancia*, el principal del subgráfico es el *nodo de instancia*. El nodo principal de esa instancia es el *gráfico de host*.
* Si ese gráfico es un gráfico raíz, entonces el principal es la *aplicación en sí* y cualquier valor que la aplicación haya establecido para un parámetro dado. Por ejemplo, los gráficos heredarán del parámetro <b>Parent Size</b> establecido en la barra de herramientas de la vista de gráfico [Graph view](../../interface/the-graph-view/the-graph-view.md).

>[!WARNING]
>
> La asociación se *aplica tal cual* al publicar un paquete en archivos de recursos de Substance 3D (SBSAR). Esto significa que si se establece cualquier parámetro en el método de herencia *Absolute*, se *bloqueará* ese parámetro con su valor actual en el activo publicado.\
> Si bien esto es deseable para [nodos Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) o [propósitos de optimización](../../best-practices/performance-optimization/performance-optimization-guidelines.md), por ejemplo, *recomendamos encarecidamente* el uso de métodos de herencia *Relativo a...* al trabajar en gráficos de Substance, a menos que haya un *propósito claro y deliberado* al hacer lo contrario.

### EDICIÓN EN CONTEXTO

Al usar [Edición en contexto](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) en un nodo de instancia de gráfico, el elemento principal del gráfico es *el nodo de instancia*. En ese caso, el valor <b>Tamaño principal</b> de la barra de herramientas de la [vista de gráfico](../../interface/the-graph-view/the-graph-view.md) está *deshabilitado*, ya que el gráfico hereda sus parámetros base del nodo de instancia.

Este rasgo es el *punto* de la edición en contexto y se debe *tener en cuenta* al establecer el método de herencia y evaluar los valores actuales de los parámetros Base de cualquier nodo.

## Herencia con varias entradas

Cuando un gráfico tiene varias entradas, cada entrada puede heredar de sus datos de entrada discretos o del gráfico, dependiendo de su método de herencia:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Icono para el método de herencia &#39;Relativo a la entrada&#39;](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-03.png "Icono para el método de herencia &#39;Relativo a la entrada&#39;"){width="128px"}

<b>Relativo a la entrada</b>

La entrada hereda de sus datos de entrada discretos, independientemente de los parámetros Base del gráfico. Esto resulta muy útil para controlar los datos por entrada.

</td>
<td style="border: 0;" valign="top">

![Icono para el método de herencia &#39;Relativo al principal&#39;](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-04.png "Icono para el método de herencia &#39;Relativo al principal&#39;"){width="128px"}

<b>Relativo al primario</b>

La entrada se hereda del gráfico y los datos que recibe se adaptan en consecuencia.

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

### Entrada principal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Color de entrada principal/escala de grises](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-09.png){width="48px"}

</td>
<td style="border: 0;" valign="top">

![Color de entrada principal](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-10.png){width="48px"}

</td>
<td style="border: 0;" valign="top">

![Escala de grises de entrada principal](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-11.png){width="48px"}

</td>
</tr>
</table>

Una de las entradas se puede establecer como **entrada principal** del gráfico; para ello, haz clic en **RMB** en ese nodo [Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) y selecciona la opción **Set as Primary Input** en el menú contextual.

</td>
<td style="border: 0;" valign="top">

![Tipos de conector de entrada](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-12.jpg "Tipos de conector de entrada")

</td>
</tr>
</table>

Cuando el gráfico se instancie en otro gráfico como un nodo de instancia, todos los parámetros Base del nodo de instancia establecidos en *Relativo a la entrada* heredarán los datos conectados a *esa entrada*. La entrada principal de un nodo de instancia se puede identificar por el pequeño punto oscuro de su conector.

Las demás entradas establecidas en *Relativo al primario* heredarán los mismos valores de parámetros base, ya que heredan del *gráfico* que hereda del *nodo de instancia\**, que hereda de la entrada principal.

\*: Esto es cierto si el gráfico usa el método de herencia* Relativo al principal*.

## Ejemplos

A continuación se muestran algunos ejemplos que cubren diferentes casos de herencia y la interacción de los métodos de herencia establecidos en los siguientes actores, de arriba abajo:

1. Aplicación
1. Gráfico de host
1. Nodo de instancia en el gráfico de host
1. Subgráfico: es decir, el gráfico al que hace referencia el nodo de la instancia
1. Nodos en subgráfico

El *método de herencia* establecido para un actor se muestra en color naranja justo encima de él. El *flujo de herencia* a su origen se muestra con líneas naranjas.

Las letras representan *conjuntos separados* de parámetros base y deben ayudar a determinar qué datos heredó cada actor.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

**Ejemplo A**

![Diagrama de herencia A](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-13.png "Diagrama de herencia A"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

**Ejemplo B**

![Diagrama de herencia B](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-14.png "Diagrama de herencia B"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

**Ejemplo C**

![Diagrama de herencia C](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-15.png "Diagrama de herencia C"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

**Ejemplo D**

![Diagrama de herencia D](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-16.png "Diagrama de herencia D"){zoomable="yes"}

</td>
</tr>
</table>

## Solución de problemas de herencia

A medida que crea el gráfico y aumenta su complejidad, es posible que encuentre resultados inesperados causados por la herencia. Si el resultado de un nodo tiene una resolución o precisión incorrectas (es decir, profundidad de bits), debe *en la cadena de herencia* para identificar de dónde vienen estos valores.

Un buen punto de partida es comprobar los datos que se muestran justo debajo de un nodo: estos son la resolución, el formato de color y la precisión del resultado de la imagen en el *primer resultado* del nodo. Aunque entender la resolución es sencillo, el segundo dato merece la pena detallarlo:

* El *prefijo de letra* hace referencia al formato de color de la imagen:
  * <b>L</b>: Luminancia (es decir, escala de grises)
  * <b>C</b>: Color
* El *número* hace referencia a la profundidad de bits de la imagen, desde la precisión más baja hasta la más alta:
  * <b>8</b>: Entero de 8 bits (256 pasos en 0-1)
  * <b>16</b>: Entero de 16 bits (65 536 pasos en 0-1)
  * <b>16F</b>: Punto flotante de 16 bits (valores de baja precisión superiores a 0-1, incluidos los negativos)
  * <b>32F</b>: Punto flotante de 32 bits (valores de alta precisión más allá del 0-1, incluidos los negativos)

Si el nodo tiene más de una salida, puede comprobar su resolución y precisión de dos maneras sencillas:

* Haga doble clic en <b>LMB</b> en el *conector de salida* para mostrar la imagen en la [vista 2D](../../interface/2d-view/2d-view.md) y compruebe la información de la imagen que se muestra en la *esquina inferior izquierda* del área de visualización de la vista 2D
* Cree un nodo [Levels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) o [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) y conecte su entrada a la salida que desee comprobar. El nodo *heredará de la salida* de forma predeterminada y, a continuación, puede comprobar los valores debajo del nodo.

Ahora puedes subir por la cadena de nodos en el gráfico e intentar encontrar el *primer nodo* donde aparecen los valores inesperados. Compruebe el método de herencia de sus parámetros Base.

Si no hay ningún problema y el nodo es un nodo de instancia, debe profundizar y abrir el gráfico al que hace referencia ese nodo de instancia. Repita el proceso comenzando desde los nodos Salida del gráfico y continuando hacia arriba.

### UN EJEMPLO COMÚN

En particular, el concepto de *entrada principal* se *pasa por alto* y puede provocar problemas de herencia.

El nodo [Blend](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) es muy susceptible a esto, ya que se usa con mucha frecuencia. Su entrada <b>Background</b> es su entrada principal.

![Herencia de tamaño de salida](inheritance-in-substance-compositing-graphs.resources/inheritance-in-substance-compositing-graphs-17.jpg "Herencia de tamaño de salida"){width="512px"}

Debe prestar atención al orden en que se mezclan las dos entradas: la entrada cuya resolución y precisión desea mantener hacia abajo en el gráfico debe estar conectada a la entrada Fondo, si el modo de fusión que necesita lo hace posible. Si no es así, es posible que deba ajustar los parámetros base del nodo de fusión y su método de herencia para compensar.
