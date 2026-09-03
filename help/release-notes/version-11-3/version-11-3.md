---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-11-3.html"
breadcrumb-title: ''
description: Consulte las notas de la versión 11.3 de Substance 3D Designer para obtener más información sobre las nuevas funciones, mejoras y correcciones de errores.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 11.3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versión 11.3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1284'
ht-degree: 1%

---


# Versión 11.3

**Substance 3D Designer**

Fecha de publicación: *24 de noviembre de 2021*

## Función principal

### Nuevas funcionalidades de gráficos de modelos

![](version-11-3.resources/version-11-3-01.jpg)

Se han añadido muchas mejoras al gráfico del modelo para ampliar las capacidades de modelado:

* <b>Nuevo flujo de trabajo de partículas</b>\
  El nuevo flujo de trabajo de modelado de partículas permite crear nubes de puntos para manipular la geometría. Se pueden utilizar para crear muchas formas nuevas, complejas o repetitivas, como las tejas de la imagen de arriba.\
  Para obtener más información sobre el nuevo flujo de trabajo de objetos, consulte las siguientes páginas de documentación:

  * Tipos de elementos de una escena
  * Partículas
  * Eliminación de partículas
  * Partículas de las instancias

  ![](version-11-3.resources/version-11-3-02.gif)

* <b>Nuevos nodos de modelado y deformación</b>\
  Se han añadido nuevos nodos adicionales para crear formas más complejas; haga clic en cada nodo para obtener más información sobre ellos:
  * Transformación generativa
  * Patrón orgánico
  * Torno
  * Recorte de curva

* <b>Mejoras generales\
  </b>El flujo de trabajo alrededor del gráfico de modelado se ha mejorado con:
  * Nuevos consejos sobre los parámetros de los nodos para que sean más fáciles de aprender.
  * La jerarquía del modelo 3D ahora se conserva al exportar en FBX
  * La asignación de material se puede exportar con los formatos de archivo OBJ y FBX.
  * Previsualice nodos intermedios en la ventana gráfica en modo de superposición.

### Interoperabilidad mejorada

![](version-11-3.resources/version-11-3-03.jpg)

Las acciones de envío se han ampliado, con dos nuevas posibilidades:

* **Enviar SBSM (archivo de modelo de substance) a Stager**\
  Los modelos 3D procedimentales ahora se pueden enviar a Stager y modificarse desde allí con los parámetros expuestos.

* **Recibir SBS/SBSAR de Sampler**\
  Ahora es posible recibir archivos de Substance generados por Sampler directamente en Designer.

### Miscelánea

![](version-11-3.resources/version-11-3-04.jpg)

Se han hecho varias mejoras en la calidad de vida:

* **Entradas relativas a las entradas**\
  Las entradas de gráficos establecidas en Relativo a entradas ahora heredarán el tamaño del nodo conectado en lugar del tamaño del gráfico principal predeterminado. Esto facilita la administración de diferentes resoluciones mediante entradas de diferentes tamaños.

  ![](version-11-3.resources/version-11-3-05.jpg){width="400px"}

* **Nueva ventana de gráfico**\
  La nueva ventana gráfica se ha rediseñado y ahora permite ver mejor los detalles de una plantilla específica y crear una nueva gráfica directamente en un paquete existente.

  ![](version-11-3.resources/version-11-3-06.png){width="400px"}

* **Cerrar todos los paquetes**\
  Una pequeña acción que hace menos tedioso administrar muchos paquetes en el explorador. Use **Archivo** > **Cerrar todos** para cerrar todos los paquetes abiertos actualmente.

  ![](version-11-3.resources/version-11-3-07.png)

* **Maximizar vista actual**\
  Use la nueva barra de título **icon** o el método abreviado **MAYÚS+Espacio** para expandir una ventana a pantalla completa. Esto también se puede usar en ventanas flotantes.

* **Mejoras en la vista 3D**\
  La vista 3D tiene nuevos ajustes de visualización para alternar la visualización de las caras traseras en un modelo 3D, así como la visualización de Vértices, Tangente y Bitangents.

### Contenido

![](version-11-3.resources/version-11-3-08.jpg)

