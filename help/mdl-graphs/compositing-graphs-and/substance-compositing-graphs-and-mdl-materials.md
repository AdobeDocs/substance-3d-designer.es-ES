---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/substance-compositing-graphs-and-mdl-materials.html"
breadcrumb-title: ''
description: Descubre cómo los Substance que componen gráficos y materiales MDL trabajan juntos en Substance 3D Designer para la creación de materiales.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Substance graphs and MDL materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gráficos de Substance y materiales MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 1%

---


# Gráficos de Substance y materiales MDL

En esta página se describen las relaciones sinérgicas entre los gráficos de [Substance](../../compositing-graphs/substance-compositing-graphs.md) y los gráficos MDL, y cómo conectar texturas de los gráficos de Substance [output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) a las entradas de los gráficos MDL.

## Información general

Los resultados de los gráficos de Substance se pueden *pasar a los parámetros expuestos* de materiales MDL de dos maneras, que se describen en esta página.

Si el material MDL aplicado actualmente en la vista 3D ha expuesto parámetros de tipo *[variable](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)*; este tipo se puede establecer mediante la opción <b>Modificador de tipo</b> en las propiedades del [parámetro expuesto](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/exposing-a-parameter-145654033.html), se pueden conectar a *texturas*:

* se puede conectar un parámetro <b>Color</b> a texturas RGBA
* un parámetro <b>Float</b> para texturas en escala de grises

En estos casos, el valor uniforme bruto se sustituye por un muestreador de textura que proporciona un valor variable. Estos muestreadores tienen un atributo <b>usage</b> definido en el parámetro expuesto, y este uso permite a Designer conectar las texturas resultantes de los gráficos de Substance al parámetro apropiado en el material MDL, mediante *usos coincidentes*.

## Gráficos de Substance en la vista 3D

Al usar la opción <b>Ver salidas en vista 3D</b> para un gráfico de Substance o arrastrar un gráfico de Substance desde el panel <b>Explorador</b> a la <b>vista 3D</b>, las salidas se conectan a los parámetros expuestos de *usos coincidentes* en el material MDL que se muestra actualmente en la vista 3D.

Las texturas individuales de una gráfica de Substance se pueden conectar a cualquiera de los parámetros de material MDL que admitan el muestreo de texturas, independientemente del identificador, pulsando RMB en el nodo de gráfica de Substance y arrastrando hasta la vista 3D. Se muestra una lista de los usos de muestra disponibles y puede seleccionar el uso de destino para la textura seleccionada.

![Entradas de gráfica MDL expuesta](../../assets/mdl-graph-inputs-samplers.png "Entradas de gráfica MDL expuesta")

*Las texturas generadas por un gráfico de Substance están conectadas a los parámetros expuestos de un gráfico MDL en la vista 3D*

## Gráficos de Substance en MDL

Las instancias de gráfica de Substance se pueden colocar directamente en gráficas MDL arrastrándolas del panel <b>Explorador</b> al gráfico MDL. Se pueden usar gráficas de Substance de <b>Substance 3D files</b> (SBS) y <b>Substance 3D asset files</b> (SBSAR) en gráficas MDL.

+++Gráfico de Substance del archivo Substance 3D (SBS)
![Gráfico de Substance del archivo SBS en el gráfico MDL](../../assets/mdl-sbs-instance-hl.png "Gráfico de Substance del archivo SBS en el gráfico MDL")



*[Gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) instancia de [archivo Substance 3D](../../getting-started/overview/overview.md) (SBS) en el gráfico MDL*

+++

+++Gráfico de Substance de Substance 3D Asset (SBSAR)
![Gráfico de Substance del archivo SBSAR en el gráfico MDL](../../assets/mdl-sbsar-instance-hl.png "Gráfico de Substance del archivo SBSAR en el gráfico MDL")



*[Gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) de [recurso de Substance 3D](../../getting-started/overview/overview.md) (SBSAR) en el gráfico MDL*

+++

Cuando se crea una instancia de gráfico de Substance, aparece como *nodo* con las siguientes características:

* Un conector *de salida con tipo* para cada una de las salidas del gráfico. Los datos de salida se escriben de la siguiente manera:
  * Mapas de bits RGBA: Color (variable)
  * Mapas de bits de escala de grises: Flotador (variable)
  * Valores: Coincidir con el tipo de valor (variable)
* Una *entrada* del tipo coordenadas UV para especificar las coordenadas UV que se deben usar para asignar las texturas de salida por el gráfico del Substance. Si no está conectado, el valor predeterminado es un degradado lineal clásico 0-1 en X e Y en el espacio UV
* El nodo está *etiquetado* después de la etiqueta de gráfico del Substance (o el identificador si no se ha definido ninguna etiqueta) y su primera salida de mapa de bits es una miniatura

Las propiedades del nodo permiten modificar *todas las propiedades dinámicas* del gráfico del Substance:

* Tamaño de salida
* Grano aleatorio
* Parámetros de entrada
* …

Las propiedades del nodo también le permiten establecer parámetros específicos de cómo se *asignan* texturas en el material MDL:

* Mosaico
* Usar Tamaño físico
* Formato normal
* Espacio tangente

La salida del nodo de la instancia del gráfico Substance puede estar conectada a cualquier entrada de nodo del tipo correspondiente en el gráfico MDL.

Tenga en cuenta que cambiar cualquier parámetro en la sección <b>Parámetros base de SBS</b> implica volver a calcular una o más de las salidas gráficas del Substance, que utiliza el <b>motor del Substance</b> e implica una *sobrecarga de rendimiento* sobre los cálculos del gráfico MDL. Se espera un impacto en el rendimiento al *modificar un gráfico de Substance* que tiene su instancia en un gráfico MDL aplicado en la vista 3D.

>[!WARNING]
>
> Cuando se utiliza un gráfico de Substance en un gráfico MDL, la exportación del gráfico MDL implica la conversión de las salidas del gráfico de Substance en mapas de bits que se exportarán como texturas combinadas con el archivo MDL exportado. Esto significa que la naturaleza paramétrica del gráfico del Substance es *lost* en el archivo MDL exportado.
