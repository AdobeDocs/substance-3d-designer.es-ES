---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/2d-view.html"
breadcrumb-title: ''
description: Utilice la vista 2D de Substance 3D Designer para previsualizar e inspeccionar las salidas de textura de los gráficos de materiales.
helpx_creative_field: ""
helpx_description: Designer > Interface > 2D view
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vista 2D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '2354'
ht-degree: 0%

---


# Vista 2D

Esta página describe la interfaz de usuario y las características del panel **Vista 2D** en Substance 3D Designer.

![Vista 2D](../../assets/2d-view-main.png "Vista 2D")

## Información general

La [vista 2D](https://substance3d.adobe.com/) es uno de los paneles principales de la interfaz de usuario de Designer. Sus principales objetivos son los siguientes:

* mostrando la salida de *value* o *image* por un *nodo* especificado o pasando por un *conector de nodo* especificado
* mostrando [mapas de bits](../../resources/bitmap-resource/bitmap-resource.md) y [gráficos vectoriales](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) [recursos](../../resources/resources.md)
* mostrando *información adicional* sobre el contenido que contiene actualmente, como canales de color o valores de color exactos
* controlando parámetros de *gizmos*

Cuando se modifica una imagen o un valor mostrados, la vista 2D *se actualiza automáticamente* para estar sincronizada con el estado actual de los datos.\
*Varios* paneles de vista 2D pueden estar activos en cualquier momento, y cada uno puede mostrar diferentes imágenes o valores. Puede controlar cuándo se debe utilizar un nuevo panel mediante la función ![](../../assets/2d-view-icon-pin.png) <b>Pin</b> del panel de la interfaz de usuario.

### Visualización de contenido en la vista 2D

>[!WARNING]
>
> Todas las menciones de acciones realizadas en *nodos* de esta sección solo se aplican a [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md).

La forma más sencilla de mostrar cualquier imagen en la vista 2D es hacer doble clic en *LMB*...

* ...en un recurso [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) o [vector graphics](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) en el [Explorador](../../interface/the-explorer-window/the-explorer-window.md)
* ...en un nodo o conector de nodo en [Graph View](../../interface/the-graph-view/the-graph-view.md)

Las imágenes también se pueden *arrastrar y soltar* directamente en la ventana gráfica manteniendo *LMB* en un [recurso](../../resources/resources.md) en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md), o *RMB* en un nodo en la vista de gráficos.

En la vista de gráfico, puede enviar una imagen a la vista 2D mediante la opción de menú contextual <b>Ver salida en vista 2D</b>, a la que se accede haciendo clic en *RMB*...

* ...en un *nodo* para mostrar *el resultado de ese nodo*. Si el nodo tiene más de una salida, seleccione la salida deseada en el submenú
* ...en *espacio vacío* en la vista de gráfico para mostrar *la salida de ese gráfico*. Si el gráfico tiene más de una salida, seleccione la salida deseada en el submenú

Al cargar un gráfico, su *primera salida* se muestra automáticamente en la vista 2D de forma predeterminada. Puede deshabilitar este comportamiento en [Preferencias](../../interface/preferences-window/preferences-window.md). Vaya a <b>Editar > Preferencias > Gráfico > Gráfico de composición de Substance</b> y *desmarque* la opción <b>Ver salida en vista 2D al abrir un gráfico</b>.

## Área de visualización

La ventana gráfica es el *área de visualización* de la <b>vista en 2D</b> y te permite *navegar* por la imagen mostrada mediante los siguientes métodos abreviados de teclado y ratón:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

* <b>Panorámica:</b> Ctrl+RMB/MMB
* <b>Zoom:</b> Alt+RMB / MouseWheel / herramienta &quot;Mostrar escala&quot;:\
  ![](../../assets/2d-view-icon-zoom.png)
* <b>Ajustar para ajustar a la ventana gráfica:</b> F / botón &#39;Ajustar a la vista&#39; ![](../../assets/2d-view-icon-fit-to-view.png)
* <b>Ajustar a escala 1:1:</b> Z / botón &#39;Ajustar a escala&#39; ![](../../assets/2d-view-icon-fit-to-scale.png)

</td>
<td style="border: 0;" valign="top">

![Navegación de ventanilla de vista en 2D](../../assets/2d-view-viewport-navigation.gif "Navegación de ventanilla de vista en 2D")

</td>
</tr>
</table>

Uso de una almohadilla táctil (solo macOS)

* Panorámica <b>: </b>Barrido con dos dedos
* <b>Zoom:</b> Pellizcar con dos dedos / Deslizar con dos dedos mientras se mantiene presionada la tecla Cmd

