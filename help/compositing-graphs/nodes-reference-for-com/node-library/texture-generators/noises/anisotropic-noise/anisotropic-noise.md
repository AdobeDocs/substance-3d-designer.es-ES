---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
breadcrumb-title: ''
description: Utilice el nodo Ruido anisotrópico para generar patrones de ruido direccional para crear efectos de textura anisotrópica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Anisotropic noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido anisotrópico
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# Ruido anisotrópico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruido anisotrópico - Icono](../../../../../../assets/anisotropic_noise_v2.png "Ruido anisotrópico - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Pila horizontal o vertical de bandas de colores aleatorios que se desvanecen entre sí.

La cantidad de tiras es ajustable, al igual que el smoothness de sus transiciones.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Salidas

</td>
<td style="border: 0;" valign="top">

### Parámetros

</td>
<td style="border: 0;" valign="top">

### Ejemplos

</td>
</tr>
</table>

## Salidas

|  |  |
| --- | --- |
| <b>Salida</b> *Escala de grises* | El ruido generado como un mapa de bits en escala de grises. |

## Parámetros

|  |  |
| --- | --- |
| <b>X amount</b> Integer | Cantidad de bandas en el eje X. |
| <b>Cantidad Y</b> Entero | Cantidad de bandas en el eje Y. |
| <b>Cantidad Y por resolución</b> Booleano | Si su valor es True, el número de bandas del eje Y será igual al tamaño de imagen de dicho eje. |
| Booleano <b>Rotate</b> | Rota el ruido 90 grados. |
| Flotador <b>Smoothness</b> | Cantidad de atenuación entre las tiras, donde 0 es sin atenuación y 1 es atenuación en toda su longitud. |
| <b>Interpolación de Smoothness</b> Float | La ponderación de los dos métodos de interpolación aplicados para desvanecer las tiras, donde 0 es lineal y 1 es gaussiano. |
| Flotador <b>Disorder</b> | Desplaza los ingredientes del ruido.   Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> Flotador | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.   Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |
| <b>Expansión no cuadrada</b> Boolean | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido anisotrópico - Ejemplo 1](../../../../../../assets/anisotropic_noise_v2_1.png "Ruido anisotrópico - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido anisotrópico - Ejemplo 2](../../../../../../assets/noise_anisotropic_noise_v2_speed0.3_aniso0.6.gif "Ruido anisotrópico - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
