---
title: Intersección suave
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Operador > Suavizado de intersección
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 1%

---


# Intersección suave

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de intersección suave](./3d-sdf-op-intersection-smooth.png "Intersección suave")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Devuelve el volumen común a dos formas SDF, de hecho el volumen creado donde se superponen dos formas, con suavizado ajustable de los bordes de su intersección.

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
| <b>Smoothness</b> *Flotador* | El smoothness de los bordes en la intersección de las dos formas SDF.<br><br><i>Nota:</i> bordes duros pueden aparecer donde se cruzan los radios de suavizado.<br><br><i>Valor predeterminado: 0</i> |
