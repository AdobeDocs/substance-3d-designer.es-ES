---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: Aprenda a importar, vincular y crear nuevos recursos en Substance 3D Designer para sus proyectos de materiales.
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Importación, vinculación y nuevos recursos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 2%

---


# Importación, vinculación y nuevos recursos

[Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html) admite tres modos de traer o crear nuevos recursos para su uso en el gráfico. Estos recursos pueden ser de muchos tipos diferentes, entre ellos [mapas de bits](../../resources/bitmap-resource/bitmap-resource.md), [gráficos vectoriales](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md), [escenas 3D](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html) y [fuentes](../../resources/font-resource/font-resource.md). Esta página explica los diferentes métodos y cuándo es mejor usar cada uno.

Se tiene acceso a todos los métodos [haciendo clic en RMB en un paquete en el Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html) [.](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)

En la siguiente tabla se ofrece una visión general rápida de la diferencia de funciones entre los métodos.

|                                                                                                                                                                         | Nuevo | Importar | Vincular |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Gráficos ([gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md), [gráficos de funciones de Substance](../../function-graphs/function-graphs.md) | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(error)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| [Mapas de bits](../../resources/bitmap-resource/bitmap-resource.md),[&#x200B; gráficos vectoriales (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| [escenas 3D](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html), [fuentes](../../resources/font-resource/font-resource.md) | <div><img alt="(error)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(error)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Se crea junto al archivo SBS | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Editable en Designer | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(error)&quot; data-preserve-html=&quot;true" src="../../assets/error.svg"/></div> |
| Las ediciones externas se sincronizan automáticamente | <div><img alt="(error)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(error)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |
| Incrustado en SBSAR publicado | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(marca)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(marca)&quot; data-preserve-html=&quot;true" src="../../assets/check.svg"/></div> |

## Nuevos recursos

Crear un nuevo recurso significa que un recurso del paquete se creará desde cero. Todos los recursos de solo Designer solo se pueden crear de esta forma, como gráficos de Substance y gráficos de funciones de Substance.

Un caso especial es cuando se crea un nuevo [mapa de bits](../../resources/bitmap-resource/bitmap-resource.md) o [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md): estos archivos aparecerán en el Explorador y se comportarán como un recurso importado, pero sin requerir un archivo externo. Se pueden modificar en Designer. Los nuevos mapas de bits y los de SVG creados de esta forma son útiles si no necesita utilizar un editor externo: por ejemplo, cuando sólo desea una forma vectorial rápida y sencilla o una máscara de mapa de bits 2D simple pintada.

## Recursos importados

Importar un recurso significa que se creará un duplicado del archivo de recursos junto al archivo SBS (en la carpeta *Graphname*.resources), [excepto para los archivos de SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md). A veces también se hace referencia a él como &quot;incrustado&quot; de un recurso.

Un recurso importado se puede editar en Designer con las [herramientas de pintura de mapas de bits](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) o las [herramientas de edición vectorial](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) de la [vista 2D](../../interface/2d-view/2d-view.md), una vez colocadas en el gráfico. Los recursos importados ya no están vinculados a sus archivos de origen originales: Esto significa que si cambia, quita o actualiza el archivo importado originalmente, esto no tendrá ningún efecto en el recurso de Designer.

En el caso de [AxF files](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md), el proceso es un poco más complicado; Los gráficos de Substance y los recursos de mapa de bits se crean a partir del paquete AxF. Sin embargo, todas ellas pueden seguir editándose en sus respectivos editores: Vista de gráfico o vista 2D.

>[!WARNING]
>
> En el caso de los paquetes nuevos, los recursos importados y nuevos no se guardan en el disco hasta que se guarda el paquete.

## Recursos vinculados

Vincular un recurso significa que Designer hará referencia al archivo de origen en su ubicación original en el disco, pero lo presentará en el Explorador como si fuera parte del paquete. No podrá editar el recurso real directamente dentro de Designer, solo utilícelo como componente en el gráfico o como origen para los mapas bancarios.

La vinculación es ideal si sabe que necesitará utilizar un editor externo para actualizar el recurso mientras trabaja simultáneamente en Designer. Los mapas de horneado son un buen ejemplo: puede disponer de mapas de bits de referencia de Designer desde una aplicación de banca externa, que volverá a cargar y actualizar automáticamente el gráfico en cuanto se cambien estos archivos. Del mismo modo, las escenas 3D solo se pueden vincular, de modo que cada vez que se exporta un nuevo archivo FBX desde una aplicación 3D, Designer actualiza automáticamente la malla utilizada en la vista 3D. Si usted está horneando mapas de esta malla tendrá que iniciar manualmente el proceso de horneado de nuevo, idealmente haciendo clic en RMB y seleccionando &#39;Actualizar todos los mapas con bake&#39;.

## Eliminación de recursos

Al eliminar un recurso de un paquete, se muestra el cuadro de diálogo <b>Confirmar la eliminación del elemento</b>. Si otros recursos ** hacen referencia a algún elemento en proceso de eliminación, como [instancias de gráficos](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) y [recursos de mapa de bits](../../resources/bitmap-resource/bitmap-resource.md) utilizados en [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md), el cuadro de diálogo incluirá una *advertencia y una lista* de estos elementos.

>[!NOTE]
>
> Se recomienda tener en cuenta estos elementos y tomar las medidas necesarias para *anticiparse a cualquier dependencia rota* que se produciría al eliminar elementos de un paquete.\
> Estas acciones pueden incluir *quitar todos los usuarios* de estos recursos antes de la eliminación.

![&#39;Recurso eliminado en uso&#39; advertencia](../../assets/confirm-item-removal.png "&#39;Recurso eliminado en uso&#39; advertencia"){width="512px"}
