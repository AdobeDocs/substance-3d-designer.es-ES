---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/release-notes/version-13-0.html"
breadcrumb-title: ''
description: Consulte las notas de la versión de Substance 3D Designer 13.0 para obtener más información sobre los nuevos nodos, Substance Engine 9.0 y nodos de portal.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 13.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versión 13.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: e540abf8ed046d72f116e9e43ae0743c5ae39c24
workflow-type: tm+mt
source-wordcount: '1671'
ht-degree: 2%

---


# Versión 13.0

Esta versión 13.0.0 de Substance 3D Designer trae mucho amor a los artistas de materiales, con una gran cantidad de nuevos nodos, el Substance Engine 9.0 introducir bucles por primera vez y con una gran adición a la gráfica: el nodo del portal. Y para satisfacer a más usuarios, presentamos una nueva pantalla de inicio y proporcionamos idiomas adicionales.

Como se ha mencionado en la versión anterior, esta versión ya no es compatible con los gráficos de modelos de Substance: Esto significa que ya no podrá abrir, editar ni exportar gráficos de este tipo en Designer. Puedes encontrar todas las razones por las que tomamos esta decisión en este [post](https://community.adobe.com/t5/substance-3d-designer-discussions/substance-model-graphs-end-of-life/td-p/13693731) en nuestro foro de la comunidad.

*Fecha de publicación: 6 de junio de 2023*

![Material que usa rutas](version-13-0.resources/Paths2.png "Material que usa rutas")

*Ilustración de [Celine Dameron](https://www.artstation.com/cline)*

## Nuevo contenido

Esta versión 13.0 trae muchos contenidos nuevos. Encontrará principalmente dos nuevas colecciones de nodos: Herramientas de spline y herramientas de trazado.

* [Herramientas de spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md) son una colección de nodos para generar y ajustar splines, así como para usarlas para asignar, dispersar o deformar imágenes.
* [Las herramientas de trazado](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-tools.md) son otro conjunto de nodos que se extraen, en forma de lista de segmentos, de los contornos de una máscara y, a continuación, se editan y mejoran.

Todos estos nodos ofrecerán muchas posibilidades y tendrán, sin duda, un montón de aplicaciones creativas. Echa un vistazo a la sección sobre [trabajar con trazados y Herramientas de spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/working-with-path-and-spl/working-with-path-and-spline-tools.md) para ver los conceptos importantes que hay que comprender para familiarizarse con este conjunto de herramientas.

![Material que usa splines](version-13-0.resources/Splines.png "Material que usa splines")

*Ilustración de [Louise Melin](https://www.artstation.com/troglodette)*

### Herramientas de Spline

Los nuevos nodos dedicados a las splines se pueden dividir en cuatro categorías:

#### Crear

La primera categoría es, por supuesto, la que permite generar splines:

* [Spline Cubic](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md): Desde dos puntos y dos tangentes;
* [Cuadrático Poly Spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md): A partir de un conjunto de puntos;
* [Círculo polinómico](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-circle/spline-circle.md): Siguiendo una forma circular.

También puede crear <b>puentes </b> entre splines para tener un conjunto completo de splines entre [2 splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines/spline-bridge-2-splines.md) o [N splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cúbica spline](version-13-0.resources/SplineCubic-Demo.gif "Cúbica spline")

</td>
<td style="border: 0;" valign="top">

![Cuadrático Poly Poly Estriado](version-13-0.resources/SplinePolyQuadratic-Demo.gif "Cuadrático Poly Estriado")

</td>
<td style="border: 0;" valign="top">

![Círculo polinómico](version-13-0.resources/SplineCircle-Demo.gif "Círculo polinómico")

</td>
<td style="border: 0;" valign="top">

![Lista Puente Spline](version-13-0.resources/SplineBridge-List_Demo.gif "Lista Puente Spline")

</td>
</tr>
</table>

#### Ensamblar

En algunos casos, tendrá que tratar varias splines como una sola entidad, por lo que necesita herramientas para administrar un conjunto de splines. La [Lista de combinación de splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md) te permite combinar todas tus splines en una sola conectando las extremidades en orden, el nodo [Append de Spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-append/spline-append.md) te permite anexar una lista de splines a otra lista y gracias al nodo [Spline Select](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-select/spline-select.md) puedes filtrar y seleccionar splines específicas de una lista dada.

#### Modificar

También proporcionamos herramientas para rehacer y retocar sus splines. Encontrarás un nodo para aplicar una [transformación 2D](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-2d-transform/spline-2d-transform.md), como una rotación, traslación, escala y otra para [deformar](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-warp/spline-warp.md)<b> </b>la forma y otros dos nodos para modificar el [thickness](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-thickness/spline-sample-thickness.md)<b> </b> o el [height](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-height/spline-sample-height.md) de las splines.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Transformación 2D Spline](version-13-0.resources/Spline2DTransform-Demo1.gif "Transformación 2D Spline")

</td>
<td style="border: 0;" valign="top">

![Deformación polinomial](version-13-0.resources/SplineWarp-Demo.gif "Deformación polinomial")

</td>
<td style="border: 0;" valign="top">

![Thickness de muestra spline](version-13-0.resources/SplineSampleThickness-Demo.gif "Thickness de muestra spline")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

#### Renderizar

La última categoría es la que crea la forma o motivo final basándose en las splines. La primera idea que vendrá a su mente será repetir una forma dada a lo largo de la spline: el nodo [Dispersión on Spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md) te permite hacerlo, con muchos parámetros para controlar perfectamente la distribución (rotación, escala, desplazamiento, colores, máscaras, etc.).

Gracias al [relleno de spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-fill/spline-fill.md)<b> </b>, puede crear fácilmente un patrón a partir de una spline cerrada. Además, si deseas asignar cualquier textura a tus splines, con un alto grado de control y precisión, el nodo [Spline Mapper](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md) está hecho para ti.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dispersión en escala de grises polinomiales](version-13-0.resources/ScatterOnSplineGrayscale-Demo.gif "Dispersión en escala de grises polinomiales")

</td>
<td style="border: 0;" valign="top">

![Relleno polinómico](version-13-0.resources/SplineFill-Demo.gif "Relleno polinómico")

</td>
<td style="border: 0;" valign="top">

![Color del asignador de spline](version-13-0.resources/SplineMapperColor-Demo.gif "Color del asignador de spline")

</td>
<td style="border: 0;" valign="top">

![Asignador de flujo spline](version-13-0.resources/SplineFlowMapper-Demo.gif "Asignador de flujo spline")

</td>
</tr>
</table>

### Herramientas de Ruta

El nodo [Mask to Paths](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) te permite extraer el borde de un patrón de escala de grises, en forma de una lista de segmentos.

A continuación, puedes procesar estas rutas con los nodos [Path 2D Transform](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md) o [Paths Warp](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) para ajustarlas según tus necesidades.  Y gracias al nodo [Rutas a spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md), puedes convertir tu ruta a spline, así que aprovecha todos los nodos dedicados a splines mencionados anteriormente, como la dispersión.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Enmascarar trazados](version-13-0.resources/MaskToPaths-Demo2.gif "Enmascarar trazados")

