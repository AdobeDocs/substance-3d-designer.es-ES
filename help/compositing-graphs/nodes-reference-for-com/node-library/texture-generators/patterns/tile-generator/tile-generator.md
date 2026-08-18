---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-generator.html"
breadcrumb-title: ''
description: Utilice el nodo Tile Generator para crear patrones de mosaico de procedimientos con controles de tamaño, desplazamiento y variación personalizables.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generador de mosaicos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---


# Generador de mosaicos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-generator.png){width="128px"}

## Tile Generator (color)

**En:** *Generadores De Texturas**/Patrones*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Tile Generator es uno de los nodos más avanzados de la biblioteca. Si aprendes a dominarlo, puedes crear cualquier tipo de patrón (dentro de algunas limitaciones). A partir de la versión 2017 2.1, ha habido algunas actualizaciones importantes, lo que pone a este nodo más en línea con lo que [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) puede hacer.

Este nodo es muy útil para una variedad de escenarios, pero tenga en cuenta que la simple lectura de parámetros no le enseñará completamente a usarlos. ¡Te sugerimos que experimentes también!

Para el 99% de todos los casos, la versión de color NO es necesaria!

Algunas sugerencias de uso general:

* Puedes empezar con una forma básica, pero si tienes una entrada personalizada (establece **Tipo de patrón** en *Entrada de imagen*), créala primero. Determina gran parte de la apariencia.
* Empieza por establecer correctamente tus cantidades X e Y.
* Encuentra el modo **Size** adecuado: Los modos relativos como **Intersticio** se comportan de manera muy diferente a los modos **Absoluto**.
* A continuación, ajuste la **escala** global y el **tamaño** no uniforme.
* Por último, modifique cualquier parámetro **&quot;Variation&quot;** hasta que cumpla sus necesidades. ¡La sutileza es clave con la variación!

## Parámetros

### Entradas

* **Entrada de patrón 1-6**: *Entrada en escala de grises*\
  Imagen de motivo personalizado, utilizada cuando el parámetro &quot;Motivo&quot; se define en &quot;Entrada de imagen&quot;.
* **Fondo**:*Entrada en escala de grises* Fondo que se va a usar en lugar de color sólido.

### Parámetros

* **Cantidad X**: *1 - 64*\
  Cantidad de repeticiones X del patrón.
* **Importe Y**: *1 - 64*\
  Cantidad de repeticiones Y del patrón.
* **Expansión no cuadrada**: *Falso/Verdadero*\
  Permite la compensación de aplastamiento y estiramiento con proporciones no cuadradas.
* **Patrón**
  * **Patrón**: *Entrada De Imagen, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media Campana, Campana Cortada, Media Luna, Cápsula, Cono*\
    Selecciona la forma de motivo que se va a utilizar.
  * **Número de entrada de patrón**: *1 - 6* Número de entradas de imagen diferentes que se deben usar. Solo está disponible cuando *Image Input* está seleccionado arriba.
  * **Distribución De Entrada De Patrón**: *Aleatorio, por número de motivo* Cómo elegir entre las diferentes entradas de imagen, si hay más de 1 seleccionado.
  * **Específico del patrón**: *0.0 - 1.0*\
    Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado.
  * **Filtrado de entrada de imagen (motor > v4 únicamente)**: *Bilineal + Mipmaps, Bilineal, Más Cercano*
  * **Rotación**: *0, 90, 180, 270* Gira todos los mosaicos globalmente por un ángulo definido en pasos de 90 grados.
  * **Aleatorio de rotación**: *0.0 - 1.0* La aleatoriedad gira un azulejo en uno de cuatro pasos de 90 grados.
  * **Voltear Quincunx**: *Falso/Verdadero* Gira cada dos mosaicos 90 grados.
  * **Aleatorio de simetría**: *0.0 - 1.0* Refleja aleatoriamente ciertos patrones según el modo aleatorio de simetría seleccionado. Cuanto más alto sea este valor, más patrones se reflejarán.
  * **Modo aleatorio de simetría**: *Horizontal + Vertical, Horizontal, Vertical* Determina el comportamiento del reflejo cuando el valor aleatorio de simetría es superior a 0.
