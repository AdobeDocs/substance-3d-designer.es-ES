---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: Utilice el nodo Sombras de RT para calcular la información de sombra en tiempo real a partir de la geometría para crear efectos de iluminación dinámicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombras de RT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Sombras de RT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de nodo de sombras de RT](rt-shadow.resources/rt-shadow-01.png "Icono de nodo de sombras de RT")

<b>En:</b> Filtros > Efectos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera sombras con trazo de rayo a partir de una entrada de mapa de altura.

Este nodo no debe utilizarse en combinación con el motor de CPU (SSE) debido al tiempo de cálculo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Ejemplos</b> <i>Entero</i> | Número de rayos utilizados para calcular las sombras.<br>Un valor más alto proporciona un resultado más suave y preciso, a expensas del rendimiento. |
| <b>Modo</b> <i>Entero</i> | El método para dibujar las sombras en la superficie. |
| <b>Escala de Height</b> <i>Flotador</i> | Un multiplicador para la intensidad del mapa de altura de entrada. |
| <b>Posición de luz</b> <i>Float2</i> | Posición de la fuente de luz en una esfera que encierra la superficie:<br><br>- <b>X</b>: posición horizontal, en número de vueltas;<br>- <b>Y</b>: posición vertical, donde 0,5 es el cenit y 0/1 es el horizonte. |
| <b>Intensidad de luz</b> <i>Flotador</i> | La intensidad de la fuente de luz. |
| <b>Tamaño ligero</b> <i>Float2</i> | (Disponible cuando <b>Modo</b> está establecido en <i>Sombreado</i>) El tamaño de la fuente de luz como un rectángulo. |
| <b>Escala de luz (sombras suaves)</b> <i>Flotador</i> | Un multiplicador para la contribución del <b>Tamaño de luz</b> a la dirección de los rayos.<br>Un valor más alto produce sombras más suaves. |
| <b>Mantener la luz sobre el horizonte</b> <i>Booleano</i> | Si <b>Light Position</b> se establece de forma que coloque la luz debajo del horizonte, este parámetro evita que la luz cruce ese umbral, lo que significa que los valores Y se fijan al rango [0;1]. |
| <b>Opacidad de la sombra</b> <i>Flotador</i> | Un multiplicador para la opacidad de las sombras dibujadas en la superficie. |
| <b>Atenuación de sombra</b> <i>Flotador</i> | Un multiplicador para la atenuación de las sombras a medida que se alejan del ángulo de avance.<br>El valor 0 da como resultado sombras uniformes (se siguen aplicando sombras suaves). |
| <b>Longitud máxima de sombras</b> <i>Flotador</i> | Distancia máxima a la que se puede dibujar una sombra desde su ángulo de avance.<br>Un valor de 0 no produce sombras visibles. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-04.jpg" />
        </td>
    </tr>
</table>
