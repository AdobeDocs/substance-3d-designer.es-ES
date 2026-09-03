---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/graph-creation-etiquette.html"
breadcrumb-title: ''
description: Descubre las prácticas recomendadas y la etiqueta para crear gráficos de Substance para garantizar flujos de trabajo limpios, mantenibles y eficientes.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Graph Creation Etiquette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Etiqueta de creación de gráficos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 0%

---


# Etiqueta de creación de gráficos

La creación de gráficos grandes y complejos puede resultar confusa y difícil de navegar rápidamente. Se pueden usar varias herramientas para aliviar estos problemas, y hay algunos buenos hábitos a los que entrar, para evitar problemas más adelante. Esta página proporciona una lista concluyente de técnicas que recomendamos usar para gráficos limpios, eficientes y funcionales que se compartan y comprendan fácilmente.

## General

### Organización de gráficos

#### Elementos de gráfico

Los elementos gráficos son objetos auxiliares que se pueden colocar junto a los nodos y alrededor de ellos en [la vista gráfica](../../interface/the-graph-view/the-graph-view.md). De los tres, el Marco proporciona las ventajas más rápidas y grandes, mientras que el Pin Comentario y Navegación son más adecuados para escenarios específicos.

#### Marcos

La primera cosa que conduce a gráficas más limpias y fáciles de leer es la colocación de Marcos alrededor de los grupos centrales de la gráfica. Sin Marcos, un gráfico grande es casi ilegible, e incluso los gráficos pequeños se vuelven mucho más fáciles de entender una vez que se dibujan los marcos. Una gran ventaja de los Marcos es que sus <b> nombres siempre se representan a la misma escala</b>, incluso si se aleja mucho.

![Marcos en Substance](graph-creation-etiquette.resources/graph-creation-etiquette-01.gif "Marcos en Substance")

Los marcos facilitan en gran medida la comprensión de lo que está sucediendo en una gráfica. Pueden ayudarle como autor volviendo a su trabajo meses más tarde, o como otro usuario, como un compañero, a encontrar su camino alrededor de un Gráfico al que no están acostumbrados.

Utilice los siguientes criterios al colocar Marcos:

* Identifique **fragmentos de funcionalidad** (por ejemplo, 8 nodos que juntos crean un efecto de dirt) y agrúpalos usando Marcos.
* Intenta siempre **usar diferentes colores** para tus Marcos: Los marcos con el mismo color azul predeterminado no se distinguen mucho entre sí.
* Utilice **nombres descriptivos claros** que no sean demasiado largos (consulte la sección siguiente para obtener más sugerencias)
* No pongas **demasiado o muy poco** en un Marco, ya que esto no ayuda a la legibilidad. La cantidad exacta obviamente difiere entre gráficos y funcionalidad.
* Si es necesario, **agregue texto en la descripción** para ayudar a comprender lo que sucede en un marco.

#### Comentarios y Pin

Los comentarios y los pin solo son secundarios a los Marcos y no son imprescindibles en el caso de los gráficos bien creados. Se pueden utilizar en los siguientes casos:

* Los comentarios son útiles para agregar texto adicional más allá de lo que permite la descripción de un marco. Puedes añadir pequeños fragmentos de texto por nodo, principalmente para pequeños fragmentos detallados de información. Los comentarios no se escalan bien y no se leen desde un nivel de zoom distante.
* Los bordes de navegación le permiten desplazarse por áreas específicas del gráfico mediante el método abreviado F2. Esto puede resultar útil para gráficos muy grandes en los que a menudo es necesario saltar entre dos áreas que están muy alejadas entre sí.

### Ubicación de entrada y salida

Las entradas y salidas deben colocarse en los extremos extremos de los gráficos: todas las salidas a la derecha, todas las entradas a la izquierda, cada una alineada verticalmente. Esto facilita su búsqueda e identificación.

![Colocación de entrada y salida](graph-creation-etiquette.resources/graph-creation-etiquette-02.gif "Colocación de entrada y salida")

El ejemplo anterior es un caso extremo: Los fotogramas no siempre son necesarios o posibles, pero debe quedar claro que la alineación vertical de las entradas y salidas es mucho más clara que la colocación aleatoria y reordenada.

### Redireccionamiento de vínculos

En gráficos grandes y muy largos, a veces los vínculos se crean en un intervalo muy grande. Esto lleva a confundir los cables de enlace que atraviesan el gráfico sin mucho control. El método abreviado &quot;Alt + Mayús Arrastrar&quot; le permite reorganizar estos vínculos, redireccionándolos en un trazado diferente subdividiendo un vínculo y añadiendo un control adicional en el centro. Se recomienda hacer uso de esto en escenarios donde tenga sentido.

