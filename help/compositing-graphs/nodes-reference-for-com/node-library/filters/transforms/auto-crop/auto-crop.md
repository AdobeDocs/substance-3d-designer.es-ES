---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Utilice el nodo Recorte automático para recortar automáticamente las texturas, eliminar los bordes vacíos y optimizar las dimensiones de la textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recorte automático
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Recorte automático

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo **Recorte automático** ajusta la **Entrada** para que su contenido se coloque en el *centro* de la imagen sin que se le cambie el tamaño, o *se cambie de tamaño según el tamaño* de la imagen.

El contenido de la imagen se define mediante un cuadro ajustado a los *primeros y últimos píxeles* de **X** e **Y**, cuyos valores son *superiores a 0* (es decir, no negros). La versión de **Color** te permite elegir entre los canales RGB y Alfa para definir ese cuadro.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo</b> <i>Entero</i> | Establezca el método de recorte que se debe aplicar:<br><br>- <i>Cuadrado de recorte</i>: la imagen se recorta de modo que la forma esté en el centro de la imagen más pequeña de <i>cuadrado</i> que pueda incluirla<br>- <i>Recortar auto</i>: La imagen se recorta de modo que la forma esté en el centro de la imagen más pequeña <i>cuadrada o no cuadrada</i> que pueda incluirla<br>- <i>Ajustar (mantener relación)</i>: El tamaño de la imagen cambia al <i>tamaño completo</i> de la imagen, pero se mantienen sus <i>proporciones</i> (es decir, la relación entre anchura y longitud)<br>- <i>Rellenar (Estirar)</i>: El tamaño de la imagen cambia al <i>tamaño completo</i> de la imagen |
| <b>Usar alfa</b> <i>Booleano</i> | Use el canal alfa de <b>Input</b> para determinar los <i>límites</i> del contenido de la imagen para el recorte. Cuando se establece en <i>False</i>, se usan píxeles negros.<br><br><i>Nota:</i> Este parámetro solo está disponible en la versión <b>Color</b> del nodo. |
| <b>Modo de filtro</b> <i>Entero</i> | Define cómo tratar los resultados muestreados al <i>interpolar</i> entre píxeles:<br><br>- <i>Más cercano</i>: mostrará exactamente el <i>mismo valor</i> (más rápido)<br>- <i>Bilineal</i>: aplicará un filtro bilineal en el resultado para un aspecto <i>más suave</i><br>- <i>Automático</i>: Utiliza el más adecuado de los dos modos anteriores, dependiendo del <b>Modo</b> seleccionado para el recorte |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-demo-01-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant4.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant3.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-node.png" />
        </td>
    </tr>
</table>
