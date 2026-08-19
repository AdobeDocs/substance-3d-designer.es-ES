---
title: Cono tapado
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Cono cerrado
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# Cono tapado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de cono cerrado](./3d-sdf-capped-cone.png "Cono cerrado")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para un cono tapado de base ajustable y radios superiores.

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
| <b>Base de radio</b> *Flotador* | Radio de la base del cono cerrado.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>Radio superior</b> *Flotador* | Radio de la parte superior del cono cerrado.<br><br><i>Valor predeterminado: 0,2</i> |
| <b>Height</b> *Flotador* | El height Z-up del cono tapado desde su base.<br><br><i>Valor predeterminado: 1</i> |
| <b>Posición central</b> *Float3* | Posición del espacio de entorno del pivote del cono cerrado.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
