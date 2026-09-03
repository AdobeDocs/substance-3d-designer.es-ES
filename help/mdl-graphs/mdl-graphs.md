---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: Aprenda a crear y utilizar gráficos de lenguaje de definición de material en Substance 3D Designer para flujos de trabajo de materiales avanzados.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gráficos MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---


# Gráficos MDL

Esta página presenta gráficos MDL en Substance 3D Designer, que le permiten crear materiales MDL y previsualizar su comportamiento en tiempo real.

![Material de Malaquita MDL](mdl-graphs.resources/mdl-graphs-01.jpg "Material de Malaquita MDL")

*Malaquita con crisocola, material MDL de [Mark Foreman](https://www.artstation.com/oggyart)* *disponible en nuestro [Substance share heredado](https://share-legacy.substance3d.com/libraries/4043)* *plataforma*

>[!WARNING]
> 
> Los gráficos MDL y todas las funciones relacionadas se eliminaron de Designer en la versión 16.0.0.
> 
> Más información aquí: [Gráfico MDL y final de la vida útil de Iray](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++Tabla de contenido

* [Conceptos principales de gráficos MDL](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [Creación de un gráfico MDL](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [Biblioteca MDL](/help/mdl-graphs/mdl-library/mdl-library.md)
* [Exposición de parámetros en gráficos MDL](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [Gráficos de Substance y materiales MDL](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [Exportación de contenido MDL](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [Advertencias en gráficos MDL](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [Recursos de aprendizaje MDL](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## Información general

MDL significa [Lenguaje de definición de materiales](http://www.nvidia.com/object/material-definition-language.html): &quot;una tecnología desarrollada por [NVIDIA](https://www.nvidia.com/) para definir materiales basados en la física para soluciones de representación basadas en la física&quot;. (Fuente: [Documentación de NVIDIA MDL](https://raytracing-docs.nvidia.com/mdl/index.html))

Con este lenguaje, una definición de material completa es portátil y, por lo tanto, se puede utilizar en aplicaciones y procesadores para obtener una salida coherente. Substance 3D Designer es actualmente la *única* aplicación que ofrece creación nodal basada en gráficos de materiales MDL, al exponer las funciones MDL y los tipos de valor como nodos en un gráfico MDL.

Al crear materiales, puedes usar el propio procesador [Iray](../interface/3d-view/iray/iray.md) de NVIDIA, incrustado en Designer y disponible en el panel [Vista 3D](../interface/3d-view/3d-view.md), para obtener una vista previa del comportamiento del material *de forma interactiva*.

Los gráficos MDL son complementarios de los [gráficos de Substance](../compositing-graphs/substance-compositing-graphs.md), ya que estos últimos generan *texturas* que el material MDL puede *muestrear* para afectar a su comportamiento y apariencia.

Sugerimos revisar las secciones de esta documentación *en orden* para obtener una ruta de aprendizaje guiada, comenzando por las propiedades de un recurso de gráfico MDL, justo debajo.\
¿Estás ansioso por saltar? Comience con los gráficos MDL en la sección de recursos de aprendizaje MDL.

>[!NOTE]
>
> Puede obtener más información sobre la implementación técnica del lenguaje de definición de materiales en la [Documentación de NVIDIA MDL](https://raytracing-docs.nvidia.com/mdl/index.html), que incluye vínculos a la especificación MDL y al [Manual MDL](http://mdlhandbook.com/), todos creados y mantenidos por NVIDIA.

![Propiedades de gráfico MDL](mdl-graphs.resources/mdl-graphs-02.png "Propiedades de gráfico MDL")

*Propiedades de gráfico MDL en el panel Propiedades*

## Propiedades del gráfico MDL

### Atributos

Esta sección incluye información sobre el material de MDL para los propósitos de identificación, clasificación y establecimiento de la autoría.

* <b>Identificador</b>: El nombre de este recurso, que debe ser único bajo su elemento principal en el paquete
* <b>Nombre para mostrar</b>: El nombre del material MDL que se muestra en la interfaz
* <b>Icono</b>: La imagen utilizada como miniatura de este gráfico en la biblioteca de Designer
* <b>Oculto\*</b>: Cuando se establece en* True*, el material MDL no está visible en una biblioteca MDL, pero aún existe internamente y se puede hacer referencia a él
* <b>Mostrar en biblioteca</b>: Cuando se establece en *True*, el gráfico MDL se muestra en la biblioteca de Designer
* <b>Descripción</b>: La descripción del material MDL, que puede mostrarse en la información sobre herramientas de los nodos de instancia que hacen referencia a este gráfico.
* <b>Categoría\*</b>: La categoría a la que pertenece el gráfico MDL - esto actualmente no tiene ningún impacto en cómo se ordena el gráfico en la [Biblioteca](../interface/the-library/the-library.md) de Designer
* <b>En el grupo\*</b>: El grupo de bibliotecas al que pertenece el material MDL
* <b>Autor\*</b>: El autor del material de MDL
* <b>Colaboradores\*</b>: Los colaboradores del material de MDL que no sean el autor
* <b>palabras clave\*</b>: Las palabras clave que se pueden utilizar para encontrar el material MDL en una búsqueda de biblioteca
* <b>Aviso de copyright\*</b>: El aviso de copyright relevante para la autoría y uso del material de MDL

Nota: Las propiedades marcadas con un asterisco (\*) son anotaciones MDL que deben utilizar las integraciones de la biblioteca MDL y no tienen* ningún impacto* en Designer.

### Entradas de gráficos

En esta sección se enumeran los parámetros interactivos conectados a los parámetros expuestos del gráfico MDL y se definen sus *valores predeterminados*. Se pueden *reorganizar* y *reordenar* en cualquier momento.

La interfaz y el comportamiento de estas entradas están definidos por el *tipo de valor* y los *rangos* de los parámetros expuestos a los que están conectadas. Por ejemplo:

* Un valor expuesto del tipo <b>Float</b> establecido en un rango suave de [0.0,4.0] se mostrará como un *regulador único* entre 0.0 y 4.0
* Se mostrará un valor expuesto del tipo <b>Color</b> como *widget de color*, que incluye un degradado de selección y una miniatura de color

Para reordenar las entradas de gráficos, coloca el cursor en el *controlador oscuro* a la izquierda del parámetro, haz clic en *mantener presionado* <b>LMB</b> y arrastra el cursor hacia arriba o hacia abajo. Este orden personalizado se utilizará para mostrar las propiedades del material MDL en los siguientes contextos:

* Nodos de instancia que hacen referencia al gráfico MDL para este material
* Las propiedades de material en la [vista 3D](../interface/3d-view/3d-view.md)
* Integraciones de MDL de terceros
