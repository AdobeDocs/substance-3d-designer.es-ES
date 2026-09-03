---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/technical-issues/incorrect-image-output.html"
breadcrumb-title: ''
description: Solucione problemas de salida de imágenes incorrectas en Substance 3D Designer y aprenda a corregir problemas de procesamiento.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Incorrect image output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Salida de imagen incorrecta
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 0%

---


# Salida de imagen incorrecta

En esta página se enumeran los problemas técnicos de Substance 3D Designer que producen una salida de imagen incorrecta o inesperada y se ofrecen pasos de solución de problemas para cada uno.

## Bandas/pasos visibles

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(error)](incorrect-image-output.resources/error.svg) Problema**

Los degradados de la imagen de salida se escalonan en lugar de suavizarse. El paso se debe a que el intervalo de valores *que usa la imagen es demasiado estrecho*.\
Esto significa que no hay suficientes valores para realizar una transición fluida de un paso de un degradado al siguiente.

Los valores de luminancia/RGBA se pueden codificar usando valores enteros o de punto flotante, lo que afecta a su *precisión*:

* **Integer** ofrece precisión de 8 bits (de 0 a 255, de modo que 256 valores posibles) y precisión de 16 bits (de 0 a 65535 de modo que 65536 valores posibles) para almacenar un valor en el intervalo 0-1.
* El **punto flotante** ofrece una precisión de 16 bits (HDR. 16F) y 32 bits (HDR. 32F), con la capacidad de almacenar valores fuera del intervalo 0-1, incluidos los valores negativos. Esto le permite trabajar con imágenes de alto rango dinámico (HDR.), donde el valor de luminancia puede superar con creces la 1.0.

Si no necesita trabajar específicamente con imágenes HDR., es probable que la mayoría de los nodos generen un valor en el rango 0-1 codificado mediante enteros. Si el formato de salida de la imagen es de 8 bits, la imagen solo puede utilizar 256 valores, lo que a menudo dará como resultado un paso visible en los degradados. Esto puede afectar especialmente al resultado de los nodos Normal.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/incorrect-image-output-01.png){width="256px"}![](incorrect-image-output.resources/incorrect-image-output-02.png){width="256px"}![](incorrect-image-output.resources/incorrect-image-output-03.png){width="256px"}

</td>
</tr>
</table>

**![(marca)](incorrect-image-output.resources/check.svg) Pasos recomendados**

Compruebe el **Formato de salida** (es decir, profundidad de bits) del nodo y de todos los nodos anteriores y asegúrese de que estos nodos utilizan *precisión Integer de al menos 16 bits*.

El parámetro Formato de salida suele establecerse en *Relativo a la entrada* [método de herencia](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), que puede propagar la baja precisión a lo largo del gráfico. Lo ideal es que al subir en el gráfico se encuentre la causa raíz del problema.

Puede identificar rápidamente la precisión del resultado de un nodo observando la información de texto que se muestra debajo del nodo:

* **L/C** se refiere a la imagen en escala de grises (es decir, luminancia) o color
* **8/16** significa codificación de enteros
* **16F/32F** significa codificación de punto flotante

Por ejemplo:

* L8: entero de escala de grises de 8 bits
* C16: color entero de 16 bits
* C32F: coma flotante de color de 32 bits (HDR)

## Pérdida de calidad en SBSAR publicado

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

<b>![(error)](incorrect-image-output.resources/error.svg) Problema</b>

La calidad de las imágenes generadas por un archivo de Substance 3D (SBSAR) es notablemente inferior a la del gráfico del archivo de Substance 3D desde el que se publica, como se muestra en la imagen de la derecha.\
El resultado aparece con baja resolución.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/incorrect-image-output-04.jpg){width="256px"}

</td>
</tr>
</table>

<b>![(marca)](incorrect-image-output.resources/check.svg) Pasos recomendados</b>

Asegúrese de que la propiedad [Output size](../../compositing-graphs/output-size/output-size.md) de todos los nodos [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) esté establecida en el *método de herencia [Absolute*](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).

Si no es así, su [recurso de mapa de bits](../../resources/bitmap-resource/bitmap-resource.md) al que se hace referencia se guardará con la resolución predeterminada de 256\*256 en el archivo de Substance 3D publicado, lo que* afectará a la calidad* de una o más salidas.

## La imagen es borrosa

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(error)](incorrect-image-output.resources/error.svg) Problema**

Las formas aparecen ligeramente desenfocadas después de usar algunos nodos, como [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) o [Blend](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md).

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/incorrect-image-output-05.jpg){width="256px"}

</td>
</tr>
</table>

**![(marca)](incorrect-image-output.resources/check.svg) Pasos recomendados**

Al reorganizar los píxeles de una imagen, por ejemplo, al cambiar el tamaño de una forma o la resolución de una imagen, hay dos formas de determinar cómo se deben *asignar* píxeles del origen al destino:

* **Más cercano**: El píxel se asignará al destino *tal cual* en la coordenada coincidente. Si el objetivo es de baja resolución, el píxel puede ignorarse por completo. Si el objetivo es de mayor resolución; se asignará a todos los píxeles que cubran su alcance. El resultado es *más nítido* y tendrá un aspecto ligeramente *suavizado*.
* **Filtrado bilineal**: Se aplica un proceso de filtrado a la imagen de origen para que sus píxeles se asignen a la resolución de destino de forma que *suavice* las transiciones entre píxeles. El resultado es *más suave* y se verá ligeramente *borroso*.

El nodo [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) proporciona la opción **Filtering method** para seleccionar cuál de estos dos métodos de asignación se debe usar.

La mayoría de los nodos - p.ej. [Fusionar](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md): valor predeterminado de *filtrado bilineal* al realizar el muestreo de una textura de entrada de diferente resolución, lo que puede provocar un desenfoque no deseado.\
Dado que el nodo Transformation 2D es *atómico*, por lo tanto muy ligero, se puede usar *incluso si no se necesitan transformaciones* para cambiar una resolución de textura mediante su propiedad [Output size](../../compositing-graphs/output-size/output-size.md) antes de enviar la textura a otro nodo, para que puedas *controlar el impacto* de este cambio de tamaño.

En el [gráfico de funciones](../../function-graphs/function-graphs.md) del nodo [Pixel processor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), los nodos **Sample** incluyen la *misma opción* para controlar cómo se debe asignar la textura muestreada a la resolución del nodo.
