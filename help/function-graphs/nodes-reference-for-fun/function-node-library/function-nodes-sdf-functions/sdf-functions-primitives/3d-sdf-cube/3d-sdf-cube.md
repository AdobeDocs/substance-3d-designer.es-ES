---
title: Cubo
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Cubo
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Cubo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de cubo](./3d-sdf-cube.png "Cubo")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para un cubo, con tamaño XYZ ajustable y redondeo de bordes.

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
| <b>Tamaño</b> *Float3* | Tamaño del cubo en X, Y y Z.<br><br><i>Valor predeterminado: (1, 1, 1)</i> |
| <b>Redondeo</b> *Flotador* | El radio de los arcos redondeados aplicados a los bordes del cubo.<br><br><i>Nota:</i> los bordes duros pueden aparecer donde se cruzan los radios de redondeo.<br><br><i>Valor predeterminado: 0</i> |
| <b>Posición de pivote (local)</b> *Float3* | Posición del espacio de entorno del giro local del cubo, donde (0, 0, 0) coloca el giro en el centro del cubo.<br><br><i>Valor predeterminado: (0, 0, -0,5)</i> |
| <b>Posición central</b> *Float3* | Posición del espacio de entorno de la tabla dinámica del cubo.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
