---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: Utilice el nodo Polígono 1 para generar patrones poligonales básicos con lados personalizables y propiedades para texturas geométricas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Polígono 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# Polígono 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](polygon-1.resources/polygon-1-01.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una forma de polígono, con muchas opciones de ajuste. Consulte [Polígono 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md) para obtener una versión más sencilla.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Lados</b> <i>3 - 32</i> | Establece la cantidad de lados que debe tener el polígono. |
| <b>Explotar</b> <i>0.0 - 1.0</i> | Separa los &quot;sectores&quot; del polígono. |
| <b>Tamaño de triángulo</b> <i>0.0 - 1.0</i> | Ajusta el tamaño de los sectores/triángulos. Cualquier ajuste podría separar la forma, solo 1,1. está perfectamente conectado! |
| <b>Escala</b> <i>0.0 - 1.0</i> | Ajusta toda la forma como una sola. |
| <b>Escala automática</b> <i>Falso/Verdadero</i> | Ajusta las escalas para que todo el polígono se ajuste a la vista, con los parámetros predeterminados. |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Gira toda la forma. |
| <b>Degradado</b> <i>Falso/Verdadero</i> | Genera sectores o triángulos de degradado en lugar de sólidos. Nota: se parece a Polígono 2 con este ajuste activado. |
| <b>Invertir degradado</b> <i>Falso/Verdadero</i> | Voltea la dirección del degradado si se activa &quot;Degradado&quot;. |
| <b>Mosaico</b> <i>1 - 16</i> | Define la cantidad de veces que el resultado debe aparecer en mosaico. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |
| <b>Mosaico no cuadrado</b> <i>Falso/Verdadero</i> | Cuando la Expansión no cuadrada está activada, esto segmentará la forma en mosaico sin aplastarla. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="polygon-1.resources/polygon-1-02.gif" />
        </td>
    </tr>
</table>