![Redireccionamiento de vínculos](graph-creation-etiquette.resources/graph-creation-etiquette-03.gif "Redireccionamiento de vínculos")

### Etiqueta, identificador y uso

Cualquier gráfico destinado a compartirse o publicarse debe tener el cuidado adecuado en los metadatos adicionales, lo que mejora la facilidad de uso. Los siguientes puntos son importantes:

Las etiquetas sugeridas predeterminadas nunca son suficientes; dedique tiempo y esfuerzo a agregar etiquetas personalizadas a los parámetros expuestos y a las entradas y salidas.

![Identificador y etiqueta](graph-creation-etiquette.resources/graph-creation-etiquette-04.png "Identificador y etiqueta")

Intente que el identificador y la etiqueta no difieran demasiado: en el caso de que el identificador se utilice en otra parte (en varias funciones), puede resultar muy difícil encontrar qué propiedad de interfaz de usuario está relacionada con qué variable.

![Claridad del identificador](graph-creation-etiquette.resources/graph-creation-etiquette-05.png "Claridad del identificador")

Intente hacer coincidir las etiquetas con los términos que utilice en marcos (etiquetas de marco) y comentarios. Facilita averiguar qué sección del gráfico está vinculada a qué parámetro expuesto

![Etiquetas de fotograma y parámetro coincidentes](graph-creation-etiquette.resources/graph-creation-etiquette-06.png "Etiquetas de fotograma y parámetro coincidentes")

### Configuración de parámetros

Al exponer Parámetros, es importante algo más que la Etiqueta y el Identificador. Se deben tener en cuenta los siguientes puntos:

* Elija el tipo de editor correcto. Un control deslizante no siempre tiene sentido: También es posible utilizar un elemento de interfaz de usuario de ángulo o desplegable.
* Configure los valores mínimos y máximos adecuados y decida si tiene sentido sujetarlos.
* Elija un valor predeterminado que tenga sentido: Se deben evitar los valores predeterminados que resulten inútiles y los resultados de los casos perimetrales.
* Considere la posibilidad de reasignar el intervalo mediante una [función](../../function-graphs/function-graphs.md), si es necesario: Un regulador de 0,125 a 0,357 no tiene ningún sentido, puede reasignarlo fácilmente con una interpolación lineal y hacer que el elemento de interfaz de usuario utilice un rango de 0 a 1.

## Gráficos de Substance

### Administración de color y escala de grises

Se requiere un gran cuidado al usar los datos de color y escala de grises, la mezcla de ambos tipos no se puede hacer fácilmente sobre la marcha. Se deben tener en cuenta los siguientes puntos:

* Los gráficos nunca deben contener vínculos de puntos rojos (errores).
* No debe haber conversiones innecesarias entre color y escala de grises y viceversa. En algunos casos, el &quot;nodo de conversión de color/escala de grises insertado automáticamente&quot; en las preferencias de gráficos puede generar cadenas largas e inútiles de nodos de conversión acoplados.
* Lo ideal es mantener los datos en la escala de grises el mayor tiempo posible y convertirlos solo cuando sea absolutamente necesario. Esto reduce la complejidad y ahorra en rendimiento.
* Las entradas y salidas deben crearse o configurarse teniendo en cuenta el tipo correcto: por ejemplo, no tiene sentido tener una entrada &quot;mask&quot; definida en color si se va a convertir a escala de grises para su uso como máscara binaria.

![Conversiones de color y escala de grises](graph-creation-etiquette.resources/graph-creation-etiquette-07.png "Conversiones de color y escala de grises")

### Control de resolución

El control de la resolución de un [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) puede resultar confuso, por lo que se requiere un cuidado adecuado para hacerlo correctamente. Cometer errores puede provocar un rendimiento gravemente afectado o resultados inútiles de baja calidad.

[Para comprender completamente este tema, asegúrese de conocer los tamaños de salida absolutos y relativos.](../../compositing-graphs/output-size/output-size.md)

* Un gráfico debe establecerse en la resolución &quot;Relativa al padre&quot; en casi todos los casos, a menos que haya una excepción muy específica donde no se requiera (muy rara).
* Por lo general, los nodos no deben tener ajustes de reemplazo para el tamaño de salida. La resolución se controla mejor mediante las propiedades Parent o Graph en la mayoría de los casos.
* Para los mapas de bits, se debe establecer un cuidado especial en que el valor predeterminado, Tamaño de salida absoluto, no se extienda por todo el gráfico. Esto se debe reemplazar en Relativo al principal. Esta es una de las pocas excepciones a la regla anterior.
