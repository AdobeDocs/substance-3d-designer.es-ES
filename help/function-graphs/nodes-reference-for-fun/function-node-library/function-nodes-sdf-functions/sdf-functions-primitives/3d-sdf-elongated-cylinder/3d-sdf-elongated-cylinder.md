---
title: Cilindro extendido
description: Designer > Gráficas de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Primitiva > Cilindro alargado
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Cilindro extendido

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de cilindro alargado](./3d-sdf-elongated-cylinder.png "Cilindro alargado")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Función SDF para un cilindro alargado de longitud ajustable, radio y redondeo de bordes.<br>El cilindro alargado es el resultado de unir dos cilindros.

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
| <b>Height</b> *Flotador* | El height Z-up de los cilindros inicial y final desde su base.<br><br><i>Predeterminado: 0,5</i> |
| <b>Radio</b> *Flotador* | Radio de los cilindros inicial y final.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>Redondeo</b> *Flotador* | El radio de los arcos redondeados aplicados a los bordes del cilindro alargado.<br><br><i>Nota:</i> los bordes duros pueden aparecer donde se cruzan los radios de redondeo.<br><br><i>Valor predeterminado: 0</i> |
| <b>Posición central</b> *Float3* | Posición del espacio de entorno del pivote del cilindro alargado.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>Distancia de prolongación</b> *Flotador* | Distancia a lo largo de la cual se alarga el cilindro inicial.<br>Es decir. la distancia entre los centros de los cilindros inicial y final.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
