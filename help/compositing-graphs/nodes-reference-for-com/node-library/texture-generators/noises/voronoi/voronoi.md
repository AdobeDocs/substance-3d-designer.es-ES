---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: Use el nodo Voronoi para generar patrones de Voronoi para crear texturas celulares y efectos de materiales orgánicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](voronoi.resources/voronoi-01.png){width="200px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo **Voronoi** genera un ruido Voronoi 3D asignado a una imagen 2D mediante una *proyección ortográfica Z-down*.

Este nodo se puede probar con [Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) como entrada en lugar de un mapa con bake real (como se muestra en la imagen de ejemplo siguiente).

>[!WARNING]
>
> Este ruido está destinado a utilizarse únicamente con el *motor de GPU* (es decir, **Direct** o **OpenGL**). Vaya a **Herramientas > Cambiar motor...** o presione la tecla **F9** para seleccionar el motor deseado.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Invertir</b> <i>Booleano</i> | Invierte la imagen de salida. |
| <b>Escala</b> <i>Flotador</i> | Controla la escala del ruido Voronoi.<br><br>*Nota*: Cuando **Tiling** está habilitado en *cualquier eje*, el ajuste de escala es *stepped*. Esto es de esperar. |
| <b>Tamaño</b> <i>Float3</i> | Controla el tamaño del ruido Voronoi en los ejes **X**, **Y** y **Z**. Los valores no uniformes dan como resultado un efecto *estirar o aplastar*.<br><br>*Nota*: Cuando **Mosaico** está habilitado en *cualquier eje*, el ajuste de tamaño es *escalonado*. Esto es de esperar. |
| <b>Desplazamiento</b> <i>Float3</i> | Aplica un desplazamiento a la *posición* del ruido Voronoi en los ejes **X**, **Y** y **Z**. |
| <b>Desorden</b> <i>Float3</i> | Intensidad del *desplazamiento aleatorio* aplicado a cada punto del ruido en los ejes **X**, **Y** y **Z**. |
| <b>Intensidad de Distorsión</b> <i>Flotador</i> | Controla la intensidad de un *efecto de deformación* aplicado al ruido Voronoi. |
| <b>Multiplicador de escala de Distorsión</b> <i>Flotador</i> | Controla la escala del *patrón de deformación* utilizado en el efecto de deformación controlado por la **Intensidad de Distorsión**. |
| <b>Curva redondeada</b> <i>Flotador</i> | Redondea la *pendiente* alrededor de cada punto del ruido para que sea *convexa*.<br><br>*Nota*: Este parámetro no está disponible cuando el parámetro **Style** está establecido en *Edge*. |
| <b>Escala de distancia</b> <i>Flotador</i> | Ajusta la *distancia del degradado* alrededor de cada punto del ruido. |
| <b>Modo de distancia</b> <i>Entero</i> | Establece el método para *calcular el degradado de distancia* alrededor de cada punto del ruido:<br><br>- *Euclidean*<br>- *Manhattan*<br>- *Chebyshev*<br>- *Minkowski* |
| <b>Número de Minkowski</b> <i>Flotador</i> | El orden *p* de la distancia de Minkowski. Si dividimos el gradiente de distancia en cuadrantes, este número afecta a estos cuadrantes de la siguiente manera:<br><br>- p es *exactamente* 1: Straight<br>- p es *inferior* a 1: Cóncavo<br>- p es *mayor* que 1: Convexo<br><br>Valores interesantes:<br><br>- *1.0*: Distancia de Manhattan<br>- *2.0*: Distancia euclidiana<br>- *Infinito*: Distancia de Chebyshev <br><br>*Nota*: Este parámetro solo está disponible cuando el parámetro **Distance Mode** está establecido en *Minkowski*. |
| <b>Estilo</b> <i>Entero</i> | Establece el método *que representa los datos* del ruido Voronoi, teniendo en cuenta que el ruido se basa en un conjunto de puntos del espacio:<br><br>- *F1*: la distancia al *punto más cercano* en el espacio<br>- *F2*: la distancia al *segundo punto más cercano* en el espacio<br>- *F2-F1*<br>- *F1\* F2 *<br>-* F1/F2 *<br>-* Edge *: el* borde entre cada celda *del ruido en el espacio<br>-* Color aleatorio *: asignar un* color plano aleatorio* a cada celda del ruido en el espacio |
| <b>Thickness Edge</b> <i>Flotador</i> | Ajusta el thickness de los bordes detectados entre las celdas del ruido Voronoi. Se detectan bordes en los ejes X, Y y Z, por lo que algunos grosores pueden aumentar más rápido que otros dependiendo de la *profundidad* de las celdas.<br><br>*Nota*: Este parámetro solo está disponible cuando el parámetro **Style** está establecido en *Edge*. |
| <b>Modo de inicialización de color aleatorio</b> <i>Entero</i> | Establece el método de *obtención* de la semilla aleatoria para la selección de color por celda:<br><br>- *Raíz aleatoria global*: Use la inicialización *heredada* por el nodo<br>- *inicialización manual*: Usar una *semilla discreta*<br><br>*Nota*: Este parámetro solo está disponible cuando el parámetro **Style** está establecido en *Random color*. |
| <b>Raíz de color aleatoria</b> <i>Entero</i> | La semilla aleatoria discreta que se debe usar para la selección de color por celda.<br><br>*Nota*: Este parámetro solo está disponible cuando el parámetro **Style** está establecido en *Random color* y el parámetro **Random Color Seed Mode** está establecido en ***Manual Seed***. |
| <b>Expansión no cuadrada</b> <i>Booleano</i> | Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-06.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-07.jpg" />
        </td>
    </tr>
</table>
