---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: Utilice el nodo Irradiancia RT para calcular la información de irradiancia en tiempo real a partir de la geometría para realizar cálculos de iluminación realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT Irradiancia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 4%

---


# RT Irradiancia

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rt-irradiance.resources/rt-irradiance.png){width="128px"}

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una irradiancia trazo de rayo en una entrada de mapa de height generada a partir de un mapa de entorno y un mapa de emisiones. Se puede utilizar para &quot;hornear&quot; la iluminación en una textura dentro de una gráfica. Se utiliza para la iluminación y el resplandor globales falsos.Este nodo no debe utilizarse en combinación con el motor de CPU (SSE) debido al tiempo de cálculo. Devuelve dos asignaciones: una salida de irradiancia en la que se aplica la irradiancia a las entradas de material, un mapa de irradiancia sin procesar que contenga solo los valores de irradiancia calculados.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height</b> <i>Entrada en escala de grises</i> | El height es la única entrada necesaria de la ranura de material. Sin él, el nodo no funcionará bien. |
| <b>Emissive</b> <i>Entrada de color</i> | El emisivo debe estar en un formato en el que el negro puro no emite luz, cualquier otro valor de color emite luz. Alpha se omite. Se requiere una conexión a esta ranura o a la ranura Entorno para ver el resultado. |
| <b>Entorno</b> <i>Entrada de color</i> | Entorno de iluminación HDR con el que calcular la irradiancia. Se requiere una conexión a esta ranura o a la ranura Emissive para ver el resultado. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Escala de Height</b> <i>0.0 - 1.0</i> | Escalar para interpretar el height en. Afecta a todo el aspecto de la escena. |
| <b>Calidad</b> <i>32 rayos, 64 rayos, 128 rayos</i> | Determina la calidad del resultado, pero también afecta al rendimiento. Menos rayos significa más ruido. |
| <b>Rebotes de cálculo</b> <i>Falso/Verdadero</i> | Conmutar el cálculo de rebotes. Afecta a la calidad y velocidad. |
| <b>Rotación de entorno</b> <i>0.0 - 1.0</i> | Rota el entorno. |
| <b>Exposición del entorno (VE)</b> <i>-4.0 - 4.0</i> | El valor de exposición que se debe utilizar para el entorno afecta al brillo total del efecto. |
| <b>Intensidad del Emisivo</b> <i>0.0 - 20.0</i> | El multiplicador para la entrada de Emisivo, afecta a la intensidad de la irradiancia del emisivo. |
| <b>Espacio de color del Emisivo</b> <i>sRGB, lineal</i> | Espacio de color utilizado para interpretar la entrada ensiva. |
| <b>Sombras IBL en el Alpha de irradiancia sin procesar</b> <i>Falso/Verdadero</i> | Alternar entre añadir sombras a la |
| <b>Emisivo LOD Bias</b> <i>-1.0 - 1.0</i> | Ajusta la calidad de la irradiancia del emisivo. Un valor más bajo significa más ruido. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-03-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-01-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irr-02-1.jpg" />
        </td>
    </tr>
</table>
