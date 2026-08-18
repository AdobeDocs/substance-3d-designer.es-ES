---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: Utilice el nodo Filtro de estación para aplicar efectos estacionales a los materiales y así crear variaciones de primavera, verano, otoño e invierno.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filtro de temporada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Filtro de temporada

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## Filtro de temporada

**En:** *Filtros/Efectos De Materiales*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo añade efectos como un nivel de agua animado, nieve, hielo y/o musgo.

Ten en cuenta que este es un filtro antiguo que no pretende ser completamente correcto para la PBR. Se conserva principalmente por motivos de compatibilidad o heredados, aunque puede seguir siendo útil en algunos casos. Se pueden encontrar versiones más recientes correctas de la PBR en [Snow Cover](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) y [Water Level](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

El nodo requiere un conjunto adecuado de entradas de material, principalmente con un mapa de altura o mapa normal decentemente detallado.

## Parámetros

### Entradas

* **Máscara** : *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;.

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Avanzado**
  * **Formato normal**: *DirectX, OpenGL*\
    Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).
  * **Máscara**: *Falso/Verdadero*\
    Activa o desactiva el uso del mapa de máscara.
  * **Intensidad de luz**: *0.0 - 1.0*\
    Intensidad de la luz (fingida).
  * **Ángulo de luz**: *0.0 - 1.0*\
    Ángulo de incidencia de la luz (falsificada)
* **Efecto**
  * **Efecto de Height o normal**: *Height, normal* Elige qué mapa de entrada controla los efectos.
  * **Nivel de agua**: *0.0 - 1.0* Sube o baja el nivel del agua según el Height/Información normal.
  * **Detalles del agua**: *0.0 - 1.0* Establece la cantidad de detalles en el agua.
  * **Refracción**: *0.0 - 1.0* Establece la cantidad de refracción falsa en el efecto.
  * **Reflejo**: *0.0 - 1.0* Define la cantidad de reflejo falso en el efecto.
  * **Distancia de reflejo**: *0.0 - 1.0* Controla los elementos visuales de reflexión.
  * **Ángulo de reflejo**: *0.0 - 1.0* Controla los elementos visuales de reflexión.
  * **Dirección de flujo**: *0.0 - 1.0* Controla el flujo de animación (usa el Substance Player para visualizar).
  * **Hielo**: *0.0 - 1.0* Establece la congelación del agua.
  * **Detalles de hielo**: *0.0 - 1.0* Establece la cantidad de detalles en el hielo.
  * **Snow**: *0.0 - 1.0* Define la cantidad de cobertura de nieve.
  * **Musgo**: *0.0 - 1.0* Define la cantidad de cobertura de musgo.
  * **Escala de musgo**: *1 - 4* Establece la escala de la textura de musgo generada.
  * **Color de musgo**: *(Valor de color)*Define el color del musgo.
  * **Color de agua**: *(Valor de color)*Define el color del agua, incluyendo alfa/opacidad.
* **Fusión**
  * **Intensidad de difusión**: *0.0 - 1.0*\
    Intensidad de fusión de la difusión.
  * **Intensidad de color base**: *0.0 - 1.0*\
    Intensidad de fusión del color base.
  * **Intensidad normal**: *0.0 - 1.0*\
    Intensidad de fusión de la Normal.
  * **Intensidad del Specular**: *0.0 - 1.0*\
    Fusión del Specular.
  * **Intensidad de brillo**: *0.0 - 1.0*\
    Fuerza de fusión del Brillo.
  * **Intensidad de rugosidad**: *0.0 - 1.0*\
    Fuerza de fusión de la rugosidad.
  * **Intensidad de Oclusión ambiente**: *0.0 - 1.0*\
    Fuerza de fusión de la Oclusión ambiente.
  * **Intensidad de Height**: *0.0 - 1.0*\
    Fusión del Height.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
