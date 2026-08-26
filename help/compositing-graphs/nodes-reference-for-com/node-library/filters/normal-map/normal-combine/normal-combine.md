---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: Utilice el nodo Combinación normal para combinar varios mapas normales para obtener detalles y detalles de la superficie de la capa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinación normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---


# Combinación normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-combine.png){width="128px"}

<b>En:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Combinación normal combina los detalles de dos mapas normales de una forma matemáticamente correcta.

Es similar al conocido método &quot;Overlay&quot; de otro software de edición de imágenes 2D, pero funciona de forma interna ligeramente diferente (tres opciones).

</td>
</tr>
</table>

Esta es la forma mejor y más correcta de añadir detalles de mapa normal generados en 2D a un mapa con bake.

Si quieres fusionar dos mapas normales sin combinar sus detalles (usando una máscara, por ejemplo), deberías usar [Fusión normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md).

## Conectores de entrada

<b>Normal 2</b> *Color* Descripción

<b>Normal 1</b> *Color* Descripción

## Parámetros

<b>Técnica</b> *Entero* Establece qué técnica de fusión interna se debe usar, cambiando la velocidad por la calidad.\
*- Whiteout (baja calidad)
* Mezclador de canales (alta calidad)
* Orientado a los detalles (alta calidad)*

## Ejemplos
