---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Utilice el nodo Fugas para generar patrones de fugas basados en la geometría de malla para crear manchas de agua y efectos de fluidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pérdidas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# Pérdidas

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Similar a [Máscaras inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) en [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Este nodo representa las fugas de dirt y suciedad procedentes de bordes afilados. A medida que se generan rayas con Posición hecha un bake, siempre se ejecutan hacia abajo.

Asegúrese de intentar cambiar la máscara de variación: debido a que impulsa la colocación de rayas, puede tener una influencia mucho mayor que con otros Generadores de máscaras.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Posición</b> <i>Entrada en escala de grises</i> | Mapa de posición hecho un bake, utilizado para direcciones de rayas. ¡Obligatorio! |
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para la colocación de rayas. ¡Obligatorio! |
| <b>Oclusión de ambiente</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. Se recomienda, pero se puede utilizar blanco plano en su lugar. |
| <b>Espacio normal</b> <i>Entrada de color</i> | Mapa normaldel espacio mundial hecho un bake, utilizado para la dirección de rayas. ¡Obligatorio! |
| <b>Máscara de variación</b> <i>Entrada en escala de grises</i> | Máscara de variación opcional, que se activa estableciendo el valor de override en True. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel</b> <i>0.0 - 1.0</i> | Nivel total del resultado. Revela el efecto progresivamente y afecta también a la longitud. Se debe establecer bastante alto para obtener goteos largos. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. |
| <b>Variación</b> <i>0.0 - 1.0</i> | Define la cantidad de variación a gran escala utilizada para enmascarar las rayas. Si establece este valor en 0, se generarán rayas uniformes, así que evite esto. |
| <b>Longitud</b> <i>0.0 - 8.0</i> | Longitud de los goteos de rayas. Si se establece este valor demasiado alto a pequeña escala, se producirá un paso visible. Juega con el nivel también. |
| <b>Ocluir</b> <i>X, Y, Z, Ninguno</i> | Define la dirección en la que debe afectar el AO. |
| <b>Omitir máscara de variación</b> <i>Falso/Verdadero</i> | Permite anular la máscara de variación con una ranura de entrada personalizada. El uso de máscaras más dispersas o más densas puede ser interesante y es una buena manera de controlar los goteos. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/leaks-ex.gif" />
        </td>
    </tr>
</table>