>[!IMPORTANT]
>
> Acciones no disponibles
> 
> *No* se puede desplazar la imagen si el tamaño de visualización actual de la imagen es *menor que el tamaño de la ventana gráfica*.
> 
> *No* se puede acercar o alejar la imagen si el contenido mostrado *ya no existe*; por ejemplo, se eliminó un recurso o nodo de referencia de una imagen.

>[!NOTE]
>
> Dirección del zoom
> 
> Cada uno de los métodos de zoom se invierte con el otro:
> 
> * La rueda del ratón *acerca la imagen*
> * Pulsa Alt+RMB y arrastra *empuja* la imagen
> 
> La dirección del zoom se puede invertir en [Preferencias](../../interface/preferences-window/preferences-window.md).

La imagen nativa *resolución*, *formato de color* y *profundidad de bits* aparecen en el área inferior izquierda de la ventana gráfica.

Además de la navegación, la ventana gráfica ofrece las siguientes funciones:

* Pantalla en mosaico: *repite la imagen* en la ventana gráfica en un patrón en mosaico. Esto resulta útil para comprobar cómo se repetirá un patrón o una textura. Se habilita mediante el botón **Barra espaciadora** o ![](../../assets/2d-view-icon-tiling.png) **Pantalla en mosaico**
* Visualización del tamaño físico: Muestra la imagen con una *proporción* que coincide con la propiedad [Tamaño físico](../../compositing-graphs/graph-parameters/graph-parameters.md) del gráfico. Está habilitada usando el botón ![](../../assets/2d-view-icon-physical-size.png) **proporción de Tamaño físico**
* Mantener tamaño de vista: Esta opción *bloquea la escala de visualización* para que sea coherente en todas las imágenes. Está *habilitado de forma predeterminada* y se puede deshabilitar usando el botón ![](../../assets/2d-view-icon-lock-scale.png) **Mantener tamaño de vista**

## Barra de herramientas principal

La barra de herramientas principal del panel <b>Vista 2D</b> te permite hacer más cosas con las imágenes que se muestran y ofrece las siguientes funciones:

+++Imagen de fondo
![Imagen de fondo de vista 2D](../../assets/2d-view-background.png "Imagen de fondo de vista 2D"){width="360px"}



Puedes *superponer una imagen diferente* encima de la que se muestra actualmente. Pulsa el botón ![](../../assets/2d-view-icon-background.png) <b>Imagen de fondo</b> y se te pedirá que selecciones un archivo de imagen para usarlo como superposición.

Una vez seleccionado el archivo, aparece una nueva barra de herramientas con los siguientes controles para la imagen superpuesta:

<b>![](../../assets/2d-view-icon-background-close.png) Cerrar:</b> *cierra* la barra de herramientas de controles de superposición y *deshabilita* la superposición de imagen de fondo.

<b>![](../../assets/2d-view-icon-background-loadpng.png) Cargar imagen:</b> selecciona *otro archivo de imagen* para usarlo como superposición.

<b>![](../../assets/2d-view-icon-background-0.png) Imagen de origen:</b> establece la imagen superpuesta en la opacidad del *0%*.

<b>![](../../assets/2d-view-icon-background-100.png) Imagen de fondo:</b> establece la imagen superpuesta en la opacidad *100%*.

<b>![](../../assets/2d-view-icon-background-50.png) Restablecer:</b> establece la imagen superpuesta en la opacidad del *50%*.

Un regulador te da *control manual* sobre la opacidad de la imagen superpuesta.

+++

+++Exportar imagen
![Imagen de exportación de vista 2D](../../assets/2d-view-export-bitmap.png "Imagen de exportación de vista 2D"){width="360px"}



La imagen mostrada actualmente se puede *exportar a un archivo de imagen*. Presione ![](../../assets/2d-view-icon-export.png) <b>Guardar imagen...</b> y se le pedirá que seleccione una *ubicación*, *nombre* y *formato de archivo* para el archivo exportado.

Aunque la imagen se exportará con su *resolución nativa*, que se muestra en el área inferior izquierda de la ventana gráfica, la *profundidad de bits* y el *formato de color* dependerán del formato de imagen *seleccionado.* Por ejemplo, las imágenes de precisión de punto flotante de 32 bits solo se pueden exportar en su rango de datos completo con formatos de imagen que admitan esta precisión, como TIFF, EXR y HDR. Si el formato de imagen no admite los datos, es probable que se produzcan abrazaderas o bandas de color en la imagen exportada.\
En general, tenga en cuenta qué precisión y funciones ofrecen los formatos de imagen que pretende utilizar: compatibilidad con coma flotante, perfiles ICC, etc.

