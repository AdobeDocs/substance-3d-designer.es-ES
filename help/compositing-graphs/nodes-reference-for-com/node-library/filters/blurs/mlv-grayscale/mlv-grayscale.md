---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: Usa el filtro de desenfoque de escala de grises MLV para aplicar efectos de desenfoque de movimiento a las texturas de escala de grises para lograr aspectos dinámicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escala de grises MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# Escala de grises MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Escala de grises ![MLV: icon](mlv-grayscale.resources/MLV_Grayscale_Icon.png "MLV escala de grises: icon")

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
> Vea también [color MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Escala de grises</i> | La imagen en escala de grises que debe procesarse. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | Imagen en escala de grises filtrada. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Intensidad</b> *Flotante* | Intensidad del filtrado aplicado a la imagen.<br><br>Los valores más altos permiten suavizar más los detalles y hacer más ruido en las áreas más planas. |
| <b>Smoothness</b> *Flotante* | Intensidad del suavizado aplicado a las áreas de estructuración, que da como resultado áreas más redondeadas y disminuye el efecto de escalonamiento que puede producirse a intensidades de filtrado más altas. |
| <b>Criterio</b> *Entero* | Criterio utilizado para seleccionar los valores que definirán las áreas de estructuración de la imagen.<br><br>En otras palabras, cómo se deben *agrupar* los píxeles en áreas que se deben suavizar.<br><br>*- Varianza:* Seleccione valores con la dispersión más baja alrededor de la media, lo que da como resultado clústeres de píxeles similares entre sí&#x200B;<br>*- Coeficiente de variación:* Seleccione los valores teniendo en cuenta la media, lo que da como resultado una variación menor en las áreas más brillantes de forma inversa |
| <b>Gaussiano</b> *Booleano* | Utilice una distribución gaussiana para agrupar píxeles en áreas de estructuración.<br><br>Si es &#39;True&#39;, esto produce áreas más suaves y un efecto de acoplado reducido. |
| <b>Iteraciones</b> *Entero* | Número de veces que se ejecuta el filtro, donde cada iteración se aplica al resultado del anterior.<br><br>Más iteraciones producen áreas de estructuración más planas y nítidas. |

## Ejemplos

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant1A.png" alt="MLV_Variant1A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>Después De</i>
    </td>
  </tr>
</table>
