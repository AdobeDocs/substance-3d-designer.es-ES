---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo de erosión de cuero para añadir patrones de desgaste y efectos de envejecimiento a los materiales de cuero en función de la curvatura de la malla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Meteorología de cuero
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 9%

---


# Meteorología de cuero

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-weathering.resources/leather-weathering-01.png){width="128px"}

<b>En:</b> Generadores Basados En Malla > Meteorización

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Se trata de un efecto de material completo que funciona en varios canales a la vez. Añade un efecto de desgaste aleatorio del cuero, con control de la edad y la suciedad. Es similar a [Fabric Weathering](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md), pero se ha ajustado específicamente para el cuero.<br>Este efecto no funciona muy bien a menos que se conecten correctamente AO hechos un bake y World Space Normalmaps, ya que es necesario para calcular y generar todo adecuadamente.

Asegúrate de que comprendes perfectamente los [modos de creación de vínculos](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) al trabajar con materiales completos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Oclusión de ambiente</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. |
| <b>Espacio normal</b> <i>Entrada de color</i> |  |
| <b>Máscara</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. |
| <b>Avanzado</b> |  |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambia entre diferentes formatos de Mapa normal (invierte el canal verde). |
| <b>Máscara</b> <i>Falso/Verdadero</i> | Activa o desactiva el uso del mapa de máscara. |
| <b>Efecto</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> | Fusiones en un efecto de dust más oscuro, basado en las áreas orientadas hacia arriba en el mapa normaldel espacio mundial. |
| <b>Suciedad</b> <i>0.0 - 1.0</i> | Fusiones en un efecto global de dirt/difuminado, basado principalmente en áreas ocluidas (oscuras) en el AO. |
| <b>Bordes Con </b> <i>0.0 - 1.0</i> | Añade un efecto de enfoque/intensificación a los bordes, basado en el material normal. |
| <b>Usado</b> <i>0.0 - 1.0</i> | Fusiones en un aspecto de piel desgastada a nivel mundial. |
| <b>Edad</b> <i>0.0 - 1.0</i> | Las Fusiones de piel desgastada se ven en pliegues basados en AO. La ubicación está muy influenciada por el umbral de edad. |
| <b>Umbral de edad</b> <i>0.0 - 1.0</i> | Establece el umbral de apariencia del efecto Edad. |
| Escala de <b>Grietas</b> <i>1.0 - 16.0</i> | Establece la profundidad del cuero desgastado del efecto Usado y Edad. |
| <b>Intensidad de deformación de Grietas</b> <i>0.0 - 1.0</i> | Define la intensidad del cuero desgastado del efecto Usado y Edad. |
| Escala de Scratches de <b>Bordes afilados</b> <i>1.0 - 32.0</i> |  |
| <b>Intensidad de deformación de los Scratches de bordes afilados</b> <i>0.0 - 1.0</i> |  |
| <b>Desaturación de cuero usado</b> <i>0.0 - 1.0</i> | Establece la saturación del aspecto de cuero usado de los efectos Edad y Utilizado. |
| <b>Brillo de cuero usado</b> <i>0.0 - 1.0</i> | Define el brillo del aspecto de cuero usado de los efectos Edad y Utilizado. |
| <b>Fusión</b> |  |
| <b>Intensidad de Difuso</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la difusión. |
| <b>Intensidad de Color base</b> <i>0.0 - 1.0</i> | Intensidad de fusión del color base. |
| <b>Intensidad normal</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la Normal. |
| <b>Intensidad del Specular</b> <i>0.0 - 1.0</i> | Fusión del Specular. |
| <b>Intensidad de Brillo</b> <i>0.0 - 1.0</i> | Fuerza de fusión del Brillo. |
| <b>Intensidad de rugosidad</b> <i>0.0 - 1.0</i> | Fuerza de fusión de la rugosidad. |
| <b>Intensidad de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Fuerza de fusión de la Oclusión ambiente. |
| <b>Intensidad de Height</b> <i>0.0 - 1.0</i> | Fusión del Height. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leather-weathering.resources/leather-weathering-02.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="leather-weathering.resources/leather-weathering-03.png" />
        </td>
    </tr>
</table>
