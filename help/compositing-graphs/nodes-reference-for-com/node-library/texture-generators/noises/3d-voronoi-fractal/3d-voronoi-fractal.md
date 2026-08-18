---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi-fractal.html"
breadcrumb-title: ''
description: Utilice el nodo 3D voronoi fractal para generar patrones fractales de Voronoi basados en la posición 3D para texturas volumétricas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D voronoi fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 0%

---


# 3D voronoi fractal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal.png){width="200px"}

**En:** *Generadores De Texturas* */Ruidos*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo **3D voronoi fractal** genera un ruido *fractal* Voronoi en el espacio 3D basado en la entrada **Position Map**.

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
  Controla la escala del ruido fractal de Voronoi 3D.\
  *Nota*: Cuando **Tiling** está habilitado en *cualquier eje*, el ajuste de escala es *stepped*. Esto es de esperar.
* **Tamaño** *Float3*\
  Controla el tamaño del ruido fractal 3D Voronoi en los ejes **X**, **Y** y **Z**. Los valores no uniformes dan como resultado un efecto de *estiramiento o aplastamiento*.\
  *Nota*: Cuando **Mosaico** está habilitado en *cualquier eje*, el ajuste de tamaño es *escalonado*. Esto es de esperar.
* **Desplazamiento** *Flotador*\
  Aplica un desplazamiento a la *posición* del ruido fractal 3D Voronoi en los ejes **X**, **Y** y **Z**.
* **Desorden** *Float3*\
  Intensidad del *desplazamiento aleatorio* aplicado a cada punto del ruido en los ejes **X**, **Y** y **Z**.
* **Intensidad de Distorsión** *Float*\
  Controla la intensidad de un *efecto de deformación* aplicado al ruido fractal 3D Voronoi.
* **Multiplicador de escala de Distorsión** *Float*\
  Controla la escala del *patrón de deformación* utilizado en el efecto de deformación controlado por la **Intensidad de Distorsión**.
* **Nivel Mínimo** *Entero*\
  Nivel mínimo de *repetición* usado en el patrón fractal. Un rango mínimo/máximo más amplio da como resultado un *patrón más enriquecido* con variaciones en rangos de frecuencia más amplios.
* **Nivel máximo** *Entero*\
  Nivel máximo de *repetición* usado en el patrón fractal. Un rango mínimo/máximo más amplio da como resultado un *patrón más enriquecido* con variaciones en rangos de frecuencia más amplios.
* **Rugosidad** *Flotante*\
  Controla el *equilibrio* entre los *niveles de repetición* bajos y altos en el patrón fractal.\
  *Nota*: Un valor de **0** da como resultado un resultado que está *fuera de línea* con otros valores bajos que lo siguen. Esto es de esperar.\
  *Nota 2*: Este parámetro solo está disponible cuando el parámetro **Blend Mode** está establecido en *Add*.
* **Lacunaridad** *Flotante*\
  Controla cómo el patrón fractal aplicado *rellena el espacio*. Un valor *superior* provoca *menos brechas* en el patrón y un ruido *más denso*.
* **Opacidad global** *Float*\
  Controla el *intervalo* de los valores de ruido fractal de Perlin 3D desde 0.
* **Curva redondeada** *Flotante*\
  Redondea la *pendiente* alrededor de cada punto del ruido para que sea *convexa*.\
  *Nota*: Este parámetro no está disponible cuando el parámetro **Style** está establecido en *Edge*.
* **Escala de distancia** *Flotante*\
  Ajusta la *distancia del degradado* alrededor de cada punto del ruido.
* **Modo de distancia** *Entero*\
  Establece el método para *calcular el degradado de distancia* alrededor de cada punto del ruido:
  * *Euclidean*
  * *Manhattan*
  * *Chebyshev*
  * *Minkowski*
* **Número de Minkowski** *Flotador*\
  El orden *p* de la distancia de Minkowski. Si dividimos el gradiente de distancia en cuadrantes, este número afecta a estos cuadrantes de la siguiente manera:
  * p es *exactamente* 1: Recto
  * p es *inferior* a 1: Cóncavo
  * p es *mayor* que 1: Convexo\
    Valores interesantes:\
    *- 1.0*: Distancia a Manhattan\
    *- 2.0*: Distancia euclidiana\
    *- Infinito*: Distancia de Chebyshev\
    *Nota*: Este parámetro solo está disponible cuando el parámetro **Distance Mode** está establecido en *Minkowski*.
* **Modo de fusión** *Entero*\
  Establece el método para fusionar los valores de *celdas superpuestas* en el espacio 3D:
  * *Agregar*: Agregar los valores
  * *Máx.*: Conservar el valor *más alto*
  * *Min*: Mantener el valor *más bajo*
* **Estilo** *Entero* Establece el método *que representa los datos* del ruido fractal 3D Voronoi, teniendo en cuenta que el ruido se basa en un conjunto de puntos en el espacio 3D:
  * *F1*: la distancia al *punto más cercano* en el espacio 3D
  * *F2*: la distancia al *segundo punto más cercano* en el espacio 3D
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Edge *: el* borde entre cada celda* del ruido en el espacio 3D
  * *Color aleatorio*: asigne un *color plano aleatorio* a cada celda del ruido en el espacio 3D
* **Thickness Edge** *Float* Ajusta el thickness de los bordes detectados entre las celdas del ruido fractal 3D Voronoi. Los bordes se detectan en los ejes X, Y y Z, por lo que algunos grosores pueden aumentar más rápido que otros dependiendo de la *profundidad* de las celdas.\
  *Nota*: Este parámetro solo está disponible cuando el parámetro **Style** está establecido en *Edge*.
* **Habilitar Mosaico** *Booleano*\
  Ajusta el ruido fractal de Voronoi 3D para que el patrón resultante *se repita* en los ejes X, Y y Z.

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant6.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant3.jpg){width="256px"}

</td>
</tr>
</table>