</td>
<td style="border: 0;" valign="top">

![Máscara a trazados 2](version-13-0.resources/MaskToPaths-Demo1.gif "Máscara a trazados 2")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

Y para ayudarle a aprender todos estos nuevos nodos, publicamos dos nuevos tutoriales:

* [Introducción a los nodos Spline](https://www.adobe.com/go/designer-tutorial-splines)
* [Introducción a los nodos Path](https://www.adobe.com/go/designer-tutorial-paths)

## Nuevo Substance Engine v9

Todos los nuevos nodos enumerados anteriormente se basan en la nueva versión de Substance Engine y están aprovechando al máximo su nueva función principal: <b>bucles</b>.

Los bucles solo se deben usar dentro de [gráficos de funciones de Substance](../../function-graphs/function-graphs.md) y lo más probable es que los implemente en un [procesador de píxeles](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), un [mapa de píxeles](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) o un [procesador de valores](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md). Los bucles, por supuesto, le permiten repetir fácilmente una función muchas veces, hasta que se respete una condición. Te ayudará a aligerar mucho tus gráficos y ganar en precisión.

Este [tutorial](https://www.youtube.com/watch?v=Ggoy8G90oDI) dedicado te ayudará a empezar a trabajar con bucles.

Substance Engine v9 también incorpora las siguientes mejoras:

* Nuevo modo sólido en el editor de degradados del nodo [Gradient Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) (es decir, no hay interpolación)
* Nodo pow() atómico en gráficas de funciones de Substance
* Añadir opciones de ajuste de bordes (sujetar a borde, repetir) en nodos de Sampler
* Muestreo más cercano en nodos [Warp](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) y [Directional Warp](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)

## Nodo Portal

El nodo [Portal](../../interface/the-graph-view/graph-items/graph-items.md) es una nueva extensión del nodo [Dot](../../interface/the-graph-view/graph-items/graph-items.md) con la posibilidad de ocultar conexiones en el gráfico.

Gracias a esta función, puede mejorar la legibilidad del gráfico ocultando conexiones muy largas y también tener un acceso rápido a nodos clave desde cualquier lugar del gráfico.

Esta nueva característica se explica detalladamente en este [tutorial](https://www.adobe.com/go/designer-tutorial-portals) dedicado.

![Nodo del portal](version-13-0.resources/PortalNodeFinal.gif "Nodo del portal")

## Pantalla de inicio

Cuando inicias Designer, sabes que tienes acceso a una [pantalla de inicio](../../interface/home-screen/home-screen.md) completamente nueva como la que tienes en otros productos de Adobe. Desde esta pantalla, puede:

* Cree rápidamente un nuevo gráfico;
* Consulte la lista de todos los archivos abiertos recientemente en Designer, con algunos detalles como el tamaño, la fecha en que se modificó por última vez o la ruta completa del archivo;
* Una página de formación en la que puede encontrar vínculos a recursos de aprendizaje, como tutoriales para presentarle nuevas funciones o descubrir sugerencias rápidas;
* Vínculos directos a la pantalla Novedades, la pantalla Acerca de, el sitio web de Substance 3D, el foro de la comunidad de asistencia, etc.

![Pantalla Inicio - Inicio](version-13-0.resources/HomeScreen.png "Pantalla Inicio - Inicio")

![Pantalla Inicio - Formación](version-13-0.resources/LearnPage.png "Pantalla Inicio - Formación")

## Nuevos idiomas

Esta versión viene con tres idiomas adicionales:

* Español (España);
* Italian (Italy);
* Portugués (Brasil).

Te recordamos que si quieres cambiar el idioma en Designer, ve a [Preferencias](../../interface/preferences-window/preferences-window.md) y encontrarás la lista de todos los idiomas disponibles en la sección General.

## Notas de la versión

### 13.0.0

*(Lanzado el 6 de junio de 2023)*

### Añadido

* [Graph] Nodo del portal
* [Onboarding] Nueva pantalla de inicio
* [Content] Nodo Spline (Cubic)
* [Content] Nodo spline (poli cuadrático)
* [Content] Nodo Círculo polinómico
* [Content] Nodo Lista de puntos
* [Content] Nodo Puente de spline (2 splines)
* [Content] Nodo Puente polinomial (lista)
* [Content] Nodo Append de Spline
* [Content] Nodo Seleccionar spline
* [Content] Nodo Lista de combinación de splines
* [Content] Nodo Transformación 2D polinomial
* [Content] Nodo Deformación de spline
* [Content] Nodo de Height de muestra de spline
* [Content] Nodo de Thickness de muestra de spline
* [Content] Nodo de procesamiento de spline
* dispersión [Content] en el nodo Color de spline
* [Content] Dispersión en el nodo Escala de grises polinomiales
* [Content] Nodo Color del asignador de spline
* [Content] Nodo de escala de grises del asignador de splines
* [Contenido] Nodo Color del asignador de puente spline
* [Contenido] Nodo de escala de grises del asignador de puente spline
* [Content] Nodo Spline Flow Mapper
* [Contenido] Nodo Color del asignador UV
* [Contenido] Nodo de escala de grises del asignador UV
* [Content] Rutas al nodo Splines
* [Content] Nodo Máscara a trazados
* [Contenido] Rutas nodo de transformación 2D
* [Content] Rutas Nodo polígono
* [Content] Nodo de rutas de previsualización
* [Content] Nodo Deformación de rutas
* [Content] Rutas Seleccionar nodo
* [Content] Rutas nodo de procesador de vértices
* [Content] Rutas Procesador de vértices Nodo simple
* [Content] Nodo Transformación cuádruple en ruta
* [Contenido] Oclusión ambiental con trazado de rayo v2
* [Contenido] Raytraced Bent Normal v2
* [Contenido] Sombras con trazo de rayo v2
* [Motor] Actualizar a la versión 9
* [Motor] Nodo de bucle en gráficos de funciones
* [Motor] Añadir modo sólido al degradado
* [Motor] Nodo Atomic pow() en Gráfica de funciones
* [Motor] Añadir opciones de ajuste de bordes (sujetar a borde / repetir) en el nodo Sampler
* [Motor] Muestreo más cercano en el nodo de deformación y Deformación direccional
* [Motor] Añada un modo &quot;punchthrough alfa&quot; al filtro Perfilar para las entradas de color
* [Motor] FxMap: Morflete de hemisferio
* [Motor] Operaciones atómicas Get/Set en gráficos de funciones
* Funciones [Engine]: use la función precisa de log/log2/exp, 2pow - Unificar funciones entre la cocina y el motor
* [Motor] Añada un parámetro de &quot;desplazamiento de intensidad&quot; al filtro de Deformación direccional
* [API] Compatibilidad con la gestión de ajustes preestablecidos para la composición de gráficos
* [Funciones] Cambiar el nombre de entrada de las funciones de los nodos atómicos
* [Localización] Añadir portugués (Brasil), italiano (Italia) y español (España)
* [Localización] Respete la regla &quot;Idioma (país)&quot; en la lista de idiomas
* [Ajustes preestablecidos] Desactivación de los paneles &quot;Previsualización&quot; y &quot;Ajustes preestablecidos&quot; en las propiedades del gráfico al utilizar la edición en contexto
* [Gráfico de modelos de Substance] Fin de la compatibilidad de gráficos de modelos de Substance

### Correcciones

* [Vista 3D] La visualización de cadenas largas en las estadísticas de escenas está cortada (solo macOS)
* [API] El módulo &#39;structure::Structure&#39; aún se incluye en la referencia de API
* [API] Los nodos de puntos de los gráficos MDL no tienen definición ni propiedades
* [API] Comportamiento incorrecto al establecer el parámetro de nodos de función
* [Contenido] Los nodos 3D Voronoi y 3D voronoi fractal generan una advertencia de cocción
* [Motor] El parámetro &quot;Desplazamiento de mapa de intensidad&quot; no tiene efecto en los datos de escala de grises del motor SSE2
* [Explorer] Se puede eliminar la e/s de gráficos
* [Graph] El mapa de bits se omite cuando se utiliza en instancias
* [Graph] Posición incorrecta del nodo de puntos al crearse un nodo a partir de un nodo
* [Graph] Enfoque incorrecto en el cuadro de diálogo &quot;Exponer parámetro&quot; al utilizar la tecla Intro
* [Gráfico] Resultado incorrecto en la exploración de histograma con mapa de bits en la edición de contexto
* [Localización] Solucionar varios problemas de recorte
* [Parameters] Bloqueo al eliminar un parámetro de entrada
* [Publish] Los gráficos de las carpetas se mueven a la raíz en el paquete publicado
* [Resources] Bloqueo al actualizar un recurso cargado en el disco
* [VisibleIf] Corregir regresión en evaluación de visibilidad condicional
