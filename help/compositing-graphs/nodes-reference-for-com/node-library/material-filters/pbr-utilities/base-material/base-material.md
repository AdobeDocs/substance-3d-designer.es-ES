---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: Utilice el nodo Material base para crear propiedades de material base para crear materiales basados en la física desde cero.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Material de base
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 6%

---


# Material de base

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](base-material.resources/pbr-base-material.png){width="128px"}

<b>En:</b> Filtros de material > Utilidades de PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

La forma más rápida y sencilla de crear un material multicanal en [Adobe Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html). Este nodo devuelve un paquete de material completo basado en valores y ajustes de color simples y sólidos. A continuación, se puede utilizar como marcador de posición o para refinar en un material complejo.

El nodo es muy útil cuando se texturizan accesorios completos y se mezclan varios materiales. De hecho, puedes iniciar cada material desde este nodo, sin necesidad de una base de materiales compleja.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
|  | Entradas opcionales para cada canal que se pueden activar con los interruptores en &quot;Entradas definidas por el usuario&quot;. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Flujo de trabajo de PBR</b> <i>Metal - Rugosidad, Specular - Brillo</i> | Establece el modelo de PBR utilizado. |
| <b>Ajuste preestablecido de material</b> <i>Personalizado, Dieléctrico, Oro, Plata, Aluminio, Hierro, Cobre, Titanio, Níquel, Cobalto, Platino</i> | Método abreviado rápido para crear ciertos metales. Deshabilita las opciones irrelevantes. |
| <b>Color base</b> <i>(Valor de color)</i> | Color sólido utilizado para el Color base. |
| <b>Metálico</b> <i>(valor de escala de grises)</i> | Valor sólido utilizado para Metallic. |
| <b>Color de Difuso</b> <i>(Valor de color)</i> | Color sólido utilizado para el Difuso. |
| <b>Specular</b> <i>(Valor de color)</i> | Color sólido utilizado para el Specular. |
| <b>Ajustes preestablecidos de Specular</b> <i>Plástico, Madera, Piedra, Ladrillo, Arena, Hormigón, Tela, Metal oxidado, Agua, Hielo, Vidrio</i> | Ajustes preestablecidos rápidos opcionales para establecer valores de Specular correctos para PBR. |
| <b>Rango de Speculares</b> <i>0.0 - 1.0</i> | Ajusta el rango de Specular. |
| <b>Rugosidad - Brillo</b> |  |
| <b>Valor de rugosidad</b> <i>(valor de escala de grises)</i> | Establezca el valor de rugosidad base global, si el canal está activo. |
| <b>Valor de Brillo</b> <i>(valor de escala de grises)</i> | Color sólido utilizado para el Brillo, si el canal está activo. |
| <b>Cantidad de Suciedades</b> <i>0.0 - 1.0</i> | Grado en el que la entrada del mapa de Suciedades opcional se mezcla en Brillo o Rugosidad. |
| <b>Mosaico de Suciedades</b> <i>1 - 16</i> | Grado de segmentación del mapa de Suciedades opcional por. |
| <b>Entrada de Suciedad personalizada</b> <i>Falso/Verdadero</i> | Habilita o deshabilita el mapa de Suciedad personalizado opcional. |
| <b>Normal</b> |  |
| <b>Normal a partir de la intensidad del Height</b> <i>0.0 - 16.0</i> | Si lo desea, convierte el mapa de altura personalizado en normal y lo devuelve como el mapa normal del material. |
| <b>Height</b> |  |
| <b>Posición del Height</b> <i>0.0 - 1.0</i> | Valor sólido utilizado para la salida de Height. |
| <b>Intervalo de Height</b> <i>0.0 - 1.0</i> | Define la influencia del mapa de altura definido por el usuario, si está activado. |
| <b>Asignaciones definidas por el usuario</b> | Activa o desactiva todas las asignaciones definidas por el usuario y las devuelve en lugar de valores sólidos. |
