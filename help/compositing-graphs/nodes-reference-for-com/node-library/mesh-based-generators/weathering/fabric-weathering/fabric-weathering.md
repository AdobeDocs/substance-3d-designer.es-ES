---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo de erosión de la tela para añadir efectos de desgaste y envejecimiento a los materiales de la tela en función de la geometría de malla y la curvatura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tejido de intemperie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 8%

---


# Tejido de intemperie

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fabric-weathering.resources/fabric-weathering.png){width="128px"}

<b>En:</b> Generadores Basados En Malla > Meteorización

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Se trata de un efecto de material completo que funciona en varios canales a la vez. Añade un efecto aleatorio de desgaste de la tela, con control de la edad y la suciedad.<br>Este efecto no funciona muy bien a menos que se conecten correctamente AO hechos un bake y World Space Normalmaps, ya que requiere que se calculen y generen adecuadamente.

Asegúrate de que comprendes perfectamente los [modos de creación de vínculos](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) al trabajar con materiales completos.

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
| <b>Usado</b> <i>0.0 - 1.0</i> | Fusiones en dirt muy oscuro acumulado en pliegues, basado en AO. Los valores máximos y mínimos tienden a ser muy extremos, úselos con cuidado. |
| <b>Edad</b> <i>0.0 - 1.0</i> | Fusiones sobre un patrón global de desgaste de azulejos. El control de umbral por debajo controla la influencia del AO. Los valores máximo y mínimo tienden a ser muy extremos. |
| <b>Umbral de edad</b> <i>0.0 - 1.0</i> | Define la medida en que el AO afecta al parámetro Age. |
| <b>Creaciones de edad</b> <i>0.0 - 1.0</i> | Controla la fusión de sutiles pliegues adicionales en el efecto Edad. |
| Escala de Scratches de <b>Bordes afilados</b> <i>1.0 - 32.0</i> | Define la escala de pequeños arañazos, que principalmente eliminan el efecto Usado y Edad. |
| <b>Intensidad de deformación de los Scratches de bordes afilados</b> <i>0.0 - 1.0</i> | Define la intensidad de la deformación para los arañazos pequeños anteriores. |
| <b>Desaturación de tejido antiguo</b> <i>0.0 - 1.0</i> | Controla la desaturación del efecto Edad. |
| <b>Brillo de tejido antiguo</b> <i>0.0 - 1.0</i> | Controla el brillo del efecto Edad. *Este es un parámetro muy importante para cambiar y obtener el aspecto deseado, pero los resultados pueden ser extremos: usar con cambios de subtítulos.* |
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
            <img src="fabric-weathering.resources/fabric-ex.gif" />
        </td>
    </tr>
</table>
