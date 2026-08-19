---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/variables/create-a-variable.html"
breadcrumb-title: ''
description: Aprenda a crear variables personalizadas en los gráficos de funciones de Substance 3D Designer para valores y parámetros reutilizables.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Create a variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crear una variable
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Crear una variable

Hay diferentes formas de crear una variable en Substance 3D Designer:

* Uso de un parámetro de entrada
* Utilice un nodo Set.

## Uso de un parámetro de entrada

Cuando se crea un parámetro de entrada, se crea una variable asociada a él. A continuación, puede reutilizar esta variable en cualquier función del gráfico.

Por lo tanto, un solo parámetro expuesto puede influir en varias partes del gráfico.

## Uso de un nodo Set

Un nodo Set es un nodo que sólo está disponible en los gráficos de funciones:

Permite al usuario crear una variable personalizada:

* El nombre se declara en los parámetros.
* El valor se define mediante la entrada.

### Cómo usar el nodo *Set*

El uso de un nodo Set es un poco particular:

cuando se declara, solo está disponible dentro del gráfico, que por defecto no es realmente útil (después de todo, ya se puede generar su valor con enlaces).

Por lo tanto, debe declarar esta nueva variable, fuera de este gráfico.

para ello, debe utilizar un nodo de secuencia y realizar los siguientes pasos:

* Vincular el nodo de salida real a la &quot;última&quot; entrada del nodo Secuencia
* Vincule el nodo Set a la entrada &quot;In&quot; del nodo de la secuencia.
* Establecer la secuencia como nodo de salida

Cuando haya hecho esto, la variable estará disponible en el otro gráfico de funciones del mismo nodo.

>[!WARNING]
>
> Cuando el motor substance procesa un nodo, sus parámetros (y las funciones que podrían controlarlos) se leen de arriba abajo. Por lo tanto, sólo se puede tener acceso a un nodo Set mediante los parámetros situados debajo de él en la pila de parámetros de nodo.

>[!NOTE]
>
> Si tiene varias variables que crear, simplemente repita la operación de creación de nodos *Set* y *Sequence* y establezca el último nodo de secuencia como el nodo de salida:
> 
> ![](../../../assets/image2015-12-18-18-43-8.png)
