---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: Utilice el nodo Normal doblada (Bent Normal) para generar mapas normales doblados que tengan en cuenta la oclusión ambiente y la luz indirecta.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal doblada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---


# Normal doblada

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Icono de nodo normal doblado](../../../../../../assets/rt-bent-normal.png "Icono de nodo normal doblado")

<b>En:</b> *Filtros/mapa normal*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

Genera un mapa normal doblado basado en una entrada de mapa de height. Un mapa normal doblado es una versión especial de [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) y [Oclusión ambiente (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md), que generan un mapa normal con oclusión ambiente incrustada.\
Esto se puede utilizar en motores en tiempo real para que la Oclusión ambiental se convierta en el mapa normal, por ejemplo para obtener reflejos de oclusión más precisos sobre los metales.

Este nodo no debe utilizarse en combinación con el motor de CPU (SSE) debido al tiempo de cálculo.

</td>
</tr>
</table>

## Parámetros

<b>Usar Tamaño físico</b> *Booleano*\
Active esta opción para usar la configuración de Tamaño físico para determinar la escala de height.

<b>Tamaño físico</b> *Float3* (disponible cuando <b>Usar Tamaño físico</b> está establecido en *Verdadero*)\
Ajusta la escala de height en función del tamaño físico real de la superficie.

<b>Ejemplos</b> *Entero*\
Número de rayos utilizados para calcular la normal doblada.\
Un valor más alto proporciona un resultado más suave y preciso al coste del rendimiento.

<b>Escala de Height</b> *Float (disponible cuando Usar Tamaño físico está establecido en False)*\
Multiplicador de la intensidad de la entrada del mapa de height.

<b>Distribución</b> *Entero*\
Establece el método de distribución. Afecta a la difuminación hacia áreas sombreadas.

<b>Distancia máxima</b> *Flotador*\
Define la distancia máxima que los rayos pueden recorrer para ser ocluidos.

<b>Ángulo de pliego</b> *Flotador*\
Define el ángulo de propagación de los rayos a los que se disparará. Un valor de 1 es un hemisferio completo.

<b>Formato normal</b> *Entero*\
Invierte el canal verde de la salida.

## Imágenes de ejemplo

![Nodo normal doblado - Ejemplo 1](../../../../../../assets/bent-normal-ex-1.jpg "Nodo normal doblado - Ejemplo 1")
