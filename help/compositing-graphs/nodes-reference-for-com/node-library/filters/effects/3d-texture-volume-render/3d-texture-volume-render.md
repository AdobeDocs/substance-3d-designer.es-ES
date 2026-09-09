---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: Utilice el nodo Procesamiento de volumen de Textura 3D para procesar texturas volumétricas de datos 3D para crear efectos de nube y niebla.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Procesamiento de volumen de Textura 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---


# Procesamiento de volumen de Textura 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-volume-render.resources/3dtexturevolumerender.png){width="200px"}

<b>En:</b> Filtro > Efecto

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo **Procesamiento de volumen de Textura 3D** procesa el volumen de una forma descrita por una *textura 3D*, utilizando su correspondiente *campo de distancia firmada* de la entrada de imagen **3D Campo de distancia con signo**.

El volumen se representa dentro de los límites de un *cubo de unidades*. La iluminación se calcula usando *luz direccional* y un *tragaluz hemisférico*.

>[!NOTE]
>
> Se espera que el campo de distancia firmado sea una textura **4096x4096** que describa la forma con una cuadrícula **16x16** de 256 sectores.\
> Puede utilizar el nodo [SDF de Textura 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) para calcular el campo de distancia firmado para una textura 3D de 256 sectores.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Campo de distancia con signo 3D</b> <i>Escala de grises</i> | Imagen de 4096x4096 que representa los 256 <i>sectores</i> del <i>campo de distancia firmado</i> de una forma, organizados en una cuadrícula de 16x16.<br>Puede usar el nodo [SDF de Textura 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) para calcular el campo de distancia firmado para una textura 3D de 256 sectores. |
| <b>Densidad</b> <i>Escala de grises</i> | Imagen de 4096x4096 que representa los 256 <i>sectores</i> de la <i>densidad</i> de una forma, organizados en una cuadrícula de 16x16. La densidad se asigna usando valores de escala de grises de 0 (totalmente transparente) a 1 (totalmente opaco).<br>Puede usar [Máscara de volumen 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) o nodos de ruido 3D ([Ruido de Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [Voronoi 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [Fractal de ruido de borde 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md), etc.), combinados con un nodo [Posición de Textura 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) como entrada de posición, para generar una máscara de volumen como una textura 3D de 256 sectores. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Resolución de salida</b> <i>Entero2</i> | La resolución de la imagen de salida en <b>X</b> e <b>Y</b>, expresada como una <i>potencia de dos</i>. |
| <b>Posición de la cámara</b> <i>Flotante2</i> | Posición de la cámara alrededor de la forma.<br>Cuando se selecciona el nodo, puedes usar el gizmo de posición en el <b>vista 2D</b> para <i>orbitar</i> la cámara. |
| <b>Posición de luz</b> <i>Flotante2</i> | Posición de la <i>luz direccional</i> alrededor de la forma.<br>Cuando el nodo esté seleccionado, puedes usar el gizmo de posición en el <b>vista 2D</b> para <i>orbitar</i> la fuente de luz. |
| <b>Distancia de cámara</b> <i>Flotante</i> | La distancia desde la cámara a la forma. |
| <b>FOV de cámara</b> <i>Flotante</i> | Campo de visión de la cámara en <i>grados</i>. |
| <b>Absorción</b> <i>Flotante</i> | Ajusta la cantidad de luz que se absorbe al pasar <i>a través</i> del volumen. |
| <b>Calado</b> <i>Flotante</i> | Multiplica el valor proporcionado por la entrada <b>Density</b> por el valor del campo de distancia <i>inner</i>.<br>Esto ajusta efectivamente la anchura del <i>degradado</i> desde el límite exterior del volumen hacia adentro. |
| <b>Modo de color claro</b> <i>Entero</i> | Establece el método para adquirir el color de la luz direccional:<br>- <i>Temperatura (Kelvin)</i>: El color es el resultado de la temperatura de la luz, donde un valor <i>inferior</i> da como resultado un color <i>más cálido</i><br>- <i>color RGB</i>: Definir el color mediante valores de RGB |
| <b>Temperatura de la luz (Kelvin)</b> <i>Flotante</i> | La temperatura de la luz direccional, que afecta a su <i>color</i>. Un valor <i>inferior</i> produce un color <i>más cálido</i>.<br>Valores útiles:<br>1800 K - Luz de vela<br>2800 K - Bombilla incandescente<br>5500 K - Luz del día<br>6200 K - Blanco natural<br>7000 K - Cielo nublado<br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Modo de color claro</b> está establecido en <i>Temperatura (Kelvin)</i>. |
| <b>Color claro</b> <i>Float3</i> | El color de la luz direccional.<br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Modo de color claro</b> está establecido en <i>Color RGB</i>. |
| <b>Intensidad de luz</b> <i>Flotador</i> | Intensidad de la luz direccional. |
| <b>Color de ambiente</b> <i>Float3</i> | El color del tragaluz ambiente. |
| <b>Intensidad del ambiente</b> <i>Flotador</i> | La intensidad del tragaluz ambiente. |
| <b>Albedo</b> <i>Float3</i> | Color de albedo del volumen. |
| <b>Modo en segundo plano</b> <i>Entero</i> | Método de sombreado del fondo de la escena representada, basado en el <b>color de fondo</b>:<br>- <i>sombreado</i>: El color se ve afectado por el <i>color</i> y la <i>intensidad</i><br>- <i>color constante</i> de la luz direccional: El color se aplica de manera uniforme <i>independientemente</i> de la luz direccional |
| <b>Color de fondo</b> <i>Float4</i> | El color utilizado para rellenar el fondo de la escena procesada. |
| <b>Tramado</b> <i>Flotador</i> | Ajusta la intensidad del <i>tramado de ruido azul</i> que se usa para suavizar el sombreado. |
| <b>Habilitar plano de tierra</b> <i>Booleano</i> | Cuando <i>True</i>, representa un plano de tierra <i>infinito</i>. El <i>cubo de unidades</i> que encierra la forma descansa en este plano. |
| <b>Plano infinito</b> <i>Booleano</i> | Establece el plano de tierra en <i>extender infinitamente</i> hasta el horizonte.<br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Habilitar plano de tierra</b> está establecido en <i>True</i>. |
| <b>Tamaño de plano de tierra</b> <i>Float2</i> | Ajusta el tamaño del plano de tierra.<br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Habilitar plano de tierra</b> está establecido en <i>True</i> y el parámetro <b>Plano infinito</b> está establecido en <i>False</i>. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-node.png" />
        </td>
    </tr>
</table>