Si <b>OCIO</b> o <b>Adobe ACE</b> [el modo de administración de color](../../color-management/color-management.md) se está usando actualmente, y hay una opción adicional disponible para seleccionar el *espacio de color* de la imagen exportada.

+++

+++Copiar en el portapapeles
![Copia de vista 2D al portapapeles](../../assets/2d-view-copy-clipboard.gif "Copia de vista 2D al portapapeles"){width="360px"}



La imagen mostrada actualmente se puede *copiar en el portapapeles*. Pulsa el botón ![](../../assets/2d-view-icon-copy.png) <b>Copiar imagen en el portapapeles</b> y la imagen estará lista para pegarse en cualquier software de terceros, como Adobe Photoshop.

La imagen se copiará como una imagen de precisión de *8 bits* con su *resolución nativa*, que se muestra en el área inferior izquierda de la ventana gráfica.

+++

+++Salidas de gráficos de conmutación
![Salidas del gráfico del conmutador de vista 2D](../../assets/2d-view-switch-graph-outputs.gif "Salidas del gráfico del conmutador de vista 2D"){width="360px"}



Si la imagen que se muestra actualmente es una *salida de gráfico*, puedes *cambiar rápidamente a cualquier* salida de gráfico mediante el botón ![](../../assets/2d-view-icon-view-outputs.png) <b>Seleccionar salida</b>.

Esta característica *no* está disponible para otros nodos, incluidos los nodos que tienen más de un resultado.

+++

+++Superposición UV
![Superposición UV de vista 2D](../../assets/2d-view-uv.png "Superposición UV de vista 2D"){width="357px"}



Si la opción <b>Mostrar UV en vista 2D</b> está habilitada en el menú <b>Escena</b> del dock [Vista 3D](../../interface/3d-view/3d-view.md), la característica de superposición UV está disponible en la vista 2D.

Puede habilitarlo mediante el botón <b>UV</b>. ![](../../assets/2d-view-icon-uv.png)

Esto muestra las UV de la malla [ seleccionada actualmente en el Vista 3D ](../../interface/3d-view/3d-view.md) como una malla metálica de color.

Si la información de color de material está disponible en el archivo de malla, el color de material se utiliza como color de la superposición UV.

Si la malla tiene <b>varios conjuntos UV</b>, se pueden seleccionar los UV deseados en la lista desplegable que se puede abrir haciendo clic en la flecha junto a la etiqueta &#39;UV&#39; en el botón.

+++

+++Información de imagen
![Información de imagen de vista 2D](../../assets/2d-view-information.png "Información de imagen de vista 2D"){width="360px"}



Puede mostrar los *valores de píxeles exactos* *y las coordenadas* en una imagen con el panel <b>Información</b>, que está habilitado mediante el botón ![](../../assets/2d-view-icon-information.png) <b>Información de la imagen</b>. Esto resulta muy útil al inspeccionar imágenes HDR, por ejemplo, o para asegurarse de que el paso entre píxeles sigue la progresión deseada.

Los colores están representados por los valores <b>RGBA</b> y <b>HSV</b>, y se muestran según la *precisión* de la imagen, de la siguiente manera:

* <b>8 bits</b>: 0-255 entero / 0,0-1,0 coma flotante

* <b>16 bits</b>: 0-65532 entero / 0,0-1,0 coma flotante

* <b>16F</b> (punto flotante de 16 bits): valor de punto flotante sin formato

* <b>32F</b> (punto flotante de 32 bits): valor de punto flotante sin formato

Las coordenadas de píxeles están representadas por los valores <b>X</b> e <b>Y</b>.

+++

+++Histograma
![histograma de vista 2D](../../assets/2d-view-histogram.png "histograma de vista 2D"){width="360px"}



Puede mostrar el *histograma* de la imagen con el panel <b>Histograma</b>, que está habilitado mediante el botón ![](../../assets/2d-view-icon-histogram.png) <b>Mostrar histograma</b>.

Están disponibles los siguientes *modos de histograma*:

* <b>Luminancia</b>

* <b>Rojo</b>

* <b>Verde</b>

* <b>Azul</b>

* <b>RGB</b>

* <b>Alpha</b>

A continuación de los modos se incluye la siguiente información:

* <b>píxeles</b>: el número de píxeles de la imagen

* <b>Intervalo</b>: todo el intervalo de valores disponible

