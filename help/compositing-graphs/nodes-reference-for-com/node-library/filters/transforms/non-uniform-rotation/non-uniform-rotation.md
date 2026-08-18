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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Rotación no uniforme

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

**En:** Filtros*/Transformaciones*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descripción

El nodo **Rotación no uniforme** gira la **entrada** mediante la entrada **Mapa de rotación**.

Los valores de la imagen representan un *número de vueltas*. La rotación se realiza alrededor de la posición especificada por el valor **Posición de pivote** o la entrada **mapa de Posición de pivote**.\
Los valores positivos en la entrada **Mapa de rotación** dan como resultado una rotación *en el sentido de las agujas del reloj*.

</td>
</tr>
</table>

## Parámetros

### Entradas

* **Entrada** *Escala de grises/Color*\
  La imagen de entrada en escala de grises que se debe rotar.
* **Mapa de rotación** *Escala de grises* El mapa utilizado para controlar la cantidad de rotación, en *número de vueltas*. Los valores muestreados se multiplican por el **multiplicador de ángulo de rotación**. Los valores negativos dan como resultado una rotación *hacia la izquierda*.
* **Mapa de Posición de pivote de rotación** *Color*\
  Imagen utilizada para especificar la posición de la rotación *pivot*. La posición **X/Y** está asignada a los **canales R/G** de la imagen.

### Parámetros

* **Multiplicador de ángulo de rotación** *Flotante*\
  Ajusta la intensidad de la entrada de **Mapa de rotación**.
* **Desplazamiento del ángulo de rotación** *Flotante*\
  Aplica la cantidad adicional de rotación especificada.
* **Usar asignación de Posición de pivote** *Boolean*\
  Use una *entrada de mapa de bits* para especificar la posición de la rotación pivot. La posición **X/Y** está asignada a los canales **R/G** de la entrada **Position Map**.
* **Posición de pivote** *Float2*\
  Posición del giro alrededor del cual gira la imagen.
* **Color de fondo** *Float/Float4*\
  Color de fondo para mostrar *fuera* de los límites de la imagen en caso de que el mosaico no esté establecido en **Mosaico H y V**.
* **Modo de filtrado** *Entero*\
  Define cómo tratar los resultados muestreados al *interpolar* entre píxeles:
  * *Más cercano*: mostrará exactamente el valor *same* (más rápido)
  * *Bilineal*: aplicará un filtro bilineal en el resultado para obtener un aspecto *más suave*

## Imágenes de ejemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-demo-02-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-variant-png.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-node.png){width="256px"}

</td>
</tr>
</table>
