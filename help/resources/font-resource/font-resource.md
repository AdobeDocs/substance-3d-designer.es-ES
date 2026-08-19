---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: Importa y utiliza recursos de fuentes en Substance 3D Designer para añadir texto y tipografía a tus materiales.
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recurso de fuente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Recurso de fuente

Los recursos de fuentes están pensados para usarse junto con el [nodo de texto atómico](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md). Le permiten utilizar fuentes que no están instaladas en el sistema, haciendo referencia a un archivo de fuente en cualquier lugar del disco.

>[!NOTE]
>
> **Fuentes en SBSAR**
> 
> Las fuentes siempre se incrustan en un SBSAR, independientemente de si proceden de un recurso vinculado o de si se utiliza una fuente instalada en el sistema. La ventaja de este método es que no es necesario instalarlo y, al exportar un archivo SBS con dependencias, puede estar seguro de que vienen los archivos de fuentes.

## Uso de recursos de fuentes personalizados

* Haga clic con el botón derecho en un paquete y elija <b>Vínculo > Fuente</b>
* Seleccione un archivo .otf o .ttf.
* Coloca un [nodo de texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) en tu [gráfico](../../compositing-graphs/substance-compositing-graphs.md).
* En la propiedad <b>Font </b>, los recursos de fuentes se encuentran en la parte superior de la lista.

Tenga en cuenta que la lista de fuentes no se actualiza automáticamente con las propiedades abiertas. Tendrá que cambiar a otra ventana de propiedades y volver a un nodo de texto para ver las fuentes recién vinculadas.
