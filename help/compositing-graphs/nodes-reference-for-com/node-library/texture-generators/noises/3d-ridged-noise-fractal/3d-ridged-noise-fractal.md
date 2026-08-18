---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Fractal de ruido de reborde 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal.png){width="200px"}

**En:** *Generadores De Texturas**/Ruidos*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo **3D Ridged Noise Fractal** genera un ruido *fractal* Ridged en el espacio 3D basado en la entrada **Position Map**.

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
  Controla la escala del ruido fractal 3D Ridged.
* **Tamaño** *Float3*\
  Controla el tamaño del ruido fractal 3D Ridged en los ejes **X**, **Y** y **Z**. Los valores no uniformes dan como resultado un efecto de *estiramiento o aplastamiento*.
* **Desplazamiento** *Flotador*\
  Aplica un desplazamiento a la *posición* del ruido fractal 3D Ridged en los ejes **X**, **Y** y **Z**.
* **Intensidad de Distorsión** *Float*\
  Controla la intensidad de un *efecto de deformación* aplicado al ruido fractal 3D Ridged.
* **Multiplicador de escala de Distorsión** *Float*\
  Controla la escala del *patrón de deformación* utilizado en el efecto de deformación controlado por la **Intensidad de Distorsión**.
* **Nivel Mínimo** *Entero*\
  Nivel mínimo de *repetición* usado en el patrón fractal. Un rango mínimo/máximo más amplio da como resultado un *patrón más enriquecido* con variaciones en rangos de frecuencia más amplios.
* **Nivel máximo** *Entero*\
  Nivel máximo de *repetición* usado en el patrón fractal. Un rango mínimo/máximo más amplio da como resultado un *patrón más enriquecido* con variaciones en rangos de frecuencia más amplios.
* **Rugosidad** *Flotante*\
  Controla el *equilibrio* entre los *niveles de repetición* bajos y altos en el patrón fractal.\
  *Nota*: Un valor de **0** da como resultado un resultado que está *fuera de línea* con otros valores bajos que lo siguen. Esto es de esperar.
* **Lacunaridad** *Flotante*\
  Controla cómo el patrón fractal aplicado *rellena el espacio*. Un valor *superior* provoca *menos brechas* en el patrón y un ruido *más denso*.
* **Opacidad global** *Float*\
  Controla el *intervalo* de los valores de ruido fractal 3D Ridged *alrededor de* el valor **Baseline**.
* **Línea de base** *Flotante*\
  Aplica un *desplazamiento* al valor de *luminancia* de línea de base para la distribución de valor de ruido 3D Ridged.
* **Contraste** *Flotante*\
  Ajusta el contraste del ruido de 3D Ridged.
* **Habilitar Mosaico** *Booleano*\
  Ajusta el ruido 3D Ridged para que el patrón resultante *se repita* en los ejes X, Y y Z.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dridgednoisefractal-variant2.jpg){width="256px"}

</td>
</tr>
</table>
