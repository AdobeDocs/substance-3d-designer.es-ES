---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ''
description: Conozca los conceptos clave de los Substance que componen gráficos, incluidos los nodos, las conexiones y los fundamentos del flujo de trabajo.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conceptos clave de gráficos de Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 1%

---


# Conceptos clave de gráficos de Substance

Esta página enumera los conceptos importantes que se deben comprender para trabajar con gráficos de Substance en Substance 3D Designer.

## Subgráficos/Publicación

[Publicar un gráfico](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) o crear un subgráfico son dos conceptos abstractos muy similares. Esto significa que cualquier gráfico o red de nodos puede ser &quot;empaquetada&quot; y convertida en un recurso independiente reutilizable. La creación de [subgráficos](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) se realiza principalmente dentro de la aplicación para que cierto contenido sea reutilizable en un flujo de trabajo eficiente e inteligente, ya que esto evita duplicar un conjunto de nodos una y otra vez. La publicación implica un paso adicional para exportar al formato de recursos de Substance 3D (SBSAR), lo que hace que el gráfico de red de nodos sea utilizable fuera de la aplicación, como cuando se crea un material para Unreal Engine.

Las entradas, salidas y parámetros expuestos son extremadamente importantes para este concepto, ya que son las únicas formas de seguir interactuando con el gráfico una vez que se utiliza como subgráfico o como recurso publicado de Substance 3D. Las razones son las siguientes:

* Si no hay salidas, el gráfico <b> no genera nada,</b> no genera ningún dato.
* Si no hay parámetros expuestos, el gráfico <b> no se puede personalizar </b> de ninguna manera. No se pueden definir aspectos como la intensidad de un efecto, la opacidad de una imagen que se está fusionando, el color de un área específica, etc.
* Sin entradas significa que, en algunos casos, no podrás personalizar el resultado de un gráfico con <b> tus propios datos de imagen</b>, como mapas de malla horneados a partir de los cuales generar efectos, una imagen de entrada sobre la que realizar un desenfoque o una máscara personalizada para aislar ciertas áreas de una imagen.

## Entradas y salidas

Un [resultado](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) es un nodo que genera un único resultado 2D. Es un punto final, un punto final para su gráfico, un resultado final. Solo los datos conectados a una salida se pueden exportar fuera de Designer o incluso utilizar en otros gráficos.

A continuación se indican algunas cosas que debe saber sobre las salidas:

* Puede tener tantas salidas como desee, pero debe tener <b>al menos una salida</b>.
* Una salida puede tener <b>cualquier resolución</b> de hasta 8192 px de ancho o alto, puede ser<b> de color o escala de grises</b> y se puede exportar a cualquier tipo de archivo compatible.
* Las salidas se pueden y se deben <b>nombrar de forma exclusiva</b> para identificarlas. Esto ayuda al exportar.
* Cada conector en el lado derecho de cualquier nodo es en realidad una salida (ver &quot;Sub-gráficos para más información)

Una [entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) es similar a una salida, es una ranura vacía y abierta para que tú u otro usuario conectes tus propios datos. Permite la creación de gráficos que aparecen en datos de imagen externos definidos por el usuario, como un filtro que modifica una imagen de entrada (por ejemplo, un desenfoque o un ajuste de contraste).

A continuación, se indican algunas cosas que debe saber acerca de las entradas:

* Las entradas son completamente <b>opcionales</b>; solo debe agregarlas si es necesario. No hay cantidad mínima ni máxima.
* Las entradas tienen una resolución definida (vinculada al gráfico en general) que se define, así como si son de escala de grises o de color. Cualquier cosa conectada a ella será convertida para que coincida con esto.
* Las entradas pueden ser archivos de mapa de bits del disco duro, otros gráficos, capas de Painter o Alchemist, etc.
* Cada conector en el lado izquierdo de cualquier Nodo es una Entrada (ver &quot;Sub-gráficos para más información)

## Herencia

A medida que las imágenes y los valores se pasan de nodos a otros, algunos *atributos* de estas imágenes, es decir, sus <b>parámetros base</b>, también se *propagan* por el gráfico, como la resolución, la precisión (es decir, la profundidad de bits), el mosaico y la semilla aleatoria.

Esta propagación está definida por los [métodos de herencia](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) que cada nodo aplica para estos atributos. De hecho, los nodos pueden *heredar atributos* de otros nodos o del gráfico en el que existen.\
Los métodos de herencia pueden ser:

* *Relativo al primario*
* *Relativo a la entrada*
* *Absoluto*: es decir, sin herencia

La herencia puede ser abstracta y complicada de administrar, por lo que le recomendamos encarecidamente que eche un vistazo a la [página dedicada](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) para comentarla en detalle.

## Parámetros de exposición

La exposición de parámetros es un concepto que puede profundizarse mucho, pero se puede resumir en seleccionar determinadas propiedades de los nodos del gráfico y crear un elemento de control de interfaz de usuario dedicado para ellos, que esté fácilmente disponible una vez que el gráfico se utilice como subgráfico o si se publica como archivo. Dado que ya no es posible seleccionar nodos de forma rápida o sencilla y ajustar sus propiedades, el objetivo es crear otro panel de control principal que agrupe todas las propiedades relevantes para este gráfico específico.

A continuación, se indican algunos aspectos que debe conocer sobre los parámetros expuestos:

* Los parámetros expuestos <b> mueven un control desde el nodo al gráfico </b>, básicamente un nivel superior en la jerarquía.
* Los parámetros expuestos no pueden cambiarse en el nodo, solo en el gráfico.
* Los parámetros expuestos se pueden personalizar completamente con nombres, etiquetas, valores, tipo de editor de IU e incluso se pueden ocultar y mostrar para ciertas condiciones.

Exponer parámetros es un concepto abstracto y difícil para los principiantes,[hay más documentación dedicada sobre este tema](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), pero se recomienda familiarizarse completamente con otros aspectos básicos del software antes de sumergirse en Exponer parámetros.
