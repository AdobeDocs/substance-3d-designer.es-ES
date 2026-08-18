---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters/parameter-presets.html"
breadcrumb-title: ''
description: Aprenda a crear y utilizar ajustes preestablecidos de parámetros en Substance 3D Designer para guardar y aplicar configuraciones de parámetros.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Parameter presets
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parámetros preestablecidos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---


# Parámetros preestablecidos

Los ajustes preestablecidos de parámetros permiten al usuario almacenar y transferir grandes cantidades de valores preconfigurados para un conjunto de parámetros.Pueden ayudar en muchos escenarios y son más útiles cuando hay una gran cantidad de parámetros con una amplia gama de posibilidades.

Hay dos formas de almacenar y cargar ajustes preestablecidos, ambas con diferentes casos de uso, que se detallan a continuación.

![Cargar/guardar ajuste preestablecido menú desplegable](../../../assets/preset-menu.gif "Cargar/guardar ajuste preestablecido menú desplegable"){width="512px"}

## Ajustes preestablecidos externos

Los ajustes preestablecidos externos implican un archivo externo en el disco y un archivo \*.SBSPRS. Se pueden transferir entre diferentes gráficos y nodos, pero solo dentro de la aplicación. Su propósito principal es exactamente este: transferir un número de valores demasiado grande para copiarlos uno a uno.

Hay ajustes preestablecidos externos disponibles para todos los parámetros específicos en [instancias de gráficos](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), para la mayoría de los parámetros específicos en [nodos atómicos](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) ([las excepciones son esos parámetros que no se pueden exponer](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)) y para los parámetros de entrada expuestos en las propiedades de un gráfico [Graph.](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html)

Simplemente se guardan y se cargan en este menú. Los archivos SBSPRS guardados se pueden cargar en cualquier otro nodo o gráfico.

>[!NOTE]
>
> Incluso las coincidencias parciales funcionarán: los parámetros almacenados en un SBSPRS que no existen en el nodo cargado, simplemente se omitirán. Esto significa que puede transferir propiedades entre nodos que son en su mayoría similares, [ como la versión en color y escala de grises de Tile Sampler](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md). Se cargarán todos los parámetros compartidos. La coincidencia se produce en el identificador y el tipo.

![Edición de ajustes preestablecidos incrustados](../../../assets/preset-embed.gif "Edición de ajustes preestablecidos incrustados"){width="512px"}

## Ajustes preestablecidos integrados

Los ajustes preestablecidos incrustados funcionan de forma diferente a los ajustes preestablecidos externos. Su principal ventaja es que están contenidos dentro del archivo SBS o SBSAR, por lo que se pueden transferir y cargar fácilmente en Substance Painter, Maya y 3DS Max (actualmente no disponible en Substance 3D Sampler, UE4 y Unity). El usuario tampoco tiene que jugar con los archivos SBSPRS.

Sirven a un propósito diferente: no es posible transferirlos entre nodos y gráficos (para ello, tendría que usar Ajustes preestablecidos externos). También solo se pueden crear en los parámetros de entrada de las propiedades de un gráfico y solo dentro del modo de vista previa.

El flujo de trabajo es el siguiente:

1. Cambie a <b>modo de vista previa</b> para los <b>parámetros de entrada</b>
1. Defina los valores en el resultado deseado
1. Haga clic en <b>+</b> junto a la lista desplegable de ajustes preestablecidos para crear un nuevo ajuste preestablecido incrustado; el ajuste preestablecido se creará y almacenará inmediatamente

Los ajustes preestablecidos incrustados no se pueden modificar posteriormente, aunque se les puede cambiar el nombre. La modificación, así como su eliminación, se produce haciendo clic en el icono de engranaje situado junto al menú desplegable y el icono +. Presione el signo menos situado junto a un ajuste preestablecido para quitarlo.

No es necesario hacer nada más para habilitar los ajustes preestablecidos: una vez publicados como SBSAR, los ajustes preestablecidos estarán disponibles en Substance Painter tras la importación.

>[!IMPORTANT]
>
> La ficha <b>Ajustes preestablecidos</b> está deshabilitada al usar [edición en contexto](../../../interface/preferences-window/preferences-window.md).