* **Tamaño**
  * **** Modo Tamaño **:***Normal - Intersticio, Normal - Tamaño, Mantener proporción, Absoluto, Píxel*Establece el comportamiento general del tamaño del patrón.\
    Normal : Intersticio permite definir el espacio entre los elementos de patrón. Se ve afectada por la cantidad X e Y.\
    Normal : Tamaño permite definir el tamaño de los elementos de patrón, independientemente del espacio. Se ve afectada por la cantidad X e Y.\
    Mantener proporción le permite establecer un tamaño afectado por la cantidad de X e Y, pero la proporción de X e Y entre los dos se deja intacta.\
    Absoluto le permite establecer un tamaño absoluto que no se vea afectado por la cantidad X e Y.\
    El píxel le permite establecer un tamaño absoluto en píxeles, sin que se vea afectado por la cantidad de X e Y. El cambio de la resolución afectará al tamaño de los elementos.
  * **Tamaño medio**: *0.0 - 1.0* Cambia el tamaño alternando columnas y filas.
  * **Intersticio X/Y**: *0.0 - 1.0* Solo disponible en modo Normal - Tamaño intersticial. Cambia la brecha intersticial. Afecta a la unión entre las formas, permite un control no uniforme a diferencia de **Scale**.
  * **Tamaño (absoluto/píxel)**: *0.0 - 1.0*\
    Solo disponible fuera del modo de tamaño normal - intersticio. Establece un tamaño no uniforme, a diferencia de **Scale**.
  * **Escala**: *0.0 - 2.0* Establece la escala global.
  * **Escala aleatoria**: *0.0 - 1.0* Establece la variación de escala global por mosaico.
  * **Velocidad aleatoria de escala**: *0 - 1000* Desplazamientos de velocidad de variación de escala.
* **Posición**
  * **Desplazamiento**: *0.0 - 1.0* Desplaza todo el patrón de forma incremental en cada fila o columna consecutiva (el comportamiento depende del parámetro Desplazamiento vertical).
  * **Desplazamiento aleatorio**: *0.0 - 1.0* Aleatoriza el desplazamiento de línea.
  * **Desplazar semilla aleatoria**: *0 - 1000* Cambia la velocidad relativa del efecto de desplazamiento aleatorio.
  * **Desplazamiento vertical**: *Falso/Verdadero* Establece si el efecto Desplazamiento se produce sobre filas o líneas; Horizontal o Vertical.
  * **Posición aleatoria**: *0.0 - 1.0* Aleatoriza la posición de forma no uniforme, con control independiente para X e Y.
  * **Desplazamiento global**: *0.0 - 1.0* Desplaza todo el resultado en los ejes X e Y.
* **Rotación**
  * **Rotación**: *0.0 - 1.0* Realiza una rotación uniforme y libre de todos los mosaicos de motivos.
  * **Aleatorio de rotación**: *0.0 - 1.0* Aleatoriza la rotación libre de todos los mosaicos. Cuanto más alto sea este valor, más mosaicos se pueden girar.
* **Color**
  * **Color**: *(Valor de escala de grises)*Define el color sólido del azulejo.
  * **Aleatorio de luminancia/color**: *0.0 - 1.0* Introduce la variación de color o luminancia por mosaico.
  * **Luminancia Por Número**: *Falso/Verdadero* Desvanece la luminancia en todo el patrón.
  * **Luminancia Por Escala**: *Falso/Verdadero* Hace que la variación de luminancia dependa de la escala del azulejo.
  * **Máscara de verificador**: *Falso/Verdadero* Oculta cada dos mosaicos.
  * **Máscara horizontal**: *Falso/Verdadero* Oculta las columnas alternas.
  * **Máscara vertical**: *Falso/Verdadero* Oculta las filas alternas.
  * **Máscara aleatoria**: *0.0 - 1.0* Oculta los mosaicos de forma aleatoria. Cuanto más alto sea este valor, más mosaicos desaparecerán.
  * **Invertir máscara**: *Falso/Verdadero* Invierte el resultado de cualquier efecto de máscara de esta sección.
  * **Modo De Fusión**: *Agregar, Máx., Agregar Sub* Establece qué modo de fusión usar.
  * **Color de fondo**: *(Valor de escala de grises)*Define el color de fondo sólido.
  * **Opacidad global**: *0.0 - 1.0* Establece la opacidad de los mosaicos globales.
  * **Orden de procesamiento inverso**: *Falso/Verdadero* Muestra los mosaicos de vuelta al frente o viceversa.

## Imágenes de ejemplo

![](../../../../../../assets/tilesampler-ex.png)

![](../../../../../../assets/image2020-9-17-14-50-18.png)

![](../../../../../../assets/image2020-9-17-14-52-4.png)

![](../../../../../../assets/image2020-9-17-14-53-47.png)

</td>
</tr>
</table>
