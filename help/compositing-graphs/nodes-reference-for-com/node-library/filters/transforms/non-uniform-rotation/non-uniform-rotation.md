---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: Utilice el nodo Rotación no uniforme para aplicar transformaciones de rotación no uniformes para crear efectos de espiral y vórtice.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotación no uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# Rotación no uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

<b>En:</b> Filtros > Transforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

El nodo **Rotación no uniforme** gira la **entrada** mediante la entrada **Mapa de rotación**.

Los valores de la imagen representan un *número de vueltas*. La rotación se realiza alrededor de la posición especificada por el valor **Posición de pivote** o la entrada **mapa de Posición de pivote**.\
Los valores positivos en la entrada **Mapa de rotación** dan como resultado una rotación *en el sentido de las agujas del reloj*.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Escala de grises/Color</i> | La imagen de entrada en escala de grises que se debe rotar. |
| <b>Mapa de rotación</b> <i>Escala de grises</i> | Mapa utilizado para controlar la cantidad de rotación, en *número de vueltas*. Los valores muestreados se multiplican por el **multiplicador de ángulo de rotación**. Los valores negativos dan como resultado una rotación *hacia la izquierda*. |
| <b>Mapa de Posición de pivote de rotación</b> <i>Color</i> | Imagen utilizada para especificar la posición de la rotación *pivot*. La posición **X/Y** está asignada a los **canales R/G** de la imagen. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Multiplicador de ángulo de rotación</b> <i>Flotador</i> | Ajusta la intensidad de la entrada de **Mapa de rotación**. |
| <b>Desplazamiento del ángulo de rotación</b> <i>Flotador</i> | Aplica la cantidad adicional de rotación especificada. |
| <b>Usar mapa de Posición de pivote</b> <i>Booleano</i> | Use una *entrada de mapa de bits* para especificar la posición de la rotación pivot. La posición **X/Y** está asignada a los canales **R/G** de la entrada **Position Map**. |
| <b>Posición de pivote</b> <i>Float2</i> | Posición del giro alrededor del cual gira la imagen. |
| <b>Color de fondo</b> <i>Float/Float4</i> | Color de fondo para mostrar *fuera* de los límites de la imagen en caso de que el mosaico no esté establecido en **Mosaico H y V**. |
| <b>Modo de filtrado</b> <i>Entero</i> | Define cómo tratar los resultados muestreados al *interpolar* entre píxeles:<br><br>- *Más cercano*: mostrará exactamente el *mismo valor* (más rápido)<br>- *Bilineal*: aplicará un filtro bilineal en el resultado para obtener un aspecto *más suave* |

## Ejemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-demo-02-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-variant-png.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-node.png" />
        </td>
    </tr>
</table>
