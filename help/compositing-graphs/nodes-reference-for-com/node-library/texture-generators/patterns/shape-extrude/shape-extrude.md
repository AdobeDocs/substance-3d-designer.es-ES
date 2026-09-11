---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Utilice el nodo Extrusión de forma para extruir formas y crear efectos de profundidad similares a 3D en texturas de Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrusión de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# Extrusión de forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude.png){width="128px"}

<b>En:</b> Generadores de Textura > Patrones

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Nodo avanzado que permite que las entradas binarias 2d de &quot;forma&quot; se representen en mapas de altura girados en 3D. Funciona de forma similar a una extrusión en un paquete 3D en el que se extruye una forma a lo largo de su eje, creando un volumen. En combinación con la máscara de degradado de perfil, también se pueden crear cuerpos de tipo Revolución/Torno. Muy útil para crear formas artificiales complejas para mapas de altura.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de extrusión de forma</b> <i>Entrada en escala de grises</i> | Si Extrusión de forma se establece en Personalizado, se debe conectar su propia máscara de forma binaria (preferiblemente) aquí. |
| <b>Degradado de perfil</b> <i>Entrada en escala de grises</i> | Si Tipo de perfil está establecido en Degradado vertical, se puede utilizar para definir la escala de la forma a lo largo del eje, para cuerpos de revolución. |
| <b>Máscara de perfil</b> <i>Entrada en escala de grises</i> | Ranura de máscara utilizada para ocultar o mostrar la forma Extruida a lo largo de su eje. Se puede utilizar para romper la continuidad de la forma a lo largo de su eje. Sólo se interpreta como binario: los valores de posición de escala de grises se redondean a 0 o 1. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Extruir Height</b> <i>0.0 - 1.0</i> | Cantidad que se extruye la forma hacia arriba desde el centro. |
| <b>Extruir Profundidad</b> <i>0.0 - 1.0</i> | Cantidad a la forma de extrusión por aguas abajo desde el centro. |
| <b>Extruir forma</b> <i>Cubo, cilindro, entrada personalizada</i> | Utilice formas integradas o introduzca su propia forma Personalizada externamente. |
| <b>Tamaño de forma de extrusión</b> <i>0.0 - 1.0</i> | Solo se utiliza con el cubo incorporado y el cilindro, determina el tamaño de la forma base, se puede escalar no uniforme. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Establezca la escala global del efecto. Con Formas incorporadas, se trata de una escala de forma base uniforme, que no afecta al Height ni a la Profundidad.<br><br>Con Entrada personalizada, se escala todo el resultado final de una manera uniforme. |
| <b>Tipo de perfil</b> <i>Degradado recto y vertical, máscara</i> | Control principal para determinar el comportamiento del efecto y el uso de mapas de entrada adicionales opcionales.<br><br>Recto es el comportamiento de extrusión estándar, Degradado vertical permite valores de escala personalizados a lo largo de todo el eje, Máscara permite ocultar secciones a lo largo del eje por máscara. |
| <b>Height biselado</b> <i>0.0 - 1.0</i> | Establezca hasta dónde llega el bisel a lo largo del eje de extrusión. |
| <b>Intensidad de bisel</b> <i>0.0 - 1.0</i> | Establezca cuánto se retrae el bisel de la forma original. |
| <b>Curva biselada</b> <i>-1.0 - 1.0</i> | Definir una curva cóncava o convexa del efecto Bisel. Un valor de 0 significa recto, sin curva. |
| <b>Bisel simétrico</b> <i>Falso/Verdadero</i> | Active esta opción para aplicar el bisel en la parte superior e inferior de la forma. |
| <b>Multiplicador de escala reducida</b> <i>0 - 2</i> | Control de reducción de escala incorporado sencillo. Se puede utilizar para agregar rápidamente suavizado; asegúrese de aumentar también la resolución del nodo. |
| <b>Posición</b> | Control principal para la rotación de resultados en el espacio 3D. Se correlaciona con el Gizmo de intersección en el Vista 2D. |
| <b>Intervalo de salida</b> <i>[0, 1], [-1, 1]</i> | Defina los valores mínimo y máximo de salida. Si el rango se establece en [-1,1], los valores negativos se presentan como negros. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-1.png" />
        </td>
    </tr>
</table>
