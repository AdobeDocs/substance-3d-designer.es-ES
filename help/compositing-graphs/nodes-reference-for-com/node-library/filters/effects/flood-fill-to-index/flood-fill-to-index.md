---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: Utilice el nodo Flood Fill a índice para rellenar regiones con valores de índice para crear patrones numerados y etiquetados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill a índice
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 2%

---


# Flood Fill a índice

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## Flood Fill a índice

**En:** *Filtros/Efectos*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Flood Fill a índice convierte cada celda de Flood Fill en un valor según su número de índice, comenzando por 0 en la esquina superior izquierda. Se puede utilizar para devolver matices de escala de grises de forma normalizada (de 0,0 a 1,0, divididos por tantas celdas como encuentre el Flood Fill) o como un valor HDR sin fijar (de 0 a n, donde n es el número de celdas).

Además, Flood Fill a índice utiliza el nuevo sistema [Value, devolviendo valores adicionales](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/values-in-substance-3d-graphs-180192235.html) que contienen la cantidad de formas encontradas y la tabla de datos interna opcional.

### Entradas

* **Flood Fill Box**: *Entrada de color* Mapa de entrada de Flood Fill estándar. Requerido.
* **Información de forma especial**: *La entrada de color* mapa de Flood Fill adicional debe habilitarse explícitamente en el nodo de Flood Fill anterior y es necesario que esté conectada.

### Parámetros

* **Salida**: *Normalizado, entero* Determina si la salida está en el rango LDR 0-1 o en el rango HDR 0-n.
* **Omitir forma menor que**: *0.0 - 1.0* Valor de tolerancia para ignorar formas pequeñas.
* **Mostrar tabla de datos del Flood Fill**: *Falso/Verdadero* Devuelve datos adicionales (de depuración) para uso avanzado.

## Ejemplos

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
