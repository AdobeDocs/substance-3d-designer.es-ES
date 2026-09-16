---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ""
description: Utilice el nodo Desenfoque direccional para aplicar efectos de desenfoque en una dirección específica para crear efectos de desenfoque de movimiento y de desenfoque.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desenfoque direccional
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 8%
---

# Desenfoque direccional

<table>
<tr style="border: 0;">
<td width="20%" style="border: 0;" valign="top">

![Nodo atómico: Desenfoque direccional](directional-blur.resources/comp_dirmotionblur_1.png "Nodo atómico: Desenfoque direccional"){width="100%"}

</td>
<td style="border: 0;" valign="top">

Aplica desenfoque en una dirección especificada de acuerdo con un mapa de intensidad.

Este nodo realiza una operación similar a un desenfoque de movimiento en una entrada. A diferencia del nodo normal &#39;[Blur](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)&#39;, que se desenfoca por igual en todas las direcciones, el &#39;Desenfoque direccional&#39; funciona en un ángulo definido por el usuario.

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="directional-blur.resources/directional-blur-tooltip.gif" alt="información sobre herramientas de desenfoque direccional" /></div>

Al igual que &quot;Desenfocar&quot;, también es una operación más rápida y de baja calidad. Se proporciona una alternativa ampliada de mayor calidad en [Desenfoque anisotrópico](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md), con una compensación de rendimiento


## Desenfoque direccional y anisotrópico

Las siguientes imágenes muestran el desenfoque direccional y el [desenfoque anisotrópico](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) en efecto en la misma forma de entrada, con parámetros similares. El desenfoque anisotrópico se ha configurado con total anisotropía y alta calidad.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Desenfoque direccional</b>

![Comparación de desenfoque direccional](directional-blur.resources/dirblur-01.png "Comparación de desenfoque direccional"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

<b>Desenfoque anisotrópico</b>

![Comparación de desenfoque anisotrópico](directional-blur.resources/aniso-01.png "Comparación de desenfoque anisotrópico"){zoomable="yes"}

</td>
</tr>
</table>


## Parámetros

|  |  |
| --- | --- |
| <b>Intensidad</b> *Flotador* | Define el radio de desenfoque en píxeles. |
| <b>Ángulo</b> *Flotador* | La dirección del efecto de desenfoque en el número de vueltas en el sentido de las agujas del reloj, comenzando desde la horizontal, es decir, el vector de dirección (1, 0). |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Escala de grises/Color* [PRINCIPAL](../../../../glossary/glossary.md) | Imagen que se va a procesar. |


## Ejemplos

*Próximamente.*
