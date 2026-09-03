---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: Utilice el nodo Color para enmascarar para convertir colores específicos en máscaras para crear efectos de procesamiento y enmascaramiento selectivos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color a máscara
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---


# Color a máscara

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Color para enmascarar - Icono](color-to-mask.resources/color-to-mask-01.png "Color para enmascarar - Icono"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Extrae una máscara de escala de grises de los colores seleccionados en una imagen en color.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Color</i> | Imagen de color de entrada de la que se debe extraer una máscara en función de sus colores. |
| <b>Entrada de color</b> <i>Color</i>   *Disponible cuando &#39;Usar entrada de color&#39; está establecido en &#39;True&#39;* | Imagen de color de entrada utilizada para definir el color de referencia por píxel. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | Máscara generada como mapa de bits en escala de grises. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Usar entrada de color</b> *Booleano* | Utilice una imagen de entrada en lugar de un color uniforme para definir un color de referencia por píxel.    La entrada <b>Color input</b> proporciona la imagen de entrada. |
| <b>Color</b> *Flotante3* *Disponible cuando &#39;Usar entrada de color&#39; está establecido en &#39;False&#39;* | Color uniforme de referencia alrededor del cual se debe realizar la selección de color. |
| <b>Umbral</b> *Flotante* | Distancia al color de referencia por debajo del cual se seleccionan los colores. |
| <b>Desvanecimiento de selección</b> *Flotador* | Desvanecer la selección de color según la distancia al color de referencia. |
| <b>Espacio de color de distancia</b> *Entero* | El proceso Ecualizar implica comparar colores para determinar la distancia entre ellos. Determinados espacios de color y algoritmos de distancia son más adecuados para casos de uso específicos.   Esta lista desplegable le permite seleccionar el espacio de color utilizado para comparar los colores:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB (Datos):</i></b> El color se divide en canales Rojo, Verde, Azul y se distribuye directamente a lo largo de esos ejes, sin tener en cuenta la percepción humana. Esto es adecuado para imágenes que contienen datos sin procesar.</li> <li data-preserve-html="true"><i>sRGB lineal (color):</i> El color se divide en canales Rojo, Verde, Azul y se distribuye en una relación lineal con la intensidad de luz de los píxeles. Esto es adecuado para imágenes que se pueden visualizar en pantallas.</li> <li data-preserve-html="true"><b><i>Luminancia (color):</i></b> El color se divide en los valores de Tono, Croma y Luminancia, donde solo se utiliza el valor de Luminancia en la comparación. Esto es adecuado para imágenes que se pueden visualizar en pantallas.</li> <li data-preserve-html="true"><i>Laboratorio (color):</i> Un espacio de color perceptual estandarizado, que distribuye los colores de tal manera que los colores que &#39;parecen&#39; cercanos están realmente cerca en el cubo. Esto es adecuado para imágenes que se pueden visualizar en pantallas.</li> <li data-preserve-html="true"><i>Ángulo (normal):</i> El color se divide en los ejes X, Y, Z de un vector y se compara mediante un producto de puntos. Esto es adecuado para imágenes que contienen normales de espacio tangente.</li> </ul> |
| <b>Grosores de distancia</b> *Float3* | El algoritmo de distancia de color Lab (DeltaE2000) introduce ciertos factores de peso para cada valor de luminosidad, croma y tono.   Los valores más bajos disminuirán la influencia de los factores en el algoritmo de diferencia de color.   Dado que el ojo generalmente acepta diferencias mayores en luminosidad (L) que en croma (C) o tono (H), una proporción predeterminada para (L:C:H) es (0,5:1:1). Una relación de 0,5:1:1 permitirá el doble de diferencia en luminosidad que en croma o tono. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
