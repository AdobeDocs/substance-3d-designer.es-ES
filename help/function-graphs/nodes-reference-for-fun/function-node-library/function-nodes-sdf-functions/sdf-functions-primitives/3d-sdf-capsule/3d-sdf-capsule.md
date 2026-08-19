---
title: Cápsula
description: Designer > Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Cápsula
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# Cápsula

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de la cápsula](./3d-sdf-capsule.png "Cápsula")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para una cápsula de longitud y radio ajustables.<br>La cápsula es el resultado de unir dos esferas.

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
| <b>Inicio</b> *Float3* | Posición de la esfera de inicio.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>Fin</b> *Float3* | Posición de la esfera final.<br><br><i>Valor predeterminado: (0, 0, 1)</i> |
| <b>Radio</b> *Flotador* | El radio de las esferas inicial y final.<br><br><i>Valor predeterminado: 0,25</i> |
| <b>Iniciar o finalizar en la sugerencia</b> *Booleano* | Controla si las posiciones <b>Inicio</b> y <b>Fin</b> deben estar en los extremos de las esferas.<br>Es decir, controla si el height de la cápsula debe incluir el radio de las esferas.<br><br><i>Valor predeterminado: False</i> |
| <b>Posición central</b> *Float3* | Posición del espacio mundial del pivote de la cápsula.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