Esta versión añade nuevos nodos de difusión y mejoras para el nodo de Renderización PBR:

* <b>Nodos de difusión</b>\
  Los nuevos nodos Color de difusión, Escala de grises de difusión y UV de difusión permiten generar desenfoques de sangrado suaves basados en una máscara de entrada.

  ![](version-11-3.resources/version-11-3-09.jpg){width="230px"}

  ![](version-11-3.resources/version-11-3-10.jpg) ![](version-11-3.resources/version-11-3-11.jpg)

* **Nodo de Renderización PBR mejorado**\
  Este nodo tuvo los siguientes cambios:
  * Nuevo modo UV cúbico para la forma Esfera.
  * Nueva compatibilidad con la dispersión subsuperficial.
  * La anisotropía ahora sigue el modelo Material de cadena de Adobe 5ASM).
  * La iluminación basada en imágenes se ha mejorado con el apoyo de la toma de muestras de importancia.
  * Se ha mejorado la iluminación emisiva con el apoyo de la toma de muestras de importancia.

## Notas de la versión

### 11.3.0

*(Publicado El 24 De Noviembre De 2021)*

**Agregado:**

* [Modelos de Substance] Añadir información sobre herramientas para parámetros de nodos
* [Modelos de Substance] Permite mostrar en superposición en la ventana gráfica 3D el resultado de un nodo intermedio
* [Modelos de Substance] Mejorar el modo en que se visualizan los Basis
* [Modelos de Substance] Conservar la jerarquía de objetos al exportar un gráfico de modelo de Substance a .fbx
* [Modelos de Substance] Compatibilidad con varios materiales en la exportación FBX/OBJ desde el gráfico del modelo de Substance
* [Modelos de Substance]&#x200B;[Contenido] Nodo de objeto
* [Modelos de Substance]&#x200B;[Contenido] Nodo Transformación generativa
* [Modelos de Substance]&#x200B;[Contenido] Nodo Organic Pattern
* [Modelos de Substance]&#x200B;[Contenido] Partículas del nodo Instancias
* [Modelos de Substance]&#x200B;[Contenido] Nodo de eliminación de partículas
* [Modelos de Substance]&#x200B;[Contenido] Torno nodo
* [Substance models]&#x200B;[Content] Nodo de shell
* [Modelos de Substance]&#x200B;[Contenido] Nodo de proyección
* [Modelos de Substance]&#x200B;[Contenido] Nodo de recorte de curva
* [Modelos de Substance]&#x200B;[Contenido] Actualizar el nodo Sampler de la curva
* [Modelos de Substance]&#x200B;[Contenido] Actualizar nodo Sampler de malla
* [Modelos de Substance]&#x200B;[Contenido] Actualizar el nodo Variación
* [UX] Botón para maximizar la vista actual
* [UX] Actualización de la ventana Nuevo gráfico
* [UX] Añada la opción &quot;Descargar reproductor&quot; en el menú Herramientas y agréguela con &quot;Localizar reproductor&quot;
* [UX] Añada la entrada &quot;Cerrar todo&quot; al menú de archivos
* [UX] Aplique un uso de mayúsculas y minúsculas uniforme en todo el menú principal
* [UX] Visualización automática de las propiedades de los elementos de gráfica duplicados
* [UX] Añada botones en la barra de herramientas del gráfico para desactivar el tamaño de pantalla constante para los títulos de fotograma, los comentarios y las ubicaciones
* [UX] Botones para copiar información de versiones al portapapeles en el cuadro de diálogo Acerca de
* [Materiales] Entradas relativas a las entradas
* [Contenido] Opción Añadir &quot;Mosaico&quot; en ruidos de Perlin 3D
* [Content] Nuevo nodo de proceso de difusión
* [Contenido] Nueva versión del nodo de Renderización PBR
* [Interoperabilidad] Recibir SBS y SBSAR de Sampler
* [Interoperabilidad] Enviar SBSM a Stager
* [Vista 3D] Añada una opción para desactivar el sacrificio de la cara posterior
* [Vista 3D] Añada una opción para mostrar el espacio de tangente de vértices
* [Explorador] Resalte el gráfico en el Explorador al hacer doble clic en el fondo de la vista de gráfico
* [Explorer] Quitar la opción &quot;Explorar&quot; en los menús contextuales
* [Panaderos] Ocultar panaderos obsoletos
* [Gestión de color] Añadir compatibilidad con las reglas del archivo de configuración de OCIO v2
* [Biblioteca] Cambiar el nombre de las categorías según los tipos de gráficos
* [Preferencias] Desactive automáticamente la CPU en las preferencias de hardware de Iray si se detecta una GPU CUDA compatible

