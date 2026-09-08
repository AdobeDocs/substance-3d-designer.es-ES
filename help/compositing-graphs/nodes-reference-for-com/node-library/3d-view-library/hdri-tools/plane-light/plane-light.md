---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Utilice el nodo Luz plana para añadir fuentes de luz plana a entornos HDRI para el control de iluminación direccional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz plana
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# Luz plana

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-plane-light.png){width="200px"}

<b>En:</b> Vista 3D > Herramientas HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Genera una forma de plano proyectada esféricamente. El plano se puede colocar y orientar en 3D mediante los parámetros de entrada.

Difiere de la sencilla [luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) en que tiene opciones de colocación más avanzadas fuera de una proyección de Distancia desde origen más simple, y se pueden aplicar más patrones y máscaras, similar a [luz de línea](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

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
| <b>Posición UV plana</b> | Solo con suelo / techo y Distancia desde origen. Establece la posición del plano en el espacio UV. |
| <b>Posición Mundial del Avión</b> <i>-2.0 - 2.0</i> | Solo con el modo Posiciones Mundiales. Establece la posición del plano en el espacio mundial. No se admite la interacción de vista 2D. |
| <b>Height absoluto de plano</b> <i>0.0 - 1.0</i> | Solo con el modo de posición de suelo / techo, establece el height absoluto desde el techo. Utilice Mostrar cuadrícula de suelo para estimar mejor la posición. |
| <b>Distancia desde origen</b> <i>0.0 - 1.0</i> | Solo con el modo de posición de Distancia desde origen. Establece la distancia desde el centro del panorama para ambos puntos. |
| <b>Modo de color de forma</b> <i>RGB, Temperatura (Kelvin), Entrada De Imagen</i> | Elija el método que desee utilizar para definir el color de la forma. La entrada de imagen permite utilizar la segunda ranura de entrada. |
| <b>Color</b> <i>(Valor de color)</i> | Solo con el modo Color de forma establecido en RGB. Selecciona el color de la forma. |
| <b>Temperatura</b> <i>800.0 - 20000.0</i> | Solo con el modo Color de forma establecido en Temperatura. Establece el valor Kelvin para el color de la forma. |
| <b>Modo UV de imagen de forma</b> <i>Estirar, Estirar solo centro, Repetir + espaciado</i> | Solo con el modo Color de forma establecido en Entrada de imagen. Define cómo se aplica la imagen a la forma de línea y determina el comportamiento de la repetición UV. |
| <b>Espaciado de repetición de la imagen de forma</b> <i>0.0 - 1.0</i> | Solo con el modo Color de forma definido en Entrada de imagen y con el modo UV definido en Repetir + Espaciado. Define el espaciado cuando la imagen se repite a lo largo de la línea. |
| <b>Gamma de imagen de forma</b> <i>sRGB, lineal</i> | Solo con el modo Color de forma establecido en Entrada de imagen. Determine cómo interpretar la entrada de imágenes de formas. |
| <b>Exposición (VE)</b> <i>0.0 - 10.0</i> | Defina el valor de exposición para la forma generada, que se corresponde perfectamente con el valor de exposición de la imagen de fondo. |
| <b>Escala de plano</b> <i>0.0 - 1.0</i> | Establecer una escala uniforme de la forma Plano. |
| <b>Tamaño de plano</b> <i>0.0 - 1.0</i> | Defina el tamaño no uniforme de la forma Plano. |
| <b>Rotación de plano</b> <i>0.0 - 1.0</i> | Girar plano a lo largo de su eje central. |
| <b>Patrón</b> <i>Cuadrado suave, Cuadrado afilado, Cono, Hemisferio, Entrada de imagen</i> | Seleccione la forma de motivo que desea utilizar. |
| <b>Dureza del motivo</b> <i>0.0 - 1.0</i> | Definir dureza/contraste para el patrón. |
| <b>Modo UV De Patrón</b> <i>Estirar, Estirar sólo el medio</i> | Define cómo usar la máscara de motivo secundaria, aplicada sobre la imagen de forma. |
| <b>Habilitar recorte de tierra</b> <i>Falso/Verdadero</i> | Active esta opción si el plano se puede recortar mediante un plano de tierra o se sigue mostrando al pasar por debajo de él. Utilice Mostrar cuadrícula de suelo para estimarlo mejor. |
| <b>Height terrestre</b> <i>-2.0 - 0.0</i> | Ajuste el height de masa para el recorte. |
| <b>Habilitar entrada de fondo</b> <i>Falso/Verdadero</i> | Cambia el uso de la imagen de fondo opcional. Las composiciones generan luz sobre el fondo. |
| <b>Color de fondo</b> <i>(Valor de color)</i> | Si no se utiliza Entrada de fondo, defina aquí un valor de fondo de color sólido. |
| <b>Gama de fondo</b> <i>sRGB, lineal</i> | Si se utiliza Entrada en segundo plano, defina cómo interpretar la entrada en segundo plano. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/plane-light-ex.gif" />
        </td>
    </tr>
</table>
