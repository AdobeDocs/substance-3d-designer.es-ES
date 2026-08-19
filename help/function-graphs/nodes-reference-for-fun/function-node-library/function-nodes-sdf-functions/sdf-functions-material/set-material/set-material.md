---
title: Establecer material
description: Establezca el color base, la rugosidad y la metalidad del material de una escena de SDF.
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---


# Establecer material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Establecer icono de material](set-material.png "Establecer material")

<b>En:</b> Función 3D > Material

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Establezca el color base, la rugosidad y la metalidad del material de una escena de SDF.

Estos valores se pueden recuperar para todas las formas SDF salpicadas en los resultados de [Shape splatter v2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md).

</td>
</tr>
</table>

>[!INFO]
> 
> Para obtener más información sobre conceptos y flujos de trabajo que implican Funciones SDF, vaya a la página dedicada: [Trabajando con Funciones SDF](../../working-with-sdf-functions.md)

## Entradas

|                            |                                  |
|----------------------------|----------------------------------|
| <b>Escena de SDF</b> *Flotador* | La escena SDF de entrada. |
| <b>Color base</b> *Float3* | Valor de color base del RGB que se va a establecer. |
| <b>Metalness</b> *Flotador* | Valor de metalness que se va a establecer. |
| <b>Rugosidad</b> *Flotador* | El valor de rugosidad que se va a establecer. |
