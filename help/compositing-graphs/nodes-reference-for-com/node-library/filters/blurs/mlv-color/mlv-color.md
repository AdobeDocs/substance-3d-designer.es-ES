---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: Usa el filtro de desenfoque de color MLV para aplicar efectos de desenfoque de movimiento a las texturas de color para lograr aspectos visuales dinámicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# Color MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Color MLV: icon](../../../../../../assets/MLV_Color_Icon.png "MLV color: icon")

<b>En:</b> Filtros > Desenfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

MLV significa <b>&#39;Media de variación mínima&#39;</b>. Este filtro mejora los bordes y suaviza el ruido de una imagen.

El filtro encuentra áreas de estructuración en una imagen y las utiliza para enfocar y acoplar. En algunos casos, esto puede dar lugar a pasos a lo largo de degradados más anchos que las áreas de estructuración.

</td>
</tr>
</table>

>[!NOTE]
>
> Vea también [escala de grises MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md).

## Conectores de entrada

<b>Entrada </b>*Color* Imagen de color que se debe procesar.

## Conectores de salida

<b>Salida</b> *Color* Imagen de color filtrada.

## Parámetros

<b>Intensidad</b> *Flotante* Intensidad del filtrado aplicado a la imagen.\
Los valores más altos dan como resultado un suavizado de los detalles y ruido en las áreas más planas.

<b>Smoothness</b> *Flotante* Intensidad del suavizado aplicado a las áreas de estructuración, que da como resultado áreas más redondeadas y disminuye el efecto de escalonamiento que puede producirse a intensidades de filtrado más altas.

<b>Criterio</b> *Entero* Criterio utilizado para seleccionar los valores que definirán las áreas de estructuración de la imagen.\
En otras palabras, cómo se deben *agrupar* los píxeles en áreas que se deben suavizar.\
*- Varianza:* Selecciona valores con la dispersión más baja alrededor de la media, lo que da como resultado clústeres de píxeles similares entre sí\
*- Coeficiente de variación:* Selecciona los valores teniendo en cuenta la media, lo que resulta en una menor variación en las áreas más brillantes de forma inversa

<b>Gaussiano</b> *Booleano* Usa una distribución gaussiana para agrupar píxeles en áreas de estructuración.\
Si es &quot;True&quot;, esto produce áreas más suaves y un efecto de acoplado reducido.

<b>Afectar alfa</b> *Booleano* Si es &#39;True&#39;, el filtrado también se aplica en el canal alfa de la imagen.\
Cuando es &#39;False&#39;, el canal alfa se omite por completo y se deja como está en la salida.

<b>Iteraciones</b> *Entero* Número de veces que se ejecuta el filtro, donde cada iteración se aplica al resultado del anterior.\
Más iteraciones producen áreas de estructuración más planas y nítidas.

## Ejemplos

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant4A.png" alt="MLV_Variant4A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant4B.png" alt="MLV_Variant4B">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant5A.png" alt="MLV_Variant5A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant5B.png" alt="MLV_Variant5B">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant3A.png" alt="MLV_Variant3A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant3B.png" alt="MLV_Variant3B">
      <br><i>Después De</i>
    </td>
  </tr>
</table>
