---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/publishing-substance-3d-asset-files-sbsar.html"
breadcrumb-title: ''
description: Aprenda a publicar archivos de recursos de Substance 3D (SBSAR) desde Designer para su uso en otras aplicaciones y motores.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Publishing Substance 3D asset files (SBSAR)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Publicación de archivos de activos de Substance 3D (SBSAR)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 806f21d88d2ce6b63164848f4f52906ec57471a3
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 1%

---


# Publicación de archivos de activos de Substance 3D (SBSAR)

Esta página explica cómo Substance 3D Designer puede publicar paquetes como archivos <b>Substance 3D asset</b>, un formato de archivo especial con la extensión <b>SBSAR</b>, que se utiliza en el ecosistema del Substance, así como en otras aplicaciones que lo admiten.

Por lo general, es mejor utilizar un recurso de Substance 3D en lugar de mapas de bits, ya que es mucho más flexible y ligero. Si los usas en Substance 3D [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home), [Sampler](https://helpx.adobe.com/substance-3d-sampler.html) o [Player](https://helpx.adobe.com/substance-3d-player/home.html), es más rápido usar la funcionalidad [Enviar a](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/send-to-215286290.html).

![Publicación de archivos SBSAR simplificada](../../assets/exportflow.png "Publicación de archivos SBSAR simplificada")

## Conceptos de publicación

es conveniente tener en cuenta lo siguiente al publicar un gráfico de Substance:

* Usted<b> publica un paquete</b>, con todo su contenido, no un [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) individual. A continuación, un recurso de Substance 3D le permite generar contenido a partir de todos los gráficos de Substance dentro de este paquete.
* Los paquetes publicados son <b>completamente independientes</b>: todos los recursos necesarios se incrustan en el archivo. Esto significa que son mucho más fáciles de compartir que los archivos SBS.
* El resultado de los recursos de Substance 3D puede ser <b>completamente dinámico</b>. [La resolución no está establecida; se pueden modificar los parámetros expuestos.](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) Sin embargo, ya no es posible editar el gráfico.
* Los recursos de Substance 3D se pueden usar fuera de Designer, en todos los productos de Adobe de Substance 3D, Adobe Dimension y cualquier otra aplicación que tenga [Substance integration](https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/home).
* Publicar es diferente de [Exportar](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md), asegúrate de entender bien la diferencia.

## Preparándose para publicar

La publicación requiere más preparación que la exportación de mapas de bits. Esto se debe a que los recursos de Substance 3D publicados son herramientas dinámicas, no solo una instantánea estática del estado actual de las texturas. En concreto, debe tener en cuenta lo siguiente:

* Asegúrate de que las resoluciones gráficas ([Tamaño de salida](../../compositing-graphs/output-size/output-size.md)) estén establecidas en el *método de herencia [Relativo al principal*](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), lo que significa que son dinámicas y se pueden cambiar sobre la marcha.
* Asegúrese de que [las salidas de gráficos](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) estén configuradas correctamente con nombres, etiquetas y etiquetas de uso.
* Asegúrese de que los [parámetros, si son necesarios, están organizados y tienen un nombre correcto](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).
* Si un gráfico describe un material, establezca su atributo [modelo de material](../graph-parameters/graph-parameters.md) en el modelo de ese material.
* Asegúrese de que la propiedad [Output size](../../compositing-graphs/output-size/output-size.md) de todos los nodos [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) esté establecida en el *método de herencia [Absolute*](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). Si no es así, su [recurso de mapa de bits](../../resources/bitmap-resource/bitmap-resource.md) al que se hace referencia se guardará con la resolución <b>256\*256</b> predeterminada en el archivo de recursos de Substance 3D publicado, lo que* afectará a la calidad* de una o más salidas.
* Si hay gráficos en el paquete que no deberían estar disponibles fuera de Designer (por ejemplo, subgráficos de herramientas o de ayudantes que solo funcionan en un contexto específico), configúrelos para que se oculten en sus propiedades. Ver más abajo.

## Métodos de publicación

Una vez que esté listo para publicar, hay dos formas de tener acceso al cuadro de diálogo Publicación, ambas a través de [la ventana del explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

En la [ventana del explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), haga clic con el botón derecho en el paquete y seleccione el archivo ![](../../assets/image2020-9-23-9-39-58.png) **Publish .sbsar...**, tecla de acceso rápido alternativa Ctrl + P.

Después de publicar con el cuadro de diálogo una vez, también puedes usar ![](../../assets/image2020-9-23-11-15-35.png) **archivo .sbsar de Publish como anterior** para repetir el proceso de publicación sin ver los cuadros de diálogo, y publicarlo inmediatamente con la misma configuración.

</td>
<td style="border: 0;" valign="top">

![](../../assets/publish-rightclick.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

En la [ventana del Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), haciendo clic en el botón Publish ![](../../assets/image2020-9-23-9-39-58.png) en la barra de herramientas superior.

Después de publicar con diálogo una vez, también puede utilizar el botón Publish como anterior ![](../../assets/image2020-9-23-11-15-35.png) para repetir el proceso de publicación sin ver los cuadros de diálogo, publicando inmediatamente con la misma configuración.

</td>
<td style="border: 0;" valign="top">

![](../../assets/publish-toolbutton.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Opciones de publicación de activos

Antes de que aparezcan las Opciones de Publish de activos, se le pedirá que guarde el archivo Substance 3D (SBS) si no se ha hecho esto, y se le preguntará dónde guardar el activo de Substance 3D. Para evitar ver las indicaciones y el cuadro de diálogo del archivo y sacar el archivo más rápido, usa <b>Publish como métodos anteriores</b> descritos anteriormente.

</td>
<td style="border: 0;" valign="top">

![Opciones de publicación de activos](../../assets/publish-dialog.png "Opciones de publicación de activos")

</td>
</tr>
</table>

Están disponibles las siguientes opciones:

<b>Ruta de archivo</b> abre un cuadro de diálogo para elegir dónde guardar el archivo de recursos de Substance 3D. La ruta predeterminada son los documentos de usuario del sistema. Si el paquete se ha guardado, la ruta es la ubicación del paquete. Si el paquete se publicó durante la sesión, la ruta es la última ubicación de publicación.

<b>Compresión de archivo</b> establece opciones de compresión para el archivo, afecta al tamaño del archivo.

<b>Generar iconos que faltan</b> usa técnicas integradas de [Renderización PBR](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) para crear miniaturas para los atributos de cada gráfico.

<b>Gráficos expuestos </b>enumera todos los gráficos que se expondrán en este paquete; vea a continuación para ver los gráficos excluidos.

>[!NOTE]
>
> **Exposición aleatoria de la semilla**
> 
> Los ajustes de exposición de Raíz aleatoria ya no están disponibles en el cuadro de diálogo Publish. En su lugar, establezca el atributo semilla aleatorio de su [gráfico en Absoluto en lugar de en relativo para evitar que esté disponible.](../../compositing-graphs/graph-parameters/graph-parameters.md)

## Exclusión de gráficos del activo publicado

Es posible que algunos gráficos de su paquete no estén pensados para su uso en exteriores. Estos subgráficos suelen ser parte de un todo más grande, una subrutina de un material maestro.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Para evitar que un gráfico se vuelva visible o utilizable dentro de un archivo de recursos de Substance 3D, accede a las propiedades de ese gráfico (haz doble clic en el área vacía de la vista del gráfico o haz clic una vez en el gráfico en el explorador) y, a continuación, abre el despliegue <b>Atributos</b>. Establezca <b>Exposed in SBSAR</b> en <b>No</b> para ocultarlo cuando se publique.

</td>
<td style="border: 0;" valign="top">

![](../../assets/image2020-9-23-10-40-21.png)

</td>
</tr>
</table>

### Advertencias del cuadro de diálogo Publish

En ocasiones, el cuadro de diálogo Publish muestra advertencias en amarillo. Los más comunes se enumeran a continuación, con una explicación y solución.

* Uno o más gráficos no tienen salida\
  Esta advertencia significa que está intentando publicar un paquete con uno o más gráficos que no tienen nodos de salida. La solución es agregar [nodos de salida](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) a los gráficos con un triángulo de advertencia amarillo.
* Uno o más gráficos tienen un parámetro de tamaño de salida no relacionado con el elemento principal\
  Esta advertencia significa que uno o más gráficos se han configurado con tamaños de salida incorrectos. Normalmente son las propiedades de un gráfico en sí. La advertencia significa que no tendrá control de resolución dinámico sobre este gráfico cuando se publique. La solución consiste en ir a las propiedades gráficas de los usuarios con un triángulo amarillo y establecer el [método de herencia](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) del tamaño de salida en *Relativo al principal*.

## Limitaciones de recursos de Substance 3D

Si bien el recurso de Substance 3D es el formato más potente y dinámico del ecosistema Substance, hay algunas pequeñas limitaciones técnicas que debe tener en cuenta.

* Los paquetes de recursos de Substance 3D publicados son un formato de archivo unidireccional. No se puede &quot;descompilar&quot; un recurso de Substance 3D en un archivo Substance 3D (SBS). La única forma de &quot;editar&quot; un recurso de Substance 3D es editar el archivo Substance 3D original. Todavía puede utilizar el contenido del paquete de recursos de Substance 3D como nodos dentro de nuevos Substance (abrir y arrastrar y soltar), por lo que no es una limitación enorme.
* Los archivos de recursos de Substance 3D tienen versiones que deducen la compatibilidad. El Substance Engine principal se actualiza de vez en cuando con nuevas funciones. las aplicaciones compatibles con estas nuevas características deben leer los paquetes que utilizan estas características. Esto no es un problema para todas las aplicaciones de Substance, ya que se actualizan al mismo tiempo, pero los complementos y las integraciones pueden tener retrasos de compatibilidad más largos.\
  Utilice las opciones de visualización de compatibilidad de Substance Engine en [Preferencias del proyecto](../../interface/preferences-window/project-settings/project-settings.md) para detectar cualquier problema potencial.
* Algunos parámetros expuestos, como *static*, están *ocultos* una vez que se publica un gráfico como parte de un recurso de Substance 3D. Consulte la sección [Limitaciones](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) de la página [Exposición de un parámetro](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) para obtener una lista de estos parámetros y obtener más información sobre los parámetros estáticos en general.
