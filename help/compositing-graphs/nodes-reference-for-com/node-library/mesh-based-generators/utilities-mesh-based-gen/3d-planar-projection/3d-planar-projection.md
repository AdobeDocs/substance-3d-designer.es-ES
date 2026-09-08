---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: Utilice el nodo Proyección Plana 3D para proyectar texturas en superficies de malla mediante la proyección plana para la asignación de texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Proyección Plana en 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# Proyección Plana en 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

<b>En:</b> Generadores basados en malla > Utilidades

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Realiza una proyección plana basada en datos de malla hechos un bake (Mapas de normales de posición y de mundo). Permite proyectar y colocar pegatinas a través de las costuras, independientemente de la asignación UV original.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Mapa de posición</b> <i>Entrada de color</i> | Mapa de posición hecho un bake |
| <b>Normal del Espacio Mundial</b> <i>Entrada de color</i> | Mapa Normal del Espacio Mundial hecho un bake |
| <b>Textura proyectada</b> <i>Entrada de color</i> | Textura de entrada al proyecto en el destino. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Colocación</b> |  |
| <b>Entrada de proyecto</b> <i>Posición UV, Posición Espacial Mundial</i> | Elija si la posición de proyección está definida en 2D/UV o en el espacio 3D/Mundo. |
| <b>Posición UV de destino</b> | Solo con entrada de posición UV, se recomienda utilizar para seleccionar un punto en la Vista 2D del mapa de posición. |
| <b>Posición de destino</b> <i>(Valor de color)</i> | Solo con Entrada de posición de espacio mundial, permite definir una coordenada 3D exacta. |
| <b>Destino normal</b> <i>(Valor de color)</i> |  |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Gira la textura proyectada a lo largo del eje normal. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Establezca la escala global de la textura proyectada. |
| <b>Tamaño</b> <i>0.0 - 2.0</i> | Realizar escalado no uniforme en la textura proyectada. |
| <b>Enmascaramiento</b> |  |
| <b>Profundidad máxima</b> <i>0.0 - 1.0</i> | Controla la profundidad a la que aparecerá la textura proyectada y el momento en que se cortará. |
| <b>Desvanecimiento de Profundidad</b> <i>0.0 - 1.0</i> | Defina la transición para que la profundidad de corte sea repentina o descolorida. |
| <b>Umbral normal</b> <i>-1.0 - 1.0</i> | Defina el umbral para las superficies que no estén exactamente alineadas con la proyección normal. |
| <b>Transición normal</b> <i>0.0 - 1.0</i> | Defina la transición para las superficies que no estén alineadas como repentinas o fundidas. |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-planar-projection-ex.gif" />
        </td>
    </tr>
</table>
