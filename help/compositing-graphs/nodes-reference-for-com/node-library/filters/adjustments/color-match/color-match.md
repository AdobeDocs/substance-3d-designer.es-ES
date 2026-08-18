---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: Utilice el nodo Coincidencia de color para hacer coincidir los colores entre texturas para crear paletas de colores uniformes y armonizar texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Coincidencia de color
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# Coincidencia de color

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## Coincidencia de color

**En:** *Filtros/Ajustes*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Intenta hacer coincidir el rango de *color de origen* definido con un rango de *color de destino*, con compatibilidad con ranuras de entrada para definir el origen y el destino.

Para obtener versiones más sencillas, vea [Reemplazar rango de color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) o [Reemplazar color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

## Parámetros

### Entradas

* **Entrada**: Entrada *Color*\
  Entrada principal que modificar para el resultado.
* **Color de origen**: *Entrada de color*\
  Ranura de entrada para el color de origen, que solo se usa cuando el modo de color de origen está establecido en *Entrada*.
* **Color de destino**: *Entrada de color* Ranura de entrada para el color de destino, que solo se usa cuando &#39;Modo de color de destino&#39; está establecido en *Entrada*.

### Parámetros

* **Modo de color de origen**: *Average, Parameter, Input* Establece si el color de origen se define calculando el promedio de la imagen de entrada, estableciendo un parámetro o utilizando una ranura de entrada.
* **Color de origen**: *(Valor de color)* Si el modo de color de origen está establecido en *Parámetro*, este parámetro determina el color de origen.
* **Modo de color de destino**: *Parámetro, entrada de imagen* Establece si el color de origen se define promediando la imagen de entrada, estableciendo un parámetro o utilizando una ranura de entrada.
* **Color de destino**: *(Valor de color)* Si el modo de color de destino está establecido en *Parámetro*, este parámetro determina el color de destino.
* **Variación de color personalizada**: False/True\
  Permite una variación de color adicional.
* **Variación de color**\
  Establece las variaciones de tono, crominancia o luminancia en el resultado si está activado.
* **Usar máscara**: *Falso/Verdadero*\
  Cambia el uso de Entrada o Salida de máscara, en función del modo de máscara que se muestra a continuación.
* **Modo de máscara**: *Parámetro, entrada* El modo de parámetro emite una máscara que detalla cómo se cambió el color. El modo de entrada permite que una máscara controle la intensidad del efecto Coincidencia de color.
* **Máscara**\
  Genera una máscara que muestra dónde se aplicó exactamente el efecto Coincidencia de color, con controles adicionales para suavizar y desenfocar la máscara resultante.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
