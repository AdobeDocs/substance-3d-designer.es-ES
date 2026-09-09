---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Utilice el nodo de filtro Clonar para duplicar y desplazar regiones de textura para crear patrones y efectos de mosaico perfectos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clonar (Nodo de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 4%

---


# Clonar (Nodo de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-filter-node.resources/clone-4.png)

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Los Clonar introducen la imagen una vez en una ubicación especificada. Puede funcionar como una cruda herramienta de &quot;tampón de clonar&quot;.

Requiere un poco de cuidado para obtener los resultados esperados:

* Lo ideal es que la imagen de entrada tenga un canal alfa (como una pegatina), ya que la fusión es solo una copia recta.
* La máscara se establece de forma predeterminada en negro, por lo que, para ver los resultados, debe conectarse al menos un valor de escala de grises blanca uniforme.
* El desplazamiento se recortará fuera de la imagen fácilmente, por lo que debe utilizar valores pequeños.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Origen</b> <i>Entrada de color</i> | Imagen para clonar. Importante: lo ideal es que la imagen tenga un canal alfa. |
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. El valor predeterminado es negro. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Desplazamiento</b> <i>-</i> | Mueve o traduce el resultado. Positivo es Izquierda y Arriba, Negativo es Derecha y Abajo. Use valores pequeños, 1.0 y superior lo mueve fuera de la imagen. |
| <b>Máscara de desenfoque</b> <i>0.0 - 10.0</i> | Aplica un filtro de desenfoque a la máscara para suavizar los bordes. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="clone-filter-node.resources/clone-example.png" />
        </td>
    </tr>
</table>
