---
title: Repetir rango de espejo
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Operador > Repetir rango de duplicación
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Repetir rango de espejo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de intervalo de duplicación de repetición](./3d-sdf-op-repeat-mirror.png "Intervalo de duplicación de repetición")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Refleja y duplica una forma SDF un número indeterminado de veces con un espaciado regular en los ejes X, Y y Z positivos o negativos.<br>Cada vez que este operador repite una forma, también la refleja. Esto produce visualmente una alternancia entre la orientación original de la forma y una copia volteada.

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
| <b>SDF</b> *Flotador* | Forma SDF de entrada. |
| <b>Importe +</b> *Entero3* | Cantidad de duplicaciones a lo largo de los ejes X, Y, Z positivos.<br><br><i>Valor predeterminado: (2, 0, 0)</i> |
| <b>Importe -</b> *Entero3* | Cantidad de duplicaciones a lo largo de los ejes X, Y, Z negativos.<br><br><i>Valor predeterminado: (2, 0, 0)</i> |
| <b>Espaciado</b> *Float3* | Espacio de mundo entre cada duplicado.<br><br>El espaciado se visualiza mediante un ayudante cúbico, cuyo tamaño es el espacio entre duplicados en las direcciones X, Y y Z. El espaciado comienza en la <b>posición de origen</b> y se incrementa simétricamente a partir de ella.<br><br><i>Valor predeterminado: (2, 2, 2)</i> |
| <b>Posición de origen</b> *Float3* | Define el centro de la forma SDF que se duplicará.<br><br>La posición de origen se visualiza mediante la posición central del ayudante cúbico.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
