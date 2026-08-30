---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: Utilice el nodo Exploración de histograma para explorar y analizar histogramas de textura con el fin de corregir y ajustar el color.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escaneo de histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# Escaneo de histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan.resources/histogram-scan-1.png){width="128px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo muy sencillo pero útil que proporciona una forma intuitiva de reasignar el contraste y el brillo de las imágenes de entrada en escala de grises. Se puede utilizar para &quot;ampliar&quot; y &quot;reducir&quot; las máscaras de forma dinámica.

[Haga clic aquí para ver un vídeo de la Academia de Substance sobre las operaciones de histograma.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Posición</b> <i>0.0 - 1.0</i> | De forma similar a un control de brillo, cambia el punto medio del resultado. Cuando se utiliza en una entrada de degradado, expande y reduce el punto de transición.<br><br>Importante: un valor predeterminado de 0 significa que el resultado final siempre es negro, así que pruebe a empezar con 0,5. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. Se puede utilizar para definir la dureza de la transición. |
| <b>Invertir posición</b> <i>Falso/Verdadero</i> | Invierte el resultado final. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan3.gif" />
        </td>
    </tr>
</table>
