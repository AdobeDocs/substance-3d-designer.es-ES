---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/release-notes/version-12-2.html"
breadcrumb-title: ''
description: Consulte las notas de la versión 12.2 de Substance 3D Designer para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versión 12.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---


# Versión 12.2

<b>Substance 3D Designer 12.2</b> ofrece compatibilidad nativa con las máquinas Apple Silicon (M1), algunas mejoras para los gráficos de modelos de Substance y otras actualizaciones pequeñas. Esta página describirá todos los detalles relativos a esta nueva versión.

Fecha de publicación: *19 de julio de 2022*

![](../../assets/final3.png)

## Funciones principales

### Soporte nativo para chips Apple Silicon (M1)

La versión 12.2 de Designer es la primera con el soporte nativo completo de los nuevos equipos Apple basados en el chip M1. Aunque Designer podía ejecutarse técnicamente en dispositivos con Apple Silicon anteriormente, la compatibilidad nativa le ofrecerá una experiencia más rápida y eficaz. Como puedes ver en la imagen siguiente, los cálculos son *hasta dos veces más rápidos* con esta nueva versión en estos equipos.

![](../../assets/ds-perf-applem1.png){width="600px"}

### Mejoras en los gráficos de modelos de Substance

* <b>Información sobre herramientas en nodos\
  </b>No siempre es posible explicar lo que hace un nodo con un solo icono y un título, por eso ahora tenemos información sobre herramientas con una *descripción completa del nodo* cuando estás en la biblioteca o en la vista de gráficos. Le ayudará a encontrar el nodo que está buscando o a entender mejor cuáles son sus capacidades. ![](../../assets/tootlipnode.png)

* <b>Métodos abreviados para la creación de nodos\
  </b>Para acelerar la creación de los nodos más utilizados, ahora puede definir sus propios métodos abreviados en Preferencias, como para los otros tipos de gráficos.![](../../assets/shorcuts.png)

* <b>Vista previa del nodo desde el menú contextual del nodo\
  </b>En nuestra última versión, hemos añadido la posibilidad de obtener una vista previa de un nodo en la Vista 3D gracias a un método abreviado de teclado (*MAYÚS + Clic* en un nodo). Esta característica ahora también está disponible en el *menú contextual del nodo* para que sea más detectable.

  ![](../../assets/previewnode.gif){width="600px"}
* <b>Búsqueda basada en la compatibilidad de nodos\
  </b>Cuando busca un nodo en el menú del nodo (accesible presionando *barra espaciadora* en la vista de gráficos), los nodos ahora se filtran correctamente para mostrar solo los que son *compatibles con el que está seleccionado* en el gráfico. Le ayuda a encontrar rápidamente el nodo que está buscando.

### Miscelánea

* <b>Mejoras de vista 2D</b>\
  Cuando en versiones anteriores era posible ver las salidas del gráfico en el Vista 3D a través del *menú contextual* del gráfico del Substance, no era posible ver una salida del gráfico en el vista 2D. Esta opción se ha añadido a este menú, con un submenú que muestra todas las salidas de gráficos que se mostrarán en la vista 2D.\
  El botón &quot;Ver resultados&quot; de la barra de herramientas vista 2D también se ha actualizado con una flecha abajo y una información sobre herramientas para que funcione mejor.\
  Y, por último, la opción &quot;Salidas automáticas de gráficas de visualización al cargar una gráfica&quot; en Preferencias se ha *dividido en dos configuraciones distintas* - para la vista 2D y la Vista 3D respectivamente - para que puedas controlar qué vista debe abrirse y rellenarse automáticamente al cargar una gráfica.

* <b>Plantilla CLO</b>\
  Para mejorar la interoperabilidad con el software CLO, hemos añadido una *nueva plantilla dedicada*. Añadirá automáticamente a tu gráfico todos los *metadatos* necesarios para importar correctamente tu material en CLO.

  ![](../../assets/clo.png){width="600px"}

* <b>Requisitos de la plataforma de referencia de VFX</b>\
  Cada año, la plataforma de referencia VFX publica una lista de herramientas y bibliotecas de versiones que se utilizarán en todos los programas para la industria de VFX para minimizar las incompatibilidades entre los programas. Como de costumbre, *actualizamos todas nuestras dependencias* para respetar todas estas recomendaciones.

