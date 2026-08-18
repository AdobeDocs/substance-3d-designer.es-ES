---
title: Simetría
description: Designer > Gráficos de composición de Substance > Referencia de nodos para Substance > Biblioteca de nodos > Función SDF > Operador > Simetría
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Simetría

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icono de simetría](./3d-sdf-op-symmetry.png "Simetría")

<b>En:</b> Función SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Voltea y duplica una forma SDF en un plano simétrico y, a continuación, devuelve la unión de la forma SDF base y sus duplicados.<br>La simetría se puede aplicar en cualquier eje de forma simultánea.

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
| <b>Posición de plano de espejo</b> *Float3* | La posición espacial mundial del centro del plano especular.<br>Todos los planos espejo comparten esta posición si la simetría se aplica en varios ejes.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>Eje de simetría</b> *Entero3* | Establece los ejes de simetría deseados.<br><br>Por ejemplo, (1, 0, 0) aplicará simetría en el eje X.<br><br><i>Valor predeterminado: (1, 0, 0)</i> |
| <b>Voltear eje</b> *Entero3* | Establece los ejes que se deben voltear.<br><br>Por ejemplo, (1, 0, 0) volteará la dirección de la simetría en el eje X.<br><br><i>Valor predeterminado: (0, 0, 0)</i> |
| <b>Desplazamiento previo</b> *Float3* | El desplazamiento en los ejes X, Y, Z se aplica a la forma antes de aplicar el operador de simetría. |
