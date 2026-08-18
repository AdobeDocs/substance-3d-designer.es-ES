---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---


# RT Irradiancia

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**En:** *Filtros/Efectos*

**Complejo**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

Genera una irradiancia trazo de rayo en una entrada de mapa de height generada a partir de un mapa de entorno y un mapa de emisiones. Se puede utilizar para &quot;hornear&quot; la iluminación en una textura dentro de una gráfica. Se utiliza para la iluminación y el resplandor globales falsos.Este nodo no debe utilizarse en combinación con el motor de CPU (SSE) debido al tiempo de cálculo. Devuelve dos asignaciones: una salida de irradiancia en la que se aplica la irradiancia a las entradas de material, un mapa de irradiancia sin procesar que contenga solo los valores de irradiancia calculados.

</td>
</tr>
</table>

## Parámetros

### Entradas

* **Height:** *El Height de entrada de escala de grises* es la única entrada necesaria de la ranura del material. Sin él, el nodo no funcionará bien.
* **Emisor:** La *entrada de color* Emisor debe tener un formato en el que el negro puro no emite luz, cualquier otro valor de color emite luz. Alpha se omite. Se requiere una conexión a esta ranura o a la ranura Entorno para ver el resultado.
* **Entorno**: *Entrada de color*\
  Entorno de iluminación HDR con el que calcular la irradiancia. Se requiere una conexión a esta ranura o a la ranura Emissive para ver el resultado.

### Parámetros

* **Escala de Height**: *0.0 - 1.0*\
  Escalar para interpretar el height en. Afecta a todo el aspecto de la escena.
* **Calidad**: *32 rayos, 64 rayos, 128 rayos*\
  Determina la calidad del resultado, pero también afecta al rendimiento. Menos rayos significa más ruido.
* **Rebotes de cálculo**: *Falso/Verdadero*\
  Conmutar el cálculo de rebotes. Afecta a la calidad y velocidad.
* **Rotación de entorno**: *0.0 - 1.0*\
  Rota el entorno.
* **Exposición del entorno (VE)**: *-4.0 - 4.0*\
  El valor de exposición que se debe utilizar para el entorno afecta al brillo total del efecto.
* **Intensidad de emisión**: *0.0 - 20.0*\
  El multiplicador para la entrada Emissive, afecta la intensidad de la irradiancia de la emisión.
* **Espacio de color emisivo**: *sRGB, lineal*\
  Espacio de color utilizado para interpretar la entrada ensiva.
* **Sombras de IBL en el Alpha de irradiancia sin procesar**: *Falso/Verdadero*\
  Alternar entre añadir sombras a la
* **Compensación LOD emisiva**: *-1.0 - 1.0* Ajuste de la calidad de la irradiancia emisiva. Un valor más bajo significa más ruido.

## Imágenes de ejemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |
