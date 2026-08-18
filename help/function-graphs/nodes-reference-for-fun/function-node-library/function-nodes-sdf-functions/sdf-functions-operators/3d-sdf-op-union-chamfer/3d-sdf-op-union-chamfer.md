---
title: chaflán de unión
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Operador > Chaflán de unión
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# chaflán de unión

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de chaflán de unión](./3d-sdf-op-union-chamfer.png "chaflán de unión")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Devuelve los volúmenes agregados de dos formas SDF, con un volumen adicional de radio ajustable a lo largo de los bordes de su intersección.

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> Para obtener más información sobre conceptos y flujos de trabajo que implican Funciones SDF, vaya a la página dedicada: [Trabajando con Funciones SDF](../../working-with-sdf-functions.md)

## Entradas

|  |  |
| :--- | :--- |
| <b>SDF 1</b> *Flotador* | La primera forma de SDF. |
| <b>SDF 2</b> *Flotador* | La segunda forma SDF. |
| <b>Radio</b> *Flotador* | Radio del volumen agregado a lo largo de los bordes de la intersección de las formas.<br><br><i>Valor predeterminado: 0</i> |
