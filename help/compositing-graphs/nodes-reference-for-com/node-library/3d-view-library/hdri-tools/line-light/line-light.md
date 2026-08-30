---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz de línea para crear fuentes de luz lineal en entornos HDRI para simular iluminación fluorescente y de banda.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz de línea
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 3%

---


# Luz de línea

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](line-light.resources/panorama-line-light.png){width="200px"}

<b>En:</b> Vista 3D > Herramientas HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una forma de línea proyectada esféricamente basada en las coordenadas de dos puntos en el espacio. En comparación con [Luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md), tiene más opciones para orientar formas y aplicar patrones repetidos a la forma de luz.

Los modos de posicionamiento para este nodo son ligeramente más complejos que otros nodos de luz HDRI. Se recomienda probar algunos modos de tamaño diferentes para encontrar cuál funciona para su escenario.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de imagen de fondo</b> <i>Entrada de color</i> | Fondo opcional sobre el que componer la luz generada. |
| <b>Entrada de imagen de forma</b> <i>Entrada de color</i> | Imagen opcional para asignar a la luz de línea. Solo se usa cuando el modo Color de forma está establecido en Entrada de imagen. |
| <b>Entrada de imagen de motivo</b> <i>Entrada en escala de grises</i> | Imagen de motivo personalizado, utilizada cuando el parámetro &quot;Motivo&quot; se define en &quot;Entrada de imagen&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de posición</b> <i>Suelo/Techo, Distancia desde origen, Posiciones Mundiales</i> | Seleccione entre tres modos de colocación diferentes. Tierra/techo y Distancia desde origen soportan la manipulación en la Vista 2D, las posiciones del mundo solo se pueden cambiar a través de propiedades, pero sí soporta una colocación más exacta. |
| <b>Mostrar cuadrícula de tierra</b> <i>Falso/Verdadero</i> | Función auxiliar para permitir que se dibuje una cuadrícula de tierra de depuración. Ayuda a estimar la posición de las líneas en el espacio. |
| <b>Coordenadas de posición</b> |  |
| <b>Vector Arriba</b> <i>Z Arriba, Y Arriba</i> | Solo con el modo Posición mundial, determine la orientación del sistema de coordenadas. |
| <b>Punto 1: Posición UV</b> | Solo con suelo / techo y Distancia desde origen. Establece la posición del primer punto en el espacio UV. |
| <b>Posición UV del punto 2</b> | Solo con suelo / techo y Distancia desde origen. Establece la posición del segundo punto en el espacio UV. |
| <b>Posición Mundial Punto 1</b> <i>-2.0 - 2.0</i> | Solo con el modo Posiciones Mundiales. Establece el primer punto en el espacio de entorno. No se admite la interacción de vista 2D. |
| <b>Posición Mundial Punto 2</b> <i>-2.0 - 2.0</i> | Solo con el modo Posiciones Mundiales. Establece el segundo punto en el espacio de entorno. No se admite la interacción de vista 2D. |
| <b>Height absoluto de línea</b> <i>0.0 - 1.0</i> | Solo con el modo de posición de suelo / techo, establece el height absoluto desde el techo. Utilice Mostrar cuadrícula de suelo para estimar mejor la posición. |
| <b>Distancia desde origen</b> <i>0.0 - 1.0</i> | Solo con el modo de posición de Distancia desde origen. Establece la distancia desde el centro del panorama para ambos puntos. |
| <b>Modo de color de forma</b> <i>RGB, Temperatura (Kelvin), Entrada De Imagen</i> | Elija el método que desee utilizar para definir el color de la forma. La entrada de imagen permite utilizar la segunda ranura de entrada. |
| <b>Color</b> <i>(Valor de color)</i> | Solo con el modo Color de forma establecido en RGB. Selecciona el color de la forma. |
| <b>Temperatura</b> <i>800.0 - 20000.0</i> | Solo con el modo Color de forma establecido en Temperatura. Establece el valor Kelvin para el color de la forma. |
| <b>Modo UV de imagen de forma</b> <i>Estirar, Estirar solo centro, Repetir + espaciado</i> | Solo con el modo Color de forma establecido en Entrada de imagen. Define cómo se aplica la imagen a la forma de línea y determina el comportamiento de la repetición UV. |
| <b>Espaciado de repetición de la imagen de forma</b> <i>0.0 - 1.0</i> | Solo con el modo Color de forma definido en Entrada de imagen y con el modo UV definido en Repetir + Espaciado. Define el espaciado cuando la imagen se repite a lo largo de la línea. |
| <b>Gamma de imagen de forma</b> <i>sRGB, lineal</i> | Solo con el modo Color de forma establecido en Entrada de imagen. Determine cómo interpretar la entrada de imágenes de formas. |
| <b>Exposición (VE)</b> <i>0.0 - 10.0</i> | Defina el valor de exposición para la forma generada, que se corresponde perfectamente con el valor de exposición de la imagen de fondo. |
| <b>Rotación de línea</b> <i>0.0 - 1.0</i> | Gira la línea a lo largo del eje de su longitud. La línea se trata como una tarjeta plana cuando se gira. |
| <b>Thickness de línea</b> <i>0.0 - 1.0</i> | Establece el thickness de la tarjeta de línea. |
| <b>Patrón</b> <i>Cuadrado suave, Cuadrado afilado, Cono, Hemisferio, Entrada de imagen</i> | Seleccione la forma de motivo que desea utilizar. |
| <b>Dureza del motivo</b> <i>0.0 - 1.0</i> | Definir la dureza/contraste del patrón. |
| <b>Modo UV De Patrón</b> <i>Estirar, Estirar solo centro, Repetir + espaciado</i> | Define cómo usar la máscara de motivo secundaria, aplicada sobre la imagen de forma. |
| <b>Espaciado de repetición de motivo</b> <i>0.0 - 1.0</i> | Solo si el modo UV de motivo está definido en Repetir + Espaciado. Defina el espaciado entre patrones repetidos. |
| <b>Habilitar recorte de tierra</b> <i>Falso/Verdadero</i> | Activar recorte de dibujo de líneas. El efecto no es visible al utilizar el modo de colocación Tierra/Techo. |
| <b>Height terrestre</b> <i>-2.0 - 0.0</i> | Define el height relativo del plano de redondeo, que se utiliza para el recorte. Afecta a la cuadrícula de suelo dibujada. |
| <b>Habilitar entrada de fondo</b> <i>Falso/Verdadero</i> | Cambia el uso de la imagen de fondo opcional. Las composiciones generan luz sobre el fondo. |
| <b>Color de fondo</b> <i>(Valor de color)</i> | Si no se utiliza Entrada de fondo, defina aquí un valor de fondo de color sólido. |
| <b>Gama de fondo</b> <i>sRGB, lineal</i> | Si se utiliza Entrada en segundo plano, defina cómo interpretar la entrada en segundo plano. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="line-light.resources/line-light-ex.gif" />
        </td>
    </tr>
</table>
