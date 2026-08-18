---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: Utilice el nodo Oclusión ambiental (RTAO) para generar mapas de oclusión ambiental en tiempo real a partir de mapas de height para un sombreado realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oclusión ambiente (RATO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Oclusión ambiente (RATO)

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Icono de nodo RTAO](../../../../../../assets/rt-ao.png "Icono de nodo RTAO")

<b>En:</b> *Filtros/Efectos*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

Genera un mapa de Oclusión ambiental basado en una entrada de mapa de height.

Este filtro proporciona resultados más precisos en comparación con el HBAO, pero no debe utilizarse en combinación con el motor de CPU (SSE) debido al tiempo de cálculo.

Consulte [Oclusión ambiental (HBAO) (nodo de filtro)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md) para obtener una alternativa más rápida y sencilla.

</td>
</tr>
</table>

## Parámetros

<b>Usar Tamaño físico</b> *Boolean*\
Active esta opción para usar la configuración de Tamaño físico para determinar la escala de height.

<b>Tamaño físico</b> *Float3* (Disponible cuando <b>Usar Tamaño físico</b> está establecido en *Verdadero*)\
Ajusta la escala de height en función del tamaño físico real de la superficie

<b>Ejemplos </b>*Entero*\
Número de rayos utilizados para calcular la oclusión ambiente.\
Un valor más alto proporciona un resultado más suave y preciso a costa del rendimiento.

<b>Escala de Height</b> *Flotante* (disponible cuando <b>Usar Tamaño físico</b> está establecido en *Falso*)\
Multiplicador de la intensidad de la entrada del mapa de height.

<b>Distribución</b> *Entero* Establece el método de distribución. Afecta a la caída hacia zonas sombreadas,

<b>Distancia máxima</b> *Flotante*\
Define la distancia máxima que los rayos pueden recorrer para ser ocluidos.

<b>Ángulo de pliego</b> *Flotante*\
Define el ángulo de propagación de los rayos a los que se disparará. Un valor de 1 es un hemisferio completo.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nodo RTAO - Ejemplo 1](../../../../../../assets/image2021-6-18-11-7-48.png "Nodo RTAO - Ejemplo 1")

</td>
<td style="border: 0;" valign="top">

![Nodo RTAO - Ejemplo 2](../../../../../../assets/image2021-6-18-11-9-0-1.png "Nodo RTAO - Ejemplo 2")

</td>
</tr>
</table>
