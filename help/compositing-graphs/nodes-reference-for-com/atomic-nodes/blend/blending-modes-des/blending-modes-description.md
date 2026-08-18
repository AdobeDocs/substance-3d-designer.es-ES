---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend/blending-modes-description.html"
breadcrumb-title: ''
description: Obtenga más información sobre los modos de fusión disponibles en Substance 3D Designer para combinar texturas con diferentes efectos de composición.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend > Blending modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modos de fusión
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 2%

---


# Modos de fusión

El nodo [Blend](../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) ofrece los siguientes modos de fusión:

## Copiar

El modo de fusión *Copiar* solo colocará el primer plano sobre el fondo.

![Modo de fusión: Copiar](../../../../../assets/image2015-8-20-9-38-0.png "modo de fusión: Copiar"){zoomable="yes"}

Para las imágenes en color, el canal alfa se tiene en cuenta de forma predeterminada en la opacidad.

Esto se puede cambiar mediante el parámetro &quot;Fusión de Alpha&quot;.

![Modo de fusión: Copiar (2)](../../../../../assets/image2015-8-20-14-15-29.png "Modo de fusión: Copiar (2)"){zoomable="yes"}

## Añadir (Sobreexposición lineal)

El modo de fusión *Agregar* agregará el valor de entrada de primer plano a cada píxel correspondiente del fondo.

![Modo de fusión: Agregar (Sobreexposición lineal)](../../../../../assets/image2015-8-20-9-38-19.png "Modo de fusión: Agregar (Sobreexposición lineal)"){zoomable="yes"}

## Restar

El modo de fusión *Substract* restará el valor de entrada de primer plano de cada píxel correspondiente del fondo.

Si el resultado de la sustracción es menor que 0, el valor se limita a 0, lo que produce un negro puro.

![Modo de fusión: Substract](../../../../../assets/image2015-8-20-9-38-35.png "Modo de fusión: Substract"){zoomable="yes"}

## Multiplicar

El modo de fusión *Multiply* multiplicará el valor de entrada de fondo por cada píxel correspondiente en primer plano.

Como el valor de cada píxel está comprendido entre 0 y 1, el resultado siempre es igual o inferior (más oscuro) en comparación con el original.

![Modo de fusión: Multiply](../../../../../assets/image2015-8-20-9-38-53.png "Modo de fusión: Multiplicar"){zoomable="yes"}

## Añadir/Restar

El modo de fusión *Agregar Sub* funciona de la siguiente manera:

* Los píxeles de primer plano con un valor superior a 0,5 se añaden a sus respectivos píxeles de fondo.
* Los píxeles de primer plano con un valor inferior a 0,5 se restan de sus respectivos píxeles de fondo.

![Modo de fusión: Agregar sub](../../../../../assets/image2015-8-20-9-39-11.png "modo de fusión: Agregar sub"){zoomable="yes"}

## Máx. (Aclarar)

El modo de fusión *Max* elegirá el valor más alto entre el fondo y el primer plano.

![Modo de fusión: Máx. (aclarar)](../../../../../assets/image2015-8-20-9-40-12.png "Modo de fusión: Máx. (aclarar)"){zoomable="yes"}

## Mín. (Oscurecer)

El modo de fusión *Min* elegirá el valor más bajo entre el fondo y el primer plano.

![Modo de fusión: Mín. (Oscurecer)](../../../../../assets/image2015-8-20-9-40-31.png "Modo de fusión: Mín. (Oscurecer)"){zoomable="yes"}

## Cambiar

El modo de fusión *Cambiar* es similar al modo Copiar, con una diferencia *crucial*:

* Opacidad establecida en 0: No se calculará la secuencia de nodos conectada a la entrada &quot;frontal&quot; **.
* Opacidad establecida en 1: No se calculará la secuencia de nodos conectada a la entrada en segundo plano **.

Por lo tanto, este modo se puede utilizar para mejorar el rendimiento del gráfico.

Los nodos [Switch](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) y [Switch grayscale](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) están configurados para usar los nodos de mezcla en estas configuraciones específicas.

![Modo de fusión: Cambiar](../../../../../assets/image2015-8-20-9-38-0.png "modo de fusión: Conmutador"){zoomable="yes"}

## Dividir

El modo de fusión *Dividir* dividirá el valor de los píxeles de entrada de fondo por cada píxel correspondiente del primer plano.

![Modo de fusión: Dividir](../../../../../assets/image2015-8-20-9-41-32.png "modo de fusión: Dividir"){zoomable="yes"}

## Superponer

El modo de fusión *Superposición* combina los modos de fusión Multiplicar y Trama:

* &#x200B;
  * Si el valor del píxel de la capa inferior es inferior a 0,5, se aplica una fusión de tipo *Multiply*
  * Si el valor del píxel de la capa inferior es superior a 0,5, se aplica una fusión de tipo *Screen*

![Modo de fusión: Superponer](../../../../../assets/image2015-8-20-9-41-50.png "modo de fusión: Superponer"){zoomable="yes"}

## Pantalla

Con el modo de fusión de pantalla, los valores de los píxeles de las dos entradas se invierten, se multiplican y, a continuación, se vuelven a invertir.

El resultado es el efecto contrario al multiplicar y siempre es igual o superior (más brillante) en comparación con el original.

![Modo de fusión: Pantalla](../../../../../assets/image2015-8-20-9-42-11.png "Modo de fusión: Pantalla"){zoomable="yes"}

## Luz suave

El modo de fusión Luz suave crea un resultado sutil más claro u oscuro en función del brillo del color frontal.

Los colores de fusión con un brillo superior al 50 % aclararán los píxeles de fondo y los colores con un brillo inferior al 50 % oscurecerán los píxeles de fondo.

![Modo de fusión: Luz suave](../../../../../assets/image2015-8-20-9-42-32.png "Modo de fusión: Luz suave"){zoomable="yes"}
