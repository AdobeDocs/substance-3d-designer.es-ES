---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Sombras de RT

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Icono de nodo de sombras de RT](../../../../../../assets/rt-shadow.png "Icono de nodo de sombras de RT")

<b>En:</b> *Filtros/Efectos*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

Genera sombras con trazo de rayo a partir de una entrada de mapa de height.

Este nodo no debe utilizarse en combinación con el motor de CPU (SSE) debido al tiempo de cálculo.

</td>
</tr>
</table>

## Parámetros

<b>Ejemplos</b> *Entero*\
Número de rayos utilizados para calcular las sombras.\
Un valor más alto proporciona un resultado más suave y preciso, a expensas del rendimiento.

<b>Modo</b> *Entero*\
El método para dibujar las sombras en la superficie.

<b>Escala de Height</b> *Flotante*\
Un multiplicador para la intensidad del mapa de height de entrada.

Posición de la luz <b>Float2 </b>**\
Posición de la fuente de luz en una esfera que encierra la superficie:
* <b>X</b>: posición horizontal, en número de vueltas;
* <b>Y</b>: posición vertical, donde 0,5 es el cenit y 0/1 es el horizonte.

<b>Intensidad de luz</b> *Flotante*\
La intensidad de la fuente de luz.

<b>Tamaño ligero</b> *Float2* (Disponible cuando <b>Mode</b> está establecido en *Shaded*)\
El tamaño de la fuente de luz como un rectángulo.

<b>Escala de luz (sombras suaves)</b> *Flotador*\
Un multiplicador para la contribución del <b>Tamaño de luz</b> a la dirección de los rayos.\
Un valor más alto produce sombras más suaves.

<b>Mantener la luz sobre el horizonte</b> *Booleano*\
Si <b>Light Position</b> se establece de forma que coloque la luz debajo del horizonte, este parámetro evita que la luz cruce ese umbral, lo que significa que los valores Y se fijan al rango [0;1].

<b>Opacidad de la sombra</b> *Flotante*\
Un multiplicador para la opacidad de las sombras dibujadas en la superficie.

<b>Atenuación de sombra</b> *Float*\
Un multiplicador para la atenuación de las sombras cuanto más lejos están de su ruedecilla.\
Un valor de 0 produce sombras uniformes (las sombras suaves se siguen aplicando).

<b>Longitud máxima de sombras</b> *Float*\
Distancia máxima a la que se puede dibujar una sombra desde su ángulo de avance.\
Un valor de 0 no produce sombras visibles.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nodo Sombras RT - Ejemplo 1](../../../../../../assets/RTShadows-01.jpg "Nodo Sombras RT - Ejemplo 1")

</td>
<td style="border: 0;" valign="top">

![Nodo Sombras RT - Ejemplo 2](../../../../../../assets/RTShadows-02.jpg "Nodo Sombras RT - Ejemplo 2")

</td>
<td style="border: 0;" valign="top">

![Nodo Sombras RT - Ejemplo 3](../../../../../../assets/RTShadows-03.jpg "Nodo Sombras RT - Ejemplo 3")

</td>
</tr>
</table>
