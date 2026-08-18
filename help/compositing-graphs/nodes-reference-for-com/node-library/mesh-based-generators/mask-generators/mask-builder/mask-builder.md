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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---


# Creador de máscaras

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mask-builder.png){width="128px"}

## Creador de máscaras

**En:** *Generadores Basados En Malla**/Generadores De Máscara*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Genera una máscara en blanco y negro basada en mapas con bake y ajustes de usuario. Esta es prácticamente la versión de Designer del Creador de máscaras de Painter.

Se trata de una herramienta complicada pensada como un creador de máscaras todo-abarcador, basado en mapas con bake, parámetros de usuario y patrones y mapas de suciedad. Está pensado principalmente como un nodo muy avanzado y de control total para mezclar el dirt de pliegue y el desgaste de los bordes. Este nodo es lo suficientemente potente como para imitar a cualquier otro generador de máscaras.

No se requieren pasteles explícitamente, pero cuanto más suministre, más podrá hacer este nodo.

## Parámetros

### Entradas

* **Oclusión de ambiente**: *Entrada en escala de grises*
* **Curvatura**: *Entrada en escala de grises*
* **Normal del Espacio Mundial**: *Entrada de color*
* **Entrada de Suciedad**: *Entrada en escala de grises*
* **Entrada de Suciedad 2**: *Entrada en escala de grises*
* **Entrada de Dispersión**: *Entrada en escala de grises*\
  Sello de dispersión personalizado, necesario para utilizar los parámetros de Dispersión.
* **Máscara (opcional)**: *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo.
* **Posición**: *Entrada de color*\
  Se utiliza para los efectos Triplanar y Superior-Inferior.

### Parámetros

* **Nivel**: *0.0 - 1.0*\
  Define el nivel total del efecto y lo revela gradualmente.
* **Contraste**: *0.0 - 1.0*\
  Ajusta el contraste del resultado.
* **Invertir**: *Falso/Verdadero*\
  Invierte el resultado. Útil para lograr lo contrario de la máscara que está construyendo.
* **Usar triplanar**: *Falso/Verdadero* Permite la proyección triplanar, evitando cualquier costura con mapas de suciedades.
* **Contraste de fusión triplanar**: *0.0 - 1.0* Establece el contraste para la fusión triplanar.
* **Suciedad**: *0.0 - 1.0* Establece la cantidad de Suciedad que se debe fusionar a nivel global.
* **Suciedad**
  * **Escala**: *0 - 10* Establece la escala de la Suciedad global.
  * **Usar Suciedad personalizada**: *Falso/Verdadero* Habilita la entrada de Suciedad personalizada.
  * **Suciedad personalizada secundaria**: *0.0 - 1.0* Habilita una segunda entrada de Suciedad personalizada.
  * **Invertir**: *Falso/Verdadero*\
    Invierte el mapa de Suciedades.
* **AO**: *-1.0 - 1.0* Establece la medida en que el efecto debe aparecer en áreas de AO ocluidas. Se puede ajustar con el grupo siguiente.
* **AO**
  * **Intervalo**: *0.0 - 1.0* Establece el umbral o intervalo para la apariencia del dirt.
  * **Contraste**: *0.0 - 1.0*\
    Ajusta el contraste del efecto AO.
  * **Ruido**: *0.0 - 1.0* Define la cantidad de ruido/suciedad que se mezclará en el efecto AO.
  * **Escala de ruido**: *0 - 10* Establece la escala del ruido/suciedad del AO.
  * **Tipo de ruido**: *Manchas, Nube, Humedad, Ruido Blanco* Cambia entre 4 tipos diferentes de ruido AO.
  * **Invertir**: *Falso/Verdadero*\
    Invierte la interpretación del mapa AO: El ruido aparecerá en las áreas de AO brillantes, no en las oscuras.
* **Curvatura**: *0.0 - 1.0* Establece el efecto que debe aparecer en los bordes de curvatura; puede ser tanto convexo como cóncavo. Ajusta esto con el grupo de abajo.
* **Curvatura**
  * **Rango convexo**: *-1.0 - 1.0* Establece el efecto que debe aparecer en los bordes de curvatura convexos (brillantes).
  * **Contraste convexo**: *0.0 - 1.0* Establece el contraste del efecto Convexo.
  * **Inversión convexa**: *False/True* Invierte la interpretación de los bordes convexos.
  * **Rango cóncavo**: *-1.0 - 1.0* Establece el efecto que debe aparecer en los bordes de curvatura cóncavos (oscuros).
  * **Contraste cóncavo**: *0.0 - 1.0* Establece el contraste del rango cóncavo.
  * **Invertir cóncavo**: *Falso/Verdadero* Invierte la interpretación de los bordes cóncavos.
  * **Smoothness**: *0.0 - 16.0* Cantidad de desenfoque y suavizado que se aplica a los bordes de Curvatura.
  * **Aumento de nivel**: *0.0 - 1.0* Refuerzo adicional si el efecto no es suficientemente visible.
  * **Ruido**: *0.0 - 1.0* Establece la influencia del ruido/suciedad en el efecto Curvatura.
  * **Escala de ruido**: *0 - 10* Establece la escala del ruido.
  * **Tipo de ruido**: *Manchas, Nube, Humedad, Ruido Blanco* Elige entre 4 tipos diferentes de Ruido.
* **Degradado superior/inferior**: *-1.0 - 1.0* Se fusiona o enmascara con un degradado de arriba a abajo basado en el mapa de posición. Los valores positivos hacen que las cosas sean más brillantes, mientras que los valores negativos enmascaran los efectos existentes.
* **Degradado**
  * **Intervalo**: *0.0 - 1.0* Establece la posición del degradado.
  * **Contraste**: *0.0 - 1.0*\
    Ajusta el contraste del degradado.
  * **Invertir**: *Falso/Verdadero*\
    Invierte el degradado. Intercambia de forma efectiva la parte inferior y superior.
* **Normal del Espacio Mundial**: *0.0 - 1.0* Similar a Degradado arriba/abajo, pero con el mapa de posición y en seis direcciones, parecido a una iluminación falsa. Los valores positivos se aclaran, los negativos se oscurecen.
* **Normal del Espacio Mundial**
  * **Intensidad superior**: *-1.0 - 1.0*
  * **Intensidad inferior**: *-1.0 - 1.0*
  * **Intensidad frontal**: *-1.0 - 1.0*
  * **Intensidad De Respaldo**: *-1.0 - 1.0*
  * **Intensidad Derecha**: *-1.0 - 1.0*
  * **Intensidad izquierda**: *-1.0 - 1.0*
* **Scratches**: *-1.0 - 1.0* Fusiona arañazos en las áreas blancas.
* **Scratches**
  * **Importe**: *0 - 4096* Define la cantidad total de arañazos.
  * **Escala**: *0.0 - 1.0* Establece la escala de arañazos individuales.
* **Dispersión**: *-1.0 - 1.0* Dispersión un sello personalizado dentro de áreas blancas.
* **Dispersión**
  * **Escala**: *0 - 50* Escala total del efecto.
  * **Densidad**: *0.0 - 1.0* Control de densidad de dispersión, número que debe aparecer.
  * **Tamaño**: *0.0 - 4.0* Tamaño del sello disperso.
  * **Variación de tamaño**: *0.0 - 1.0* Variación dentro del tamaño de sello.
  * **Variación de opacidad**: *0.0 - 1.0* Variación dentro de la opacidad del sello.

## Imágenes de ejemplo

|  |
| --- |
| No hay imágenes adjuntas a esta página. |

</td>
</tr>
</table>