* <b>Intervalo usado</b>: el rango de valores desde el píxel de valor más bajo hasta el más alto

Además, puedes hacer clic en **LMB** en el histograma o *mantener* **LMB** y *arrastrar* por el histograma para *seleccionar una parte específica* de los datos. A continuación, se muestra la siguiente información para esta selección:

* **Píxeles seleccionados**: el número de píxeles que tienen los valores seleccionados

* **Intervalo seleccionado**: el rango de valores de la parte seleccionada

* **Máximo seleccionado**: el número más alto de píxeles que tienen un valor incluido en la parte seleccionada

La selección se puede *borrar* haciendo clic en **RMB** en el histograma.

El modo en que se representan algunos de los valores anteriores depende de la precisión seleccionada en la sección inferior del panel, como se indica a continuación:

* **8 bits**: 0-255 entero

* **16 bits**: 0-65532 entero

* **32 bits**: valor de punto flotante sin formato

Algunas partes del histograma pueden incluir valores de recuento de píxeles muy bajos y, por lo tanto, son difíciles de leer. En este caso, puede habilitar el modo **raíz cuadrada** mediante el botón **Sqrt**, que usa la *raíz cuadrada de los valores reales* para dibujar el histograma.

+++

## Barra de herramientas Mostrar

La barra de herramientas **Display**, que se encuentra en la *parte inferior* del panel **Vista en 2D** de forma predeterminada, te permite controlar cómo se muestra la imagen en la ventana gráfica.

La sección *más a la izquierda* incluye controles para *color* y *transparencia*, mientras que la sección *más a la derecha* incluye los controles de *ventanilla* detallados en la sección Ventana gráfica de esta página.

>[!NOTE]
>
> La barra de herramientas se puede *recolocar* alrededor del panel **Vista en 2D** usando el *controlador* más a la izquierda representado por tres líneas paralelas.

![Canales de color de vista 2D](../../assets/2d-view-color-channel.png "Canales de color de vista 2D"){width="360px"}

### Canales de color

Puede mostrar un solo canal de la imagen mediante el botón ![](../../assets/2d-view-icon-channels.png) <b>Canales de color</b>. Se abre un cuadro combinado que permite seleccionar los canales <b>Rojo</b>, <b>Verde</b>, <b>Azul</b> y <b>Alpha</b> que se deben mostrar. El aspecto normal de la imagen con todos los canales se restaura seleccionando la opción <b>RGB</b>.

Se pueden usar los siguientes *métodos abreviados de teclado* para cambiar rápidamente a canales de color diferentes:

* RGB: <b>C</b>
* Rojo: <b>R</b>
* Verde: <b>G</b>
* Azul: <b>B</b>
* Alpha: <b>A</b>

El *icono* del botón <b>Canales de color</b> *cambia* dependiendo de los canales de visualización actuales.

>[!NOTE]
>
> Los métodos abreviados de teclado solo se pueden utilizar si el panel Vista 2D tiene el foco. Puede hacer clic en este panel al menos una vez para asegurarse de que es así.
> 
> Dado que el panel necesita foco, estos métodos abreviados *no interfieren* con ningún *método abreviado personalizado* que hayas establecido para crear nodos en el gráfico. Obtén más información sobre esta función [aquí](../../interface/preferences-window/preferences-window.md).

![conmutador de transparencia de vista 2D](../../assets/2d-view-transparency.png "conmutador de transparencia de vista 2D"){width="360px"}

### Alternar Transparencia

La visualización de transparencias se puede activar y desactivar mediante el botón ![](../../assets/2d-view-icon-transparency-off.png)/![](../../assets/2d-view-icon-transparency-on.png) <b>Mostrar tablero de ajedrez</b>. Cuando esta opción está activada, la transparencia se muestra mediante un patrón de tablero de ajedrez.

Hay dos formas principales de interpretar la transparencia, que se pueden seleccionar mediante el botón ![](../../assets/2d-view-icon-transparency-straight.png)/![](../../assets/3d-view-icon-transparency-premultiplied.png) <b>Modo de transparencia</b>:

<b>![](../../assets/2d-view-icon-transparency-straight.png) Recto:</b> la información de transparencia solo se almacena en el canal alfa y no afecta a ningún otro aspecto de la imagen

<b>![](../../assets/3d-view-icon-transparency-premultiplied.png) Premultiplicado:</b> la información de transparencia se almacena en el canal alfa y también afecta a los canales RGB, ya que se multiplican de forma efectiva en el canal alfa

