---
title: Roca
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance de composición > Biblioteca de nodos > Función SDF > Primitiva > Roca
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Roca

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de roca](./3d-sdf-rock.png "Roca")

<b>En:</b> Función SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Una Función SDF para una forma de roca paramétrica y aleatoria, construida con Funciones SDF.

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
| <b>Máx. facetas</b> *Entero* | Número máximo de facetas de la roca (hasta 32).<br><br><i>Valor predeterminado: 8</i> |
| <b>Smoothness</b> *Flotador* | El radio de los arcos redondeados aplicados a los bordes de la roca.<br><br><i>Valor predeterminado: 0</i> |
| <b>Aleatoriedad</b> *Flotador* | Variación de la orientación de las caras y la distancia al centro.<br>Como resultado, los valores mayores dan como resultado una roca más pequeña.<br><br><i>Valor predeterminado: 0</i> |
| <b>Raíz</b> *Flotador* | Raíz para el parámetro <b>Randomness</b>.<br><br><i>Predeterminado: 0</i> |
| <b>Escala</b> *Flotador* | Escala global de la forma de la roca.<br>Aplicado después de <b>Aleatoriedad</b> y antes del <b>Smoothness</b>.<br><br><i>Valor predeterminado: 0,5</i> |
| <b>Posición central</b> *Float3* | Posición espacial mundial del pivote de la roca.<br><br><i>Predeterminado: (0, 0, 0,5)</i> |
| <b>P</b> *Float3* | La posición espacial mundial transformada. Utilice esta entrada para aplicar transformaciones adicionales mediante los nodos <b>Desplazamiento P</b> y <b>Rotar P</b>.<br><i>Valor predeterminado: La posición espacial mundial sin transformar.</i> |
