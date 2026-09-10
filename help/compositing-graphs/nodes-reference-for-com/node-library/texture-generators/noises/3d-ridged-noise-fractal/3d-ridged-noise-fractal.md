---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
breadcrumb-title: ''
description: Utilice el nodo Fractal de ruido de reborde 3D para generar patrones de ruido fractal de reborde en el espacio 3D para crear texturas similares a las de una montaña.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Ridged Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fractal de ruido de reborde 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# Fractal de ruido de reborde 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-ridged-noise-fractal.resources/3dridgednoisefractal.png){width="200px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo <b>3D Ridged Noise Fractal</b> genera un ruido <i>fractal</i> Ridged en el espacio 3D basado en la entrada <b>Position Map</b>.

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
| <b>Escala</b> <i>Flotador</i> | Controla la escala del ruido fractal 3D Ridged. |
| <b>Tamaño</b> <i>Float3</i> | Controla el tamaño del ruido fractal 3D Ridged en los ejes <b>X</b>, <b>Y</b> y <b>Z</b>. Los valores no uniformes dan como resultado un efecto de <i>estiramiento o aplastamiento</i>. |
| <b>Desplazamiento</b> <i>Float3</i> | Aplica un desplazamiento a la <i>posición</i> del ruido fractal 3D Ridged en los ejes <b>X</b>, <b>Y</b> y <b>Z</b>. |
| <b>Intensidad de Distorsión</b> <i>Flotador</i> | Controla la intensidad de un <i>efecto de deformación</i> aplicado al ruido fractal 3D Ridged. |
| <b>Multiplicador de escala de Distorsión</b> <i>Flotador</i> | Controla la escala del <i>patrón de deformación</i> utilizado en el efecto de deformación controlado por la <b>Intensidad de Distorsión</b>. |
| <b>Nivel Mínimo</b> <i>Entero</i> | Nivel mínimo de <i>repetición</i> usado en el patrón fractal. Un rango mínimo/máximo más amplio da como resultado un <i>patrón más enriquecido</i> con variaciones en rangos de frecuencia más amplios. |
| <b>Nivel máximo</b> <i>Entero</i> | Nivel máximo de <i>repetición</i> usado en el patrón fractal. Un rango mínimo/máximo más amplio da como resultado un <i>patrón más enriquecido</i> con variaciones en rangos de frecuencia más amplios. |
| <b>Rugosidad</b> <i>Flotador</i> | Controla el <i>equilibrio</i> entre los <i>niveles de repetición</i> bajos y altos en el patrón fractal.<br><br><i>Nota</i>: Un valor de <b>0</b> da como resultado un resultado que está <i>fuera de línea</i> con otros valores bajos que lo siguen. Esto es de esperar. |
| <b>Lacunaridad</b> <i>Flotador</i> | Controla cómo el patrón fractal aplicado <i> rellena el espacio </i>. Un valor <i>superior</i> provoca <i>menos brechas</i> en el patrón y un ruido <i>más denso</i>. |
| <b>Opacidad global</b> <i>Flotador</i> | Controla el <i>intervalo</i> de los valores de ruido fractal 3D Ridged <i>alrededor de</i> el valor <b>Baseline</b>. |
| <b>Línea de base</b> <i>Flotador</i> | Aplica un <i>desplazamiento</i> al valor de <i>luminancia</i> de línea de base para la distribución de valor de ruido 3D Ridged. |
| <b>Contraste</b> <i>Flotador</i> | Ajusta el contraste del ruido de 3D Ridged. |
| <b>Habilitar Mosaico</b> <i>Booleano</i> | Ajusta el ruido 3D Ridged para que el patrón resultante <i>se repita</i> en los ejes X, Y y Z. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3dridgednoisefractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3dridgednoisefractal-variant2.jpg" />
        </td>
    </tr>
</table>
