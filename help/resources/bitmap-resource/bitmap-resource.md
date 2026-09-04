---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: Aprenda a importar, crear y utilizar recursos de mapa de bits en Substance 3D Designer para la creación de materiales basados en texturas.
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recurso de mapa de bits
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 2%

---


# Recurso de mapa de bits

Un recurso de mapa de bits es un recurso de un paquete de Substance. Es diferente del nodo de mapa de bits atómico [. El nodo de mapa de bits atómico &#x200B;](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) es una representación específica de ese mapa de bits dentro de [un gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md).

Los mapas de bits son algunos de los recursos no gráficos más comunes de Substance 3D Designer, y su uso suele clasificarse en una de las siguientes categorías:

* Un mapa con bake, [hecho un bake internamente por Designer](../../bakers/bakers.md) o externamente por otra aplicación.
* Una textura auxiliar, como un patrón, mapa de suciedades o pegatina.
* Una simple máscara de escala de grises para fusionar, ya sea creada internamente usando [el nodo de mapa de bits](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) o con una aplicación externa.

## Almacenamiento de mapa de bits

Los mapas de bits suelen ser el recurso más grande con el que Designer trata. Es por eso que es bueno que entiendas cómo maneja Designer estos archivos con sus dos tipos de archivo principales.

### En archivos de Substance 3D (SBS)

El modo en que se almacenan los mapas de bits en SBS depende de si los [vincula o los importa, asegúrese de que está familiarizado con el concepto primero.](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) Los mapas de bits importados se pueden editar con las [herramientas de pintura de mapas de bits](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

A diferencia de los recursos de SVG (Gráficos vectoriales), los mapas de bits siempre se almacenan externamente, incluso cuando se crean como un nuevo recurso o se importan. En el caso de los paquetes de Substance nuevos, se guardan en la memoria hasta que se guarda el archivo .SBS en el disco. Una vez guardados en el disco, los mapas de bits se almacenan en una carpeta */resources* junto al archivo SBS.

### En Substance 3D Assets (SBSAR)

En [archivos SBSAR](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md), los mapas de bits están incrustados, lo que significa que tienen un gran impacto en el tamaño del archivo SBSAR final. Puede obtener más información sobre el impacto en el tamaño del archivo en esta página. Cuando se publican archivos SBSAR, sólo se incrustan los mapas de bits que se utilizan para calcular la salida de un gráfico. Cualquier mapa de bits no utilizado se optimiza y se excluye del paquete SBSAR final, sin efecto en el tamaño del archivo.

## Tipo de archivo, modo de color y resolución

Substance 3D Designer puede editar y reorganizar fácilmente los datos de mapas de bits, pero es mejor tener en cuenta lo siguiente:

* Define tus resoluciones para que sean compatibles con power of 2, lo que significa que debes cumplir con el tamaño de textura estándar en tiempo real, como <b>256, 512, 1024, 2048,</b>, etc. Designer reajustará las texturas fuera de este intervalo a la resolución coincidente más cercana. Tenga en cuenta que no tienen que estar en proporciones cuadradas.
* Se admiten muchos tipos de archivo, pero elija el que mejor se adapte a su caso. Los tipos de archivo <b>sin pérdida de compresión o incluso sin comprimir</b>, como PNG o TGA, ofrecen mejor calidad que JPG DDS o el .
* Asegúrate de <b>configurar el modo de color correctamente</b>, dependiendo de si necesitas color, escala de grises o un canal alfa.

## Atributos de mapa de bits

Los recursos de mapa de bits de un paquete tienen una serie de atributos que puede personalizar. La mayoría de los atributos no tienen un propósito principal y son para filtros de biblioteca, aunque una minoría afecta al tamaño de archivo.

| Nombre del atributo | Propósito |
| --- | --- |
| Identificador | Se utiliza para hacer referencia al recurso de mapa de bits en un paquete, debe ser único. |
| Ruta de archivo | Ruta de acceso en disco del mapa de bits al que hace referencia el recurso. |
| Descripción | La descripción que se muestra en la información sobre herramientas de [Explorer](../../interface/the-explorer-window/the-explorer-window.md) y [Library](../../interface/the-library/the-library.md) para este recurso. |
| Categoría | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| Etiqueta | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| Autor | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| URL del autor | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| Etiquetas | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| Datos del usuario | Datos adicionales opcionales, no utilizados en mapas de bits. |
| Mostrar en biblioteca | Determina si el mapa de bits debe estar oculto en [la vista de biblioteca.](../../interface/the-library/the-library.md) |
| Formato de mapa de bits | Tanto RAW como Jpeg, tienen un gran efecto en el tamaño de archivo SBSAR. Consulta nuestras [directrices de reducción de tamaño de archivo](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) para obtener más información. |
| Calidad de compresión de mapa de bits | Solo tiene un efecto con la compresión JPEG y determina el equilibrio calidad/tamaño de archivo. |

## Reducción de tamaño de archivo

Consulte la página [Directrices de reducción de tamaño de archivo](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) en la sección [Prácticas recomendadas](../../best-practices/best-practices.md) para ver nuestras recomendaciones sobre cómo minimizar el tamaño de archivo de los mapas de bits incrustados en [contenidos de Substance 3D publicados (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md).
