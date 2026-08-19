---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: Utilice el nodo Ruido de Perlin 3D para generar patrones de ruido de Perlin suaves en el espacio 3D para crear texturas volumétricas de aspecto natural.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruido de Perlin en 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# Ruido de Perlin en 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise.png){width="200px"}

**En:** *Generadores De Texturas**/Ruidos*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo **3D Perlin Noise** genera un ruido Perlin en el espacio 3D basado en la entrada **Position Map**.

Este nodo se puede probar con [Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) como entrada en lugar de un mapa con bake real (como se muestra en la imagen de ejemplo siguiente).

>[!WARNING]
>
> Este ruido está destinado a utilizarse únicamente con el *motor de GPU* (es decir, **Direct3D** o **OpenGL**). Vaya a **Herramientas > Cambiar motor...** o presione la tecla **F9** para seleccionar el motor deseado.

</td>
</tr>
</table>

## Parámetros

* **Invertir** *Booleano*\
  Invierte la imagen de salida.
* **Escala** *Flotante*\
  Controla la escala del ruido de Perlin 3D.
* **Tamaño** *Float3*\
  Controla el tamaño del ruido de Perlin 3D en los ejes **X**, **Y** y **Z**. Los valores no uniformes dan como resultado un efecto de *estiramiento o aplastamiento*.
* **Desplazamiento** *Flotador*\
  Aplica un desplazamiento a la *posición* del ruido de Perlin 3D en los ejes **X**, **Y** y **Z**.
* **Intensidad de Distorsión** *Float*\
  Controla la intensidad de un *efecto de deformación* aplicado al ruido de Perlin 3D.
* **Multiplicador de escala de Distorsión** *Float*\
  Controla la escala del *patrón de deformación* utilizado en el efecto de deformación controlado por la **Intensidad de Distorsión**.
* **Línea de base** *Flotante*\
  Aplica un *desplazamiento* al valor de *luminancia* de línea de base para la distribución de valor de ruido de Perlin 3D.
* **Contraste** *Flotante*\
  Ajusta el contraste del ruido de Perlin 3D.
* **Absoluto** *Booleano*\
  Utiliza valores absolutos en el ruido de Perlin 3D. Esto *invierte* la distribución de valor para los valores *inferiores a 0,5*.
* **Habilitar Mosaico** *Booleano*\
  Ajusta el ruido de Perlin 3D para que el patrón resultante *se repita* en los ejes X, Y y Z.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlin.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant.jpg){width="256px"}

</td>
</tr>
</table>
