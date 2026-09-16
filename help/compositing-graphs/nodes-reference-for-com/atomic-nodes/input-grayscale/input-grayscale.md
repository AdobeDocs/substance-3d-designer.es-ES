---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/input-grayscale.html"
breadcrumb-title: ""
description: Utilice el nodo Escala de grises de entrada para crear parámetros de entrada de escala de grises para gráficas de Substance que los usuarios pueden exponer y ajustar.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Input grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escala de grises de entrada
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 1%
---

# Escala de grises de entrada

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Nodo atómico: Entrada en escala de grises](input-grayscale.resources/comp_inputgrayscale_1.png "Nodo atómico: Escala de grises de entrada"){width="100%"}

<b>En:</b> nodos atómicos

</td>
<td style="border: 0;" valign="top">

## Descripción

Los nodos de entrada son un tipo especial de nodo que crea una ranura dinámica en el gráfico, lo que permite que cualquier entrada se conecte una vez que el gráfico se utiliza en otro contexto.

A diferencia de [nodos de salida](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), debe colocar explícitamente una entrada Color, Escala de grises o Valor. No es posible crear sus propias entradas &quot;agnósticas&quot; que cambian de tipo dependiendo de lo que esté conectado a ellas.

Los nodos de entrada no son tan cruciales como [nodos de salida](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md): puede tener gráficos avanzados que funcionen a la perfección y que no necesiten una entrada. Las entradas solo se utilizan cuando se desea basar el resultado del gráfico o de la instancia de nodo en una entrada externa, por ejemplo, al crear una [instancia](../../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) o un [filtro](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/effects/filter) para Substance 3D Painter.

Consulte también: [Color de entrada](../input-color/input-color.md), [Valor de entrada](../input-value/input-value.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="input-grayscale.resources/input-grayscale-tooltip.gif" alt="Información sobre herramientas de escala de grises" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

## Parámetros

De forma predeterminada, un color de entrada o una escala de grises devuelve negro si no hay nada conectado. Puedes establecer un valor predeterminado diferente o arrastrar un [recurso de mapa de bits](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) existente desde el [Explorador](../../../../interface/the-explorer-window/the-explorer-window.md) hasta el nodo Entrada del gráfico, para obtener una vista previa de estos datos en la ranura. Esto solo funciona para las entradas de color y escala de grises. El valor predeterminado es persistente cuando se utiliza en otros contextos, el mapa de bits de previsualización se descarta en cualquier otro lugar.

Si desea verla con los resultados de otro gráfico, deberá exportar dicho gráfico a Bitmap para el método anterior o utilizar la edición &quot;en contexto&quot;.

|  |  |
| --- | --- |
| <b>Ruta de acceso de recurso PKG</b> *Cadena* | Señala a un recurso de mapa de bits personalizado para previsualizarlo. |
| <b>Valor predeterminado</b> *Color/Escala de grises/Valor* | Permite utilizar otro valor distinto del negro como entrada predeterminada, si no hay nada conectado a esta ranura. |

## Atributos

|  |  |
| --- | --- |
| <b>Identificador</b> *Cadena* | El único atributo único y obligatorio. No puede contener espacios. Este se utiliza para etiquetar entradas si no se ha configurado ninguna etiqueta y para diferenciar las diferentes salidas. ¡No deje esto en &quot;input\_1&quot;! |
| <b>Descripción</b> *Cadena* | Descripción opcional utilizada en la biblioteca de Designer y el estante de Painter. |
| <b>Etiqueta</b> *Cadena* | Etiqueta de interfaz de usuario utilizada para un etiquetado agradable en la interfaz de usuario de Designer y Painter. Puede contener espacios. Se recomienda configurar con un nombre similar al Identificador, solo con barras espaciadoras en lugar de guiones bajos. |
| <b>Datos de usuario</b> *Cadena* | Datos de usuario adicionales y opcionales que se pueden utilizar para operaciones de filtrado específicas. Básicamente, un campo de datos personalizado y comodín. |
| <b>Grupo</b> *Cadena* | Atributo de grupo utilizado para agrupar entradas para los [Modos de creación de vínculos](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) de Designer. Las entradas con un atributo de grupo idéntico (distingue mayúsculas de minúsculas) se presentarán como una única conexión en el modo de material compacto. |

## Herencia

<table>
<tr style="border: 0;">
<td style="border: 0; vertical-align: top">

Cuando hay varias entradas, debes prestar atención a la forma en que el gráfico [heredará sus parámetros base](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) de estas entradas.\
Los parámetros base incluyen, entre otros, <b>Tamaño de salida</b>, <b>Formato de salida</b> y <b>Modo de mosaico</b>.

Una entrada se puede definir como [entrada principal](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). A continuación, esta entrada controla los atributos de todas las entradas cuyo método de herencia está establecido en *Relativo al principal*. Este es el método de herencia *establecido de forma predeterminada* en los nodos Input.

</td>
<td width="25%" style="border: 0;" valign="top">

![Entrada principal en el gráfico del Substance](input-grayscale.resources/node-primary-input.png)

</td>
</tr>
</table>

Puede establecer un nodo de entrada como entrada principal de un gráfico haciendo clic en *RMB* en el nodo y seleccionando la opción <b>Establecer como entrada principal</b> en el menú contextual.\
La entrada principal de un nodo está marcada con un *pequeño punto oscuro en el conector* (en un círculo rojo en el ejemplo al lado de esta sección).

Alternativamente, cualquier entrada establecida en el método de herencia *Relativo a la entrada* heredará los atributos del nodo al que está conectada, *independientemente* de la entrada principal.

Por último, puede reemplazar cualquier valor para un atributo determinado estableciendo su método de herencia en *Absolute*.

>[!TIP]
>
> Para obtener más información sobre la herencia, vaya a la página [Herencia en los gráficos del Substance](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) de esta documentación.

>[!IMPORTANT]
>
> El método de herencia *Relativo a la entrada* para nodos de entrada *no es compatible* en [Substance 3D Assets (SBSAR)](../../../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md). Establezca todos los métodos de herencia de los nodos Input en *Relativo al principal* antes de publicar el paquete.

## Atributos de integración

Las entradas no se envían directamente a la Vista 3D, pero [Substance 3D Painter](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/home) utiliza sus atributos de uso para rellenar automáticamente las ranuras con determinados mapas (la mayoría de ellos se usan con [Filters](https://experienceleague.adobe.com/es/docs/substance-3d-painter/using/effects/filter)).

Además, los atributos de uso también se utilizan con [Modos de creación de vínculos](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md), para que coincidan con las ranuras de entrada y salida correctas.

<b>Uso</b>

|  |  |
| --- | --- |
| <b>Componente</b> *Cadena* | Esto determina qué canales están realmente en la entrada resultante. Se trata de una configuración heredada que ya no utilizan las integraciones ni los gráficos. |
| <b>Uso</b> *Cadena* | Defina un tipo o uso para esta entrada. Indica cómo deben conectarse otros nodos a esta entrada. |
| <b>Espacio de color</b> *Cadena* | Define el espacio de color en el que debe interpretarse esta entrada. |
