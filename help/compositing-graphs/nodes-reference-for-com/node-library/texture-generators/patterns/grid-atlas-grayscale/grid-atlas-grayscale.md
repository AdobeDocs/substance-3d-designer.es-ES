---
title: escala de grises del atlas de cuadrícula
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Generador > Patrón > Escala de grises de Atlas de cuadrícula
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# escala de grises del atlas de cuadrícula

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![icono de escala de grises de Atlas de cuadrícula](grid-atlas-grayscale.resources/grid-atlas-grayscale.png "escala de grises de Atlas de cuadrícula")

<b>En:</b> Generador > Patrón

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Incluye hasta 16 imágenes en escala de grises en una cuadrícula de tamaño XY ajustable.<br>La imagen del atlas de resultados se puede muestrear desde un nodo [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) o [Shape splatter mapper grayscale](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md).

Vea también [color de Atlas de cuadrícula](../grid-atlas-color/grid-atlas-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|                             |                                |
|:----------------------------|:-------------------------------|
| <b>Entrada 1</b> *Escala de grises* | Entrada de imagen en escala de grises #1. |
| <b>Entrada 2</b> *Escala de grises* | Entrada de imagen en escala de grises #2. |
| <b>Entrada 3</b> *Escala de grises* | Entrada de imagen en escala de grises #3. |
| <b>Entrada 4</b> *Escala de grises* | Entrada de imagen en escala de grises #4. |
| <b>Entrada 5</b> *Escala de grises* | Entrada de imagen en escala de grises #5. |
| <b>Entrada 6</b> *Escala de grises* | Entrada de imagen en escala de grises #6. |
| <b>Entrada 7</b> *Escala de grises* | Entrada de imagen en escala de grises #7. |
| <b>Entrada 8</b> *Escala de grises* | Entrada de imagen en escala de grises n.º 8. |
| <b>Entrada 9</b> *Escala de grises* | Entrada de imagen en escala de grises n.º 9. |
| <b>Entrada 10</b> *Escala de grises* | Entrada de imagen en escala de grises #10. |
| <b>Entrada 11</b> *Escala de grises* | Entrada de imagen en escala de grises #11. |
| <b>Entrada 12</b> *Escala de grises* | Entrada de imagen en escala de grises #12. |
| <b>Entrada 13</b> *Escala de grises* | Entrada de imagen en escala de grises #13. |
| <b>Entrada 14</b> *Escala de grises* | Entrada de imagen en escala de grises #14. |
| <b>Entrada 15</b> *Escala de grises* | Entrada de imagen en escala de grises #15. |
| <b>Entrada 16</b> *Escala de grises* | Entrada de imagen en escala de grises #16. |

<a name="outputs"></a>

## Salidas

|               |                                  |
|:--------------|:---------------------------------|
| <b>Salida</b> | El atlas de cuadrícula de escala de grises de salida. |

<a name="parameters"></a>

## Parámetros

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Tamaño de cuadrícula X</b> *Entero* | El tamaño de la cuadrícula en el eje X.<br>Es decir. el número de imágenes que se van a empaquetar en el eje X. |
| <b>Tamaño de cuadrícula Y</b> *Entero* | El tamaño de la cuadrícula en el eje Y.<br>Es decir. el número de imágenes que se van a empaquetar en el eje Y. |
| <b>Modo de tamaño de salida</b> *Entero* | Método para definir el tamaño de la imagen de salida según el parámetro base &quot;Tamaño de salida&quot; del nodo:<br><br>- <b>Manual:</b> Utilice el tamaño tal cual.<br>- <b>Proporción automática:</b> Ajuste la proporción de la imagen según el tamaño de la cuadrícula para minimizar el tamaño de la imagen. La deformación ocurrirá para cuadrículas no cuadradas usando 3 filas o columnas, p.ej. (3, 2, 4, 3) |

## Ejemplos

<img src="./grid-atlas-grayscale.resources/grid-atlas-grayscale-graph.png" alt="Atlas de cuadrícula de un nodo de escala de grises en el contexto de una gráfica" style="width: 50%"><br>
<i>Nodo de escala de grises de Atlas de cuadrícula en el contexto de un gráfico</i>
