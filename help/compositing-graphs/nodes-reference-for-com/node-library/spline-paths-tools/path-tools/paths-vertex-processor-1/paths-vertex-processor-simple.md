---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor-simple.html"
breadcrumb-title: ''
description: Utilice el nodo Simple del procesador de vértices de trazados para procesar vértices de trazado con opciones de transformación simplificadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor Simple
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Procesador de vértices de trazados simple
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# Procesador de vértices de trazados simple

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](paths-vertex-processor-simple.resources/paths-vertex-processor-simple-01.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de trazado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Aplica una transformación en la posición de los vértices de la entrada <b>Paths</b>.

1. Edite la función de parámetro <b>Por función de vértice</b>;
1. Use un nodo <b>Get Flotante2</b> en la variable *vertex.pos*;
1. Realice algunas operaciones con este valor (p. ej., multiplíquelo para escalar los trazados);
1. Defina el resultado del cálculo como salida.

</td>
</tr>
</table>

Puede utilizar imágenes de entrada y tomar muestras de ellas desde la función. Primero debe conectar una entrada para poder muestrearla desde la función. (Tenga cuidado, la primera entrada es *Imagen 1*!)\
También puede tener acceso a las variables *vertex.corner* (bool) y *path.id* (float).

>[!TIP]
>
> Para usuarios avanzados, la [Especificación de formato de trazados](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) explica cómo se codifican los datos de los trazados en imágenes en color y proporciona sugerencias para manipular estos datos directamente.

>[!NOTE]
>
> Consulte también [Procesador de vértices de rutas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Rutas</b> <i>Color</i> | Una lista de los segmentos codificados de las rutas. Conecte esta entrada al resultado de [Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a otro nodo de procesamiento de rutas. |
| <b>Entrada #</b> <i>Color/Escala de grises</i> | Entradas para imágenes que deben muestrearse en la función de parámetro <b>Por función de vértice</b>. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Rutas</b> <i>Color</i> | Los trazados transformados. Puedes usar [rutas de vista previa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para hacerte una idea de lo que representa el resultado, usar otro nodo de procesamiento de rutas o escribirlo en [rutas de acceso a spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para procesarlo aún más como splines. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Recuento de entrada de imagen</b> <i>Entero</i> | Número de conectores de entrada <b>Input #</b> visibles para conectar imágenes que se deben muestrear en la función de parámetro <b>Por función de vértice</b>.<br>Una vez que hayas terminado de configurar todas las muestras deseadas, puedes ocultar los pin no utilizados reduciendo el valor de este parámetro a 0.<br>Si necesitas más entradas, usa [Paths Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) en su lugar. |
| <b>Por función de vértice</b> <i>Float2</i> | Función aplicada a cada vértice. Debe devolver la nueva posición del vértice.<br>Consulte la sección <b>Descripción</b> de esta página para obtener instrucciones. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](paths-vertex-processor-simple.resources/paths-vertex-processor-simple-02.gif "Ejemplo de nodo 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
