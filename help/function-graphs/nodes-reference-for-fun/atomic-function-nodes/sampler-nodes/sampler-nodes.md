---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/sampler-nodes.html"
breadcrumb-title: ''
description: Acceda a nodos de muestra en gráficos de funciones de Substance 3D Designer para muestrear texturas y extraer valores de color.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Samplers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Samplers
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Nodos de Sampler

![Nodos de Sampler](../../../../assets/image2016-1-12-14-45-43.png "Nodos de Sampler")

Estos nodos muestrean un valor en una imagen de entrada en las coordenadas 2D proporcionadas:

<b>Gris de muestra</b> muestra un valor de luminancia en la entrada <b>Posición</b> en una imagen de escala de grises y lo emite como un valor <b>Float</b>.

<b>Sample Color</b> muestrea un valor RGBA en la entrada <b>Posición </b> de una imagen de color y lo emite como un valor <b>Float4</b> donde los componentes R, G, B y A se asignan a los componentes X, Y, Z y W respectivamente.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Las coordenadas comienzan desde la esquina superior izquierda de una entrada y oscilan entre 0 y 1 horizontal y verticalmente.

Las posiciones fuera de este intervalo se controlan según el <b>modo de direccionamiento</b> seleccionado (véase a continuación).

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Coordenadas de píxeles](../../../../assets/samplercoords.png "Coordenadas de píxeles")

</td>
</tr>
</table>

>[!NOTE]
>
> La entrada <b>Position</b> debe ser un valor Float2 donde las coordenadas X e Y de la imagen se asignan a los componentes X e Y del valor respectivamente

## Parámetros

+++Imagen de entrada
Permite seleccionar la entrada de nodo que se utilizará para el muestreo.

La lista se adapta dinámicamente a las entradas conectadas actualmente. Esto significa que las entradas se añaden a medida que se conectan las entradas de nodo.

La numeración de las entradas comienza en 0, de modo que una imagen conectada a la primera entrada del nodo aparece como *Imagen de entrada 0*.

+++

+++Modo de filtrado
Permite definir cómo gestionar la interpolación cuando los píxeles de la imagen muestreada no se asignan exactamente a la imagen de salida, debido a las diferencias de resolución.

<b>Más cercano</b>\
El píxel se asignará al destino *tal cual* en la coordenada coincidente. Si el objetivo es de baja resolución, el píxel puede ignorarse por completo. Si el objetivo es de mayor resolución; se asignará a todos los píxeles que cubran su alcance. El resultado es *más nítido* y tendrá un aspecto ligeramente *suavizado*.

<b>Filtrado bilineal</b>\
Se aplica un proceso de filtrado a la imagen de origen para que sus píxeles se asignen a la resolución de destino de forma que *suavice* las transiciones entre píxeles. El resultado es *más suave* y se verá ligeramente *borroso*.

+++

+++Modo de direccionamiento
Controla cómo se manejan los valores de posición fuera del intervalo [0;1].

<b>Repetir</b>\
Realiza un bucle en el rango [0;1] a medida que aumenta el valor.\
Por ejemplo: 3,4 es 0,4, -1,7 es 0,3.

<b>Fijación a borde</b>\
Fija los valores fuera del rango [0;1] a su límite más próximo.\
Por ejemplo: .3.4 es 1, -1.7 es 0.

+++