Para mostrar *colores correctos*, debe seleccionarse el modo de transparencia apropiado en el panel <b>vista 2D</b> para que coincida con el método de transparencia que se aplicó cuando se *creó* la imagen.

![Espacio de color de vista 2D](../../assets/2d-view-viewport-color-space.png "Espacio de color de vista 2D"){width="360px"}

### Espacio de color

Para obtener la representación más precisa del color, las imágenes se muestran de forma predeterminada en un *espacio de color* que coincide con el utilizado por el *monitor*.

Los controles disponibles y el efecto del botón ![](../../assets/2d-view-icon-color-space.png)/![](../../assets/2d-view-icon-color-space-linear.png) <b>Espacio de color</b> dependerán del [Modo de administración de color](../../color-management/color-management.md) establecido en la [configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md). Obtenga más información sobre estos controles en la sección Administración de color de esta página.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Herramientas de pintura de mapa de bits

Las <b>herramientas de pintura de mapas de bits</b> están disponibles para [recursos de mapas de bits](../../resources/bitmap-resource/bitmap-resource.md) que cumplen estos criterios:

* El mapa de bits usa la precisión de *8 bits*
* El recurso de mapa de bits está *importado* en el paquete, las imágenes vinculadas *no* son compatibles

>[!NOTE]
>
> Los *nuevos* recursos de mapa de bits creados en Substance 3D Designer *coincidirán* automáticamente con estos criterios.

</td>
<td style="border: 0;" valign="top">

![Herramientas de pintura de mapa de bits de vista 2D](../../assets/2dview-paintingtools-main.png "Herramientas de pintura de mapa de bits de vista 2D")

</td>
</tr>
</table>

>[!TIP]
>
> Puede obtener más información en la página [Herramientas de pintura de mapas de bits](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) de la documentación.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Editor de vectores

El <b>Editor de gráficos vectoriales</b> está disponible para *recursos de [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) importados*, los recursos vinculados *no* son compatibles.

>[!NOTE]
>
> Los *nuevos* recursos de SVG creados en Substance 3D Designer *coincidirán automáticamente* con este criterio.

</td>
<td style="border: 0;" valign="top">

![Editor de gráficos vectoriales de vista 2D](../../assets/2dview-vectorediting-main.png "Editor de gráficos vectoriales de vista 2D")

</td>
</tr>
</table>

>[!TIP]
>
> Puede obtener más información en la página [Herramientas de edición de vectores](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) (obsoletas) de la documentación.

![Administración de color de vista 2D](../../assets/2d-view-color-management-ocio.png "Administración de color de vista 2D"){width="360px"}

## Gestión de colores

La <b>vista 2D</b> ofrece controles sencillos de *administración del color* para permitirte elegir qué *espacio de color de visualización* se debe usar al mostrar la imagen.

Estos controles se adaptarán al [modo de administración de color](../../color-management/color-management.md) actual establecido en la [configuración del proyecto](../../interface/preferences-window/project-settings/project-settings.md), de la siguiente manera:

* <b>Heredado:</b> se puede disp.lay la imagen en los espacios de color sRGB ![](../../assets/2d-view-icon-color-space.png) o sRGB lineal ![](../../assets/2d-view-icon-color-space-linear.png);
* <b>ACE de Adobe:</b> puedes *habilitar* la administración de color y establecer el espacio de color más apropiado para el *monitor actual* según lo detectado por el motor de ACE de Adobe, o ![](../../assets/2d-view-icon-color-space-linear.png) *deshabilitar* la administración de color y mostrar la imagen usando los valores de color RAW;![](../../assets/2d-view-icon-color-space.png)
* <b>OCIO:</b> puede ![](../../assets/2d-view-icon-color-space.png)habilitar *la administración de color y establecer la más adecuada para el* monitor actual *según lo detecte el motor de OCIO, usar el cuadro combinado y seleccionar cualquiera de los* espacios de color de visualización *disponibles en el [OCIO archivo de configuración](../../color-management/color-management.md) que se usa actualmente, o ![](../../assets/2d-view-icon-color-space-linear.png)* deshabilitar *la administración de color y mostrar la imagen usando los valores de color Raw.*

>[!WARNING]
>
> Ten en cuenta que estos controles *solo* afectan al *espacio de color de visualización*. El *espacio de color original* de las imágenes y el *espacio de color de trabajo* también deben tenerse en cuenta para garantizar que los colores se muestren correctamente en el **vista 2D**.

>[!TIP]
>
> Vaya a la sección [Administración de color](../../color-management/color-management.md) de esta documentación para obtener más información sobre esta función y su implementación más amplia en Designer.
