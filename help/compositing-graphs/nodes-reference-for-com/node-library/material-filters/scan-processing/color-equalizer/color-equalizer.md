---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Utiliza el nodo de Color Equalizer para equilibrar las variaciones de color en los materiales escaneados y conseguir un aspecto de textura uniforme.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## Color Equalizer

**En:** *Procesamiento De Escaneo/Filtros De Materiales*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Este nodo funciona como un [Paso alto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) de alta calidad para las diferencias de color. Cuando un Paso alto normal elimina la saturación y puede provocar una nitidez no deseada, el Color Equalizer funciona para eliminar las diferencias de color al anochecer y eliminar los matices no deseados a una escala seleccionable por el usuario.

Esto resulta muy útil si una fotografía o digitalización presenta diferencias de color no deseadas o un matiz que desea eliminar. Si ha utilizado [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), este nodo le resultará familiar.

Las opciones de enmascaramiento están pensadas para eliminar matices muy específicos o para funcionar solo en rangos de valores específicos. Úselos si cree que el efecto es demasiado amplio.

## Parámetros

### Entradas

* **Entrada**: *Entrada de color*
* **Entrada de máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo. Solo está activo cuando Máscara está configurada como &quot;Entrada&quot;.

### Parámetros

* **Mosaico de entrada**: *False/True* Conserva opcionalmente el mosaico en los bordes.
* **Radio**: *0.0 - 50.0* Establece el radio de ecualización. Un radio mayor solo eliminará las grandes diferencias de color. Esto requiere un ajuste para cada imagen.
* **Equilibrio de brillo/oscuridad**: *0.0 - 1.0* Ajuste de sesgo para dejar o quitar matices más oscuros.
* **Variación de color personalizada**: *Falso/Verdadero* Permite variar el efecto según el color especificado por el usuario.
* **Variación de color**\
  Solo está activo si la opción Variación de color personalizada está activada. Los ajustes permiten seleccionar un desplazamiento de matiz hacia el que ecualizar.
  * **Tono**: *0.0 - 360.0*
  * **Croma**: *0.0 - 1.0*
  * **Luminancia**: *0.0 - 1.0*
* **Origen de máscara**: *Ninguna, media de imagen, parámetro de color, entrada* Establece si debe producirse algún tipo de enmascaramiento. El parámetro de color habilita los siguientes ajustes adicionales. La entrada cambia a una entrada de máscara definida por el usuario.
* **Máscara**\
  Esta opción solo está activa con las máscaras de parámetros de color. Parámetros de enmascaramiento adicionales para determinar la máscara en función de la propia imagen. Los siguientes parámetros permiten convertir con precisión un matiz en una máscara binaria en la que se aplica la ecualización. Tenga en cuenta que los efectos del parámetro Radio pueden ser mucho menos pronunciados al utilizar estos ajustes.
  * **Color**: *(Valor de color)*
  * **Intervalo de tono**: *0.0 - 360.0*
  * **Rango de croma**: *0.0 - 1.0*
  * **Rango De Luminancia**: *0.0 - 1.0*
  * **Desenfocar**: *0.0 - 2.0*
  * **Smoothness**: *0.0 - 2.0*

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
