---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/vector-graphics-svg-resource.html"
breadcrumb-title: ''
description: Importa y utiliza gráficos vectoriales de SVG como recursos en Substance 3D Designer para la creación de materiales por procedimientos.
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recurso de gráficos vectoriales (SVG)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 2%

---


# Recurso de gráficos vectoriales (SVG)

Substance 3D Designer admite una forma limitada de gráficos vectoriales, a través del formato de gráficos vectoriales escalables. Los archivos de SVG se pueden incorporar como recursos de diferentes maneras para utilizarlos como recursos para los gráficos.

Los archivos de SVG [ se pueden crear o editar a través del nodo del SVG atómico,](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) también se pueden crear a través de [el UV para el SVG baker.](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/convert-uv-to-svg)

>[!NOTE]
>
> Los archivos de Adobe Illustrator (**.ai**) *no* son compatibles actualmente.

## Almacenamiento de SVG

El almacenamiento del SVG depende de si están vinculados o importados. Los archivos de SVG importados se incrustan en el archivo SBS, por lo que [no requieren archivos externos como Bitmaps](../../resources/bitmap-resource/bitmap-resource.md), y se pueden editar con las [herramientas de edición de vectores](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Atributos de SVG

Los recursos de SVG de un paquete tienen una serie de atributos que puede personalizar. La mayoría de los atributos no tienen un propósito principal y son para filtros de biblioteca, pero una minoría afecta a la calidad de procesamiento.

| Nombre del atributo | Propósito |
| --- | --- |
| Identificador | Se utiliza para hacer referencia al recurso SVG en un paquete, debe ser único. |
| Ruta de archivo | Ruta de acceso en el disco del archivo de SVG al que hace referencia el recurso. |
| Descripción | La descripción que se muestra en la información sobre herramientas de [Explorer](../../interface/the-explorer-window/the-explorer-window.md) y [Library](../../interface/the-library/the-library.md) para este recurso. |
| Categoría | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| Etiqueta | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| Autor | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| URL del autor | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| Etiquetas | Se usa para [ordenar y seleccionar el recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) en la [biblioteca](../../interface/the-library/the-library.md). |
| Datos del usuario | Datos adicionales opcionales que no se utilizan en gráficos vectoriales. |
| Mostrar en biblioteca | Determina si el recurso SVG debe estar oculto en [la vista Biblioteca.](../../interface/the-library/the-library.md) |
| calidad de gráficos vectoriales | Afecta a la calidad de procesamiento. El rango no es lineal y la mejor calidad se alcanza en 0,5. |

## Creación de SVG

Dado que solo se admite un conjunto limitado de funciones, la creación de documentos de SVG está restringida.

En general, lo siguiente es cierto:

* Sólo se garantiza que las formas simples y simples y los trazados se dibujen correctamente;
* El trazo es compatible, pero solo produce un trazo de 1 píxel de ancho y el estilo del trazo se omite;
* Los estilos de línea discontinua se romperán definitivamente;
* El texto debe convertirse en trazados o contornos para que se pueda representar;
* No se admiten [rutas compuestas](https://helpx.adobe.com/ie/illustrator/using/combining-objects.html#compound_paths);
* Las funciones avanzadas como los degradados no son compatibles;
* No se admiten elementos de estilo para propiedades CSS.

## Opciones de exportación recomendadas

Las opciones de exportación son ligeramente diferentes para cada aplicación:

### Adobe Illustrator

[Illustrator](https://www.adobe.com/products/illustrator.html) te ofrece el máximo control sobre las exportaciones de tu SVG si prestas atención a las siguientes opciones.

* Use solo <b>Guardar como</b>, *no* Exportar como.
* <b>Perfil del SVG</b> no importa mucho, aunque el perfil Pequeño (en su mayoría) utilizará de forma predeterminada configuraciones que son definitivamente correctas;
* <b>Las fuentes</b> se deben establecer en <b>Convertir en esquema</b> para que funcionen;
* <b>Propiedades CSS</b> si *no* se establece en Elementos de estilo, el resto de opciones funcionarán;
* Desmarque <b>Conservar capacidades de edición de Illustrator</b>;
* Desmarque <b>Responsive</b>;
* Los trazos no funcionarán bien. Usa <b>Objeto > Ruta > Dar contorno a trazado</b> para que aparezcan.

La imagen de la derecha muestra las opciones de exportación recomendadas, haga clic en ella para mostrarla a tamaño completo.

>[!IMPORTANT]
>
> Las mesas de trabajo pueden afectar al resultado del archivo de SVG generado. Algunas plantillas de archivo de Illustrator presentan varias mesas de trabajo.\
> Intente tener solo una mesa de trabajo recortada correctamente y seleccionarla en la ventana Mesa de trabajo al guardarla como SVG.

![Opciones de exportación de SVG de Illustrator](../../assets/svg-export-options-ai.jpg "Opciones de exportación de SVG de Illustrator"){width="512px"}

### Inkscape

Inkscape guarda de forma nativa como SVG, pero con menos control sobre el formato de archivo. Los archivos de Inkscape funcionarán principalmente de forma nativa en la aplicación, pero con algunas limitaciones:

* Los trazos solo se muestran con un ancho de 1 px en Substance 3D Designer. Usa <b>Ruta > Trazo a trazado</b> para que funcionen.
* El texto no funcionará. Usa <b>Ruta > Objeto a ruta</b> para que el texto funcione.

### Adobe Photoshop

Photoshop tiene un exportador de SVG muy limitado (<b>Archivo > Exportar > Exportar como...</b>) que actualmente no puede producir resultados correctos para Substance 3D Designer. Puede obtener información sobre la forma y la ruta, pero Style siempre se guarda como Elements, lo que no es compatible.

Se puede usar para máscaras de formas simples en blanco y negro, donde una solución es extraer el Alpha del SVG usando [Alpha Split](../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md).

Como alternativa, un SVG exportado por Photoshop puede ser [Importado](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md), lo que le permite [editar la información de estilo de forma nativa dentro de la aplicación.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)