## Notas de la versión

### 12.2.0

*(Publicado El 19 De Julio De 2022)*

<b>Agregado:</b>

* [Apple] Compatibilidad nativa con Apple Silicon (M1) (solo versión de Creative Cloud)
* [Gráfico de modelo de Substance] Mostrar información sobre herramientas de nodos en la vista de gráficos
* [Gráfico de modelo de Substance] Mostrar información sobre herramientas de nodos en la biblioteca
* [Gráfico de modelo de Substance] Añadir una entrada de menú contextual a los nodos de previsualización
* [Gráfico de modelo de Substance] Permite al usuario crear accesos directos para la creación de nodos
* [UI] Añada la opción &quot;Ver salida en vista 2D&quot; en el menú contextual del gráfico del Substance
* [UI] Dividir el ajuste &quot;Visualización automática de salidas&quot; en ajustes específicos de Vista 2D/Vista 3D
* [UI] Añada una flecha desplegable y la información sobre herramientas al botón &quot;Ver salida&quot; en la barra de herramientas Vista 2D
* [UI] Volver a escribir y reordenar elementos en el panel Información del Explorador
* [Gestión de color] Añadir espacios de color de exportación &quot;Linear Adobe RGB (1998)&quot; y &quot;Adobe RGB (1998)&quot; para Adobe ACE
* [Gestión de color] Añadir espacio de color de trabajo &quot;Lineal Adobe RGB (1998)&quot; para Adobe ACE
* [Gestión de color] Añadir compatibilidad con pantallas OCIO ICC
* [Gestión de color] Ocultar el espacio de color de trabajo de Adobe RGB de las preferencias de ACE
* [Gestión de color] Mejora la calidad de las LUT 3D horneadas en modo ACE
* [Gestión de color] Uso del nuevo motor de GPU en el visor 3D
* [Localización] Actualización completa del idioma coreano
* [Motor] Actualizar a la versión 8.6.0
* [Graph] Asignar un identificador de gráfico predeterminado cuando la propiedad se deja en blanco
* [Biblioteca] Desactivar hipervínculos de información sobre herramientas para nodos que no son instancias
* [NewProject] Actualizar la resolución predeterminada
* [Templates] Agregar plantilla de CLO
* [API] Expone la propiedad defaultParentSize de los objetos SDSBSCompGraph
* [Dependencias] Actualizar Alembic a la versión 1.8.3
* [Dependencias] Actualice AXF a la versión 1.9.0
* [Dependencias] Actualizar Boost a la versión 1.76
* [Dependencias] Actualice FBX a la versión 2020.2.1
* [Dependencias] Actualice IRay a la versión 2021.1.0
* [Dependencias] Actualice OpenColorIO a la versión 2.1.1
* [Dependencias] Actualizar el OpenEXR a la versión 3.1.5
* [Dependencias] Actualizar TBB a la versión 2020.3
* [Dependencias] Actualizar USD a la versión 0.2.3
* [Quitar] Desactivar la función de efectos posteriores (Yebis)
* [Quitar] Quitar el comando &quot;Guardar procesamiento en Artstation&quot; del menú Vista 3D

<b>Corregido:</b>

* [Modelos de Substance] El rango definido en el parámetro expuesto se guarda al dejar de exponer
* [Modelos de Substance] El identificador no es fácil de usar en nodos constantes
* [Modelos de Substance] Mejora la búsqueda en función de la compatibilidad de nodos
* [UI] El orden del submenú &quot;Nuevo&quot; es incorrecto para los recursos de carpeta
* [UI] El tamaño predeterminado de la ventana principal es muy pequeño
* [UI] Las barras de herramientas no se ven afectadas por la opción Restablecer diseño
* [UI] Cuadrícula de transparencia visible en el icono de recurso de fuente en el Explorador
* [Cooker] Los gráficos de Substance que aparecen en el gráfico MDL siempre se vuelven a guardar por completo
* [Graph] Bloqueo al pegar un nodo copiado de un gráfico con identificador en blanco
* [MDL] Bloqueo al cerrar un gráfico MDL específico
* [Performance] La aplicación no responde cuando se cargan paquetes muy grandes
* [Resources] Los recursos de escena 3D se pueden importar en un caso específico
