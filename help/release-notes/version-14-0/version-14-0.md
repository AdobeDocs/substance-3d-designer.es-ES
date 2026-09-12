---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-14-0.html"
breadcrumb-title: ''
description: Consulte las notas de la versión de Substance 3D Designer 14.0 para obtener más información sobre los nuevos nodos, la navegación por gráficos y las mejoras de rendimiento.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 14.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versión 14.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: e540abf8ed046d72f116e9e43ae0743c5ae39c24
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---


# Versión 14.0

<b>Substance 3D Designer 14.0 </b> ofrece varias mejoras en la calidad de vida (navegación por gráficos, actuaciones, ...) pero sobre todo incluye muchos nodos nuevos (manipulación de color, filtro Kuwahara, herramientas de histograma, suavizado de bisel, distancia direccional, ...). Consulte a continuación para obtener más información sobre todos estos cambios.

*Fecha de publicación: 30 de julio de 2024*

![](version-14-0.resources/2024-BannerRN.png)

## Nuevo contenido

Esta versión 14.0 trae mucho contenido nuevo con los nuevos nodos que se enumeran a continuación:

* <b>Nodos dedicados a la manipulación de color: </b>un nodo <b>(</b>[Cuantificar color](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)<b>) </b>a<b> </b>reduce el número de colores de una imagen y extrae una paleta de ella, una familia de nodos de herramientas para crear tu propia paleta de colores ([Ver](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) / [Crear](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md) / [Modificar](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)<b> </b>paleta de colores) y una para aplicarla a otra imagen mediante un mapa de ID ([Aplicar paleta de colores](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md)). También encontrarás el nodo [ID para enmascarar escala de grises](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/id-to-mask/id-to-mask.md) para convertir tu mapa de ID —calculado por cuantificar color— en una máscara de escala de grises. Con este conjunto completo de nodos, tiene todo lo que necesita para crear efectos de estilización con colores.

![](version-14-0.resources/GIF2_2.gif){zoomable="yes"}

![Cuantificar color 2](version-14-0.resources/GIF3_2.gif){zoomable="yes"}

* <b>Filtro de Kuwahara</b>: si quieres ir más allá con la estilización, puedes generar algunos efectos pictóricos gracias a los filtros [Anisotropic Kuwahara color](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/anisotropic-kuwahara/anisotropic-kuwahara.md) / [escala de grises](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/anisotropic-kuwahara-gra/anisotropic-kuwahara-grayscale.md). En los detalles, aplica un desenfoque direccional anisotrópico que se ajusta a los detalles de la imagen. El resultado es una imagen que parece fluir en la dirección de las formas que contiene.

