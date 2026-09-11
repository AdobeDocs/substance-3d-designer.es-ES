---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: Utilice el nodo Mezclador de datos de malla de material para fusionar datos de malla de material para crear transiciones suaves entre diferentes zonas de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mezclador de datos de malla de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 8%

---


# Mezclador de datos de malla de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-mesh-data-blender.resources/material-mesh-data-blender.png){width="128px"}

<b>En:</b> Generadores basados en malla > Utilidades

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Este nodo está diseñado para facilitar la adición de detalles en función de los datos predefinidos. Viene con una gran cantidad de reguladores para modificar una entrada de material completo, basado en cualquier y todos los mapas con bake como entrada. Experimenta con él, ya que hay muchas opciones.

Es útil para hacer cosas como añadir resaltado de bordes basado en curvatura u otros mapas, mezclar en algunos AO con el color difuso/básico, añadir Oclusión de Specular basada en curvatura y/o AO, etc.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de material completa (grupo &quot;Material&quot;)</b> | Conjunto completo de mapas de materiales.<br><br>Este nodo los modifica y, a continuación, se devuelven de nuevo como resultados. |
| <b>Oclusión de ambiente</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. |
| <b>Curvatura</b> <i>Entrada en escala de grises</i> | Mapa con bake utilizado para efectos internos y máscaras. |
| <b>Height</b> <i>Entrada en escala de grises</i> |  |
| <b>Normal</b> <i>Entrada de color</i> |  |
| <b>Color de vértice</b> <i>Entrada de color</i> |  |
| <b>Normal del Espacio Mundial</b> <i>Entrada de color</i> |  |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Canales</b> | Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad. Afecta a la disponibilidad de los siguientes parámetros. |
| <b>Mapas con bake</b> | Si se deben o no utilizar los mapas con bake enumerados para los cálculos. Afecta a la disponibilidad de los siguientes parámetros. |
| <b>Difuso AO</b> <i>0.0 - 1.0</i> | Cantidad de Oclusión ambiental que se va a fusionar en la Difuso. |
| <b>Bordes afilados de Difuso</b> <i>0.0 - 1.0</i> | Cantidad del mapa de curvatura que se va a fusionar en la Difuso. |
| <b>Color De Difuso Del Color Del Vértice</b> <i>0.0 - 1.0</i> | Cantidad de color del vértice hecho un bake para fusionarse en la Difuso. |
| <b>Iluminación previa de Difuso</b> <i>0.0 - 1.0</i> | Cantidad de preiluminación (falsa), basada en las normas espaciales mundiales. |
| <b>Equilibrio de iluminación de dibujos animados</b> <i>0.0 - 1.0</i> | Cambia entre una iluminación realista y caricaturesca para el Difuso. |
| <b>Capas de iluminación previa de dibujos animados de Difuso</b> <i>0 - 10</i> | Controla el aspecto de los cálculos de iluminación de dibujos animados. |
| <b>Contornos de dibujos animados de Difuso</b> <i>0.0 - 1.0</i> | Controla el aspecto de los cálculos de iluminación de dibujos animados. |
| <b>Color base AO</b> <i>0.0 - 1.0</i> | Cantidad de Oclusión ambiental que se va a fusionar en el color base. |
| <b>Color base bordes afilados</b> <i>0.0 - 1.0</i> | Cantidad del mapa de curvatura que se va a fusionar en el color base. |
| <b>Color base Del Color Del Vértice</b> <i>0.0 - 1.0</i> | Cantidad de color del vértice hecho un bake para fusionarse en el color base. |
| <b>Intensidad de material normal</b> <i>0.0 - 1.0</i> | Intensidad de fusión del mapa normal hecho un bake (tangente). |
| <b>SpecularAO</b> <i>0.0 - 1.0</i> | Fuerza de fusión del AO en el Specular. |
| <b>Specular Brillante Bordes Afilados</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la Curvatura en el Specular. |
| <b>Contornos de dibujos animados de Specular</b> <i>0.0 - 1.0</i> | Intensidad de fusión de un efecto de contorno de borde de un Specular de dibujos animados, basado en la curvatura. |
| <b>Bordes nítidos oscuros de Brillo</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la curvatura en el Brillo. |
| <b>Bordes brillantes y nítidos de rugosidad</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la curvatura en la rugosidad. |
| <b>Contornos de dibujos animados de rugosidad</b> <i>0.0 - 1.0</i> | Intensidad de fusión de un efecto de contorno de borde de Rugosidad de dibujo animado, basado en la Curvatura. |
| <b>Bordes brillantes y brillantes metálicos</b> <i>0.0 - 1.0</i> | Intensidad de fusión de la curvatura en el panel Metálico. |
| <b>Contornos de dibujos animados metálicos</b> <i>0.0 - 1.0</i> | Intensidad de fusión de un efecto de contorno de borde metálico de dibujo animado, basado en la curvatura. |
| <b>Intensidad del material AO</b> <i>0.0 - 1.0</i> | Intensidad de Fusión del mapa con bake AO con material-generado AO, qué grado combinar ambos mapas AO en. |
| <b>Intensidad del material de Height</b> <i>0.0 - 1.0</i> | Fuerza de Fusión del Height de mapa con bake con Height generado por Material, qué grado combinar ambos mapas de Altura en. |
| <b>Tipo De Fusión De Material De Height</b> <i>Reforzar, Interpolación</i> | Modo de Fusión para combinar ambos mapas de altura. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-mesh-data-blender.resources/blenddata-ex.gif" />
        </td>
    </tr>
</table>
