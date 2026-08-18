---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: Utilice el nodo Máscara de volumen 3D para crear máscaras volumétricas basadas en la posición 3D para efectos de materiales avanzados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Máscara de volumen 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# Máscara de volumen 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask.png){width="256px"}

**En:** Generador*/Patrón*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo **Máscara de volumen 3D** genera una representación de una *forma primitiva* basada en el mapa de entrada **Posición**.

</td>
</tr>
</table>

## Parámetros

### Entradas

* **Posición** *Color*\
  El mapa que describe las *coordenadas de espacio 3D* en las que se representa la primitiva.\
  Las coordenadas **X/Y/Z** se asignan a los canales **R/G/B**, respectivamente.

### Parámetros

* **Forma** *Entero*\
  Forma primitiva que debe representarse:
  * *Cubo*- *Cilindro*- *Esfera*
* **Escala** *Flotante*\
  Define la escala *global* de la primitiva, aplicada *uniformemente* en todos los ejes.
* **Tamaño** *Float3*\
  Define el tamaño de la forma en cada eje.
* **Entrada de posición** *Entero*\
  El método de *representar el espacio* mediante la entrada **Position**:
  * *Posición UV*: Utilice un *mapa UV*. Las coordenadas X/Y (U/V) se asignan a los canales R/G, respectivamente. Se supone que el eje Z es el vector *orthogonal forward*.
  * *Posición espacial mundial*: Utilice un *mapa de posición* para asignar el primitivo en el espacio 3D. Las coordenadas X/Y/Z se asignan a los canales R/G/B respectivamente.
* **Posición UV** *Float2*\
  La posición de lo primitivo en el espacio UV.\
  *Nota*: Este parámetro solo está disponible cuando el parámetro **Position Input** está establecido en *UV Position*.
* **Posición** *Float3*\
  La posición de lo primitivo en el espacio mundial.\
  *Nota*: Este parámetro solo está disponible cuando el parámetro **Position Input** está establecido en *World Space Position*.
* **Rotación** *Float3*\
  Define el giro de la forma en el espacio de entorno.
* **Ancho de calado** *Flotante*\
  Ajusta la anchura del *degradado* desde la superficie del primitivo hacia adentro.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant4.jpg){width="256px"}

</td>
</tr>
</table>
