---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ""
description: Utilice el nodo Mapa de bits para importar y utilizar imágenes de mapa de bits como texturas en los gráficos de composición de Substance.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapa de bits
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%
---

# Mapa de bits

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atómico: Bitmap](bitmap.resources/comp_bitmap.png "Nodo atómico: Bitmap"){width="20%"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Carga un [recurso de mapa de bits](../../../../resources/bitmap-resource/bitmap-resource.md) en el gráfico.

Este nodo se utiliza para importar un [mapa de bits](../../../../glossary/glossary.md) en el gráfico o para crear un nuevo mapa de bits para su uso con las [herramientas de pintura de mapas de bits](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

Hay varias formas de crear este nodo, y todas ellas requieren que entiendas[ la diferencia entre vincular e importar recursos.](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="bitmap.resources/bitmap-tooltip.gif" alt="información sobre herramientas de mapa de bits" /></div>

Puede crear el nodo desde cero o soltando un [mapa de bits](../../../../glossary/glossary.md) en un formato compatible en la vista de gráficos.


>[!TIP]
>
> Los mapas de bits de 8 bits generados o importados se pueden pintar usando las [herramientas de pintura de mapas de bits](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) del conjunto acoplado [Vista 2D](../../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Este nodo depende de un recurso externo, por lo que hay algunos puntos que se deben tener en cuenta al trabajar con ellos:
> 
> * Los nodos de mapa de bits pueden devolver color o escala de grises, pero el valor predeterminado es color aunque el recurso sea un mapa de bits en escala de grises. Esto puede afectar al rendimiento y la complejidad del gráfico, así que asegúrese siempre de cambiar al [modo de color](#parameters) de escala de grises si es necesario.
> * Al eliminar un nodo de mapa de bits no se elimina el [recurso de mapa de bits](../../../../resources/bitmap-resource/bitmap-resource.md) en el [paquete](../../../../glossary/glossary.md); debe hacerlo manualmente en el [Explorador](../../../../interface/the-explorer-window/the-explorer-window.md).
> * Por otro lado, tenga cuidado al eliminar un [recurso de mapa de bits](../../../../resources/bitmap-resource/bitmap-resource.md) en el Explorador: seguirá funcionando en el gráfico de esa sesión, ya que se guarda en la caché, pero el recurso se marcará como ausente la próxima vez que cargue el [paquete](../../../../glossary/glossary.md).
> * Cuando un gráfico de Substance está [preparado](../../../../glossary/glossary.md), la resolución del mapa de bits se fija en su resolución dentro del gráfico y no se basa en su tamaño original. Se recomienda asegurarse de que el &#39;Tamaño de salida&#39; [parámetro base](../../../../glossary/glossary.md) de un nodo de mapa de bits usa el [método de herencia](../../../../glossary/glossary.md) &#39;Absoluto&#39;, y el nodo va seguido de un nodo [Transformar 2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) establecido en &#39;Relativo al principal&#39; (es decir, la resolución del gráfico del host).


## Parámetros

|  |  |
| --- | --- |
| <b>Modo de color</b> *Booleano* | Determina el tipo de salida del nodo, para que se devuelva en color o en escala de grises. |
| <b>Ruta de acceso de recurso PKG</b> *Cadena* | Ruta de acceso al [recurso Bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) al que hace referencia el nodo.   Se recomienda no escribir manualmente, pero copiar un recurso del explorador y pegarlo en el campo de texto del parámetro, o arrastrar y soltar un recurso de mapa de bits directamente desde el [Explorador](../../../../interface/the-explorer-window/the-explorer-window.md) al nodo Mapa de bits del gráfico. |
| <b>Método Resize</b> *Entero* | Método de remuestreo que se utiliza para aumentar o reducir la escala de un mapa de bits:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Ampliación suave:</i> Aplica [filtrado bilineal](../../../../glossary/glossary.md) para interpolar sobre los píxeles de origen de la imagen ampliada.</li> <li data-preserve-html="true"><i>Ampliación más cercana:</i> Estire la imagen y use el color del píxel de origen más cercano tal cual.</li> </ul> |

## Herramientas de pintura de mapa de bits

Los mapas de bits se pueden editar en Designer. Obtenga más información sobre las herramientas de edición en [esta sección](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).


## Ejemplos

*Próximamente.*
