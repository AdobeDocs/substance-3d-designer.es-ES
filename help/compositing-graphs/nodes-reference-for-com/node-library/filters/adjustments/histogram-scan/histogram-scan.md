---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: Utilice el nodo Exploración de histograma para explorar y analizar histogramas de texturas con el fin de corregir y ajustar el color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escaneo de histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 5%

---


# Escaneo de histograma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

## Escaneo de histograma

**En:** *Filtros/Ajustes*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Descripción

Nodo muy sencillo pero útil que proporciona una forma intuitiva de reasignar el contraste y el brillo de las imágenes de entrada en escala de grises. Se puede utilizar para &quot;ampliar&quot; y &quot;reducir&quot; las máscaras de forma dinámica.

[Haga clic aquí para ver un vídeo de la Academia de Substance sobre las operaciones de histograma.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

## Parámetros

* **Posición**: *0.0 - 1.0* De forma similar a un control de brillo, cambia el punto medio del resultado. Cuando se utiliza en una entrada de degradado, expande y reduce el punto de transición.\
  Importante: un valor predeterminado de 0 significa que el resultado final siempre es negro, así que pruebe a empezar con 0,5.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado. Se puede utilizar para definir la dureza de la transición.
* **Invertir posición**: *Falso/Verdadero* Invierte el resultado final.

## Imágenes de ejemplo

![](../../../../../../assets/histogram-scan.gif)

![](../../../../../../assets/histogram-scan2.gif)

![](../../../../../../assets/histogram-scan3.gif)

</td>
</tr>
</table>
