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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# Renderizado de superficie de textura 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender.png){width="200px"}

**En:** *Filtro/Efecto*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

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

## Parámetros

### Entradas

* **Campo de distancia 3D** *Escala de grises*\
  Imagen de 4096x4096 que representa los 256 *sectores* del *campo de distancia* de una forma, organizados en una cuadrícula de 16x16.\
  Puede utilizar el nodo [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) para calcular el campo de distancia de una textura 3D de 256 sectores.
* **Entorno** *Color*\
  La imagen que representa el *entorno*, que debe asignarse a una esfera infinita en el renderizado y utilizarse para calcular la *iluminación*.\
  La imagen también se usa para representar el fondo de la escena cuando el parámetro **Background Mode** está establecido en *Ambient* o *Environment*.

### Parámetros

* **Resolución de salida** *Integer2*\
  La resolución de la imagen de salida en **X** e **Y**, expresada como una *potencia de dos*.
* **Posición de la cámara** *Float2*\
  Posición de la cámara alrededor de la forma.\
  Cuando el nodo esté seleccionado, puedes usar el gizmo de posición en la **Vista en 2D** para *orbitar* la cámara.
* **Distancia de cámara** *Flotante*\
  La distancia desde la cámara a la forma.
* **Fov de cámara** *Float*\
  Campo de visión de la cámara en *grados*.
* **Albedo** *Float3*\
  Color de albedo de la superficie de la forma.
* **Modo en segundo plano** *Entero*\
  El método para representar el fondo de la escena procesada:
  * *Irradiancia del suelo*: La irradiancia calculada del plano de tierra
  * *Ambiente*: El color de ambiente de la entrada de imagen **Environment** asignada a una esfera infinita, que es similar a una versión muy borrosa de la imagen
  * *Color uniforme*: Rellenar el fondo de manera uniforme con un color especificado
  * *Entorno*: La entrada de imagen **Environment** asignada a una esfera infinita
* **Color de fondo** *Float4*\
  El color utilizado para rellenar uniformemente el fondo de la escena procesada.\
  *Nota*: Este parámetro solo está disponible cuando el parámetro **Background Mode** está establecido en *Uniform Color*.
* **Habilitar plano de tierra** *Boolean*\
  Cuando *True*, representa un plano de tierra. El *cubo de unidades* que encierra la forma descansa en este plano.
* **Plano infinito** *Booleano*\
  Establece el plano de tierra para *extender infinitamente* hasta el horizonte.\
  *Nota*: Este parámetro solo está disponible cuando el parámetro **Habilitar plano de tierra** está establecido en *True*.
* **Tamaño de plano de tierra** *Float2* Ajusta el tamaño del plano de tierra.\
  *Nota*: Este parámetro solo está disponible cuando el parámetro **Habilitar plano de tierra** está establecido en *True* y el parámetro **Plano infinito** está establecido en *False*.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-node.png){width="512px"}

</td>
</tr>
</table>
