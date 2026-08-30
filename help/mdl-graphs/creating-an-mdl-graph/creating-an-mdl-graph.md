---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: Aprenda a crear gráficos de Lenguaje de definición de material en Substance 3D Designer para la creación de material personalizado.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Creación de un gráfico MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Creación de un gráfico MDL

Esta página describe el proceso de creación de un gráfico MDL para crear materiales MDL en Substance 3D Designer.

![Rutas de creación de gráficos MDL](creating-an-mdl-graph.resources/mdl-new-graph-hl.png "Rutas de creación de gráficos MDL")

*Rutas para crear un nuevo gráfico MDL en la interfaz de Designer*

## Métodos para crear un gráfico MDL

Puede crear un gráfico MDL mediante cualquiera de los métodos siguientes:

* Seleccione la opción **Archivo > Nuevo > Gráfico MDL** en la *barra de menú principal*
* Haga clic en el botón ![](creating-an-mdl-graph.resources/mdl-new-graph-icon.png) **Agregar gráfico MDL** en la *barra de herramientas principal*
* Haga clic con el botón derecho en un *paquete existente* en el panel **Explorador** y seleccione la opción **Nuevo > Gráfico MDL**

Se le mostrará el cuadro de diálogo **Nuevo gráfico MDL**, consulte a continuación.

![Cuadro de diálogo Nuevo gráfico MDL](creating-an-mdl-graph.resources/mdl-templates.png "Cuadro de diálogo Nuevo gráfico MDL")

*Cuadro de diálogo Nuevo gráfico MDL*

## Cuadro de diálogo Nuevo gráfico MDL

Independientemente del método utilizado para crear un nuevo gráfico MDL, siempre aparecerá el cuadro de diálogo <b>Nuevo gráfico MDL</b>, que le permite configurar el nuevo gráfico.

### Plantillas

La sección <b> plantillas</b> le permite seleccionar una plantilla de gráfico, que incluye nodos preconfigurados para comenzar a trabajar con el gráfico más rápido. Los nodos preconfigurados incluyen nodos de salida, nodos simples para pasar valores a estas salidas, por ejemplo, Color uniforme y nodos de entrada en función de la plantilla.

Para comenzar desde un gráfico *vacío* completo, selecciona la plantilla <b>Vacío</b>.

La opción <b>Project</b> le permite filtrar la lista de plantillas por archivo de proyecto. Esto facilita la búsqueda de las plantillas personalizadas en las ubicaciones agregadas en la sección <b>General</b> de la configuración del proyecto para el archivo de proyecto.

>[!WARNING]
>
> Si selecciona la plantilla incorrecta, *no puede* cambiar a una plantilla diferente después de crear el gráfico.\
> Para trasladar el gráfico existente a otra plantilla, puede crear un nuevo gráfico utilizando la plantilla adecuada y copiar y pegar el gráfico en el nuevo. Vuelva a conectar los nodos según corresponda, incluido el nodo [Root](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md).

La lista de plantillas se puede mostrar en diferentes modos mediante *botones* junto al cuadro combinado **Proyecto**:

* **![](creating-an-mdl-graph.resources/mdl-template-recent-icon.png)Mostrar usado recientemente**: filtra la lista para mostrar las últimas plantillas utilizadas en orden de *más recientes a menos recientes*, siendo el elemento superior el más reciente
* **![](creating-an-mdl-graph.resources/mdl-template-graphs-icon.png)Mostrar gráficos**: las plantillas se muestran por su *solo etiqueta*, en el orden de los archivos [Substance 3D](https://www.adobe.com/es/products/substance3d/3d-augmented-reality.html) del directorio de plantillas
* **![](creating-an-mdl-graph.resources/mdl-template-packages-icon.png)Mostrar archivos de Substance 3D**: las plantillas se muestran por su etiqueta como *elementos secundarios del archivo de Substance 3D al que pertenecen*, en el orden de los archivos del directorio de plantillas
* **![](creating-an-mdl-graph.resources/mdl-template-directory-icon.png)Mostrar directorios**: las plantillas se muestran en su etiqueta como *elementos secundarios del directorio al que pertenecen*, en el orden de los archivos del directorio de las plantillas

### Propiedades

La sección <b>Propiedades de gráfico </b> le permite configurar información básica sobre el nuevo gráfico. Cualquiera de estas opciones se puede cambiar posteriormente en cualquier momento, pero tiene sentido prestar atención al principio y configurarlas de forma adecuada para su caso de uso.

* <b>Nombre del gráfico</b>: el identificador del gráfico. Debe ser único para un paquete determinado y no puede incluir espacios ni algunos caracteres especiales.
* <b>Crear gráfico en el paquete</b>: Puede usar este cuadro combinado para crear un *nuevo* paquete para el nuevo gráfico o agregar el nuevo gráfico a cualquier *paquete* existente ya cargado en el panel Explorador.\
  Nota: Si el proceso de creación se inicia mediante el método <b>4</b> (ver arriba), este parámetro es *preset* para el paquete existente desde el que se inició el proceso.
* <b>Detalles de la plantilla</b>: esta sección proporciona un breve texto que explica las características y el propósito de la plantilla
