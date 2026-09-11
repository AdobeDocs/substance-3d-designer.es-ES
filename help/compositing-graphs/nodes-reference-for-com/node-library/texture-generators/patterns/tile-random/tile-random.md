---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: Utilice el nodo Azulejo aleatorio para crear patrones de azulejo aleatorios con variación procedimienta para los efectos de textura orgánica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Azulejo aleatorio
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# Azulejo aleatorio

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random.resources/tile-random.png){width="128px"}

<b>En:</b> Generadores > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Tile Random genera un patrón de mosaico procedimiento que tiene un poco más de caos en las formas de mosaico que su contraparte, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Esto lo hace dividiendo aleatoriamente ciertos azulejos en azulejos más pequeños. Le sugerimos que primero encuentre su camino alrededor de Tile Generator antes de abordar Tile Random, ya que muchos conceptos son similares.

Se utiliza Tile Random en lugar de [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) cuando el objetivo es un patrón más antiguo y menos organizado. Sin embargo, tiene sus limitaciones, así que considera [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) para cualquier otra necesidad avanzada.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de patrón</b> <i>Entrada de escala de grises (entrada de color)</i> | Imagen de motivo personalizado, utilizada cuando el parámetro &quot;Motivo&quot; se define en &quot;Entrada de imagen&quot;. |
| <b>Entrada en segundo plano</b> <i>Entrada de escala de grises (entrada de color)</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Cantidad X</b> <i>1 - 64</i> | Cantidad de repeticiones X del patrón. |
| <b>Importe Y</b> <i>1 - 64</i> | Cantidad de repeticiones Y del patrón. |
| <b>Expansión no cuadrada</b> <i>Falso/Verdadero</i> | Permite la compensación de calabaza y estira con proporciones no cuadradas. |
| <b>Patrón</b> |  |
| <b>Patrón</b> <i>Entrada De Patrón, Cuadrado, Disco, Paraboloide, Campana, Gaussiano, Espina, Pirámide, Ladrillo, Gradación, Ondas, Media campana, Campana Cuadrada, Media Luna, Cápsula, Cono</i> | Selecciona la forma de motivo que se va a utilizar. |
| <b>Filtrado de entrada de imagen (Motor > v4)</b> <i>Bilineal + Mipmaps, Bilineal, Más Cercano</i> |  |
| <b>Específico del patrón</b> <i>0.0 - 1.0</i> | Permite cambiar la forma del motivo seleccionado. El efecto depende del patrón seleccionado. |
| <b>Aleatorio específico de motivo</b> <i>0.0 - 1.0</i> | El efecto Aleatorización depende del patrón seleccionado. |
| <b>Rotación</b> <i>0, 90, 180, 270, horizontal al azar, vertical al azar</i> | Define la rotación en pasos de 90 grados, con aleatorización opcional. |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Añade rotación libre aleatoria. |
| <b>Aleatorio de Simetría</b> <i>0.0 - 1.0</i> | Refleja aleatoriamente determinados patrones en el modo aleatorio de Simetría seleccionado. Cuanto más alto sea este valor, más patrones se reflejarán. |
| <b>Modo aleatorio de Simetría</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Determina el comportamiento del reflejo cuando el valor aleatorio de Simetría es superior a 0. |
| <b>División</b> |  |
| <b>Modo</b> <i>ninguno, automático, horizontal automático, vertical automático, aleatorio h+v</i> | Establece la regla sobre cómo dividir los mosaicos. |
| <b>Umbral</b> <i>0.0 - 1.0</i> | Umbral de tamaño para dividir un azulejo. |
| <b>Multiplicador</b> <i>0 - 10</i> | Multiplicador de división. Cuanto mayor sea este valor, más se dividirá. |
| <b>Tamaño</b> |  |
| <b>X aleatorio</b> <i>0.0 - 1.0</i> | Aleatoriza la escala no uniforme sobre el eje X. |
| <b>Y aleatorio</b> <i>0.0 - 1.0</i> | Aleatoriza la escala no uniforme sobre el eje Y. |
| <b>Intersticio</b> |  |
| <b>Modo</b> <i>Relativo al ladrillo más pequeño, Relativo al ladrillo más grande</i> | Establece a qué intersticio de tamaño de ladrillo es relativo. |
| <b>Importe</b> <i>0.0 - 1.0</i> | Define el tamaño del hueco entre los ladrillos. |
| <b>Forma</b> |  |
| <b>Escala</b> <i>0.0 - 1.0</i> | Escala globalmente cada mosaico. |
| <b>Escala aleatoria</b> <i>0.0 - 1.0</i> | Escala aleatoria por mosaico. |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Rotación global para cada mosaico. |
| <b>Aleatorio de rotación</b> <i>0.0 - 1.0</i> | Rota aleatoriamente por mosaico. |
| <b>Restricción de rotación</b> <i>Falso/Verdadero</i> | Restringe la escala para que los mosaicos rotados nunca se superpongan. |
| <b>Posición</b> |  |
| <b>Desplazamiento</b> <i>0.0 - 1.0</i> | Mueve o traduce los mosaicos globalmente y sólo se desliza sobre el eje X |
| <b>Desplazamiento aleatorio</b> <i>0.0 - 1.0</i> | Aleatoriza el desplazamiento por azulejo, sólo se desliza sobre el eje X |
| <b>Aleatorio</b> <i>0.0 - 1.0</i> | Aleatoriza la posición, los mosaicos se mueven en los ejes X e Y. |
| <b>Restricciones aleatorias</b> <i>Falso/Verdadero</i> | Las restricciones cambian de escala para que los mosaicos se toquen, pero no se superpongan. Reduce significativamente el efecto Posición aleatoria. |
| <b>Color</b> |  |
| <b>Color</b> <i>(valor de escala de grises) / (valor de color)</i> | Define el color sólido de todos los azulejos. |
| <b>Aleatorio de color</b> <i>0.0 - 1.0</i> | Aleatoriza el color según el azulejo. |
| <b>Parametrización de color</b> <i>ninguno, área, tamaño x, tamaño y</i> | Hace que la variación de color dependa de uno de estos ajustes. |
| <b>Intensidad de parametrización de color</b> <i>0.0 - 1.0</i> | Multiplicador para el efecto de parametrización anterior. |
| <b>Efecto de parametrización de color (solo para Color)</b> <i>RGB+Alpha, solo RGB, solo Alpha</i> | Determina el efecto de parametrización de solo color. |
| <b>Color de fondo</b> <i>(valor de escala de grises) / (valor de color)</i> | Define el color de fondo sólido. |
| <b>Modo De Fusión</b> <i>Agregar/Inferior, Máx./Agregar/Inferior, Fusión de Alpha (Color)</i> | Establece el modo de fusión de los mosaicos en el fondo. |
| <b>Máscara</b> |  |
| <b>Aleatorio</b> <i>0.0 - 1.0</i> | Comienza a enmascarar los azulejos de forma aleatoria. Cuanto mayor sea el valor, más mosaicos desaparecerán. |
| <b>Invertir</b> <i>Falso/Verdadero</i> | Invierte el resultado de la máscara. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random.resources/tile-random-1.png" />
        </td>
    </tr>
</table>
