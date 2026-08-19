---
title: superficie de intersección
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Operador > Superficie de intersección
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# superficie de intersección

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de superficie de intersección](./3d-sdf-op-intersection-surface.png "Superficie de intersección")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Devuelve la superficie de la parte de una forma SDF base que está intersecada por otra forma SDF, con thickness ajustable.

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
| <b>SDF base</b> *Flotador* | Forma SDF en la que se basa la superficie resultante. |
| <b>SDF en intersección</b> *Flotador* | Forma SDF que intersecta con la forma SDF base. |
| <b>Thickness</b> *Flotador* | Thickness de la superficie resultante.<br><br><i>Valor predeterminado: 0,02</i> |
