---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Utilice el nodo Resplandor para añadir efectos de resplandor a las texturas para crear apariencias de materiales luminosos y de emisivo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Resplandor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---


# Resplandor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](glow.resources/glow-greyscale.png){width="128px"}

![](glow.resources/glow-3.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza un efecto del tipo &quot;Resplandor externo&quot;, como se ve en otros programas conocidos de edición de imágenes. Básicamente, añade un contorno de degradado atenuado alrededor de la entrada.

Tenga en cuenta que esto no está destinado a funcionar para imágenes con canales alfa, como cabría esperar. Incluso la versión en color solo espera máscaras binarias, negras y blancas como entrada; solo permite utilizar un resplandor de color. Si busca una versión que funcione en imágenes con transparencia, consulte [Resplandor de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Importante: asegúrese de utilizar la versión adecuada para su entrada! Utilice &quot;Resplandor&quot; para las entradas de color o &quot;Escala de grises&quot; para las entradas de escala de grises.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad de resplandor</b> <i>0.0 - 1.0</i> | Opacidad global para el efecto de resplandor. |
| <b>Borrar cantidad</b> <i>0.0 - 1.0</i> | Umbral para cuando cortar el efecto de resplandor. Útil para áreas semitransparentes. |
| <b>Tamaño de resplandor</b> <i>0.0 - 20.0</i> | Controla hasta dónde llega el efecto de brillo. |
| <b>Color de resplandor</b> <i>(valor de color) (solo versión de color)</i> | Define el color del efecto de resplandor. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="glow.resources/glow-ex.png" />
        </td>
    </tr>
</table>
