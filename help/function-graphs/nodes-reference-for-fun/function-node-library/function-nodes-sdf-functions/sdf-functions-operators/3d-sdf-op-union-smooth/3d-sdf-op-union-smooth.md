---
title: Unión suave
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Operador > Suavizado de uniones
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Unión suave

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de unión suave](./3d-sdf-op-union-smooth.png "Unión suave")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Devuelve los volúmenes agregados de dos formas SDF, con suavizado ajustable de los bordes de su intersección.

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
| <b>SDF 1</b> *Flotante* | La primera forma de SDF. |
| <b>SDF 2</b> *Flotante* | La segunda forma SDF. |
| <b>Smoothness</b> *Flotante* | El radio de suavizado, comenzando por los bordes de la intersección.<br><br><i>Valor predeterminado: 0</i><br><br><i>Nota:</i> pueden aparecer bordes duros donde se cruzan los radios de suavizado. |
