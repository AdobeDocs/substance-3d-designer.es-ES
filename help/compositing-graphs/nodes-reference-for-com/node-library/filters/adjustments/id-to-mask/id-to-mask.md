---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: Utilice el nodo ID para enmascarar escala de grises para convertir los valores de mapa de ID en máscaras de escala de grises para la selección de materiales.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ID para enmascarar escala de grises
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---


# ID para enmascarar escala de grises

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Id. para enmascarar icono de escala de grises](../../../../../../assets/IDToMask.png "Id. para enmascarar icono de escala de grises"){width="200px"}

<b>En:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Crea una máscara a partir de un mapa de ID en el que los píxeles con los valores de píxeles seleccionados son blancos.

Un mapa de ID es una imagen en la que los píxeles que forman parte de un todo (por ejemplo, una forma) tienen el mismo valor de identificación único. En este caso, el valor es un entero.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>ID</b> <i>Escala de grises</i> PRINCIPAL | Mapa de ID de entrada del que se debe extraer una máscara. |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Salida</b> <i>Escala de grises</i> | Máscara binaria extraída de la asignación de ID de entrada. |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Modo de selección</b> *Entero* | Método de selección de los valores de píxeles en el mapa de ID que deben ser blancos en la máscara:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Solo:</b> Seleccione un valor de píxel único</li> <li data-preserve-html="true"><b>Rango:</b> Seleccione un rango de valores de píxeles</li> </ul> |
| <b>Entero de Id.</b> *Entero* *Disponible cuando &#39;Selection Mode&#39; está establecido en &#39;Solo&#39;* | El valor de píxel en el mapa de ID que debe ser blanco en la máscara de salida. |
| <b>Intervalo de ID</b> *Integer2* *Disponible cuando &#39;Selection Mode&#39; está establecido en &#39;Range&#39;* | Rango de valores de píxeles del mapa de ID, de principio a fin, que debería ser blanco en la máscara de salida. |

## Ejemplos

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>Después De</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Id. para enmascarar: Ejemplo 2](../../../../../../assets/id_to_mask_example_2.gif "ID para enmascarar: Ejemplo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Id. para enmascarar: Ejemplo 3](../../../../../../assets/id_to_mask_example_3.png "ID que enmascarar: Ejemplo 3"){zoomable="yes"}

</td>
</tr>
</table>
