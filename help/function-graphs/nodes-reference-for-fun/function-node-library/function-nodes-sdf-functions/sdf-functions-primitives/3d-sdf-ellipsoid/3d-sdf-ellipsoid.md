---
title: Elipsoide
description: Designer > Gráficas de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Elipsoide
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---


# Elipsoide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de elipsoide](./3d-sdf-ellipsoid.png "Elipsoid")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Función SDF de un elipsoide, que es una forma redondeada de radio tridimensional ajustable.

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
| <b>Radio</b> *Float3* | Radio del elipsoide en X, Y y Z.<br><br><i>Valor predeterminado: (0,35, 0,35, 0,5)</i> |
| <b>Posición central</b> *Float3* | Posición del espacio de entorno del pivote del elipsoide.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
