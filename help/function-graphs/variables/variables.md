---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables.html"
breadcrumb-title: ''
description: Aprenda a utilizar variables en los gráficos de funciones de Substance 3D Designer para almacenar y reutilizar valores de forma eficaz.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variables
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Variables

>[!NOTE]
>
> Para obtener información sobre la creación y el uso de nodos de variables, consulte la sección *[Nodos de variables](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)*.

## Definición

Si usted tiene poco conocimiento en programación, es posible que esté familiarizado con el concepto de variable.

En caso contrario, se trata de una definición simple:

>[!NOTE]
>
> Una variable es simplemente un &quot;contenedor&quot; con un nombre específico que contiene un valor.
> 
> Puede utilizar el valor contenido en una variable llamándola con su nombre.

## Tipos de variables

En Substance 3D Designer, hay dos familias de variables: Numéricos y booleanos.

## Variables numéricas

Las variables numéricas son básicamente números. Pero hacemos una distinción clara entre dos tipos de números:

* Enteros : 0 | 1 | -1 | 203568 , etc...
* Flotantes: 0,23 | 1,0 | -0,3546 | etc..

>[!WARNING]
>
> Designer establece una distinción clara entre enteros y elementos flotantes : de forma predeterminada, no se pueden utilizar de forma conjunta.
> 
> Afortunadamente, puede utilizar los nodos *To Integer* o To Float para realizar conversiones de tipos.

### Varios valores numéricos en la misma variable

Dependiendo de sus necesidades, puede acumular hasta 4 valores numéricos dentro de la misma variable.

Una vez más, todos los valores deben ser del mismo tipo.

Para ello, puede elegir entre todos estos valores numéricos:

![](../../assets/image2015-12-18-14-10-36.png)

## Booleano

Un valor booleano es un valor binario puro, lo que significa que su valor solo puede ser *True* o *False* (también puede decir 0 o 1).
