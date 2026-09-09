---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: Utilice el nodo Procesamiento de superficie de textura 3D para procesar texturas de superficie a partir de datos 3D para crear efectos de superficie de procedimiento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderizado de superficie de textura 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Renderizado de superficie de textura 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-surface-render.resources/3dtexturesurfacerender.png){width="200px"}

<b>En:</b> Filtro > Efecto

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo **3D Texture Surface Render** representa la superficie de una forma descrita por una *textura 3D*, utilizando su correspondiente *campo de distancia* de la entrada de imagen del **Campo de distancia 3D**.

La superficie se representa dentro de los límites de un *cubo de unidades*. La iluminación se calcula utilizando la imagen de entrada **Environment** asignada a una esfera infinita.

>[!NOTE]
>
> Se espera que el campo de distancia sea una textura **4096x4096** que describa la forma con una cuadrícula **16x16** de 256 sectores.\
> Puede utilizar el nodo [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) para calcular el campo de distancia de una textura 3D de 256 sectores.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Campo de distancia 3D</b> <i>Escala de grises</i> | Imagen de 4096x4096 que representa los 256 <i>sectores</i> del <i>campo de distancia</i> de una forma, organizados en una cuadrícula de 16x16.<br>Puede usar el nodo [SDF de Textura 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) para calcular el campo de distancia de una textura 3D de 256 sectores. |
| <b>Entorno</b> <i>Color</i> | La imagen que representa el <i>entorno</i>, que debe asignarse a una esfera infinita en el renderizado y utilizarse para calcular la <i>iluminación</i>.<br>La imagen también se usa para representar el fondo de la escena cuando el parámetro <b>Background Mode</b> está establecido en <i>Ambient</i> o <i>Environment</i>. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Resolución de salida</b> <i>Entero2</i> | La resolución de la imagen de salida en <b>X</b> e <b>Y</b>, expresada como una <i>potencia de dos</i>. |
| <b>Posición de la cámara</b> <i>Float2</i> | Posición de la cámara alrededor de la forma.<br>Cuando se selecciona el nodo, puedes usar el gizmo de posición en el <b>vista 2D</b> para <i>orbitar</i> la cámara. |
| <b>Distancia de cámara</b> <i>Flotante</i> | La distancia desde la cámara a la forma. |
| <b>FOV de cámara</b> <i>Flotante</i> | Campo de visión de la cámara en <i>grados</i>. |
| <b>Albedo</b> <i>Flotante3</i> | Color de albedo de la superficie de la forma. |
| <b>Modo en segundo plano</b> <i>Entero</i> | El método para representar el fondo de la escena representada:<br>- <i>Irradiancia del suelo</i>: La irradiancia calculada del plano de tierra<br>- <i>Ambiente</i>: El color de ambiente de la entrada de imagen <b>Environment</b> asignada a una esfera infinita, que es similar a una versión muy borrosa de la imagen<br>- <i>Color uniforme</i>: Rellene el fondo de manera uniforme con un color especificado: <br>- <i>Entorno</i>: La entrada de imagen <b>Environment</b> está asignada a una esfera infinita |
| <b>Color de fondo</b> <i>Flotante4</i> | Color utilizado para rellenar uniformemente el fondo de la escena procesada.<br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Background Mode</b> está establecido en <i>Color uniforme</i>. |
| <b>Habilitar plano de tierra</b> <i>Booleano</i> | Cuando <i>True</i>, representa un plano de tierra. El <i>cubo de unidades</i> que encierra la forma descansa en este plano. |
| <b>Plano infinito</b> <i>Booleano</i> | Establece el plano de tierra en <i>extender infinitamente</i> hasta el horizonte.<br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Habilitar plano de tierra</b> está establecido en <i>True</i>. |
| <b>Tamaño de plano de tierra</b> <i>Flotante2</i> | Ajusta el tamaño del plano de tierra.<br><i>Nota</i>: Este parámetro solo está disponible cuando el parámetro <b>Habilitar plano de tierra</b> está establecido en <i>True</i> y el parámetro <b>Plano infinito</b> está establecido en <i>False</i>. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-node.png" />
        </td>
    </tr>
</table>
