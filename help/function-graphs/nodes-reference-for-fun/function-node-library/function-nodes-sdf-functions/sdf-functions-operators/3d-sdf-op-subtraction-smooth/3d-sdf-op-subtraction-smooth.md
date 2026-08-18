---
title: 'Suavizado de resta '
description: 'Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Operador > Suavizado de resta '
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# Suavizado de resta

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono Suavizado de resta](./3d-sdf-op-subtraction-smooth.png "Suavizado de resta ")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Resta el volumen de la forma SDF 1 de la forma SDF 2, con suavizado ajustable aplicado en la intersección de las dos.

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
| <b>SDF 1</b> *Flotador* | Forma SDF de la que se va a restar. |
| <b>SDF 2</b> *Flotador* | Forma SDF que se resta de la forma SDF 1. |
| <b>Smoothness</b> *Flotador* | El suavizado aplicado en la intersección de las dos formas.<br><br><i>Nota:</i> pueden aparecer bordes duros donde se cruzan los radios de suavizado. |
