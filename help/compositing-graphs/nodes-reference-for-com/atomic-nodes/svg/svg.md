---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ""
description: Utilice el nodo SVG para importar y procesar gráficos vectoriales de SVG como texturas para crear elementos gráficos escalables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%
---

# SVG

<table>
<tr style="border: 0;">
<td width="20%" style="border: 0;" valign="top">

![Nodo atómico: SVG](svg.resources/comp_svg_1.png "Nodo atómico: SVG"){width="100%"}

</td>
<td style="border: 0;" valign="top">

Representa una [imagen de SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) como mapa de bits. En otras palabras, asigna formas vectoriales a píxeles.

Hay varias formas de crear este nodo, y todas ellas requieren que entiendas[la diferencia entre vincular e importar recursos](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="svg.resources/svg-tooltip.gif" alt="información sobre herramientas svg" /></div>

Puede crear el nodo desde cero o soltar un archivo de SVG en la vista de gráfico.


>[!TIP]
>
> Las imágenes de SVG generadas o importadas se pueden editar mediante las [herramientas de edición vectorial](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) del conjunto acoplado de la [vista en 2D](../../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Este nodo depende de un recurso externo, por lo que hay algunos puntos que deben tenerse en cuenta al trabajar con ellos:
> 
> * Los nodos SVG pueden devolver color o escala de grises, pero el valor predeterminado es color incluso si el recurso es un vector de escala de grises. Esto puede afectar al rendimiento y la complejidad del gráfico, así que asegúrese siempre de cambiar al [modo de color](#parameters) de escala de grises si es necesario.
> * Al eliminar un nodo de SVG no se elimina el [recurso de SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) en el [paquete](../../../../glossary/glossary.md), tienes que hacerlo manualmente en el [Explorador](../../../../interface/the-explorer-window/the-explorer-window.md).
> * Las formas de SVG se [teselan](../../../../glossary/glossary.md) en geometría/polígonos y, a continuación, se *rasterizan* para utilizarlas en Substance como mapas de bits. La tecnología utilizada para estas operaciones no admite varias propiedades vectoriales, como contornos. Obtenga más información sobre estas limitaciones [aquí](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

>[!WARNING]
>
> Las formas de SVG se [teselan](../../../../glossary/glossary.md) en geometría/polígonos y, a continuación, se *rasterizan* para utilizarlas en Substance como mapas de bits.
> 
> La tecnología utilizada para estas operaciones no admite varias propiedades vectoriales, como contornos.
> 
> Obtenga más información sobre estas limitaciones [aquí](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).


## Parámetros

|  |  |
| --- | --- |
| <b>Modo de color</b> *Booleano* | Determina el tipo de salida del nodo, para que se devuelva en color o en escala de grises. |
| <b>Color de fondo</b> *Color/Escala de grises* | Define el color de fondo de la imagen de salida para que se utilice en áreas no cubiertas por una forma vectorial.   La entrada &#39;[Background](#inputs)&#39; invalida *cuando esa entrada está conectada.* |
| <b>Ruta de acceso de recurso PKG</b> *Cadena* | Ruta de acceso al [recurso SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) al que hace referencia el nodo.   Se recomienda no escribir manualmente, pero copiar un recurso del explorador y pegarlo en el campo de texto del parámetro, o arrastrar y soltar un recurso de mapa de bits directamente desde el [Explorador](../../../../interface/the-explorer-window/the-explorer-window.md) al nodo SVG en el gráfico. |

## Herramientas de edición de vectores

Las formas vectoriales se pueden editar en Designer. Obtenga más información sobre las herramientas de edición en [esta sección](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Fondo</b> *Escala de grises/Color* PRINCIPAL | Define el color de fondo de la imagen de salida para que se utilice en áreas no cubiertas por una forma vectorial.   *Reemplaza el parámetro &#39;[Color de fondo](#parameters)&#39; al conectarse.* |


## Ejemplos

*Próximamente.*
