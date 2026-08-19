---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: Utilice el nodo Físico de SunSky para generar entornos de iluminación de sol y cielo físicamente precisos para una previsualización realista del material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CieloSolFísico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# Sol/Cielo físico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-physical-sun-sky.png){width="200px"}

## Sol/Cielo físico

**En:** *Herramientas HDRI/vistas 3D*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descripción

Implementación física de Sol y Cielo basada en el modelo de claraboya Hosek-Wikie. Proporciona una base excelente para un HDRI artificial.

## Parámetros

* **Posición Sun**:\
  intervalo = [0,1]x[0,1] (ángulos de longitud-latitud)
* **Turbidez**: *1.0 - 10.0*\
  La turbidez varía de 1 a 10
* **Albedo**: *0.0 - 1.0*\
  El albedo va de 0 a 1.
* **Color de tierra**: *(Valor de color)*\
  Color del plano de tierra.
* **Exposición (VE)**: *-1.0 - 4.0*\
  Valor de exposición del resultado.
* **Tamaño Sun**: *0.0 - 4.0*\
  Escala del Sol, cualquier valor diferente a 1 no es físicamente correcto. ¡El valor tiene efectos sutiles!
* **Intensidad del sol**: *0.0 - 1.0*\
  Intensidad del disco solar. El disco Sun es bastante pequeño, por lo que el efecto no se ve inmediatamente.
* **Intensidad del cielo**: *0.0 - 1.0* Intensidad del cielo. También afecta la llamarada del sol en el cielo, no el disco en sí.

## Imágenes de ejemplo

![](../../../../../../assets/sky-ex.gif)

</td>
</tr>
</table>
