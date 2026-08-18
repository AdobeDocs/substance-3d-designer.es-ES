---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: Utilice el nodo Varios Colores Equalizer para ecualizar los colores en varios canales de textura para un procesamiento coherente de materiales digitalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Varios Colores Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---


# Varios Colores Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

## Varios Colores Equalizer

**En:** *Procesamiento De Escaneo/Filtros De Materiales*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Esta es la versión de entrada múltiple de [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Unifica las diferencias de color y elimina los matices no deseados a una escala que el usuario puede seleccionar. Está pensado principalmente para fotos de varios ángulos, que luego se combinan con [Multi-Ángulo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Multi-Ángulo a Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulta el [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) original para obtener más información.

## Parámetros

### Entradas

* **Entrada 1-8**: *Entrada de color* Varias entradas para procesar.
* **Entrada de máscara**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.

### Parámetros

* **Recuento de entradas**: *1 - 8* Establece el número de entradas para procesar en paralelo.
* **Mosaico de entrada**: *False/True* Conserva opcionalmente el mosaico en los bordes.
* **Radio**: *0.0 - 50.0* Establece el radio de ecualización. Un radio mayor solo eliminará las grandes diferencias de color. Esto requiere un ajuste para cada imagen.
* **Equilibrio de brillo/oscuridad**: *0.0 - 1.0* Ajuste de sesgo para dejar o quitar matices más oscuros.
* **Variación de color personalizada**: *Falso/Verdadero* Permite variar el efecto según el color especificado por el usuario.
* **Variación de color**\
  Solo está activo si la opción Variación de color personalizada está activada. Los ajustes permiten seleccionar un desplazamiento de matiz hacia el que ecualizar.
  * **Tono**: *0.0 - 360.0*
  * **Croma**: *0.0 - 1.0*
  * **Luminancia**: *0.0 - 1.0*
* **Origen de máscara**: *Ninguna, media de imagen, parámetro de color, entrada* Establece si debe producirse alguna máscara. El parámetro de color habilita los ajustes adicionales que se indican a continuación. La entrada cambia a una entrada de máscara definida por el usuario.
* **Máscara**\
  Solo está activo con máscaras de parámetros de color. Contiene parámetros de máscara adicionales para determinar la máscara en función de la propia imagen. Los siguientes parámetros permiten convertir con precisión un matiz en una máscara binaria en la que se aplica la ecualización. Tenga en cuenta que los efectos del parámetro Radio pueden ser mucho menos pronunciados al utilizar estos ajustes.
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
