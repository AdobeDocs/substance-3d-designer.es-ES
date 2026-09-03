---
helpx_url: ""
breadcrumb-title: ''
description: Utilice la ventana emergente de Desplazamiento para ajustar rápidamente el desplazamiento y la teselación aplicados a las mallas en una escena 3D.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Vista 3D: ventana emergente de Desplazamiento'
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# Ventana emergente de desplazamiento

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>La ventana emergente de Desplazamiento disponible en la barra de herramientas Vista 3D ofrece controles directos para el desplazamiento y la teselación de mallas.</p>
            <p>Hay tres parámetros:<ul>
                <li>Escala de altura</li>
                <li>Nivel de altura</li>
                <li>Teselación</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/displacement-01.gif" alt="Ventana emergente desplazamiento en la vista 3D" />
        </td>
    </tr>
</table>

## Escala de altura

Distancia máxima del desplazamiento para los vértices de malla a lo largo de su normal, en unidades de escena.<br>
Esta es la distancia recorrida para un valor de 1,0 en el mapa de height.

Cuando un gráfico de Substance está conectado a un material y ese gráfico incluye un [nodo de salida](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) con
<code>heightScale</code> , el parámetro de escala de Height en la ventana emergente está *deshabilitado* para ese material
ya que actualmente está siendo manejado por el gráfico.

>[!TIP]
> 
>Use el nodo [Height a unidades del mundo normal](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md) y haga que su parámetro &#39;profundidad de Height&#39; coincida con el valor &#39;escala de Height&#39;
>para garantizar el sombreado correcto al utilizar desplazamiento.

## Nivel de altura

Valor de escala de grises en la asignación de height que se utiliza como *punto medio* para el height de desplazamiento.
Es decir, el valor de umbral utilizado como elevación 0,0.

Los valores por debajo de ese umbral dan como resultado que los vértices se desplacen hacia atrás, mientras que los valores por encima del umbral dan como resultado
los vértices se desplazan hacia adelante.

## Teselación

La teselación implica la subdivisión de caras de malla individuales mediante la adición de un vértice en sus segmentos y, a continuación, la conexión
todos los vértices a un nuevo vértice en su centro, de modo que 1 cara se convierta en **6**.

El parámetro define la cantidad de veces que las caras se deben subdividir recursivamente.

El *ámbito* del parámetro de teselación varía según el *procesador* que se esté utilizando actualmente: se puede aplicar
por malla o por material.

### Por malla

Al utilizar el procesador [Rasterizer](../3d-renderers/3d-renderers.md#rasterizer) o [Trazador de ruta de GPU](../3d-renderers/3d-renderers.md#gpu-pathtracer), cada objeto Mesh de la escena tiene *un procesador independiente*
valor de subdivisión.

La subdivisión es contextual: está optimizada de tal manera que solo aparece con un *valor de height no uniforme* o
se subdividirá un *mapa de altura no plana*, independientemente del valor del parámetro.

### Por material

Al utilizar el procesador [OpenGL](../3d-renderers/3d-renderers.md#opengl), cada material de la escena tiene un valor de subdivisión *independiente*, que
se aplica a *todas las caras que usan ese material*.

La subdivisión no es contextual: las superficies se subdividen la cantidad de veces especificada, independientemente de su corriente
valor de height o textura.

## Visualización de teselación

Puede visualizar el resultado de la teselación comprobando la **malla metálica** de la malla.<br>
A continuación se describen los pasos para mostrar la malla metálica de cada procesador:

### Rasterizador/Trazador de ruta de GPU

Utilice la <img src="../3d-view.resources/3d-view-18.png" width="22" /> **Configuración del procesador**
 y, en el conjunto acoplado Propiedades, ve a **Configuración de procesamiento > Modo de diagnóstico** y selecciona la Malla metálica **(espacio de entorno) opción**.

### OpenGL

Utilice la <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **Malla metálica**
 botón.
