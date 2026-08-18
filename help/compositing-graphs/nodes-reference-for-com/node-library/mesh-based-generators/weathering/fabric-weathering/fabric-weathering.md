---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Utilice el nodo de erosión de la tela para añadir efectos de desgaste y envejecimiento a los materiales de la tela en función de la geometría de malla y la curvatura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tejido de intemperie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# Tejido de intemperie

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

## Tejido de intemperie

**En:** *Generadores Basados En Malla**/Meteorología*

**Complejo**

</td>
<td style="border: 0;" valign="top">

## Descripción

Se trata de un efecto de material completo que funciona en varios canales a la vez. Añade un efecto aleatorio de desgaste de la tela, con control de la edad y la suciedad.\
Este efecto no funciona muy bien a menos que tenga conectado un AO y un World Space Normalmaps adecuados, ya que requiere que estos calculen y generen todo adecuadamente.

Asegúrate de que comprendes perfectamente los [modos de creación de vínculos](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) al trabajar con materiales completos.

## Parámetros

### Entradas

* **Oclusión de ambiente**: *Entrada en escala de grises*\
  Mapa con bake utilizado para efectos internos y máscaras.
* **Espacio normal**: *Entrada de color*
* **Máscara** : *Entrada en escala de grises*\
  Ranura de máscara utilizada para enmascarar los efectos del nodo. Se puede activar y desactivar con el parámetro &quot;Mask&quot;.

### Parámetros

* **Canales**
  * Activa y desactiva los canales de material en este grupo, por ejemplo, al utilizar mapas de Specular/brillo en lugar de Metálico/Rugosidad.
* **Avanzado**
  * **Formato normal**: *DirectX, OpenGL*\
    Cambia entre diferentes formatos de Mapa normal (invierte el canal verde).
  * **Máscara**: *Falso/Verdadero*\
    Activa o desactiva el uso del mapa de máscara.
* **Efecto**
  * **Dust**: *0.0 - 1.0* Se fusiona en un efecto de dust más oscuro, basado en las áreas que se encuentran hacia arriba en el mapa normal del espacio mundial.
  * **Suciedad**: *0.0 - 1.0* Se mezcla en un efecto de dirt/difuminado global, basado principalmente en áreas ocluidas (oscuras) en el AO.
  * **Bordes Con**: *0.0 - 1.0* Agrega un efecto de enfoque/intensificación a los bordes, basado en Material Normal.
  * **Usado**: *0.0 - 1.0* Se mezcla en dirt muy oscuro acumulado en pliegues, basado en AO. Los valores máximos y mínimos tienden a ser muy extremos, úselos con cuidado.
  * **Edad**: *0.0 - 1.0* Se combina con un patrón de desgaste global de las baldosas. El control de umbral por debajo controla la influencia del AO. Los valores máximo y mínimo tienden a ser muy extremos.
  * **Umbral de edad**: *0.0 - 1.0* Establece la medida en que el AO afecta al parámetro Age.
  * **Creaciones de edad**: *0.0 - 1.0* Controla la fusión de arrugas adicionales sutiles en el efecto Edad.
  * **Escala de Scratches de bordes afilados**: *1.0 - 32.0* Define la escala de pequeños arañazos, que principalmente eliminan el efecto Usado y Edad.
  * **Intensidad de deformación de los Scratches de bordes afilados**: *0.0 - 1.0* Define la intensidad de la deformación para los arañazos pequeños anteriores.
  * **Desaturación de tejido antiguo**: *0.0 - 1.0* Controla la desaturación del efecto Edad.
  * **Brillo de tejido antiguo**: *0.0 - 1.0* Controla el brillo del efecto Edad. *Este es un parámetro muy importante para cambiar y obtener el aspecto deseado, pero los resultados pueden ser extremos: usar con cambios de subtítulos.*
* **Fusión**
  * **Intensidad de difusión**: *0.0 - 1.0*\
    Intensidad de fusión de la difusión.
  * **Intensidad de color base**: *0.0 - 1.0*\
    Intensidad de fusión del color base.
  * **Intensidad normal**: *0.0 - 1.0*\
    Intensidad de fusión de la Normal.
  * **Intensidad del Specular**: *0.0 - 1.0*\
    Fusión del Specular.
  * **Intensidad de brillo**: *0.0 - 1.0*\
    Fuerza de fusión del Brillo.
  * **Intensidad de rugosidad**: *0.0 - 1.0*\
    Fuerza de fusión de la rugosidad.
  * **Intensidad de Oclusión ambiente**: *0.0 - 1.0*\
    Fuerza de fusión de la Oclusión ambiente.
  * **Intensidad de Height**: *0.0 - 1.0*\
    Fusión del Height.

## Imágenes de ejemplo

![](../../../../../../assets/fabric-ex.gif)

</td>
</tr>
</table>
