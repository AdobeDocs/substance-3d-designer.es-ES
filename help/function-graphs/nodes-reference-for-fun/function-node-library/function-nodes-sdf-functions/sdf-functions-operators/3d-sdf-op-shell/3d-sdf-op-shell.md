---
title: Concha
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Operador > Shell
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---


# Concha

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de shell](./3d-sdf-op-shell.png "Shell")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Hace que una forma SDF sea hueca, con thickness ajustable para su envolvente resultante.

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
| <b>Thickness</b> *Flotador* | El thickness de la cáscara, aplicado tanto hacia dentro como hacia fuera.<br>El shell se redondea al aumentar el thickness.<br><br><i>Valor predeterminado: 0,02</i> |
