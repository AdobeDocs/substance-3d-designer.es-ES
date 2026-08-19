---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
breadcrumb-title: ''
description: Utilice el nodo Procesador de vértices de trazados para transformar y manipular los vértices de trazado con opciones avanzadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Procesador de vértices de rutas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---


# Procesador de vértices de rutas

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/paths-vertex-processor-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de trazado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aplica una transformación en la posición de los vértices de la entrada <b>Paths</b>.

El nodo debe utilizarse de la siguiente manera:

1. Edite la función de parámetro </b> del Por función de vértice <b>;
1. Use <b>Obtener flotante2</b> nodos para adquirir; las variables *vertex.pos*, *prev.pos* o *next.pos*
1. Realice algunas operaciones con esos valores (por ejemplo, multiplíquelos para escalar los trazados);
1. Defina el resultado del cálculo como salida.

</td>
</tr>
</table>

Asegúrese de establecer los valores <b>Se ha tenido acceso a vértices anteriores</b> y <b>Se ha tenido acceso a vértices siguientes</b> antes de consultar *prev.pos* o *next.pos*\
También puede añadir imágenes de entrada y tomar muestras de ellas desde la función. Primero debe conectar una entrada para poder muestrearla desde la función. (Tenga cuidado, la primera entrada es *Imagen 1*!)\
También puede tener acceso a las variables *prev[2].pos* (Float2), *next[2].pos* (Float2), *vertex.corner* (bool) y *path.id* (float).

>[!TIP]
>
> Para usuarios avanzados, la [Especificación de formato de trazados](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) explica cómo se codifican los datos de los trazados en imágenes en color y proporciona sugerencias para manipular estos datos directamente.

>[!NOTE]
>
> Consulte también [Procesador simple de vértices de rutas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md).

## Conectores de entrada

<b>Rutas</b> *Color*\
Una lista de los segmentos codificados de las rutas. Conecte esta entrada al resultado de un nodo de procesamiento de [Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a otro nodo de procesamiento de *Path*.

<b>Entrada #</b> *Color/Escala de grises*\
Entradas para imágenes que deben muestrearse en la función de parámetro <b>Por función de vértice</b>.

## Conectores de salida

<b>Rutas</b> *Color*\
Los trazados transformados. Puedes usar [rutas de vista previa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para hacerte una idea de lo que representa el resultado, usar otro nodo de procesamiento de rutas o escribirlo en [rutas de acceso a spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para procesarlo aún más como splines.

## Parámetros

<b>Se ha obtenido acceso a vértices anteriores</b> *Integer*\
El uso de este parámetro le permitirá obtener la posición del vértice anterior a lo largo de la ruta de acceso (*prev.pos*) y el vértice anterior (*prev[2].pos*) utilizando los nodos <b>Get</b> en la función de parámetro <b>Por función de vértice</b>.

<b>Se ha obtenido acceso a los siguientes vértices</b> *Entero*\
El uso de este parámetro le permitirá obtener la posición del siguiente vértice a lo largo de la ruta (*next.pos*) y el siguiente vértice (*next[2].pos*) mediante los nodos <b>Get</b> en la función de parámetro <b>Por función de vértice</b>.

<b>Recuento de entrada de imagen</b> *Entero*\
Número de conectores de entrada <b>Input #</b> visibles para conectar imágenes que se deben muestrear en la función de parámetro <b>Por función de vértice</b>.\
Una vez que haya terminado de configurar todas las muestras deseadas, puede ocultar los bordes no utilizados reduciendo el valor de este parámetro de nuevo a 0.

<b>Por función de vértice</b> *Float2*\
Función aplicada a cada vértice. Debe devolver la nueva posición del vértice.\
Consulte la sección <b>Descripción</b> de esta página para obtener instrucciones.

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/PathsVertexProcessor-Demo2.gif "Ejemplo de nodo 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
