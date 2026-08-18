---
title: Transformar
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Operador > Transformar
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Transformar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de transformación](./3d-sdf-op-morph.png "Cambio")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Devuelve la interpolación lineal entre una forma de SDF base y una forma de SDF de destino de acuerdo con un factor de mezcla ajustable.

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
| <b>SDF base</b> *Flotador* | Forma SDF base. |
| <b>SDF de destino</b> *Flotador* | Forma de SDF de destino. |
| <b>Factor de mezcla</b> *Flotador* | El factor de mezcla utilizado para transformar las formas de entrada, donde 0 es la forma base y 1 la forma de destino. |
