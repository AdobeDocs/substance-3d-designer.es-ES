---
title: Alargar
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Transformar > Alargar
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# Alargar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de alargar](./3d-sdf-transform-elongate.png "alargar")

<b>En:</b> Función SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Alargar una forma SDF desde una posición ajustable.<br>Extiende linealmente de manera efectiva el volumen de una forma SDF a partir de un sector ajustable.

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
| <b>SDF</b> *Flotador* | Forma SDF de entrada. |
| <b>Alargamiento</b> *Float3* | Longitud de alargamiento en los ejes X, Y, Z. |
| <b>Posición central</b> *Float3* | Posición del espacio mundial desde la que se alargará la forma.<br>Es decir, la posición del sector que se alarga. |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
