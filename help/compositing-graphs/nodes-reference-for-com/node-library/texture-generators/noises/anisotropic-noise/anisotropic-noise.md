---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
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
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# Ruido anisotrópico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruido anisotrópico - Icono](anisotropic-noise.resources/anisotropic_noise_v2.png "Ruido anisotrópico - Icono"){width="200px"}

<b>En:</b> Generadores de texturas > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Pila horizontal o vertical de bandas de colores aleatorios que se desvanecen entre sí.

La cantidad de tiras es ajustable, al igual que el smoothness de sus transiciones.

</td>
</tr>
</table>

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | El ruido generado como un mapa de bits en escala de grises. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Importe X</b> <i>Entero</i> | Cantidad de bandas en el eje X. |
| <b>Importe Y</b> <i>Entero</i> | Cantidad de bandas en el eje Y. |
| <b>Importe Y por resolución</b> <i>Booleano</i> | Si su valor es True, el número de bandas del eje Y será igual al tamaño de imagen de dicho eje. |
| <b>Rotar</b> <i>Booleano</i> | Rota el ruido 90 grados. |
| <b>Smoothness</b> <i>Flotador</i> | Cantidad de atenuación entre las tiras, donde 0 es sin atenuación y 1 es atenuación en toda su longitud. |
| <b>Interpolación de Smoothness</b> <i>Flotante</i> | La ponderación de los dos métodos de interpolación aplicados para desvanecer las tiras, donde 0 es lineal y 1 es gaussiano. |
| <b>Desorden</b> <i>Flotante</i> | Desplaza los ingredientes del ruido.   Se puede utilizar para animar el ruido. |
| <b>Velocidad del desorden</b> <i>Flotante</i> | Ajusta la distancia de desplazamiento aplicada por el parámetro <b>Disorder</b>.   Se puede utilizar para controlar la velocidad del desplazamiento al animar el ruido. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | En imágenes no cuadradas, mantiene el cuadrado del mosaico generado y expande la generación de ruido a los límites de la imagen. |

## Ejemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruido anisotrópico - Ejemplo 1](anisotropic-noise.resources/anisotropic_noise_v2_1.png "Ruido anisotrópico - Ejemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruido anisotrópico - Ejemplo 2](anisotropic-noise.resources/noise_anisotropic_noise_v2_speed0.3_aniso0.6.gif "Ruido anisotrópico - Ejemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
