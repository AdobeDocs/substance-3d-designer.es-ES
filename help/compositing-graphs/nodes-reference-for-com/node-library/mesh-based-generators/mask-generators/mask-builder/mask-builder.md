---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/mask-builder.html"
breadcrumb-title: ''
description: Utilice el nodo Generador de máscaras para combinar varias entradas de máscara y crear patrones de máscara complejos para efectos de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Mask Builder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Creador de máscaras
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 10%

---


# Creador de máscaras

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/mask-builder.png){width="128px"}

<b>En:</b> Generadores basados en malla > Generadores de máscaras

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Esta es prácticamente la versión de Designer del Creador de máscaras de Painter.

Se trata de una herramienta complicada pensada como un creador de máscaras todo-abarcador, basado en mapas con bake, parámetros de usuario y patrones y mapas de suciedad. Está pensado principalmente como un nodo muy avanzado y de control total para mezclar el dirt de pliegue y el desgaste de los bordes. Este nodo es lo suficientemente potente como para imitar cualquier otro Generador de máscaras.

No se requieren hagas un bake explícitamente, pero cuanto más suministre, más podrá hacer este nodo.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Oclusión de ambiente</b> <i>Entrada en escala de grises</i> |  |
| <b>Curvatura</b> <i>Entrada en escala de grises</i> |  |
| <b>Normal del Espacio Mundial</b> <i>Entrada de color</i> |  |
| <b>Entrada de Suciedad</b> <i>Entrada en escala de grises</i> |  |
| <b>Entrada de Suciedad 2</b> <i>Entrada en escala de grises</i> |  |
| <b>Entrada de Dispersión</b> <i>Entrada en escala de grises</i> | Sello de dispersión personalizado, necesario para utilizar los parámetros de Dispersión. |
| <b>Máscara (opcional)</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para enmascarar los efectos del nodo. |
| <b>Posición</b> <i>Entrada de color</i> | Se utiliza para los efectos Triplanar y Superior-Inferior. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Nivel</b> <i>0.0 - 1.0</i> | Define el nivel total del efecto y lo revela gradualmente. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del resultado. |
| <b>Invertir</b> <i>Falso/Verdadero</i> | Invierte el resultado. Útil para lograr lo contrario de la máscara que está construyendo. |
| <b>Usar triplanar</b> <i>Falso/Verdadero</i> | Permite la proyección triplanar, evitando cualquier costura con mapas de suciedad. |
| <b>Contraste de fusión triplanar</b> <i>0.0 - 1.0</i> | Define el contraste para la fusión triplanar. |
| <b>Suciedad</b> <i>0.0 - 1.0</i> | Define la cantidad de Suciedad que se debe fusionar globalmente. |
| <b>Suciedad</b> |  |
| <b>Escala</b> <i>0 - 10</i> | Define la escala de la Suciedad global. |
| <b>Usar Suciedad personalizada</b> <i>Falso/Verdadero</i> | Habilita la entrada de Suciedad personalizada. |
| <b>Suciedad secundaria personalizada</b> <i>0.0 - 1.0</i> | Habilita una segunda entrada de Suciedad personalizada. |
| <b>Invertir</b> <i>Falso/Verdadero</i> | Invierte el mapa de Suciedades. |
| <b>AO</b> <i>-1.0 - 1.0</i> | Define el grado en el que el efecto debe aparecer en áreas de AO ocluidas. Se puede ajustar con el grupo siguiente. |
| <b>AO</b> |  |
| <b>Intervalo</b> <i>0.0 - 1.0</i> | Establece el umbral o el intervalo para el aspecto del dirt. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del efecto AO. |
| <b>Ruido</b> <i>0.0 - 1.0</i> | Define la cantidad de ruido/suciedad que se debe fusionar en el efecto AO. |
| <b>Escala de ruido</b> <i>0 - 10</i> | Define la escala del ruido/suciedad de AO. |
| <b>Tipo de ruido</b> <i>Manchas, Nube, Humedad, Ruido Blanco</i> | Cambia entre 4 tipos diferentes de ruido de AO. |
| <b>Invertir</b> <i>Falso/Verdadero</i> | Invierte la interpretación del mapa AO: El ruido aparecerá en las áreas de AO brillantes, no en las oscuras. |
| <b>Curvatura</b> <i>0.0 - 1.0</i> | Define el efecto que debe aparecer en los bordes de curvatura; puede ser tanto convexo como cóncavo. Ajusta esto con el grupo de abajo. |
| <b>Curvatura</b> |  |
| <b>Rango convexo</b> <i>-1.0 - 1.0</i> | Define el efecto que debe aparecer en los bordes de curvatura convexos (brillantes). |
| <b>Contraste convexo</b> <i>0.0 - 1.0</i> | Define el contraste del efecto Convexo. |
| <b>Inversión convexa</b> <i>Falso/Verdadero</i> | Invierte la interpretación de los bordes convexos. |
| <b>Rango cóncavo</b> <i>-1.0 - 1.0</i> | Define el efecto que debe aparecer en los bordes de curvatura cóncavos (oscuros). |
| <b>Contraste cóncavo</b> <i>0.0 - 1.0</i> | Define el contraste del rango cóncavo. |
| <b>Invertir cóncavo</b> <i>Falso/Verdadero</i> | Invierte la interpretación de los bordes cóncavos. |
| <b>Smoothness</b> <i>0.0 - 16.0</i> | Cantidad de desenfoque y suavizado que se aplica a los bordes de Curvatura. |
| <b>Aumento de nivel</b> <i>0.0 - 1.0</i> | Refuerzo adicional si el efecto no es lo suficientemente visible. |
| <b>Ruido</b> <i>0.0 - 1.0</i> | Define la influencia del ruido/suciedad en el efecto Curvatura. |
| <b>Escala de ruido</b> <i>0 - 10</i> | Define la escala del ruido. |
| <b>Tipo de ruido</b> <i>Manchas, Nube, Humedad, Ruido Blanco</i> | Elija entre 4 tipos de ruido diferentes. |
| <b>Degradado superior/inferior</b> <i>-1.0 - 1.0</i> | Fusiones sobre o máscaras con un degradado de arriba abajo basado en el mapa de posición. Los valores positivos hacen que las cosas sean más brillantes, mientras que los valores negativos enmascaran los efectos existentes. |
| <b>Degradado</b> |  |
| <b>Intervalo</b> <i>0.0 - 1.0</i> | Establece la posición del degradado. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta el contraste del degradado. |
| <b>Invertir</b> <i>Falso/Verdadero</i> | Invierte el degradado. Intercambia de forma efectiva la parte inferior y superior. |
| <b>Normal del Espacio Mundial</b> <i>0.0 - 1.0</i> | Similar a Degradado arriba/abajo, pero con el mapa de posición y en seis direcciones, parecido a una iluminación falsa. Los valores positivos se aclaran, los negativos se oscurecen. |
| <b>Normal del Espacio Mundial</b> |  |
| <b>Intensidad superior</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidad inferior</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidad frontal</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidad De Respaldo</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidad derecha</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensidad izquierda</b> <i>-1.0 - 1.0</i> |  |
| <b>Scratches</b> <i>-1.0 - 1.0</i> | Fusión arañazos en las áreas blancas. |
| <b>Scratches</b> |  |
| <b>Importe</b> <i>0 - 4096</i> | Define la cantidad total de arañazos. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Define la escala de arañazos individuales. |
| <b>Dispersión</b> <i>-1.0 - 1.0</i> | Dispersión un sello personalizado dentro de áreas blancas. |
| <b>Dispersión</b> |  |
| <b>Escala</b> <i>0 - 50</i> | Escala total del efecto. |
| <b>Densidad</b> <i>0.0 - 1.0</i> | Control de densidad de dispersión, número que debe aparecer. |
| <b>Tamaño</b> <i>0.0 - 4.0</i> | Tamaño del sello disperso. |
| <b>Variación de tamaño</b> <i>0.0 - 1.0</i> | Variación dentro del tamaño de sello. |
| <b>Variación de opacidad</b> <i>0.0 - 1.0</i> | Variación dentro de la opacidad del sello. |
