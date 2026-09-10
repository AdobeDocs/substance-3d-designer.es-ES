---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi.html"
breadcrumb-title: ''
description: Utilice el nodo Voronoi 3D para generar patrones Voronoi basados en la posición mundial 3D para crear texturas celulares volumétricas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---


# 3D Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi.resources/3dvoronoi.png){width="200px"}

<b>En:</b> Generadores de Textura > Ruidos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo <b>3D Voronoi</b> genera un ruido Voronoi en el espacio 3D basado en la entrada <b>Mapa de posición</b>.

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
| <b>Escala</b> <i>Flotador</i> | Controla la escala del ruido Voronoi 3D.<br><br><i>Nota</i>: Cuando <b>Tiling</b> está habilitado en <i>cualquier eje</i>, el ajuste de escala es <i>stepped</i>. Esto es de esperar. |
| <b>Tamaño</b> <i>Float3</i> | Controla el tamaño del ruido Voronoi 3D en los ejes <b>X</b>, <b>Y</b> y <b>Z</b>. Los valores no uniformes dan como resultado un efecto <i>estirar o aplastar</i>.<br><br><i>Nota</i>: Cuando <b>Mosaico</b> está habilitado en <i>cualquier eje</i>, el ajuste de tamaño es <i>escalonado</i>. Esto es de esperar. |
| <b>Desplazamiento</b> <i>Float3</i> | Aplica un desplazamiento a la <i>posición</i> del ruido Voronoi 3D en los ejes <b>X</b>, <b>Y</b> y <b>Z</b>. |
| <b>Desorden</b> <i>Float3</i> | Intensidad del <i>desplazamiento aleatorio</i> aplicado a cada punto del ruido en los ejes <b>X</b>, <b>Y</b> y <b>Z</b>. |
| <b>Intensidad de Distorsión</b> <i>Flotador</i> | Controla la intensidad de un <i>efecto de deformación</i> aplicado al ruido Voronoi 3D. |
| <b>Multiplicador de escala de Distorsión</b> <i>Flotador</i> | Controla la escala del <i>patrón de deformación</i> utilizado en el efecto de deformación controlado por la <b>Intensidad de Distorsión</b>. |
| <b>Curva redondeada</b> <i>Flotador</i> | Redondea la <i>pendiente</i> alrededor de cada punto del ruido para que sea <i>convexa</i>.<br><br><i>Nota</i>: Este parámetro no está disponible cuando el parámetro <b>Style</b> está establecido en <i>Edge</i>. |
| <b>Escala de distancia</b> <i>Flotador</i> | Ajusta la <i>distancia del degradado</i> alrededor de cada punto del ruido. |
| <b>Modo de distancia</b> <i>Entero</i> | Establece el método para <i>calcular el degradado de distancia</i> alrededor de cada punto del ruido:<br><br>- <i>Euclidean</i><br>- <i>Manhattan</i><br>- <i>Chebyshev</i><br>- <i>Minkowski</i> |
| <b>Número de Minkowski</b> <i>Flotador</i> | El orden <i>p</i> de la distancia de Minkowski. Si dividimos el gradiente de distancia en cuadrantes, este número afecta a estos cuadrantes de la siguiente manera:<br><br>- p es <i>exactamente</i> 1: Straight<br>- p es <i>inferior</i> a 1: Cóncavo<br>- p es <i>mayor</i> que 1: Convexo<br><br>Valores interesantes:<br>- <i>1.0</i>: Distancia de Manhattan<br>- <i>2.0</i>: Distancia euclidiana<br>- <i>Infinito</i>: Distancia de Chebyshev<br><br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Distance Mode</b> está establecido en <i>Minkowski</i>. |
| <b>Estilo</b> <i>Entero</i> | Establece el método <i>que representa los datos</i> del ruido 3D Voronoi, teniendo en cuenta que el ruido se basa en un conjunto de puntos en el espacio 3D:<br><br>- <i>F1</i>: la distancia al <i>punto más cercano</i> en el espacio 3D<br>- <i>F2</i>: la distancia al <i>segundo punto más cercano</i> en el espacio 3D<br>- <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F1/F2</i><br>- <i>Edge</i>: el <i>borde entre cada celda</i> del ruido en el espacio 3D<br>- <i>Color aleatorio</i>: asignar un <i>color plano aleatorio</i> a cada celda del ruido en el espacio 3D |
| <b>Thickness Edge</b> <i>Flotador</i> | Ajusta el thickness de los bordes detectados entre las celdas del ruido Voronoi 3D. Se detectan bordes en los ejes X, Y y Z, por lo que algunos grosores pueden aumentar más rápido que otros dependiendo de la <i>profundidad</i> de las celdas.<br><br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Style</b> está establecido en <i>Edge</i>. |
| <b>Habilitar Mosaico</b> <i>Booleano</i> | Ajusta el ruido Voronoi 3D para que el patrón resultante <i>se repita</i> en los ejes X, Y y Z. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant2.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3dvoronoi-variant6.jpg" />
        </td>
    </tr>
</table>
