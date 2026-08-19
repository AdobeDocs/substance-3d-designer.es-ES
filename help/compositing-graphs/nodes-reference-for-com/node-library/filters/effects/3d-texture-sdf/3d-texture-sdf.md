---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Utilice el nodo SDF de textura 3D para generar texturas de campo de distancia firmadas a partir de datos 3D para crear formas y efectos suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Textura 3D SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# Textura 3D SDF

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

**En:** *Filtro/Efecto*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo **3D Texture SDF** genera el *campo de distancia firmado* de una forma a partir de la máscara *3D Texture* de **Input** que representa los sectores del *volumen* de la forma.

</td>
</tr>
</table>

## Parámetros

### Entradas

* **Entrada de máscara** *Escala de grises*\
  La máscara de *textura 3D* representa los sectores del *volumen* de una forma.

### Parámetros

* **Umbral** *Flotante*\
  Cuando el volumen de la forma se describe mediante un *degradado*, establece el valor de degradado en el que se *detecta* la *superficie* de la forma.
* **Salida** *Entero*\
  El tipo de campo de distancia que debe generarse:
  * *Campo de distancia*: genera un campo de distancia que describe las distancias *fuera* de la forma.
  * *Campo de distancia con signo*: genera un campo de distancia que describe las distancias *exterior* (positivo) e *interior* (negativo) de la forma.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-node.png){width="256px"}

</td>
</tr>
</table>
