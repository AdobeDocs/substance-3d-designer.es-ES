---
title: color del atlas de cuadrícula
description: Designer > Gráficos de composición de Substance > Referencia de nodos para gráficos de composición de Substance > Biblioteca de nodos > Generador > Patrón > Color de Atlas de cuadrícula
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# color del atlas de cuadrícula

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![icono de color de Atlas de cuadrícula](grid-atlas-color.resources/grid-atlas-color-01.png "color de Atlas de cuadrícula")

<b>En:</b> Generador > Patrón

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Empaquetado de hasta 16 imágenes en color en una cuadrícula de tamaño XY ajustable.<br>La imagen del atlas de salida se puede muestrear desde un nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) o [Shape splatter mapper color](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md).

Vea también [escala de grises del Atlas de cuadrícula](../grid-atlas-grayscale/grid-atlas-grayscale.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|                         |                            |
|:------------------------|:---------------------------|
| <b>Entrada 1</b> *Color* | Entrada de imagen de color #1. |
| <b>Entrada 2</b> *Color* | La entrada de imagen de color #2. |
| <b>Entrada 3</b> *Color* | Entrada de imagen de color #3. |
| <b>Entrada 4</b> *Color* | Entrada de imagen de color #4. |
| <b>Entrada 5</b> *Color* | Entrada de imagen de color #5. |
| <b>Entrada 6</b> *Color* | Entrada de imagen de color #6. |
| <b>Entrada 7</b> *Color* | Entrada de imagen de color #7. |
| <b>Entrada 8</b> *Color* | Entrada de imagen de color #8. |
| <b>Entrada 9</b> *Color* | La imagen de color de entrada #9. |
| <b>Entrada 10</b> *Color* | La entrada de imagen de color #10. |
| <b>Entrada 11</b> *Color* | La entrada de imagen de color #11. |
| <b>Entrada 12</b> *Color* | La entrada de imagen de color #12. |
| <b>Entrada 13</b> *Color* | La entrada de imagen de color #13. |
| <b>Entrada 14</b> *Color* | La entrada de imagen de color #14. |
| <b>Entrada 2</b> *Color* | La entrada de imagen de color #15. |
| <b>Entrada 2</b> *Color* | La entrada de imagen de color #16. |

<a name="outputs"></a>

## Salidas

|               |                              |
|:--------------|:-----------------------------|
| <b>Salida</b> | El atlas de cuadrícula de color de salida. |

<a name="parameters"></a>

## Parámetros

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Tamaño de cuadrícula X</b> *Entero* | El tamaño de la cuadrícula en el eje X.<br>Es decir. el número de imágenes que se van a empaquetar en el eje X. |
| <b>Tamaño de cuadrícula Y</b> *Entero* | El tamaño de la cuadrícula en el eje Y.<br>Es decir. el número de imágenes que se van a empaquetar en el eje Y. |
| <b>Modo de tamaño de salida</b> *Entero* | Método para definir el tamaño de la imagen de salida según el parámetro base &quot;Tamaño de salida&quot; del nodo:<br><br>- <b>Manual:</b> Utilice el tamaño tal cual.<br>- <b>Proporción automática:</b> Ajuste la proporción de la imagen según el tamaño de la cuadrícula para minimizar el tamaño de la imagen. La deformación ocurrirá para cuadrículas no cuadradas usando 3 filas o columnas, p.ej. (3, 2, 4, 3) |

## Ejemplos

<img src="./grid-atlas-color.resources/grid-atlas-color-02.png" alt="Nodo de color de atlas de cuadrícula en el contexto de una gráfica" style="width: 50%"><br>
<i>Nodo de color de Atlas de cuadrícula en el contexto de un gráfico</i>