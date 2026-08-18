---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: Utilice el nodo Rutas de acceso de vista previa para visualizar los datos de las rutas de acceso en la vista 2D con fines de depuración y verificación.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Previsualizar trazados
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# Previsualizar trazados

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo](../../../../../../assets/preview-paths-icon.png "Icono de nodo")

<b>En:</b> Herramientas de spline y trazado > Herramientas de trazado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Traza segmentos y vértices del trazado sobre el fondo dado. Un color aleatorio por trazado.

Obtendrás un resultado similar al de la salida de <b>Vista previa</b> de [Máscara a trazados](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md), pero con más opciones.

</td>
</tr>
</table>

## Conectores de entrada

<b>Fondo</b> *Color*\
Una imagen de fondo encima de con muestra el trazado. Esto también controla el tamaño de procesamiento.

<b>Rutas</b> *Color*\
Una lista de los segmentos codificados de las rutas. Conecte esta entrada al resultado de [Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a otro nodo de procesamiento de rutas.

## Parámetros

<b>Mostrar vértices</b> *Boolean*\
Muestra un cuadrado en cada vértice marcado como esquina (fusión aditiva).

<b>Mostrar vértices</b> *Boolean*\
Muestra una forma circular en cada vértice (fusión aditiva). Las esquinas se siguen mostrando como cuadrados.

<b>Thickness de segmentos (px)</b> *Float*\
Ajusta el thickness de los segmentos procesados en píxeles.

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ejemplo de nodo 1](../../../../../../assets/PathsToSpline-Variant2-Before_1.jpg "Ejemplo de nodo 1")

</td>
<td style="border: 0;" valign="top">

![Ejemplo de nodo 2](../../../../../../assets/PathsToSpline-Variant1-Before_1.jpg "Ejemplo de nodo 2")

</td>
</tr>
</table>
