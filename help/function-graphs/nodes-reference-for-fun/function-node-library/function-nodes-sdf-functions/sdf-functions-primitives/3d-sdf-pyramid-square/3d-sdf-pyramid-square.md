---
title: Pirámide cuadrada
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Primitiva > Cuadrado piramidal
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# Pirámide cuadrada

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de cuadrado de pirámide](./3d-sdf-pyramid-square.png "Cuadrado de pirámide")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para una pirámide con una base cuadrada, con height ajustable y posición base.

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
| <b>Height</b> *Flotador* | El height Z-up del ápice de la pirámide desde su base.<br><br><i>Valor predeterminado: 1</i> |
| <b>Tamaño base</b> *Flotador* | La longitud de los bordes base de la pirámide.<br>Todos los bordes tienen la misma longitud.<br><br><i>Valor predeterminado: 1</i> |
| <b>Posición base</b> *Float3* | Posición del espacio mundial de la base de la pirámide.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
