---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ""
description: Utilice el nodo Ruido de Perlin 3D para generar patrones de ruido de Perlin suaves en el espacio 3D para crear texturas volumétricas de aspecto natural.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido de Perlin en 3D
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%
---

# Ruido de Perlin en 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise.resources/3dperlinnoise.png){width="200px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo <b>3D Perlin Noise</b> genera un ruido Perlin en el espacio 3D basado en la entrada <b>Position Map</b>.

Este nodo se puede probar con [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) como entrada en lugar de un mapa con bake real (como se muestra en la imagen de ejemplo siguiente).

</td>
</tr>
</table>

>[!WARNING]
>
> Este ruido está destinado a utilizarse únicamente con el <i>motor de GPU</i> (es decir, <b>Direct3D</b> o <b>OpenGL</b>). Vaya a <b>Herramientas > Cambiar motor...</b> o presione la tecla <b>F9</b> para seleccionar el motor deseado.

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Invertir</b> <i>Booleano</i> | Invierte la imagen de salida. |
| <b>Escala</b> <i>Flotador</i> | Controla la escala del ruido de Perlin 3D. |
| <b>Tamaño</b> <i>Float3</i> | Controla el tamaño del ruido de Perlin 3D en los ejes <b>X</b>, <b>Y</b> y <b>Z</b>. Los valores no uniformes dan como resultado un efecto de <i>estiramiento o aplastamiento</i>. |
| <b>Desplazamiento</b> <i>Float3</i> | Aplica un desplazamiento a la <i>posición</i> del ruido de Perlin 3D en los ejes <b>X</b>, <b>Y</b> y <b>Z</b>. |
| <b>Intensidad de Distorsión</b> <i>Flotador</i> | Controla la intensidad de un <i>efecto de deformación</i> aplicado al ruido de Perlin 3D. |
| <b>Multiplicador de escala de Distorsión</b> <i>Flotador</i> | Controla la escala del <i>patrón de deformación</i> utilizado en el efecto de deformación controlado por la <b>Intensidad de Distorsión</b>. |
| <b>Línea de base</b> <i>Flotador</i> | Aplica un <i>desplazamiento</i> al valor de <i>luminancia</i> de línea de base para la distribución de valor de ruido de Perlin 3D. |
| <b>Contraste</b> <i>Flotador</i> | Ajusta el contraste del ruido de Perlin 3D. |
| <b>Absoluto</b> <i>Booleano</i> | Utiliza valores absolutos en el ruido de Perlin 3D. Esto <i>invierte</i> la distribución de valor para los valores <i>inferiores a 0,5</i>. |
| <b>Habilitar Mosaico</b> <i>Booleano</i> | Ajusta el ruido de Perlin 3D para que el patrón resultante <i>se repita</i> en los ejes X, Y y Z. |

## Ejemplos

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="3d-perlin-noise.resources/3dperlin.gif" class="modal-image" alt="Ruido 3D Perlin - Ejemplo 1" />
        </td>
        <td style="border: 0;">
            <img src="3d-perlin-noise.resources/3dperlinnoise-variant2.jpg" class="modal-image" alt="Ruido 3D Perlin - Ejemplo 2" />
        </td>
        <td style="border: 0;">
            <img src="3d-perlin-noise.resources/3dperlinnoise-variant.jpg" class="modal-image" alt="Ruido 3D Perlin - Ejemplo 3" />
        </td>
    </tr>
</table>
