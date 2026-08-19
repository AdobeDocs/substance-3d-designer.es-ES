---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: Utilice el nodo No uniforme de exploración de histograma para realizar una exploración no uniforme del histograma para obtener una corrección de color avanzada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exploración de histograma no uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# Exploración de histograma no uniforme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-non-uniform.png){width="128px"}

## Exploración de histograma no uniforme

**En:** *Filtros/Ajustes*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Versión avanzada de [Histogram Scan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), con controles adicionales y entrada para controlar el efecto a nivel de píxel, en lugar de hacerlo uniformemente en toda la imagen. Se puede utilizar para conseguir un contraste y transiciones aún más intrincados en las máscaras.

Es mucho más complejo de usar que la [exploración por histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) normal, así que asegúrate de estar familiarizado con eso antes de intentar usar la versión no uniforme.

## Parámetros

### Entradas

* **Entrada**: *Entrada en escala de grises* Resultado de origen que se debe modificar.
* **Mapa de posición**: *Entrada en escala de grises* Ranura de entrada para controlar el parámetro Posición. Se activa cuando &quot;Usar entrada de posición&quot; se establece en True. El rango de valor efectivo es pequeño y depende del ajuste y el mapa de contraste.
* **Mapa de contraste**: *Entrada en escala de grises* Ranura de entrada para controlar el parámetro de contraste. Se activa cuando &quot;Utilizar entrada de contraste&quot; se establece en True. El rango de valor efectivo es pequeño.

### Parámetros

* **Usar entrada de posición**: *Falso/Verdadero* Cambiar el uso de la ranura de entrada Mapa de posición.
* **posición**: *0.0 - 1.0* Controla o modifica los resultados del mapa para controlar la configuración de posición.
* **Usar entrada de contraste**: *Falso/Verdadero* Cambiar el uso de la ranura de entrada de Mapa de contraste.
* **contraste**: *0.0 - 1.0* Controla o modifica los resultados del mapa para establecer el contraste.

## Imágenes de ejemplo

</td>
</tr>
</table>