Estos nodos (Cuantificar color y Kuwahara anisotrópico) se explican en [este tutorial](https://www.adobe.com/go/designer-tutorial-quantize). Se muestra cómo utilizarlos para estilizar los materiales, así como para manejar los colores de manera más eficiente e intuitiva.

Otros nodos poderosos se unen al partido:

* [<b>Curvatura suave</b>](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md): esta nueva versión ahora es compatible correctamente con todos los modos de mosaico, añade dos nuevas salidas (convexidad y concavidad) y mejora tanto la precisión como el rendimiento.
* <b>[Histograma ecualizado](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-equalize/histogram-equalize.md):</b> este nodo ecualiza el histograma de una imagen de escala de grises ajustando los valores para obtener una distribución igual. Estos nodos vienen con dos nodos complementarios: [El histograma se procesa](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-render/histogram-render.md) para mostrar el histograma de la imagen y el [Histograma ](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-compute/histogram-compute.md)<b> </b> para codificar un histograma como una fila de píxeles.
* <b>[Suavizado de bisel](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/bevel-smooth/bevel-smooth.md):</b> gracias a este, puedes dibujar un degradado o un color plano desde los bordes de una máscara (hacia fuera, hacia dentro o ambos). El nodo [Distancia direccional](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/directional-distance/directional-distance.md)<b> </b>también dibuja degradados pero en una dirección específica.
* <b>[Normal uncombine](../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-uncombine/normal-uncombine.md):</b> Este nodo es el opuesto al nodo [Normal combine](../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md), quita de un mapa normal los detalles de superficie descritos por un mapa de height.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Curvatura suave

<table>
  <tr>
    <td>
      <img src="version-14-0.resources/curvature_smooth_example_1_before.jpg" alt="curvature_smooth_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="version-14-0.resources/curvature_smooth_example_1_after.jpg" alt="curvature_smooth_example_1_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

Ecualización del histograma

<table>
  <tr>
    <td>
      <img src="version-14-0.resources/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="version-14-0.resources/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Suavizado de bisel

<table>
  <tr>
    <td>
      <img src="version-14-0.resources/bevel_smooth_example_6_before.jpg" alt="bevel_smooth_example_6_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="version-14-0.resources/bevel_smooth_example_6_after.jpg" alt="bevel_smooth_example_6_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

Normal descombinar

<table>
  <tr>
    <td>
      <img src="version-14-0.resources/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="version-14-0.resources/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

## Mejoras en la calidad de vida

* Se han mejorado el <b>rendimiento </b> y la <b>capacidad de respuesta</b> al trabajar en grandes proyectos. Por ejemplo, la eliminación de nodos puede ser hasta 75 veces más rápida. El tiempo de [cocción](../../glossary/glossary.md) también se ha reducido para los gráficos que hacen referencia varias veces al mismo mapa de bits.
* <b>Parámetros heredados</b>: cuando un parámetro es [heredado](../../glossary/glossary.md), en lugar de mostrar el valor predeterminado, ahora mostramos el heredado para que sepa el valor utilizado actualmente. Obtenga más información sobre la herencia en [esta página dedicada de nuestra documentación](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).
* <b>La compatibilidad con Trackpad</b> en MacOS se ha rediseñado por completo para que sea más natural y esté en línea con otro software. También se ha rediseñado el desplazamiento de nodos más allá de los bordes de [Graph View](../../interface/the-graph-view/the-graph-view.md) para que sea más fluido y coherente en todos los sistemas operativos.

* <b>Vista 2D: </b>si la visualización en mosaico está habilitada en la [vista 2D](../../interface/2d-view/2d-view.md), ahora puedes obtener valores incluso para los píxeles que no están en el mosaico original: ayuda mucho comprobar [muestreo](../../glossary/glossary.md) y las transiciones de valores entre los mosaicos.

![vista 2d](version-14-0.resources/2dview.gif){width="320px" zoomable="yes"}

* <b>Mapa de degradado</b>: usa el botón central del ratón para desplazar todas las [teclas de degradado](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) hacia la izquierda o la derecha (y así conservar todos los espacios entre todas las teclas).
* <b>Parámetros</b>: para insertar funciones personalizadas a través de parámetros, ahora puede utilizar el widget de función Editar. Es una solución eficaz para crear herramientas personalizadas en las que desea controlar parámetros mediante un [gráfico de funciones de Substance](../../function-graphs/the-function-graph/the-function-graph.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Editar función](version-14-0.resources/functionedit.png){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Editar función 2](version-14-0.resources/functionedit2.png){zoomable="yes"}

</td>
</tr>
</table>

## Mejoras de API

La API de scripts incluye cuatro nuevos métodos:

* Métodos para obtener y establecer el tipo de gráfica de una gráfica de composición de Substance: myGraph.setGraphType(&quot;newType&quot;) ; myGraph.getGraphType()
* Método para abrir un recurso de paquete en su editor (p. ej., un gráfico de Substance en la vista de gráficos): myUIManager.openResourceInEditor(myResource)
* Método para seleccionar un recurso de paquete en el Explorador (p. ej., un gráfico de Substance): myUIManager.setExplorerSelection(myResource)
* Método para enmarcar un nodo específico en la vista de gráfico: myUIManager.focusGraphNode(myGraphViewID, myNode)

## Requisitos de la plataforma VFX

Todos los años, la [Plataforma de Referencia de VFX](https://vfxplatform.com/) publica una lista de herramientas y versiones de bibliotecas que se usarán en todos los programas para la industria de VFX con el fin de minimizar las incompatibilidades entre los programas. Como de costumbre, *actualizamos todas nuestras dependencias* para respetar todas estas recomendaciones.

Tenga en cuenta que estas actualizaciones tienen dos consecuencias principales:

* <b>Los requisitos de Linux</b> han cambiado y Designer ahora requiere la versión 8 o 9 de RHEL (CentOS ya no es compatible). Todos los detalles se encuentran en la página [Requisitos del sistema](../../getting-started/system-requirements/system-requirements.md).
* <b>Los complementos para Designer deben actualizarse </b>ya que algunas funciones han quedado obsoletas en Qt6. Encontrará toda la información necesaria para actualizar sus complementos en el [foro de la comunidad](https://community.adobe.com/t5/substance-3d-designer-discussions/plugins-required-updates-in-designer-14-0/td-p/14768559).

## Notas de la versión

### 14.0.0

*(Lanzado el 30 de julio de 2024)*

### Añadido

* [Contenido] Nuevo filtro Kuwahara anisotrópico
* [Content] Nuevo nodo de Suavizado de bisel
* [Contenido] Nuevo nodo Curvatura suave v2
* [Content] Nuevo nodo de Distancia direccional
* [Contenido] Nuevas herramientas de histograma: Calcular, ecualizar, procesar
* [Contenido] Nuevo nodo ID a máscara
* [Content] Nuevo nodo Normal Uncombine
* [Content] Nuevos nodos de la paleta: Crear, Aplicar, Modificar, Ver
* [Content] Nuevo nodo Cuantificar color
* [Contenido] Deformación direccional no uniforme: Defina el valor predeterminado de Asignación de intensidad en 1
* [Contenido] Añada el sufijo &quot;Color&quot; o &quot;Escala de grises&quot; a todas las etiquetas de nodo que tengan estas versiones
* [Contenido] Si se anula el &quot;ruido blanco&quot;, solo se mantiene &quot;ruido blanco rápido&quot;
* [Content] Pase al nodo &#39;Negate Float1&#39; en el gráfico de funciones del Substance
* [Contenido] Cambie el nombre &quot;Cuantizar color&quot; por &quot;Cuantificar color (simple)&quot;
* [Vista 2D] Visualización de valores en el panel de información para píxeles fuera del rango 0-1
* [Motor][Texto] Nuevo kerning para algunas fuentes
* [Graph] Mejora el tiempo de invalidación al editar subgráficos profundos mientras usas la edición en contexto
* [Vinculador] No duplicar mapas de bits en SBSASM
* [Parámetros] Añada un nuevo widget de &quot;función&quot; para todos los tipos de parámetros de entrada
* [Propiedades] Mejorar la visualización de los parámetros heredados
* [UX] Mejora de la compatibilidad con Trackpad (solo Mac)
* [UX] Modernizar la panorámica al alcanzar el borde del gráfico al seleccionar
* [UX] Eliminación de la funcionalidad &quot;Desactivar alta PPP&quot;
* [Branding] Nueva marca para la pantalla de bienvenida y la ventana Acerca de
* [Mapa de degradado] Añade una forma de desplazar todas las teclas y el bucle
* [Biblioteca] Cambiar todos los filtros predeterminados a mayúsculas y minúsculas de oración
* [API] Método Add para encuadrar un nodo específico en la ventana gráfica de la vista de gráficos
* [API] Añadir método para abrir un recurso de paquete en su editor (p. ej., un gráfico de Substance en la vista de gráficos)
* [API] Añadir método para seleccionar un recurso de paquete en el Explorador (p. ej., un gráfico de Substance)
* [API] Agregue métodos para obtener y establecer el tipo de gráfico de un gráfico de composición de Substance
* [ThirdParty] Sigue las recomendaciones de las plataformas VFX 2023
* [ThirdParty] Sigue las recomendaciones de las plataformas VFX 2024
* [ThirdParty] Actualizar Boost a 1.82.0 + USD a 23.08
* [ThirdParty] Actualizar NGL a 1.38
* [ThirdParty] Actualizar OpenColorIO a 2.3.x
* [ThirdParty] Actualice OpenExr a 3.2.x
* [ThirdParty] Actualizar OpenSubdiv a 3.6.x
* [ThirdParty] Actualizar Python a 3.11.x
* [ThirdParty] Actualice Qt a 6.5.x
* [ThirdParty] Actualizar gcc a 11.2.1
* [ThirdParty] Actualizar glibc a 2.28
* [ThirdParty] Actualizar ABI de libstdc++ a C++11 uno
* [Documentación] Nueva página de &#39;Glosario&#39;

### Correcciones

* [Bakers] Bloqueo al retocar una escena cuyo nombre de archivo se ha cambiado
* [Bakers] Bloqueo al guardar el ajuste preestablecido de bakers en un archivo JSON
* [Content] &#39;Dispersión en spline&#39;: Exponer parámetro alfa de imagen de entrada
* [Contenido] &#39;Color del Sampler de mosaico&#39;: falta la expresión visibleif
* [Contenido] Ruido anisotrópico: valor negativo para la cantidad X/Y produce un resultado incorrecto
* [Contenido] Ruido anisotrópico: Problema de segmentación al utilizar un valor impar como cantidad X y sin smoothness
* [Content] Función de distribución normal: una posición incorrecta de max() puede provocar NaN
* [Contenido] Las sombras TRAO, Bent Normal y RT no funcionan correctamente en algunas plataformas
* [Contenido] Color de fusión de salpicaduras de formas: Los mapas normales de OpenGL no se mezclan correctamente
* [Contenido] Espacio injustificado después del prefijo &quot;Multi&quot; en las etiquetas de nodo
* [Dependencies] Bloqueo al mover un gráfico dentro de un paquete o entre paquetes
* [Motor] Error de precisión en nodos de deformación que afectan a los nodos de desenfoque de Pendiente
* [Motor] La capa SBSAR en SD no puede leer SBSAR con contenido SBSASM > 2 GB
* [Gráfico de funciones] Resultado incorrecto para 0^n
* [Graph] La opción &quot;Mostrar tamaño de nodo&quot; no está etiquetada correctamente
* [Graph] Bloqueo al copiar un comentario principal a otro gráfico
* [Graph] Bloqueo al pulsar alt y arrastrar un nodo de punto
* [Graph] En la búsqueda de nodos pueden faltar coincidencias obvias en algunos casos
* [Graph] Problema de rendimiento al editar un gráfico de funciones con instancias múltiples con supergraph abierto
* [Graph] Demasiadas invalidaciones al crear una salida
* [Seguridad] Vulnerabilidad de escritura fuera de límites del análisis ICO
* [Security] Anular el uso de algún formato de imagen
* [Parámetros] La ruta del recurso PKG de mapa de bits no debe poder editarse
* [Parámetros] Se han solucionado problemas relacionados con la exposición por lotes del parámetro de un procesador de valores
* [Parámetros] Los parámetros de cadena se omiten al exponer lotes
* [Propiedades] Problema de rendimiento al editar un gráfico de funciones con instancias múltiples con propiedades abiertas
* [SVG] Las ediciones de formas no se aplican en imágenes rasterizadas
* [IU] Solucione algunos errores o incoherencias con widgets desplazables (solo Windows)
* [UI] Orden incoherente de los formatos de archivo de escena 3D en las listas de importación/exportación
* [UI] Las acciones de la ventana se duplican en la IU
* [Control de versiones] El script &#39;perforce.py&#39; no funciona en Python 3
