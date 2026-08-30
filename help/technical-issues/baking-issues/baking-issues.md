---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: Busque pasos de solución de problemas técnicos relacionados con la hace un bake de texturas en Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemas de horneado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Problemas de horneado

Esta página enumera problemas técnicos relacionados con [hacer un bake texturas](../../bakers/bakers.md) en Substance 3D Designer y ofrece pasos de solución de problemas para cada uno.

## En esta página

La coincidencia por nombre no funciona

## La coincidencia por nombre no funciona

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![(error)](baking-issues.resources/error.svg) Problema</b>

Cuando la opción &#39;Coincidencia&#39; se establece en &#39;Por nombre de malla&#39;, la coincidencia no parece aplicarse o no de forma coherente en todos los objetos de escena.

<b>![(marca)](baking-issues.resources/check.svg) Pasos recomendados</b>

En las versiones 14.1 y anteriores de Designer, los objetos de poli bajo y poli alto coincidían con el nombre de sus objetos *principales*; en la mayoría de los casos, su objeto principal transforma.

Desde Designer 15.0, el nombre de los objetos *geometry* se usa directamente.

</td>
<td style="border: 0;" valign="top">

![Objeto de geometría y su elemento primario en el árbol de escenas](baking-issues.resources/sceneTree_objectsName.png "Objeto de geometría y su elemento primario en el árbol de escenas"){zoomable="yes"}

</td>
</tr>
</table>

Hay dos caminos que puede tomar para obtener la coincidencia esperada:

* Ajuste el nombre de los objetos de geometría para aplicar nombres coincidentes.
* Vuelva al comportamiento o a las versiones anteriores de Designer, ajustando la opción [&#39;modo de filtro de nombres&#39;](../../interface/preferences-window/project-settings/project-settings.md) en la configuración del proyecto:
  1. Vaya a Editar > Preferencias > Proyectos
  1. Seleccione el último archivo de proyecto de la lista
  1. Debajo de la lista de archivos de proyecto, seleccione la pestaña &quot;Bakeres&quot;
  1. Establezca el &quot;modo de filtro de nombre&quot; en &quot;Nombre principal (heredado)
