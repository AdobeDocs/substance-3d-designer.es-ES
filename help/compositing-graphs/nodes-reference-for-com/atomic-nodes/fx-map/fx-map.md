---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ""
description: Utilice el nodo FX-Map para aplicar gráficos de funciones a las texturas para crear patrones y efectos de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FX-Map
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%
---

# FX-Map

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Nodo atómico: FX-Map](fx-map.resources/fxmap.png "Nodo atómico: FX-Map"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0;" valign="top">

El FX-Map puede replicar y subdividir una entrada de imagen o patrón una y otra vez, y controlar la distribución de cada patrón gracias a los parámetros y funciones lógicas.

Es uno de los nodos atómicos más potentes, así como el nodo más complejo disponible en la aplicación.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="fx-map.resources/fxmap-tooltip.gif" alt="información sobre herramientas de fx-map" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

De manera similar al [procesador de píxeles](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), depende de usted definir y crear las funciones que determinan el comportamiento y la salida de este nodo.


>[!TIP]
>
> Echa un vistazo a la [guía especializada](../../../../function-graphs/fxmaps/fxmaps.md) para obtener más información sobre el proceso FX-Map.

>[!IMPORTANT]
>
> Se recomienda estar muy familiarizado con todos los aspectos del software y no tener problemas para crear [funciones matemáticas](../../../../function-graphs/function-graphs.md) para los parámetros antes de intentar usar el nodo FX-Map.


Tenga en cuenta que, a diferencia de otros nodos, la mayoría del comportamiento de FX-Map no está determinado por los parámetros, sino más bien [por la edición de las funciones FX-Map](../../../../function-graphs/fxmaps/fxmaps.md) que contiene.

|  |  |
| --- | --- |
| <b>Modo de color</b> *Booleano* | Alterna entre una imagen de salida en escala de grises y en color. El color será mucho más lento que la escala de grises. |
| <b>Fondo</b> *Float/Float4* | Define el color inicial del fondo en el que se deben componer los resultados. |
| <b>Área de procesamiento</b> *Float4* | Permite definir el rango de píxeles inicial para cada lado del FX-Map, lo que resulta en un efecto de estiramiento. |
| <b>Región de mosaico</b> *Float4* | Permite desplazar la distancia de mosaico del FX-Map. |
| <b>Sacar fuera</b> *Booleano* | Realiza una optimización mediante [selección](../../../../glossary/glossary.md) de patrones que se encuentran fuera del intervalo normal. |
| <b>Rugosidad</b> *Flotante* | Funciona como un multiplicador de profundidad y opacidad. Aplica un sesgo al proceso de fusión de mapa de divisas. |
| <b>Opacidad global</b> *Flotante* | Define la opacidad global de la salida del mapa de efectos. |

## Guía de FX-Map

*Próximamente.*

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Fondo</b> *Escala de grises/Color* PRINCIPAL | Color de fondo de la imagen de salida. |
| <b>Imagen de entrada #</b> *Escala de grises/Color* |  |


## Ejemplos

![](fx-map.resources/image2015-9-10-17-28-32.png)
