---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/fxmaps/the-iterate-node.html"
breadcrumb-title: ''
description: Utilice el nodo iterar de FXMaps para crear patrones repetidos y variaciones de procedimiento en los materiales.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Iterate Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: El nodo iterado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# El nodo iterado

El nodo iterar permite multiplicar las imágenes de un nodo de cuadrante y es esencialmente un nodo &quot;repetidor&quot;. Un nodo cuadrante a una profundidad de 1 normalmente generaría 4 cuadrantes. El nodo iterar le permite repetir sus imágenes de salida tantas veces como desee, con cada conjunto de repeticiones tratadas por separado.

El nodo iterar no tiene otras propiedades aparte de &quot;¿Qué repeticiones desea?&quot; parámetro. El resultado es que las nuevas imágenes se superponen, de forma predeterminada, a las creadas por el nodo Cuadrante y se fusionan con ellas.

El nodo de iteración repite la imagen de entrada recibida. El número de repeticiones se define mediante su propiedad Iterations:

La clave para utilizar el nodo iterar es que también se procesarán las funciones dinámicas asociadas a cada imagen repetida. Esto significa que cada repetición puede tener su propio conjunto de ajustes únicos. Puede utilizar la propiedad Raíz aleatoria del nodo Iteración para modificar cómo funciona esto. También puede tener acceso a la variable de sistema *$number* dentro de las funciones dinámicas para determinar qué repetición se está procesando actualmente y modificar el resultado de la función en consecuencia.

Por ejemplo: si aplica una rotación aleatoria a cada imagen de un nodo Cuadrante y, a continuación, proporciona la salida de ese nodo Cuadrante a la entrada activa de un nodo iterado, cada una de las imágenes repetidas también tendrá su propia rotación aleatoria.

Todas las mismas características dinámicas disponibles en el nodo Cuadrante también se aplican a las imágenes repetidas producidas por el nodo Iteración. Es como si el nodo duplicara el nodo Cuadrante en el mismo nivel, en lugar de agregar otro nivel de profundidad.

## El conector de paso

Cada nodo iterado tiene dos conectores a lo largo de su base. El conector izquierdo es un conector de acceso directo. La imagen que recibe se pasa directamente al conector de salida del nodo, donde se mezcla con cualquier imagen repetida:

Tenga en cuenta que la imagen de paso siempre pasa intacta, independientemente de la configuración del parámetro Iteración.

![](the-iterate-node.resources/iterate.jpg)