**Corregido:**

* [Modelos de Substance] Bloqueo en Mac al utilizar la opción &quot;as sudb&quot; en .fbx
* [Modelos de Substance] Bloqueo al exportar a SBSM en un caso específico
* [Modelos de Substance] Error de exportación al exportar parámetros expuestos cuyos widgets nunca se han creado
* [Modelos de Substance] Bloqueo aleatorio al abrir un gráfico que hace referencia a varios archivos .fbx
* [Modelos de Substance] Los rangos no se aplican dinámicamente en los widgets de los parámetros expuestos
* [Modelos de Substance] La opción Volver a cargar malla no funciona en los recursos utilizados en el gráfico de modelos de Substance
* [Modelos de Substance] Las escenas no se muestran en una vista 3D disponible en un caso específico
* [UI] El área de desactivación es demasiado grande en las opciones de material
* [UI] Problema de estilo en el cuadro de diálogo &quot;Archivo de paquete no guardado&quot;
* [UI] La tecla de tabulación se debe presionar dos veces para desplazarse por los valores
* [UI] El zoom con la acción de arrastrar del ratón se invierte entre la vista 3D y otras ventanas gráficas
* [UI] Al cargar un SBS ya abierto mediante la lista &quot;Archivos recientes&quot;, se activa incorrectamente el mensaje &quot;Paquete no encontrado&quot;
* [UI]&#x200B;[macOS] Diseño de interfaz predeterminado incorrecto después de iniciar la aplicación
* [UI] Los paquetes no se pueden guardar en la raíz de una unidad (solo Windows)
* [Graph] La opción &quot;Mostrar automáticamente en vista 2D&quot; no es coherente en un caso específico
* [Graph] La opción &#39;Open Reference&#39; está disponible para los nodos de instancia SBSAR
* [Graph] Las propiedades de posicionamiento solo se muestran cuando se crea el elemento
* [Graph] Las reglas de las cadenas de pines se aplican de forma incoherente
* [Graph] Bloqueo al guardar un gráfico vacío
* [Vista 3D] El ángulo de Anisotropía se invierte en el sombreador de ASM
* [Vista 3D] Sombreado de ASM: problemas de linealización con mapas relacionados con SSS
* [Vista 3D] Se ha roto el procesamiento de OpenGL después de cerrar vistas 3D adicionales en un caso específico
* [Vista 3D] Las posiciones predefinidas de las cámaras no son correctas en la vista 3D con algunos archivos .fbx
* [MDL] La opción Añadir nodo del menú contextual no funciona con gráficos MDL.
* [MDL] Error: La conexión del nodo falla cuando se usan componentes float2.x y similares (SD 11.1.2)
* [MDL] Bloqueo al abrir un archivo específico .sbs
* [MDL] Las unidades de escena por metro en Irán no se configuran al iniciar la sesión de procesamiento
* [MDL] Se congela al retocar un nodo de alabeo en el gráfico MDL.
* [MDL] Orden de los parámetros en el código MDL exportado
* [Explorer] Se crea una carpeta de recursos vacía después de cancelar la creación de recursos
* [Explorer] Solo se puede mover el primer elemento de un paquete al final de la lista
* [Contenido] RT Bent Normal y RT AO activan el cálculo de nodos en gráficos anidados
* [Nodo de entrada] El mapa de bits de los nodos de entrada no se actualiza cuando cambia el UDIM
* [Iray] Se tarda mucho tiempo al intentar mostrar una escena de modelos de Substance con muchas instancias
* [Preferencias] Línea vacía al cancelar la adición de un archivo de proyecto
* [Editor de Python] La opción &quot;Cerrar&quot; permanece habilitada después de cerrar el último script y sigue incluyendo su nombre æ
