---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/all-changes.html"
breadcrumb-title: ''
description: Revisa todos los cambios y actualizaciones en las versiones de Substance 3D Designer para realizar un seguimiento de la evolución y las mejoras de las funciones.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > All changes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Todos los cambios
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49d7d426f1b687cf6087bb1c9735a9060af48041
workflow-type: tm+mt
source-wordcount: '32039'
ht-degree: 0%

---


# Todos los cambios

## Versión 16

### 16.0.5

*(Lanzado el 26 de agosto de 2026)*

**Agregado:**

* [Vista 3D] Se ha añadido un botón para seleccionar el archivo AOV actual
* [Contenido] Ruido Perlin/Gaussiano: desabrochar parámetro de escala
* [Contenido] Ocultar recursos de mapa de bits innecesarios de la biblioteca
<!--
* &#91;Legal&#93; To meet generative AI transparency legal requirements, this version is updated to automatically attach Content Credentials to qualifying content created or edited with generative AI tools.  
-->

**Corregido:**

* [Vista 3D] Los cambios de visibilidad del entorno realizados en OpenGL no se transfieren a los procesadores Eclair
* [Panaderos] El contexto de panificación no se destruyó después de actualizar los pasteles para un recurso de mapa de bits UDIM eliminado
* [Bakers] Se ha corregido un bloqueo al eliminar un recurso de mapa de bits UDIM mientras se actualizaban sus pasteles
* [Contenido] Forma salpicadura v2: el height de forma de cilindro no es correcto
* [Contenido] Forma salpicadura v2: El mapa de densidad no funciona correctamente cuando el tamaño del nodo supera 4096
* [Contenido] Forma salpicadura v2: el uso del SDF &quot;Rock&quot; detrás de un If/Else puede conducir a un bucle infinito
* [Seguridad] Se ha corregido una vulnerabilidad de referencia de puntero NULO en el análisis de archivos AXF
* [Seguridad] Se ha corregido una vulnerabilidad de desreferencia de puntero NULO en el análisis de archivos GLB
* [Seguridad] Se han corregido las vulnerabilidades de escritura fuera de límites en el análisis de archivos SBSAR
* [Seguridad] Se ha corregido una vulnerabilidad de daños en el montón en el análisis de archivos DDS
* [Seguridad] Se ha corregido una vulnerabilidad de daños en el montón en el análisis de archivos GLB
* [Seguridad] Se ha corregido una vulnerabilidad de daños en el montón en el análisis de archivos TGA
* [Seguridad] Se ha corregido una vulnerabilidad de daños en el montón en el análisis de archivos de TIFF
* [Seguridad] Se ha corregido una vulnerabilidad de daños en el montón en el análisis de archivos USDA
* [Seguridad] Se ha corregido una vulnerabilidad de daños en el montón en el análisis de archivos WEBP
* [UI] El cuadro de diálogo de elementos en los menús de la casilla de verificación persistente solo abarca el texto del elemento


### 16.0.4

*(Publicado el 2 de julio de 2026)*

**Agregado:**

* [Vista 3D] Fijar la resolución de procesamiento a 4096 en X e Y
* [Panaderos] Actualice bake-sdk a 3.22.3.
* [Motor] Actualice el motor del Substance a la versión 9.4.4
* [OpenGL] [OpenPBR] Reducir el ruido en el lóbulo del specular para obtener una mayor rugosidad + anisotropía
* [Escenas] Conservar el modo de interpolación UV principal

**Corregido:**

* [Vista 3D] Exportación de USD: las rutas de acceso de los recursos se almacenan con rutas absolutas
* [Panaderos] La cocción falla cuando se cancela la carga de malla de polietileno alta (Windows)
* [Bakers] La lista de escenas 3D de alto poli no incluye recursos con el mismo identificador que el de bajo poli
* [Panaderos] Espacio mundial normal: Siempre se devuelve una normal WS cuando hay una normal de entrada
* [Contenido] Normal incorrecta al escalar el patrón de forma no uniforme en Shape Splatter V2
* [Contenido] Forma salpicadura V2: Reglas negras para las formas &quot;Plano&quot; y &quot;Disco&quot;
* [Contenido] Forma salpicadura v2: la primera forma no se mezcla correctamente con el fondo
* [Bloqueo] Bloqueo aleatorio posiblemente vinculado a vídeo (información enriquecida sobre herramientas)
* [Graph] Bloqueo al pegar un nodo copiado de un nuevo gráfico con un identificador en blanco
* [PSD] Los archivos de PSD se cargan demasiadas veces

### 16.0.3

*(Publicado El 29 De Mayo De 2026)*

**Corregido:**

* [Bloqueo] Se ha corregido una regresión introducida en la versión 16.0.2 que provocaba un bloqueo al iniciarse para algunos usuarios.

### 16.0.2

*(Publicado El 28 De Mayo De 2026)*

**Agregado:**

* [OpenPBR] Añadir compatibilidad para constantes de color base/AO

**Corregido:**

* [Vista 3D] Pérdida de VRAM en el rastreador de rutas de GPU cuando se activa el desplazamiento
* [Vista 3D] El subproceso principal permanece ocupado cuando existe la vista 3D
* [Vista 3D][OpenPBR] OpenGL: Los widgets de &#39;Grosor&#39; parecen estar sujetos, pero aceptan valores fuera de rango
* [Bloqueo] Bloqueo al mover la entrada de referencia más de un lugar a la vez
* [Crash] Bloqueo al desmaximizar una ventana
* [Crash] Bloqueo al escribir TARGA o BMP desde el panadero
* [Bloqueo] Bloqueo aleatorio al mostrar la vista 3D
* [Graph] Orden incorrecto de los pines de E/S al mover E/S después de editar los identificadores
* [Linux] [Exportar] Los cuadros de diálogo &quot;Publish sbsar&quot; y &quot;Enviar a&quot; no añaden la extensión de archivo

### 16.0.1

*(Publicado El 5 De Mayo De 2026)*

**Agregado:**

* [Muestras] Añadir una muestra de material dedicada a SDF / Shape Splatter
* [Contenido] Visor 3D: Cambiar el estado predeterminado
* [Contenido] Visor 3D: Añadir entorno predeterminado
* [Contenido] Asignador de salpicaduras de formas v2: Añadir parámetro de centro de proyección por eje para la asignación triplanar
* [Contenido] Asignador de salpicaduras de formas v2: Añadir parámetro de segmentación
* [Contenido] Forma salpicadura v2: Habilitar extrusión de forma predeterminada
* [3DView] Compatibilidad con las GPU Intel Panther Lake en el trazador de trazados
* [Vista 3D] Mejorar el formato de las sugerencias emergentes de Desplazamiento
* [Motor] Actualizar a Substance Engine v9.4.3
* [OpenPBR] geometry_tangent: agregar compatibilidad para constantes
* [Preferencias] Añada una opción para que TGA/BMP escriba el canal alfa si es completamente opaco
* [ThirdParty] Actualización a &quot;Adobe Color Engine&quot; (ACE) 7.0
* [UI] Hacer que la ventana Administrador de complementos sea siempre visible (modal)

**Corregido:**

* [Vista 3D] La escala de la ventana gráfica se aplica al utilizar una resolución fija
* [Vista 3D] [OpenPBR] Bloqueo al cargar una escena GLTF exportada de Designer y utilizar un material de OpenPBR
* [Vista 3D] [OpenPBR] Los materiales exportados de Painter no se pueden reemplazar en Designer
* [Contenido] Visor 3D: shape.id no se ha inicializado y genera mensajes en la consola
* [Contenido] Escala de grises del asignador de salpicaduras de formas v2: La entrada de patrón 4 no se utiliza en la proyección triplanar
* [Contenido] Asignador de salpicaduras de formas v2: El ID de SDF se desfasa -1 al utilizar el modo &quot;1 imagen por ID de material&quot;
* [Eclair][USD] Resultado incorrecto al aplicar un material en un USD generado por Designer
* [Motor] Cálculo de un nuevo nodo de niveles Forma salpicadura V2 gráfico principal codificado después de los cálculos
* [Motor] El módulo de una variable frente a su valor igual no devuelve 0 con el motor de GPU en algunos casos
* [Motor][Contenido] La tangente de arco 2 devuelve 0 o Pi para vectores de X derecha en un caso específico
* [Engine][Ubuntu][SSE2] Bloqueo al cargar SBSAR específico en el gráfico
* [Graph] Bloqueo al conectar la salida del procesador de valores a la entrada de mapa de bits
* [Graph] Bloqueo al conectar valor a la entrada de imagen en algunos casos
* [Graph] El gráfico se calcula automáticamente en cada autoguardado cuando se usan mapas con bake
* [GraphRender] Bloqueo al conectar la salida de valor del Atlas scatter a la entrada de imagen del Atlas splitter
* [Linux] [Exportar] El formato de archivo editado se omite en los cuadros de diálogo de guardado de archivos
* [Mac] [Steam] Aparece un mensaje emergente de seguridad al iniciar Designer
* [Malla] Los materiales OBJ no se importan correctamente
* [PSD] El importador de PSD solicita extraer capas del archivo de PSD en cada autoguardado

### 16.0.0

*(Publicado El 14 De Abril De 2026)*

**Agregado:**

* [Contenido] Nodo de salpicaduras de formas v2
* [Contenido] Nódulos de color/escala de grises del asignador de salpicaduras de formas v2
* [Contenido] Salpicadura de forma v2 en nodo de máscara
* Nodos de Atlas de cuadrícula de [Content]
* [Content] Nodo del visor 3D
* [Contenido] Nodos de operador 3D SDF
* [Contenido] Nodos simples de 3D SDF
* [Contenido] Nodos de transformación de 3D SDF
* [Contenido] Nodos de materiales 3D SDF
* [Contenido] Ángulo al nodo vectorial
* [Content] Nodos de valor constante
* [Vista 3D] Sombreado de OpenPBR para el procesador OpenGL
* [Vista 3D] Sombreador de OpenPBRs para procesadores Rasterizer y Trazador de ruta de GPU
* [Vista 3D] Ventana de Desplazamiento para definir la escala de height, el nivel de height y la teselación
* [Vista 3D] Reorganizar los elementos de la barra de herramientas
* [Vista 3D] Establezca OpenPBR como modelo de material predeterminado en la vista 3D
* [Vista 3D] Haga que la vista 3D tenga en cuenta el atributo de gráfico &quot;Modelo de material&quot;
* [Vista 3D] Sincronizar modelos de material al cambiar entre los procesadores Rasterizer/Trazador de ruta de GPU y OpenGL
* [Vista 3D] Asegúrese de que el modelo de material sea persistente al cambiar de procesador 3D y de que los cambios en la definición de materiales estén sincronizados
* [Vista 3D] Trazador de ruta de GPU: Habilitar el ciclo de píxeles de ruido azul
* [Vista 3D] Exponer control de opacidad de oclusión ambiental
* [Vista 3D] Establecer el intervalo de parámetros de segmentación en [0, 10] para todos los sombreadores
* [Vista 3D] Cambiar el nombre de la acción &quot;Enfoque&quot; a &quot;Marco&quot;
* [Vista 3D] Controle el nuevo parámetro refineLevel que reemplaza a tessellationFactor
* [Vista 3D] Agregar contador FPS
* [Vista 3D] Mueva la barra de progreso en la misma barra de herramientas horizontal que el espacio de color de la parte inferior
* [Bakers] Muestra la UV del baker seleccionado en la vista previa
* [Graph] Añada el nuevo atributo &#39;Modelo de material&#39; a los Substance
* [NewGraph] Agregar separadores en la vista de miniaturas
* [Parámetros] Defina el valor de constante predeterminado para los parámetros de entrada con el editor &#39;Function&#39;
* [Parámetros] Rellenar el cuadro combinado de parámetros de nodo `Set` y `Is defined` con variables disponibles
* [Preferencias] Eliminación de la opción obsoleta &quot;Desescalar factor&quot; en la ficha &quot;Vista 3D&quot;
* [Publish] Cuadro de diálogo de Publish: Incluir modelo de material en la información del gráfico
* [Python] Agregue la nueva clase SDMaterialModelDescription para obtener la información de un modelo de material
* [Python] Permite obtener o establecer la propiedad de modelo de material de los objetos SDSBSCompGraph
* [Editor de Python] Aumentar tamaño de fuente a 12
* [Plantillas] Añadir plantillas de OpenPBR
* [Templates] Convertir muestras de material en OpenPBR
* [ThirdParty] Actualizar Boost a la versión 1.88
* [ThirdParty] Actualizar la API de C++ a C++20
* [ThirdParty] Actualizar NGL a 1.42
* [ThirdParty] Actualizar oneTBB a la versión 2022.x
* [ThirdParty] Actualice OpenColorIO a la versión 2.5.x
* [ThirdParty] Actualizar el OpenEXR a la versión 3.4.x
* [ThirdParty] Actualice Qt y QtForPython a 6.8.x y Python a 3.13.x
* [ThirdParty] Actualizar TBB a oneTBB 2021.x
* [Rechazo] Eliminar Iray y el Editor MDL

**Corregido:**

* [Vista 2D] El intervalo de selección del histograma no se conserva cuando la anchura del widget se vuelve pequeña
* [Exportación 3D] Las mallas exportadas desde Designer no se procesan igual en usdview
* [Vista 3D] Al asignar elementos que no son de audio a la vista 3D, se deja el modo de procesamiento de un solo azulejo
* [Vista 3D] Resultado de sujeción al utilizar OCIO
* [Vista 3D] Bloqueo al aplicar una textura de gráfico a un material no modificado para una escena específica
* [Vista 3D] Bloqueo al crear búferes de fotogramas
* [Vista 3D] Trazador de ruta de GPU Eclair: Geometría rota y bajo rendimiento al renderizar un modelo específico
* [Vista 3D] Transformación de textura incorrecta para escenas específicas
* [Vista 3D] Encuadre incoherente de la escena/selección al utilizar una resolución de procesamiento fija
* [Vista 3D] Color difuso incorrecto al procesar un determinado archivo GLTF
* [Vista 3D] Entorno invisible al cambiar de procesador en un caso específico
* [Vista 3D] Los materiales no se detectan correctamente al importar algunos archivos .fbx
* [Vista 3D] Al reemplazar materiales más de una vez, el mosaico se restablece en 1
* [Vista 3D] Las propiedades de la categoría &#39;UV&#39; no se guardan en archivos SBSCN
* [Vista 3D] La opción Restablecer y ver salidas en vista 3D de gráficos de una sola salida no restablece los materiales
* [Vista 3D] &quot;Guardar procesamiento&quot;: El formato de imagen editado no se conserva
* [Vista 3D] La selección no funciona en GPU AMD
* [Vista 3D] La escena 3D independiente no se actualiza cuando se modifica en el disco
* [Vista 3D] Algunas propiedades de material de color no se administran correctamente cuando se anulan
* [Vista 3D] Las texturas UDIM no se aplican correctamente en una malla específica
* [Vista 3D] La escena USD con material MaterialX ya no se procesa correctamente
* [Bakers] Se bloquea con algunas mallas
* [Panaderos] Transferencia de texturas: Bloqueo en bkBufferViewCopy
* [Cooker] Bucle infinito en el nodo de Bucle &quot;While&quot; en un caso que podría evitarse
* [Motor] Detener el motor del Substance al cerrar la aplicación
* [General] Evite el bloqueo aleatorio al salir de la aplicación (solo Windows)
* [Graph] Gráfico de funciones: la propagación de tipos no funciona correctamente en algunas situaciones
* [Graph] Los vínculos de gráficos se eliminan cuando se cambia el nombre de un nodo de entrada de imagen
* [Graph] Los vínculos y los bordes a veces muestran defectos
* [Preferencias] Se invierte la escala de la ventana gráfica
* [Propiedades] Bloqueo al modificar el ajuste de entrada de gráfico mientras se muestran los parámetros de instancia
* [Python] No se pueden importar módulos PySide6 (posible conflicto con la instalación PySide6 existente)
* [Python] Los módulos PySide y Shiboken existentes entran en conflicto con los módulos Designer
* [UI] El estilo de desplazamiento desaparece en los botones en casos específicos (solo Windows)
* [UI] El estilo del ratón sobre el vínculo no está visible en los botones desplegables al hacer clic (solo macOS)
* [UI] Botón &#39;Más información&#39; en &#39;?&#39; La información sobre herramientas no funciona cuando está fuera de los límites del cuadro de diálogo (solo Windows)

**Problemas conocidos:**

* [Graph] Los iconos generados para los gráficos de OpenPBRs no son precisos
* [Vista 3D] Las escenas con animaciones simples no se admiten correctamente
* [Vista 3D] El trazador de trazados no es compatible con todas las tarjetas gráficas AMD

## Versión 15

### 15.1.3

*(Lanzado El 10 De Marzo De 2026)*

**Agregado:**

* [Bakers] Agregar macros de tamaño de salida para el nombre de archivo
* [Panaderos] Evite cargar la malla alta antes de hornear
* [Bakers] CLI: Actualizar la descripción de la opción &#39;output-size&#39; con macros de tamaño
* [Bakers] Convertir el formato de textura de entrada al formato solicitado
* [Bakers] Desactive la opción &quot;Mapa de desplazamiento&quot; cuando se marque &quot;Usar jaula&quot;
* [Bakers] Mostrar ya los mapas con bake cuando se vuelva a abrir la ventana del horno
* [Panaderos] Mantenga la ventana de cocción abierta hasta que todos los procesos de cocción se cancelen efectivamente
* [Bakers] Migración de la función BindTexture
* [Panaderos] [Configuración] Establezca el valor predeterminado del &#39;Modo de filtrado de nombres&#39; en &#39;Nombre principal (heredado)&#39;
* [Bakers] [Tooltip] Añada el valor &#39;Modo de filtrado de nombres&#39; al parámetro &#39;Match&#39; tooltip
* [Motor] Actualice el motor del Substance a la versión 9.3.4

**Corregido:**

* [Vista 3D] La opción Ver salidas en vista 3D no anula la asignación existente en gráficos con una sola salida
* [Vista 3D] No se pueden mostrar UV en algunos casos
* [Vista 3D] Las tangentes calculadas aparecen rotas para USD
* [Vista 3D] Bloqueo al abrir el menú Procesador
* [Bakers] No se puede establecer una distancia mayor que 1 cuando la opción &quot;Relativo a Bbox&quot; está desactivada
* [Panaderos] El panadero de color tarda demasiado en terminar en casos específicos
* [Panaderos] Color: Bloqueo al hornear Islas de UV
* [Panaderos] Los rangos de los parámetros de distancia y radio son demasiado estrechos cuando el valor es absoluto
* [Panaderos] Fallo al hornear desde tangentes de alto contenido polivinílico que faltan y bitangentes que no son necesarios
* [Bakers] Los colores del material no son correctos en la línea de comandos de baker
* [Panaderos] Múltiples mallas altas de polietileno se ignoran en algunas situaciones
* [Panaderos] Normal: Salida en negro al utilizar suavizado y difusión (solo macOS)
* [Bakers] La comprobación de ruta de mapa de desplazamiento informa de errores inesperados al utilizar recursos de paquete de mapa de bits
* [Bakers] La información sobre el mapa de desplazamiento es incorrecta
* [Panaderos] Colocar el recurso en una carpeta específica de la malla no funciona
* [Panaderos] Transferencia de texturas: El valor &#39;UV set&#39; no se restaura como estaba al volver a abrir la ventana de horno
* [Panaderos] Transferencia de texturas: Una entrada de escala de grises no genera una salida de escala de grises
* [Panaderos] La advertencia de panadero heredado deshabilitado no se borra al cambiar el origen de textura en el panadero de destino
* [Bakers] [UDIM] El mapa de desplazamiento solo se aplica a UDIM 1001
* [Graph] UDIM 1001 siempre se calcula independientemente del archivo UVT que se utilice

### 15.1.2

*(Publicado El 3 De Febrero De 2026)*

**Corregido:**

* Niveles [del motor]: Los valores de punto flotante siempre se fijan en [0, 1]
* [Bakers] La coincidencia de geometría por nombre principal (heredado) no funciona en las submallas
* [Panaderos] Color: Las ediciones de los colores de material en la interfaz de usuario se omiten
* [Vista 3D] [Panaderos] El archivo OBJ tarda mucho tiempo en cargarse

### 15.1.1

*(Publicado El 20 De Enero De 2026)*

**Agregado:**

* [Ejemplos] Agregue dos ejemplos para crear secciones para alimentar la herramienta de cinta de Painter
* [Motor] Actualizar a Substance Engine v9.3.2
* [Motor][Metal] Mejora de las prestaciones
* [Motor] La interpolación bilineal de texturas enteras ahora se realiza con mayor precisión (back-end de CPU)
* [Panaderos] Registre una advertencia si falta el color del vértice en la malla de alta densidad
* [Marca] Iconos de actualizar tipos de archivo
* [NewGraph] Aplique estilos de cursor encima en el icono (i) de los modos de vista &#39;Lista&#39;, &#39;Paquetes&#39; y &#39;Directorios&#39;

**Corregido:**

* [3DView] Las mallas UDIM ya no procesan un solo azulejo
* [3DView] Bloqueo cuando no se detecta renderDevice
* [Branding] Corrección de iconos para archivos .SBS en Linux
* [Content] RGB de la función HSL: Resultado incorrecto para casi 0 entradas
* [Graph] El generador de iconos/miniaturas de gráficos no funciona
* [Graph] Menú de nodos: los elementos agrupados sin miniatura no tienen sangría
* [Motor][Contenido] Color para enmascarar la versión 2: Artefactos en el motor SSE2 al utilizar el espacio de color de distancia Lab
* [Motor][Contenido] Color para enmascarar la versión 2: Artefactos en los motores de GPU arm64 al utilizar el espacio de color de distancia Lab
* [Motor] [Metal] Salida de irradiancia negra para nodo de Renderización PBR
* [Motor] [Mac] Resultado incorrecto en una función de procesador de píxeles en Metal
* [Motor] [Mac] Mejora la precisión de algunas instrucciones utilizadas en procesadores de píxeles en las GPU Apple Silicon M1/M2
* [Motor] El cambio de tamaño de las imágenes de entrada (o los recursos incrustados) ya no introduce artefactos de borde (back-end de CPU)
* [Motor] El filtro Niveles ya no fija sus valores de entrada de punto flotante al generar texturas 8I/16I (back-end de CPU)
* [Motor] Se ha corregido un error de FxMaps por el que las imágenes de entrada de escala de grises consumidas por los nodos de FxMaps podían muestrearse incorrectamente (back-end de la CPU).
* [Motor] Se han corregido algunos defectos en la versión de 1 inicialización del filtro Distancia (backends de GPU)

### 15.1.0

*(Publicado El 11 De Diciembre De 2025)*

**Agregado:**

* [NewGraph] Repaso de la nueva ventana gráfica
* [NewGraph] Agregar muestras de materiales y muestras avanzadas
* [NewGraph] Añada un nuevo atributo de gráfico para los datos de plantilla (categoría y subtítulo)
* [NewGraph] Opción Quitar formato de salida
* [Contenido] Añadir funciones hash
* [Contenido] Añadir tonemappers a functions.sbs
* [Contenido] Ruido anisotrópico v2: agregar formato de salida predeterminado, agregar desorden
* [Content] Aplicación de mayúsculas y minúsculas de oración a etiquetas de nodo y parámetros
* [Contenido] Puntos BnW 1 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] BnW spots 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] BnW spots 3 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Celdas 1,2,3,4 v2: añadir formato de salida predeterminado, sin soporte de mosaico, opciones de desorden
* [Contenido] Nubes 1 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Nubes 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Nubes 3 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Color para enmascarar v2
* [Contenido] Ruido direccional 1 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Ruido direccional 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Ruido direccional 3 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Ruido direccional 4 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Arañazos direccionales v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 1 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 3 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 4 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Dirt 5 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Degradado de Dirt v2: añadir formato de salida predeterminado, nuevas opciones de desorden
* [Content] Base de Suma fractal v2: agregar formato de salida predeterminado, desorden, sin compatibilidad con mosaicos
* [Contenido] Suma fractal 1,2,3,4 v2: agregar formato de salida predeterminado
* [Contenido] Ruido gaussiano v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Manchas gaussianas 1 y 2 v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Fibras sucias 1,2,3 v2: añadir formato de salida predeterminado, sin soporte de mosaico, opciones de desorden
* [Contenido] Ruido de humedad v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Nuevo nodo &quot;Ruido de humedad 2&quot;
* [Contenido] Ruidos: actualizar para agregar el formato de salida predeterminado
* [Contenido] Ruido de Perlin v2: agregar formato de salida predeterminado, sin compatibilidad con mosaicos
* [Contenido] Asignador de formas: agregar modo de filtrado
* [Contenido] Mapeador UV: agregar modo de filtrado
* [Contenido] Forma de onda 1 v2: usar formato de salida predeterminado + nuevas opciones
* [Contenido] Ruido blanco v2: usar formato de salida predeterminado, agregar opciones de distribución
* [Bakers] Muestra solo las UV de la malla seleccionada
* [Bakers] Añada una opción para seleccionar el método de coincidencia de geometría por nombre
* [Panaderos] Seleccione el panadero más cercano cuando se elimine un panadero
* [Panaderos] UDIM: definir una lista de azulejos UV para hornear
* [Panaderos] Actualice bake sdk a 3.15.4.
* [Vista 3D/Explorador de escenas] Evite seleccionar un elemento UsdPrimitive al hacer clic con el botón derecho en él
* [ColorManagement] Compatibilidad con ACES 2.0
* [Gráfica de composición] Permite definir un nodo de salida como &quot;Salida predeterminada&quot;
* [Cooker] Quitar advertencia en entradas no conectadas de instancias de función††
* [Funciones] Añadir operador isDefined
* [Graph] Agrupe los elementos por atributo &#39;group&#39; en el menú de nodos
* [Graph] Mejora la representación de miniaturas

**Corregido:**

* [Vista 3D] La textura de escala de grises L16 se muestra con un matiz rojo cuando se conecta al entorno o a baseColor
* [Vista 3D] Al cambiar el enlace de material de una escena sin material, se crea un nuevo material &quot;predeterminado&quot;
* [Vista 3D] Las normales calculadas no son correctas para mallas OBJ específicas
* [Vista 3D] El entorno personalizado de SBSSCN no está visible al cargar en Pathtracer
* [Vista 3D] Errores en la consola al girar un entorno desactivado
* El Specular level [Vista 3D] no se aplica correctamente
* [Vista 3D] El Specular edge color no funciona al utilizar el rasterizador de Eclair
* [Vista 3D] El material añadido por el usuario no se aplica en escenas predeterminadas
* [Vista 3D] [Panaderos] El color del material es demasiado oscuro una vez se ha anulado o al utilizar un panadero de &quot;Color&quot;
* [Vista 3D][Panaderos] No hay color de material del archivo FBX
* [Bakers] Los colores del material en los archivos FBX no se detectan correctamente
* [Bakers] La opción &#39;recompute\_tangents&#39; siempre es &#39;false&#39; en las exportaciones de ajustes preestablecidos de JSON
* [Bakers] CLI: Bloqueo al ejecutar el mismo panadero de forma consecutiva a través del archivo JSON
* [Bakers] La actualización del parámetro &#39;color-generator&#39; no funciona para &#39;Grayscale&#39;
* [Contenido] Enmascarar trazados: Error en las proporciones no cuadradas
* [Contenido] Procesador de Renderizaciones PBR/iconos: Lóbulo de specular incorrecto
* [Contenido] Trazados a spline: Establezca el &#39;Tamaño de salida&#39; en &#39;Relativo al principal&#39; de forma predeterminada.
* [Contenido] Lista de puntos: Los puntos no están en el orden correcto cuando la textura de los datos no es cuadrada
* [Contenido] Asignador de splines: Error de línea de 1px en casos aleatorios
* [Contenido] Asignador de splines: UV estirados en algunos casos cuando el thickness es 0
* [Graph] Bloqueo al eliminar la salida de un subgráfico de función
* [Graph] El tipo de color del nodo de entrada se puede cambiar en paquetes de solo lectura
* [Graph] La entrada principal se puede cambiar en paquetes de solo lectura
* [Propiedades] El color del widget de previsualización de color no coincide con el estado del botón sRGB
* [Scene] No se puede cargar un archivo OBJ de más de 2 GB
* [UI] Los estados de acoplamiento de la consola y el administrador de dependencias no se restauran después de reiniciar

### 15.0.3

*(Publicado El 23 De Octubre De 2025)*

**Corregido:**

* [Contenido] La vista previa de los nodos de Herramientas de spline no se muestra de forma predeterminada
* [Graph] Bloqueo al eliminar la salida de un subgráfico de función

### 15.0.2

*(Lanzamiento 18 de septiembre de 2025)*

**Agregado:**

* [Vista 3D/OpenGL] Quitar el efecto malla metálica aplicado en la malla seleccionada
* [Vista 3D] Permita el uso de la tecla &quot;F&quot; para centrarse en una malla seleccionada cuando el navegador de escenas está seleccionado
* [Vista 3D] El procesamiento no se actualiza al cambiar el formato de mapa de normales
* [BakersCLI] Opción Añadir para controlar el tamaño de la caché de la superficie
* [BakersCLI] Cambie el nombre de la opción &quot;use\_cache&quot; a &quot;keep\_meshes\_in\_cache&quot;
* [UI] Icono Actualizar para escenas 3D en biblioteca

**Corregido:**

* [Vista 3D] Bloqueo al asignar un nodo de material a una escena de varios materiales
* [Vista 3D] El gráfico creado a partir de entradas de textura siempre se ve en la vista 3D, independientemente de las preferencias
* [Vista 3D] Uso incorrecto de la información sobre herramientas de la insignia &quot;Vista en vista 3D&quot; en un caso específico
* [Vista 3D] Muchos errores de USD al anular escenas específicas
* [Vista 3D] Artefactos de sombras al utilizar el desplazamiento en una escena plana en el rasterizador
* [Vista 3D] Algunas escenas específicas no están visibles al utilizar el procesador OpenGL
* [Vista 3D] El cuadro de diálogo utilizado para &quot;Seleccionar el Gráfico de Substance de destino&quot; siempre tiene el icono de gráfico &quot;Pendiente&quot;
* [Vista 3D] El menú contextual de la ventana gráfica no se muestra para escenas específicas
* Las insignias [Vista en vista 3D] no se borran al cambiar de escena en un caso específico
* [Vista 3D] Lavado del color en la vista 3D al utilizar la gestión de color de Adobe ACE
* [Vista 3D] [Linux] Varias escenas se procesan en negro en el procesador OpenGL
* [Vista 3D] [Explorador de escenas] Las teclas de flecha mueven la selección a la raíz
* [BakerCLI] No se pueden invalidar algunos parámetros
* [Panaderos] Artefactos en dilatación al usar panaderos normales con antialiasing
* [Bakers] El proceso de horneado se detuvo abruptamente en CLI mientras horneaba una gran cantidad de UDIM en 4K
* [Bakers] Bloqueo al empujar a baker hacia abajo en la lista de baker en un caso específico
* [Bakers] La selección de formato cambia de .surface a .dds
* [Panaderos] Se congela al hornear una gran cantidad de UDIM en 4K
* [Bakers] [macOS] Bloqueo al realizar una transferencia de textura con suavizado
* [Contenido] Lista de puntos: Los puntos no están en el orden correcto cuando la textura de los datos no es cuadrada
* [Contenido] Ver paleta de colores: Los nodos internos se calculan a resoluciones demasiado altas
* [Data] Bloqueo al cambiar el nombre de la salida para corregir la salida fantasma en la instancia
* Distancia [del motor]: se altera la luminancia de la máscara de entrada
* [FxMap] $tiling no tiene efecto si FX-Map está dentro de un subgráfico
* [Graph] La búsqueda aproximada devuelve resultados irrelevantes
* [Editor de Python] Los scripts cargados no se vuelven a abrir en las sesiones

### 15.0.1

*(Publicado El 22 De Julio De 2025)*

**Agregado:**

* [Vista 3D] Permitir aplicar texturas a mallas USD que tengan enlaces displayColor y no Material
* [Vista 3D] No cree automáticamente un material por malla que no tenga una unión de material
* [Vista 3D] Cambie el nombre &quot;Muestras de píxeles convergentes&quot; por &quot;Muestras&quot;
* [Vista 3D] Cambie el nombre del parámetro &quot;Escala de UV habilitada&quot; a &quot;Habilitar Tamaño físico desde gráfico&quot;
* [Vista 3D] Reduzca la intensidad del desplazamiento según el parámetro &quot;Mosaico&quot;
* [Vista 3D/OpenGL/Iray] Añada un mensaje en la ventana gráfica cuando el entorno predeterminado esté desactivado
* [Bakers] Utilice iconos para botones para reordenar líneas en la lista de procesamiento de Bakers
* [Preferencias] Añada una opción para definir el procesador de vista 3D predeterminado
* [Propiedades] Hacer que &#39;Restablecer valores predeterminados&#39; utilice los valores predeterminados creados, si los hay

**Corregido:**

* [Vista 3D] Artefactos en una escena específica cuando se procesan con OpenGL
* [Vista 3D] El entorno predeterminado no se desactiva al cargar un recurso de escena 3D en USD que contiene uno
* [Vista 3D] Mostrar el menú contextual de la ventana gráfica tarda varios segundos en escenas grandes
* [Vista 3D] &quot;Intensidad de emisión&quot; es 0 cuando se reemplazan materiales que no son de USD solo con &quot;Color de emisión&quot;
* [Vista 3D] Los canales rojo y azul se intercambian en una textura de 8 bits utilizada como entorno
* [Vista 3D] La función de arrastrar y soltar de RMB no funciona de forma coherente debido al registro del botón derecho
* [Vista 3D] La opción &quot;Mostrar solo&quot; del subconjunto oculta su malla principal
* [Vista 3D] Las escenas predeterminadas cargadas desde archivos aparecen con un color base incorrecto
* [Vista 3D] La propiedad &quot;Escala de UV&quot; se restablece al cambiar de OpenGL a otro procesador y viceversa
* [Vista 3D] [Israel] Los procesamientos suelen estar borrosos y pixelados
* [Panaderos] Artefactos al utilizar la difusión en una GPU AMD
* [Panaderos] La cocción falla con algunas escenas para conjuntos UV distintos de 0
* [Panaderos] &#39;Textura transferida&#39;: La lista &quot;UV Set&quot; no tiene en cuenta la opción &quot;Usar poly alta como baja&quot;
* [Panaderos] La selección de azulejos UV siempre se restablece en &#39;Todo&#39;
* [Graph] Bloqueo al eliminar un nodo en contexto
* [Mac OS] [Vista 3D] Resolución de procesamiento incorrecta en pantallas mac
* Los parámetros modificados no se estilizan en la primera visualización
* [UX] Los elementos desactivados en el menú desplegable no son visibles

### 15.0.0

*(Publicado El 15 De Julio De 2025)*

**Agregado:**

* [Vista 3D] Nuevo procesador, con modos rasterizador y trazador de rutas
* [Vista 3D] Añadir una herramienta de selección para seleccionar un objeto en la escena 3D
* [Vista 3D] Añade el nuevo mensaje &quot;Exportar escena con capas...&quot; en el menú &quot;Escena&quot;
* [Vista 3D] Añadir nuevos botones de la barra de herramientas
* [Vista 3D] Añada la posibilidad de cambiar entre varias cámaras incluidas en una escena en USD
* [Vista 3D] Permitir que el objeto seleccionado se centre al pulsar &#39;F&#39; en la ventana gráfica
* [Vista 3D] Permite generar un gráfico de composición de Substance a partir de un material existente
* [Vista 3D] Permite enviar un gráfico de composición SBS en la vista 3D y asignar su salida única al uso de entorno/panorama
* [Vista 3D] Borre la selección actual pulsando la tecla Escape
* [Vista 3D] Visualización de una escena 3D importada con texturas
* [Vista 3D] Distingue los controles de repetición de texturas X e Y
* [Vista 3D] Activar / Desactivar sombras
* [Vista 3D] Activar/Desactivar plano de tierra
* [Vista 3D] En el menú &quot;Materiales&quot;, añada &quot;Quitar&quot; solo para el material que se ha añadido manualmente y que no se utiliza
* [Vista 3D] En el menú &quot;Materiales&quot;, elimine la acción &quot;Eliminar todo&quot;
* [Vista 3D] Convertir archivos USDZ exportados en archivos independientes
* [Vista 3D] Hacer que las propiedades del procesador persistan al cambiar el modo del procesador
* [Vista 3D] Conservar las entradas de material existentes al sustituir un material
* [Vista 3D] Reorganizar propiedades de la cámara
* [Vista 3D] Quitar acciones &quot;Cámara/Guardar captura de pantalla...&quot; y &quot;Camera/Copy screenshot to clipboard&quot;
* [Vista 3D] Quitar la acción de menú &quot;Material/Reconstruir todo&quot;
* [Vista 3D] Quite el prefijo &quot;Predeterminado&quot; de la etiqueta de la cámara predeterminada
* [Vista 3D] Establezca la acción de menú &quot;Restablecer valor predeterminado&quot; como la última en el menú de hamburguesa de propiedades de entrada de material
* [Vista 3D] Ajustes de método abreviado
* [Vista 3D] Compatibilidad con sombras y translucidez en modo de tiempo real
* [Vista 3D] Compatibilidad con sombreadores MaterialX de una escena importada en USD
* [Vista 3D / OpenGL] Cambie el nombre del parámetro &quot;Escala de UV habilitada&quot; a &quot;Habilitar Tamaño físico desde gráfico&quot;
* [Vista 3D / Efectos posteriores] Floración
* [Vista 3D / Post effects] Profundidad de campo
* [Vista 3D / Efectos posteriores] Asignación de tonos
* [Vista 3D / Explorador de escenas] Permite mostrar las propiedades de material al seleccionarlo en el Explorador de escenas
* [Vista 3D / Explorador de escenas] Ocultar la columna &quot;Material&quot;
* [Vista 3D / Navegador de escenas] Ponga en negrita las primitivas USD que están controladas por una entidad predefinida
* [Bakers] Añade un menú contextual en la vista de árbol con las acciones &quot;Seleccionar todo&quot;/&quot;Deseleccionar todo&quot;
* [Bakers] Añadir una opción para controlar la interpolación de bitangentes
* [Bakers] Añadir divisor horizontal en GUI
* [Bakers] Añadir macro UDIM de forma predeterminada en el nombre de salida cuando la escena es udim
* [Panaderos] Permitir el cálculo de la tangente
* [Panaderos] Permitir cambiar el nombre de un panadero sin romper los vínculos
* [Bakers] Cambiar el tamaño predeterminado del panel central
* [Bakers] Textura de entrada para flujo de trabajo UDIM
* [Bakers] Hacer que el orden de lista de mapas de vistas 2D coincida con el orden de lista de procesamiento de Bakers
* [Panaderos] Convertir la ventana de panadería en modal
* [Panaderos] Administrar parámetros de asignación de tonos
* [Bakers] Quitar selección de complemento de espacio tangente
* [Panaderos] Estado de guardado &quot;activado&quot; o &quot;desactivado&quot; para panaderos al guardar un ajuste preestablecido
* [Bakers] Seleccionar material de forma predeterminada en el widget de selección
* [Bakers] Establecer la orientación predeterminada de la textura de salida Normal en relación con la preferencia
* [Panaderos] Establecer los mosaicos UV en Todo de forma predeterminada
* [Bakers] Opción de adición WordSpaceDirection FromTexture/FromValue
* [Bakers] Mundo a tangente: defina la entrada predeterminada en &quot;desde textura&quot;
* [SBSBaker] Crear una opción para controlar el orden de backend
* [SBSBaker] Mejorar el uso del argumento StringList
* [SBSBaker] Cambie el nombre &quot;match\_source\_instance&quot; por &quot;match\_mesh\_name&quot;
* [SBSBaker] Cambiar el nombre &quot;Submalla&quot; a &quot;GeomSubset&quot;
* [SBSBaker] Cambiar nombre a substance3d\_baker
* [Contenido] Añada la forma &quot;Hemisferio&quot; a los nodos del generador para exponer las formas Cuadrante
* [Interop] Compatibilidad con el formato de archivo GLTF
* [Interop] Compatibilidad con el formato de archivo PLY
* [Interop] Compatibilidad con el formato de archivo STL
* [Biblioteca] Uniformizar información sobre herramientas para nodos atómicos
* [Mac] Dejar de admitir la plataforma MacIntel
* [Nodes] Añadir información valiosa para nodos atómicos
* [Parameters] Cerrar la sección &#39;Attributes&#39; de forma predeterminada
* [Parámetros] Permite que el usuario especifique valores predeterminados de parámetros base para nuevas instancias
* [Preferencias] Panaderos: añadir una opción booleana para calcular el espacio tangente por fragmento
* [Preferencias] Quitar los complementos de espacio tangente
* [Preferencias] Almacenar las preferencias por versión secundaria de SD (XX.X)
* [VFX] Actualizar a 1.85.0
* [VFX] Actualice MacOS versión mínima a 12.0
* [VFX] Actualice OpenColorIO a 2.4.2.
* [VFX] Actualice OpenColorIO a 2.4.x
* [VFX] Actualice OpenExr a 3.3.x
* [VFX] Actualizar Qt a 6.5.8

**Corregido:**

* [Vista 3D] Las texturas de la escena en USD exportada no se aplican correctamente
* [Vista 3D] [UDIM] No se pueden ver las salidas del gráfico UDIM en la vista 3D cuando la visualización automática al abrir el gráfico está desactivada en las preferencias del gráfico
* [Bakers] &#39;Anti-alias.&#39; y &quot;Promedio. las celdas normales de los panaderos no aplicables están en blanco y se pueden editar
* [Bakers] La acción Actualizar utiliza el back-end de trazado de rayos cuando está desactivada en las preferencias
* [Panaderos] Panaderos bloqueados como ocupados después de un fallo durante el proceso de &#39;Actualizar todos los mapas con bake&#39;
* [Bakers] Bloqueo en más de 180 UDIM al hacer el mapa de posición de OpenGL en una malla específica
* [Bakers] Bloqueo al abrir el cuadro de diálogo &quot;Hornear información de modelo&quot; varias veces seguidas (solo macOS)
* [Bakers] En la exportación de ajustes preestablecidos de JSON, el valor &#39;udim&#39; se reemplaza por &#39;1001&#39; cuando se estableció en &#39;All&#39;
* [Bakers] La memoria no se detecta correctamente en Linux
* [Bakers] La falta de dependencia de entrada de mapa no activa la advertencia ni bloquea el procesamiento
* [Bakers] No hay etiqueta de error cuando el nombre de salida está vacío
* [Bakers] Cambiar la malla de alta polietileno del archivo no tiene efecto
* [Panaderos] El panadero de destino no se selecciona de forma predeterminada al utilizar la acción &quot;Volver a hornear&quot;
* Distancia [del motor]: &quot;corte&quot; visible en algunas situaciones
* [Motor] Fx-Map: Los colores negativos no se admiten cuando la profundidad de bits es de 8 bits (solo motores GPU)
* [Localización] La entrada de caracteres vuelve del japonés al latín en el menú de nodos
* [Seguridad] Vulnerabilidad de escritura fuera de límites en el análisis de archivos USDC
* [Security] Vulnerabilidad de ESCRITURA fuera de límites II, al analizar el archivo NEF
* [Security] Vulnerabilidad de lectura fuera de límites III al analizar archivos DNG
* [Preferencias] Problemas de experiencia de usuario en la configuración de proyectos de solo lectura
* [Resources] No se muestran varios conjuntos UV al abrir archivos FBX
* [UI] Etiquetas superpuestas en la barra de estado
* [UI] No se muestran las sugerencias del menú desplegable &quot;Modo de creación de vínculos&quot;

## Versión 14

### 14.1.2

*(Publicado El 15 De Abril De 2025)*

**Agregado:**

* [Graph] Utilice el motor de GPU predeterminado para generar miniaturas del gráfico actual
* [Biblioteca] Utilice el motor de GPU predeterminado para generar miniaturas de la biblioteca

**Corregido:**

* [Graph] En algunos casos, no es posible mover conexiones en el modo de creación de vínculos &#39;Standard&#39;
* [Contenido] Artefactos en la salida del filtro de MLV en un caso específico
* [Contenido] Atlas splitter/dispersión: solo se dibuja correctamente la primera celda (solo motor macOS + GPU)
* [Contenido] Suavizado de bisel: formato es 32f absoluto
* [Contenido] Fibras 1: defectos visuales al convertir a mapa normal
* [Contenido] RT AO, Shadows, Bent Normal se procesan incorrectamente en algunos casos
* [Bakers] Los elementos de menú con submenús pierden algún margen a la derecha del texto
* [MacArm][sbsrender] Motor de CPU incorrecto cuando no se encuentra el motor de GPU
* [Mac/Linux] [sbsrender] Motor de GPU predeterminado incorrecto

### 14.1.1

*(Publicado El 20 De Febrero De 2025)*

**Agregado:**

* [Graph] Herramientas de alineación de nodos: Restablezca los métodos abreviados de teclado y active el apilamiento de forma predeterminada
* [MDL] Advertencia a los usuarios de que los &quot;gráficos MDL&quot; dejarán de utilizarse en versiones futuras
* [Preferencias] Advertencia a los usuarios de que los &quot;complementos de espacio tangente personalizado&quot; dejarán de utilizarse en versiones futuras

**Corregido:**

* [Vista 2D] Mostrar coordenadas de píxeles centrales en lugar de las coordenadas de la parte superior izquierda
* [Contenido] Escala de grises de Kuwahara anisotrópico: Advertencia de la cocina para la falta de la variable &#39;ignore\_alpha&#39;
* [Contenido] Advertencias de cookies en algunos nodos de Suciedad
* [Contenido] Errores de cocción por falta de parámetro en el nodo &quot;Niveles automáticos&quot;
* [Contenido] Errores de cocina en la consola al procesar miniaturas de algunos paquetes
* [Contenido] Muesca de borde: Aviso de cocción en la consola
* [Contenido] Color MLV: Sangrado de color a pesar de utilizar Sin segmentación en un caso específico
* [Contenido] Máscara a trazados: Los trazados pueden ser demasiados, demasiado pocos o de longitud cero en casos específicos
* [Contenido] Renderización PBR v1: Algunos gráficos de utilidades se muestran en Biblioteca
* [Contenido] Dispersión en spline: se dibuja un patrón aunque no haya entrada de spline
* [Parámetros] Etiqueta de &#39;valor fantasma&#39; al pegar un parámetro de lista con un índice que no coincide
* [UI] Bloqueo al cerrar Designer mediante la acción &quot;Salir&quot; en el Dock de macOS (solo macOS)
* [UI] Las rutas de textura en las propiedades de sombreado no se recortan al ancho del conjunto acoplado

### 14.1.0

*(Lanzado El 14 De Enero De 2025)*

**Agregado:**

* [Vista 2D] Adición de una visualización de píxeles anclados en el panel Información
* [API] Exponga el tamaño del cuadro de nodos en la escena de la vista de gráficos
* [Content] &#39;Fusión de Height de material&#39;: Agregar salida de máscara de Height
* [Content] &#39;Procesador de vértices de ruta&#39;: Usar el botón &quot;Editar función&quot; para el parámetro &quot;Por función de vértice&quot;
* [Contenido] Niveles automáticos: Limpiar los parámetros no utilizados, ajustar las etiquetas y la información sobre herramientas
* [Contenido] Máscara en rutas v2
* [Contenido] Nuevo nodo Media de Varianza Mínima (MLV)
* [Content] Nuevo nodo de filtro mediano
* [Contenido] Cuantificar color: Añadir la opción de filtrado Más cercana
* [Content] Lista de puentes polinomiales: Añadir parámetros de desvío de spline aleatorio
* herramientas de spline [Content]: Nuevo nodo Spline (Quadratic)
* Triangle Grid [Content]: cambiar el método de triangulación y usar bucles
* [Contenido] Nueva Dispersión Splines en el nodo Splines
* [Cooker] Exponer el parámetro base de &#39;Proporción de píxeles&#39; como variable estática &#39;$pixelratio&#39;
* [CrashReport] Integrar nueva ventana de informe de bloqueo
* [Motor] Añada la versión Vulkan/Metal del motor de mezcla
* Modo de material [Graph]: permitir que la conexión entre sin uso cuando se selecciona un solo vínculo
* [Graph] Vínculo de material: permitir conexiones estándar cuando la conexión no es ambigua
* [Graph] Herramientas de alineación de nodos: añadir distribuciones horizontales/verticales, alineaciones izquierda/derecha/superior/inferior y nodos de soporte apilados
* [Biblioteca] Corrección del color del texto en menús contextuales
* [Parámetros] Copiar parámetros de un nodo a otro
* [Propiedades] &quot;Restablecer todo&quot;: Quitar la ventana emergente de confirmación
* [Resources] Establezca el formato en &quot;All format&quot; (Todos los formatos) en el cuadro de diálogo &quot;Link Bitmap&quot; (Vincular mapa de bits)
* [Buscar] Agregar una forma de habilitar/deshabilitar un modo recursivo
* [Buscar] Añada una forma de activar o desactivar la búsqueda aproximada
* [Buscar] Mostrar siempre y establecer el foco en el campo de término de búsqueda al habilitar el Buscador de nodos usando su método abreviado de teclado
* [Buscar] Volver a trabajar la opción de filtro
* [Atajos] Permite asignar las teclas &#39;V&#39;, &#39;H&#39; y &#39;S&#39;
* [ThirdParty] Actualización a Qt 6.5.7
* [UX] Los cuadros de diálogo modales no se deben minimizar
* [UX] Eliminación del desplazamiento horizontal en el cuadro de diálogo de alerta

**Corregido:**

* [Contenido] Bisel: El formato normal no se ve afectado por la preferencia global
* [Contenido] El nodo Color a máscara no omite el alfa
* distancia direccional [Content]: Resultado incorrecto cuando la entrada tiene una proporción de imagen vertical
* [Content] Asignador de Flood Fill: Advertencia provocada para la variable ausente
* [Contenido] Histograma Compute: El resultado es 16 veces más de lo que debería ser
* [Contenido] La cáustica de RT no funciona en resoluciones no cuadradas
* [Content] Lista de puentes polinomiales: Resultado incorrecto al utilizar desplazamientos de inicio/fin
* [Content] Selección de spline: la cantidad de spline de salida puede ser mayor que la cantidad de spline de entrada
* [Contenido] Deformación polinomial produce un resultado negro con el motor SSE
* Triangle Grid [Content]: el patrón no está colocando el mosaico correctamente
* Triangle Grid [Content]: El mosaico se rompe en un caso específico
* [Data] Bloqueo al cambiar el identificador de entrada de gráfico en un caso específico
* [Gráfica de funciones] Los valores largos aparecen superpuestos en los nodos &#39;Float&#39;
* [Fx-Map] Bloqueo al mostrar las propiedades del nodo Cuadrante
* [Graph] [UDIM] Tener una barra de desplazamiento en la lista UDIM da como resultado 1.1 1.2 entradas
* [Graph][Shortcuts] El nodo creado mediante un método abreviado no se coloca en el vínculo existente después de la duplicación del nodo
* [Propiedades] Visualización incorrecta del parámetro cuando el valor no es válido
* [Publish] Las dependencias recíprocas producen un bucle infinito al publicar un paquete
* [Publish] Error silencioso al utilizar la acción &quot;Publish&quot; en un paquete con dependencia descargada
* [UI] El widget &quot;Tamaño principal&quot; no se muestra correctamente cuando se expande y puede bloquear la interfaz (solo macOS)
* [UI] La ventana principal se oculta tras otras aplicaciones en algunos casos (solo Windows)

### 14.0.2

*(Publicado El 10 De Octubre De 2024)*

<b>Agregado:</b>

* [Gráfico de funciones] Mejora de la alineación del texto en los nodos
* [MacOS] Repermitir la instalación en la versión Big Sur (11.0)
* [Windows] Repermitir la instalación en Windows 10 19H2

<b>Corregido:</b>

* [Bitmap] Los trazos de pintura en el recurso de mapa de bits no marcan el paquete host como modificado
* [Gráfica de funciones] Bloqueo al cerrar un paquete con un gráfico de funciones que aloja un nodo de instancia
* [Gráfico de funciones] Bloqueo al deshacer dos ajustes de nodo de color de muestra en una fila

### 14.0.1

*(Publicado El 24 De Septiembre De 2024)*

<b>Agregado:</b>

* [Motor] Actualizar a Substance Engine 9.1.4
* Triangle Grid [Content]: cambiar el método de triangulación y usar bucles

<b>Corregido:</b>

* [API] Los complementos descargados no se pueden volver a cargar
* [Contenido] Histograma Compute: El resultado es 16 veces más de lo que debería ser
* Triangle Grid [Content]: el patrón no está colocando el mosaico correctamente
* [Data] Bloqueo al cambiar el identificador de entrada de gráfico en un caso específico
* [Motor] El nodo Distancia produce defectos al utilizar tamaños de píxeles muy bajos
* [Motor] Resultado incorrecto del nodo de distancia a una resolución de 8K en el motor SSE2
* [Gráfica de funciones] Los valores largos aparecen superpuestos en los nodos &#39;Float&#39;
* [Graph][Shortcuts] El nodo creado mediante un método abreviado no se coloca en el vínculo existente después de la duplicación del nodo
* [Propiedades] Visualización incorrecta del parámetro cuando el valor no es válido

### 14.0.0

*(Publicado El 30 De Julio De 2024)*

<b>Agregado:</b>

* [Contenido] Nuevo filtro Kuwahara anisotrópico
* [Content] Nuevo nodo de Suavizado de bisel
* [Contenido] Nuevo nodo Curvatura suave v2
* [Content] Nuevo nodo de Distancia direccional
* [Contenido] Nuevas herramientas de histograma: Calcular, ecualizar, procesar
* [Contenido] Nuevo nodo ID a máscara
* [Content] Nuevo nodo Normal Uncombine
* [Content] Nuevos nodos de la paleta: Crear, Aplicar, Modificar, Ver
* [Content] Nuevo nodo Cuantificar color
* [Contenido] Deformación direccional no uniforme: Defina el valor predeterminado de Asignación de intensidad en 1
* [Contenido] Añada el sufijo &quot;Color&quot; o &quot;Escala de grises&quot; a todas las etiquetas de nodo que tengan estas versiones
* [Contenido] Si se anula el &quot;ruido blanco&quot;, solo se mantiene &quot;ruido blanco rápido&quot;
* [Content] Pase al nodo &#39;Negate Float1&#39; en el gráfico de funciones del Substance
* [Contenido] Cambie el nombre &quot;Cuantizar color&quot; por &quot;Cuantificar color (simple)&quot;
* [Vista 2D] Visualización de valores en el panel de información para píxeles fuera del rango 0-1
* [Motor][Texto] Nuevo kerning para algunas fuentes
* [Graph] Mejora el tiempo de invalidación al editar subgráficos profundos mientras usas la edición en contexto
* [Vinculador] No duplicar mapas de bits en SBSASM
* [Parámetros] Añada un nuevo widget de &quot;función&quot; para todos los tipos de parámetros de entrada
* [Propiedades] Mejorar la visualización de los parámetros heredados
* [UX] Mejora de la compatibilidad con Trackpad (solo Mac)
* [UX] Modernizar la panorámica al alcanzar el borde del gráfico al seleccionar
* [UX] Eliminación de la funcionalidad &quot;Desactivar alta PPP&quot;
* [Branding] Nueva marca para la pantalla de bienvenida y la ventana Acerca de
* [Mapa de degradado] Añade una forma de desplazar todas las teclas y el bucle
* [Biblioteca] Cambiar todos los filtros predeterminados a mayúsculas y minúsculas de oración
* [API] Método Add para encuadrar un nodo específico en la ventana gráfica de la vista de gráficos
* [API] Añadir método para abrir un recurso de paquete en su editor (p. ej., un gráfico de Substance en la vista de gráficos)
* [API] Añadir método para seleccionar un recurso de paquete en el Explorador (p. ej., un gráfico de Substance)
* [API] Agregue métodos para obtener y establecer el tipo de gráfico de un gráfico de composición de Substance
* [ThirdParty] Sigue las recomendaciones de las plataformas VFX 2023
* [ThirdParty] Sigue las recomendaciones de las plataformas VFX 2024
* [ThirdParty] Actualizar Boost a 1.82.0 + USD a 23.08
* [ThirdParty] Actualizar NGL a 1.38
* [ThirdParty] Actualizar OpenColorIO a 2.3.x
* [ThirdParty] Actualice OpenExr a 3.2.x
* [ThirdParty] Actualizar OpenSubdiv a 3.6.x
* [ThirdParty] Actualizar Python a 3.11.x
* [ThirdParty] Actualice Qt a 6.5.x
* [ThirdParty] Actualizar gcc a 11.2.1
* [ThirdParty] Actualizar glibc a 2.28
* [ThirdParty] Actualizar ABI de libstdc++ a C++11 uno
* [Documentación] Nueva página de &#39;Glosario&#39;

<b>Corregido:</b>

* [Bakers] Bloqueo al retocar una escena cuyo nombre de archivo se ha cambiado
* [Bakers] Bloqueo al guardar el ajuste preestablecido de bakers en un archivo JSON
* [Content] &#39;Dispersión en spline&#39;: Exponer parámetro alfa de imagen de entrada
* [Contenido] &#39;Color del Sampler de mosaico&#39;: falta la expresión visibleif
* [Contenido] Ruido anisotrópico: valor negativo para la cantidad X/Y produce un resultado incorrecto
* [Contenido] Ruido anisotrópico: Problema de segmentación al utilizar un valor impar como cantidad X y sin smoothness
* [Content] Función de distribución normal: una posición incorrecta de max() puede provocar NaN
* [Contenido] Las sombras TRAO, Bent Normal y RT no funcionan correctamente en algunas plataformas
* [Contenido] Color de fusión de salpicaduras de formas: Los mapas normales de OpenGL no se mezclan correctamente
* [Contenido] Espacio injustificado después del prefijo &quot;Multi&quot; en las etiquetas de nodo
* [Dependencies] Bloqueo al mover un gráfico dentro de un paquete o entre paquetes
* [Motor] Error de precisión en nodos de deformación que afectan a los nodos de desenfoque de Pendiente
* [Motor] La capa SBSAR en SD no puede leer SBSAR con contenido SBSASM > 2 GB
* [Gráfico de funciones] Resultado incorrecto para 0^n
* [Graph] La opción &quot;Mostrar tamaño de nodo&quot; no está etiquetada correctamente
* [Graph] Bloqueo al copiar un comentario principal a otro gráfico
* [Graph] Bloqueo al pulsar alt y arrastrar un nodo de punto
* [Graph] En la búsqueda de nodos pueden faltar coincidencias obvias en algunos casos
* [Graph] Problema de rendimiento al editar un gráfico de funciones con instancias múltiples con supergraph abierto
* [Graph] Demasiadas invalidaciones al crear una salida
* [Seguridad] Vulnerabilidad de escritura fuera de límites del análisis ICO
* [Security] Anular el uso de algún formato de imagen
* [Parámetros] La ruta del recurso PKG de mapa de bits no debe poder editarse
* [Parámetros] Se han solucionado problemas relacionados con la exposición por lotes del parámetro de un procesador de valores
* [Parámetros] Los parámetros de cadena se omiten al exponer lotes
* [Propiedades] Problema de rendimiento al editar un gráfico de funciones con instancias múltiples con propiedades abiertas
* [SVG] Las ediciones de formas no se aplican en imágenes rasterizadas
* [IU] Solucione algunos errores o incoherencias con widgets desplazables (solo Windows)
* [UI] Orden incoherente de los formatos de archivo de escena 3D en las listas de importación/exportación
* [UI] Las acciones de la ventana se duplican en la IU
* [Control de versiones] El script &#39;perforce.py&#39; no funciona en Python 3

## Versión 13

### 13.1.2

*(Publicado El 16 De Abril De 2024)*

<b>Agregado:</b>

* [Graph] No coloque nodos duplicados encima del nodo original
* [Graph] Mejorar la alineación de los comentarios adjuntos a los nodos
* [Graph] Mejorar el movimiento de comentarios
* [Graph] Ajuste los fotogramas y comentarios pegados o duplicados a la cuadrícula
* [Frames] Ajuste nuevos marcos y comentarios a la cuadrícula
* [Content] &#39;Curvatura suave&#39;: Agregue una nota sobre la compatibilidad de mosaico en la descripción
* [3DView][IRay] Permite asignar la salida int al parámetro enum
* [AxF] Agregar propiedades sobre el modelo de capa transparente
* [AxF] Mejora de la gestión de errores durante la exportación
* [AxF] Mejora de los materiales GLSLFX y MDL para la representación &quot;SVBRDF&quot; tal y como se almacenan en un archivo AXF
* [AxF] Quitar la propiedad &#39;CC No Refraction&#39; de la plantilla &#39;AxF to AxF&#39;
* [AxF] Cambie el nombre de las propiedades &quot;properties.has\_xxx&quot; por &quot;features.has\_xxx&quot;
* [AxF] Actualizar plantilla para incluir todas las propiedades utilizadas por nuestros sombreadores SVBRDF

<b>Corregido:</b>

* [Vista 3D] Bloqueo al restablecer un parámetro Int MDL asignado a una enumeración MDL
* [Vista 3D] Widgets incorrectos para las propiedades del sombreador SVBRDF cuando se restablece el material después de cambiar la escena 3D
* [Vista 3D] Widgets incorrectos para las propiedades del sombreador SVBRDF cuando no se aplica ningún gráfico
* [Vista 3D] El botón &quot;Mostrar entorno&quot; está desactivado para las nuevas vistas sin archivo SBSCN predeterminado
* [Vista 3D] Cambiar del procesador de Iray al de OpenGL desconecta una salida de gráfico
* [AxF] La variante de Fresnel no se actualiza en la salida del gráfico
* [AxF] Las etiquetas de las propiedades del sombreador AxF tienen un formato incoherente
* [AxF] La advertencia sobre los recursos no modificados solo aparece en la consola
* [Content] &#39;Non-Uniform&#39; no se escribe de forma coherente en todos los nodos
* [Contenido] Dispersión en spline: Patrones que faltan en las splines del puente
* [Content] Asignador de splines: Bloqueo al establecer un valor negativo de &#39;Cantidad de segmento&#39;
* [Content] &#39;Simetría&#39;: Faltan etiquetas y son incoherentes
* [Gráfico] Los comentarios existentes se desplazan ligeramente
* [Seguridad] Vulnerabilidad de lectura fuera de límites del análisis de archivos RAS

### 13.1.1

*(Publicado el 8 de febrero de 2024)*

<b>Agregado:</b>

* [AxF] Añadir propiedades booleanas hasClearCoat, hasSheen, etc.
* [AxF] Agregar algunas propiedades que faltan
* [AxF] Permitir la importación de EP-SVBRDF
* [AxF] Cambiar el nombre de las propiedades &quot;anisotropic&quot;, &quot;fresnel&quot; y &quot;fresnel variant&quot;
* [AxF] Actualización a AxF-Editing 1.0.0
* [Graph] Pegar en la posición del ratón si está en la vista de gráfico
* [UX] Aumente el height del campo de texto &quot;Descripción&quot; del marco y el comentario.
* [UX] Centrarse en los campos de edición de texto al crear marcos, comentarios o chinchetas

<b>Corregido:</b>

* [AxF] Los valores del mapa &quot;Color de Specular&quot; son incorrectos al exportar
* [AxF] La vista previa y las texturas no se muestran correctamente en el cuadro de diálogo Importar AxF
* [AxF] La propiedad &#39;CC No Refraction&#39; no se ha insertado correctamente en la plantilla &#39;AxF to AxF&#39;
* [Contenido] &#39;Flood Fill a posición&#39; no está en la biblioteca
* [Content] &#39;Splatter Circular&#39;: Los valores negativos de &#39;Cantidad de patrón&#39; dan como resultado cálculos muy largos e intensivos
* [Content] &#39;Lista de combinación de spline&#39;: Orden de entrada incorrecto
* [Dependencias] La dependencia se reasigna a su copia después de guardarla como copia
* [Fotogramas] El botón Habilitar marcado de HTML no se activa al deshacer su uso
* [Frames] Al seleccionar un marco con el recuadro y su contenido, se mueve todo el contenido del marco mientras se expande automáticamente
* [Gráfico] Los comentarios duplicados de los comentarios primarios siempre se colocan en el origen del gráfico
* [Graph] El salto de línea en el comentario es más duro en la creación
* [Publish] Establezca la ruta predeterminada para la publicación SBSAR en la carpeta &quot;Mis documentos&quot;
* [SBSAR] Al rehacer la carga SBSAR, esta se puede editar y se pueden perder sus datos

### 13.1.0

*(Publicado El 12 De Diciembre De 2023)*

<b>Agregado:</b>

* [Frames] Expansión automática
* [Frames] Cambiar reglas para definir cuándo un objeto pertenece a un marco
* [Frames] Desactivar la escala de texto para la descripción de marcos
* [Marcos] Ajustar tamaño al contenido
* [Fotogramas] Nuevos estados predeterminados, de cursor encima y seleccionados
* [Fotogramas] Ajustar a cuadrícula grande
* [Frames] Código de HTML de soporte para descripción de marcos
* [Frames] Actualizar zonas de interacción
* [Frames] Actualizar aspecto visual
* [Gráfico] Cree el nodo en el centro del vínculo visible en lugar de en el centro del vínculo
* [Graph] Muestra las propiedades de un elemento si es el único elemento con propiedades disponibles en una selección
* [Gráfico] Eliminación de la opción &quot;Escalado&quot; de los comentarios del gráfico
* [Graph] Ajuste nodos en la cuadrícula principal al copiar y pegar
* [UX] Permitir búsqueda difusa en el menú Nodo y en la búsqueda de biblioteca
* [UX] Hacer que la lista de menús de nodos se reproduzca en bucle
* [AxF] Compatibilidad con exportación AxF
* [AxF] Desactivar AxF en Linux
* [API] Establezca la propiedad &#39;Visible if&#39; de los parámetros de gráficos, entradas y salidas mediante la API de Python
* [API] Establecer el orden de las E/S de gráficos mediante la API de Python
* [Dependencias] Actualizar Boost a 1.80.0
* [Dependencias] Actualizar OpenSubdiv a 3.5.x
* [Dependencias] Actualizar gcc a 11.2.1 - Problema Iray/MDL C++20
* [Dependencias] Actualizar FBX SDK a 2020.3
* [Dependencias] Actualizar NGL a 1.35.0.20
* [Gestión de color] Añadir compatibilidad con pantallas OCIO ICC
* [Niveles] Agregue una forma de restablecer el histograma
* [Python] Advertir a los usuarios si no se puede importar QtForPython
* [Vista 2D] Guarde el estado de las opciones de vista
* [Vista 3D] Añadir la técnica Posición al sombreador de información de malla
* [Exportar] Añada un botón &quot;Guardar configuración&quot; para guardar los cambios en las opciones de exportación

<b>Corregido:</b>

* [Vista 3D] No se puede asignar una textura a una entrada de tipo texture\_2d de un material MDL
* [AxF] Los identificadores de gráficos de la lista de plantillas pueden estar en blanco
* [AxF] El campo de plantilla de gráfica de Substance está en blanco de forma predeterminada
* atlas scatter [Content]: comportamiento incorrecto en casos específicos
* [Content] Asignador de Flood Fill: salida en blanco cuando todas las formas tienen el mismo tamaño de cuadro de texto
* [Contenido] FloodFill a posición: Artefactos de imprecisión en algunas situaciones
* [Content] Salida incorrecta de &#39;Specular&#39; en el nodo &#39;BaseColor/Metallic/Roughness converter&#39;
* [Contenido] Máscara a trazado no funciona en vertical no cuadrado
* [Contenido] Falta la descripción de los nodos Valor de entrada, Escala de grises de entrada, Color de entrada y Salida
* [Content] Falta la descripción de los nodos Set y Sequence
* [Contenido] Salpicadura de forma: Artefactos de imprecisión en la salida de datos de salpicaduras 2
* [Motor] Los valores booleanos de los procesadores de valores siempre se evalúan como &#39;False&#39; (solo Apple Silicon)
* [Explorer] El orden de los botones de la barra de herramientas es incoherente entre los sistemas operativos
* [Frames] No agarrar nodos al mover un marco con el modificador CTRL
* [Mapa de degradado] la opción restablecer todo también debe restablecer el widget de degradado
* [GraphRender] Algunos nodos se vuelven negros al ajustar en el modo de vista previa
* [Graph] La previsualización del &quot;valor de entrada&quot; se bloquea en &quot;False&quot; al ajustar el valor booleano predeterminado (solo Apple Silicon)
* [Graph] Los nodos de puntos cercanos al borde del marco no se mueven por el marco
* [Interoperabilidad] El icono Volver a enviar no se actualiza después de enviarlo a Substance 3D Stager
* [MDL] Imposible cambiar el valor de Rugosidad en los nodos donde este parámetro está disponible
* [MDL] Conexiones no válidas en la plantilla &#39;AxF to Metallic Roughness&#39;
* [UI] La ventana &quot;Exportar salidas&quot; se puede minimizar (solo Windows)
* [UI] Las imágenes aparecen pixeladas en la pantalla Acerca de al utilizar la escala de visualización
* [UI] Las herramientas de alineación de nodos de la barra de herramientas de gráficos crean varios pasos de deshacer

### 13.0.2

*(Publicado El 27 De Julio De 2023)*

<b>Agregado:</b>

* [Gráfico de funciones] Agregar variable de sistema $getPhysicalSize
* [Pantalla de inicio] Compatibilidad para abrir archivos SBS arrastrándolos y soltándolos
* [Contenido] Asignador de splines/Asignador de flujo de spline : Añadir el parámetro &quot;Corrección no cuadrada&quot;

<b>Corregido:</b>

* [Pantalla de inicio] No mostrar la pantalla de inicio cuando se envía un archivo desde otro software
* [Pantalla de inicio] Estado incorrecto del icono de Designer en la barra de herramientas de Windows
* atlas splitter [Content]: La descripción es incorrecta
* [Contenido] Valor de referencia incorrecto en la función &#39;Lineal a sRGB (luminancia)&#39;
* [Contenido] La herramienta de visualización de números no admite resoluciones que no sean cuadradas
* Lista de puntos de [Content]: El parámetro &quot;Número de punto&quot; tiene un valor mínimo incorrecto
* [Contenido] Sombra paralela de forma: La sombra puede desaparecer cuando el mosaico está desactivado
* [Contenido] Spline (poli cuadrático): Tangentes de previsualización y thickness incorrectos en resoluciones no cuadradas no corregidas
* [Contenido] Spline (poli cuadrático): Las etiquetas de puntos no se ocultan al utilizar las opciones de inicio/fin de conexión
* [Content] Puente polinómico (lista): El parámetro &quot;Corrección no cuadrada&quot; no tiene ningún efecto
* [Contenido] Cúbica polinomial: El parámetro Corrección no cuadrada no tiene efecto en la salida de previsualización
* [Content] Asignador de splines: Procesamiento incorrecto cuando la spline tiene un thickness muy pequeño
* [Content] Nodos polinomiales: Descripción del signo alfa invertido en la información sobre herramientas de Spline Cords
* [Content] Nodos polinomiales: El parámetro &quot;Corrección no cuadrada&quot; no tiene efecto en la salida de previsualización
* [Content] Procesamiento de spline: El formato de salida es 32F absoluto
* [Content] Procesamiento de spline: La salida se fija en el rango [0, 1]
* [Content] Thickness de muestra de spline: La spline se puede restar en valores negativos
* [Content] Selección de spline: Las splines se cierran con un solo segmento de forma predeterminada
* [Bloqueo] [Cooker] Bloqueo al cargar gráficos específicos
* [Crash][UI] Bloqueo al habilitar los menús después de cargar el paquete desde la pantalla de inicio
* El vínculo &quot;Documentación del usuario&quot; de la referencia de scripts de [API] está obsoleto
* [Propiedades] La función de procesador de valores no se puede abrir en un gráfico bloqueado
* [Publish] No se pueden publicar paquetes que contengan gráficos MDL
* [UI] &#39;Administrar mi cuenta...&#39; está desactivada en el menú Ayuda
* [UI] Faltan entradas en el menú Ayuda al abrir Designer mediante un archivo

### 13.0.1

*(Publicado El 27 De Junio De 2023)*

<b>Agregado:</b>

* [Content] Spline (Poly Quadratic), Lista de puntos: agregar nombre de puntos en la salida de previsualización
* [Content] Asignador de splines: añadir un parámetro para desplazar el centro del perfil del cilindro
* [DotNode] Ordenar alfabéticamente la lista de portales de entrada

<b>Corregido:</b>

* [Contenido] Resultado incorrecto en varios nodos Spline al utilizar una distribución uniforme
* [Contenido] Errores menores en la información sobre herramientas de los nodos Spline y Path
* [Content] Transformación cuádruple en trazado: los valores predeterminados de p01 y p10 se cambian
* [Content] Transformación cuádruple: resultado incorrecto en una situación específica
* [Contenido] Círculo polinómico: El resultado &quot;Voltear dirección&quot; es incorrecto cuando no se utiliza la distribución uniforme
* [Contenido] Círculo polinómico: Las tangentes son incorrectas al ajustar los parámetros de espiral y tamaño
* [Content] Mapeado de flujo de spline: rayas negras en el resultado al utilizar alta potencia en espiral en el círculo polinómico
* [Contenido] Asignador de splines/Asignador UV: El color de fondo no funciona
* [Content] Asignador de splines: el height base es 0, lo que produce un recorte
* [Content] Asignador de splines: El height de spline se modifica mediante el multiplicador de entrada incluso cuando dicha entrada no está conectada
* [Content] Asignador de splines: no se asignan las splines que coinciden con un borde de imagen
* [Content] Asignador de splines: La escala de UV Y no tiene efecto cuando se utiliza una forma no plana
* [Content] Asignador de splines: Resistencia Z al procesar splines superpuestas del mismo height
* [Contenido] Poly Quadratic Spline: El resultado &quot;Voltear dirección&quot; es incorrecto cuando no se utiliza la distribución uniforme
* [Content] Procesamiento de spline: las uniones no se manejan de forma coherente en las opciones de Estilo de spline
* [Content] Procesamiento de spline: último segmento no dibujado
* [Content] Procesamiento de spline: la corrección no cuadrada no se aplica correctamente
* [Contenido] El color del asignador UV aparece dos veces en la biblioteca
* [DotNode] El área de ajuste de la conexión no se actualiza después de desactivar el límite de escala de texto
* [DotNode] La creación a través del menú contextual está dañada
* [DotNode] La posición del nombre del portal de entrada no se ajusta después de deshacer o rehacer un cambio de nombre
* [GraphRender] Demasiadas invalidaciones al modificar un gráfico de funciones
* [Graph] La posición del widget de transformación no se ha actualizado visualmente correctamente
* [Localización] Los valores de &#39;Rango suave&#39; y &#39;Rango duro&#39; no se localizan en los gráficos MDL
* [Parámetros] Los cambios de texto consecutivos no se registran en la pila de historial
* [Parámetros] El Hitbox para mover parámetros de entrada de gráficos en la lista no es fiable
* [Propiedades] El clic simple se considera doble en el widget de cuadro de número en proyectos pesados
* [Publish] El orden de los recursos del paquete no se conserva en el recurso publicado

### 13.0.0

*(Publicado El 6 De Junio De 2023)*

<b>Agregado:</b>

* [Graph] Nodo del portal
* [Onboarding] Nueva pantalla de inicio
* [Content] Nodo Spline (Cubic)
* [Content] Nodo spline (poli cuadrático)
* [Content] Nodo Círculo polinómico
* [Content] Nodo Lista de puntos
* [Content] Nodo Puente de spline (2 splines)
* [Content] Nodo Puente polinomial (lista)
* [Content] Nodo Append de Spline
* [Content] Nodo Seleccionar spline
* [Content] Nodo Lista de combinación de splines
* [Content] Nodo Transformación 2D polinomial
* [Content] Nodo Deformación de spline
* [Content] Nodo de Height de muestra de spline
* [Content] Nodo de Thickness de muestra de spline
* [Content] Nodo de procesamiento de spline
* dispersión [Content] en el nodo Color de spline
* [Content] Dispersión en el nodo Escala de grises polinomiales
* [Content] Nodo Color del asignador de spline
* [Content] Nodo de escala de grises del asignador de splines
* [Contenido] Nodo Color del asignador de puente spline
* [Contenido] Nodo de escala de grises del asignador de puente spline
* [Content] Nodo Spline Flow Mapper
* [Contenido] Nodo Color del asignador UV
* [Contenido] Nodo de escala de grises del asignador UV
* [Content] Rutas al nodo Splines
* [Content] Nodo Máscara a trazados
* [Contenido] Rutas nodo de transformación 2D
* [Content] Rutas Nodo polígono
* [Content] Nodo de rutas de previsualización
* [Content] Nodo Deformación de rutas
* [Content] Rutas Seleccionar nodo
* [Content] Rutas nodo de procesador de vértices
* [Content] Rutas Procesador de vértices Nodo simple
* [Content] Nodo Transformación cuádruple en ruta
* [Contenido] Oclusión ambiental con trazado de rayo v2
* [Contenido] Raytraced Bent Normal v2
* [Contenido] Sombras con trazo de rayo v2
* [Motor] Actualizar a la versión 9
* [Motor] Nodo de bucle en gráficos de funciones
* [Motor] Añadir modo sólido al degradado
* [Motor] Nodo Atomic pow() en Gráfica de funciones
* [Motor] Añadir opciones de ajuste de bordes (sujetar a borde / repetir) en el nodo Sampler
* [Motor] Muestreo más cercano en el nodo Deformación y Deformación direccional
* [Motor] Añada un modo &quot;punchthrough alfa&quot; al filtro Perfilar para las entradas de color
* [Motor] FxMap: Morflete de hemisferio
* [Motor] Operaciones atómicas Get/Set en gráficos de funciones
* Funciones [Engine]: use la función precisa de log/log2/exp, 2pow - Unificar funciones entre la cocina y el motor
* [Motor] Añada un parámetro de &quot;desplazamiento de intensidad&quot; al filtro Deformación direccional
* [API] Compatibilidad con la gestión de ajustes preestablecidos para la composición de gráficos
* [Funciones] Cambiar el nombre de entrada de las funciones de los nodos atómicos
* [Localización] Añadir portugués (Brasil), italiano (Italia) y español (España)
* [Localización] Respete la regla &quot;Idioma (país)&quot; en la lista de idiomas
* [Ajustes preestablecidos] Desactivación de los paneles &quot;Previsualización&quot; y &quot;Ajustes preestablecidos&quot; en las propiedades del gráfico al utilizar la edición en contexto
* [Gráfico de modelos de Substance] Fin de la compatibilidad de gráficos de modelos de Substance

<b>Corregido:</b>

* [Vista 3D] La visualización de cadenas largas en las estadísticas de escenas está cortada (solo macOS)
* [API] El módulo &#39;structure::Structure&#39; aún se incluye en la referencia de API
* [API] Los nodos de puntos de los gráficos MDL no tienen definición ni propiedades
* [API] Comportamiento incorrecto al establecer el parámetro de nodos de función
* [Contenido] Los nodos 3D Voronoi y 3D voronoi fractal generan una advertencia de cocción
* [Motor] El parámetro &quot;Desplazamiento de mapa de intensidad&quot; no tiene efecto en los datos de escala de grises del motor SSE2
* [Explorer] Se puede eliminar la e/s de gráficos
* [Graph] El mapa de bits se omite cuando se utiliza en instancias
* [Graph] Posición incorrecta del nodo de puntos al crearse un nodo a partir de un nodo
* [Graph] Enfoque incorrecto en el cuadro de diálogo &quot;Exponer parámetro&quot; al utilizar la tecla Intro
* [Gráfico] Resultado incorrecto en la exploración de histograma con mapa de bits en la edición de contexto
* [Localización] Solucionar varios problemas de recorte
* [Parameters] Bloqueo al eliminar un parámetro de entrada
* [Publish] Los gráficos de las carpetas se mueven a la raíz en el paquete publicado
* [Resources] Bloqueo al actualizar un recurso cargado en el disco
* [VisibleIf] Corregir regresión en evaluación de visibilidad condicional

## Versión 12

### 12.4.1

*(Lanzado: 30 de marzo de 2023)*

**Agregado:**

* [Cooker][Graph] Tenga en cuenta las etiquetas de transformación EXIF en el archivo de JPEG
* [Security] Actualización a 23,02 USD
* [Seguridad] Quitar la compatibilidad de la importación de formato de archivo Collada (.dae)
* [Modelos de Substance] Advertencia sobre el final de la vida útil de los gráficos de modelos de Substance en la próxima versión principal

**Corregido:**

* [Vista 3D][ASM] Artefacto de rugosidad de recubrimiento al utilizar CoatNormal
* [Content] Se invierte el parámetro &quot;Celdas con relleno de degradado&quot; del nodo Alveolus
* [Content] Entrada El número de nodos Multi-Switch no está sujeto
* [Contenido] Advertencia de cocción en el nodo Normal del generador de Scratches
* [Data] Bloqueo al cargar el paquete manualmente después de deshacer su carga anterior
* [Data] Bloqueo al deshacer rápidamente varias operaciones gráficas hasta la carga del paquete

### 12.4.0

*(Lanzado: 31 de enero de 2023)*

**Agregado:**

* [Vista 3D] Añadir todas las opciones del menú Mostrar como botones de la barra de herramientas
* [API] Permitir la adición de acciones a las barras de herramientas de la vista de gráfico
* [API] Permite crear/editar/evaluar un gráfico de modelo de Substance desde la API.
* [Gestión de color] Mejora la calidad de las LUT 3D horneadas en modo ACE
* [Documentación] Ejemplos de proyectos para Substance que componen gráficos
* [Documentación] Proyecto de muestra para gráficos de funciones
* [Explorer] Permite mover gráficos y recursos de un elemento principal a otro sin cerrar ni invalidar los widgets
* [Editor de degradado] Seleccionar la chincheta seleccionada al mostrar el editor de degradado
* [Graph] Añadir opción en el menú contextual de un nodo para seleccionar todos sus hijos
* [Graph] Limpia la herramienta de gráficos para detectar y eliminar los nodos no utilizados en todos los tipos de gráficos y gráficos de propiedades
* [Graph] Transformar la entrada de imagen a color/escala de grises
* [Parámetros] Añadir un bloqueo en widgets integer2
* [Parámetros] Permite escribir fórmulas básicas como un parámetro
* [Modelo de Substance] Alternar para cambiar entre valores e iconos para nodos de valores
* [UI] Botón para generar un valor aleatorio cuando se requiere una semilla aleatoria
* [UI] El elemento enfocado no se resalta en el navegador de escenas
* [UX] Restablecer intervalos del regulador cuando se restablece su valor

**Corregido:**

* [API] SDProperty.getDefaultValue() casi siempre devuelve None
* [Vista 3D] El valor de la propiedad &quot;Normal de DirectX&quot; no se comparte entre los procesadores
* [Vista 3D] La visualización de estadísticas de escena se amplía cuando la ventana gráfica es pequeña
* [Vista 3D] La propiedad de visualización de Mallas metálicas no se guarda
* [Contenido] Los parámetros de color de desenfoque radial no afectan al canal alfa
* [Localización] Se muestran reguladores y botones adicionales en Propiedades de OpenGL de entorno.
* [MDL][Modelo de Substance] Bloqueo al eliminar nodos expuestos
* [Preferencias] El archivo Default\_config nunca se vuelve a crear si se elimina
* [Modelo de Substance] Parámetro de reordenación de bloqueo que no aparece en el nivel de instancia

### 12.3.1

*(Lanzado: 24 de noviembre de 2022)*

**Agregado:**

* [3DView] Procesamiento optimizado para escenas con muchos materiales
* [3DView] Ver las salidas de un gráfico de modelo de Substance al soltarlo desde el Explorador
* [Licencia] Limpiar sistema heredado para usuarios de Linux
* [Onboarding] Actualización de la transparencia del fondo
* [Modelos de Substance] Se muestra una advertencia en la vista de gráfico cuando la entrada y la salida comparten el mismo identificador

**Corregido:**

* [3D Assets] &quot;Ayuda > Substance 3D Assets&quot; se dirige por error a Creative Cloud Desktop en Linux
* [Vista 3D] Los materiales no se crean cuando se carga la malla
* [Vista 3D] Se abre la lista de materiales al soltar el gráfico del modelo de Substance en la ventana gráfica
* [Explorer] No se puede eliminar la selección con el teclado si se incluye un gráfico de modelo de Substance
* [Explorer] Bloqueo al abrir el menú contextual del elemento de material de un recurso de malla en Mac
* [Graph] Las instancias cuyas imágenes de entrada dependen de Values generan un resultado incorrecto en los nodos siguientes
* [Gráfico] Resultado incorrecto al utilizar una cadena de subgráficos con la edición de gráficos contextual activada.
* [MDL] Bloqueo al cargar un gráfico MDL que hace referencia a un gráfico de composición con salidas obsoletas
* [MDL] El nodo de textura 2D ya no funciona
* [Onboarding] Textos recortados y no localizados
* [Incorporación] Los paneles no se muestran correctamente al iniciar la aplicación al abrir un archivo
* [Preferencias] La caché de imágenes omite la ubicación de los archivos temporales definida por el usuario
* [Propiedades] Las modificaciones realizadas en los paneles de previsualización/ajuste preestablecido se combinan en la pila Deshacer
* [Acceso directo] Los accesos directos asignados a nodos obsoletos crean conflictos y no se pueden limpiar
* [Modelos de Substance] Bloqueo al cerrar un paquete después de realizar acciones específicas
* [Modelos de Substance] Los nodos de instancia y los vínculos de los paquetes reubicados no se actualizan correctamente
* [Modelos de Substance] Al deshacer la eliminación de subgráficos, no se actualizan los nodos y vínculos de instancias de forma coherente
* [Modelos de Substance] El valor aumenta demasiado rápido en el nodo de transformación
* [UI] Los iconos de advertencia de la propiedad &quot;Visible if&quot; no tienen información sobre herramientas
* [UI] El texto de información de imagen es demasiado oscuro en la ventana gráfica de la vista 2D
* [Deshacer] Al mover un widget de posición en el modo de vista previa se almacenan todos los valores intermedios

### 12.3.0

*(Lanzado: 6 de octubre de 2022)*

**Agregado:**

* [General] Panel de bienvenida para nuevos usuarios
* [General] Panel Novedades para mejorar la detección de nuevas funciones
* [Modelo de Substance] Compatibilidad con subgráficos e instancias
* [Modelo de Substance] Compatibilidad visible Si para los parámetros expuestos
* [Modelo de Substance] Agregar compatibilidad con nodos de salida
* [Modelo de Substance] Nodo de desplazamiento de curva
* [Modelo de Substance] Curva revertir nodo
* [Modelo de Substance] Nodo de suavizado de curvas
* [Modelo de Substance] Nodo de subdivisión de curvas
* [Modelo de Substance] Nodo de inserción
* [Modelo de Substance] Actualizar el nodo &quot;Escena de filtro&quot;
* [Modelo de Substance] Hacer que los nodos no atómicos sean detectables en el menú Nodo
* [Modelo de Substance] Añada la acción &quot;Abrir referencia&quot; en el menú contextual de un nodo de instancia
* [Modelo de Substance] Añada una acción &quot;Ver en 3DView&quot; en el menú contextual de nodos que se pueden enviar a 3DView
* [Modelo de Substance] Muestra automáticamente las propiedades de un nodo después de exponerlo
* [Modelo de Substance] Crear la ventana &#39;Nuevo gráfico de modelo de Substance&#39; con la lista de plantillas
* [UI] Mejora la coherencia de las opciones de guardado de imágenes en la vista 2D y la vista 3D
* [UI] Cambie el nombre &quot;Vínculo > Malla 3D&quot; a &quot;Vínculo > Escena 3D&quot; en el menú contextual del Explorador
* [UI] El diseño de restablecimiento ahora se aplica a todas las ventanas flotantes
* [UI] Uso de la etiqueta &quot;Ver resultados en vista 3D&quot; en menús contextuales para gráficos
* [Biblioteca] Compatibilidad con gráficos de modelos de Substance no atómicos
* [SBSAR] Gráfico de soporte muestra la descripción de los resultados en SBSAR
* [Shader] Establezca el valor predeterminado del factor de teselación en 1 para todos los sombreadores
* [UI] Exponer el widget de 2 botones para parámetros booleanos
* [Motor] Actualizar a la versión 8.6.4
* [Steam] Compilación optimizada para chipset Apple Silicon (Apple M1 / M2)

**Corregido:**

* [UI] Resolver problemas de escalado de pantallas de alta resolución
* [UI] Falta la plantilla &#39;$(udim)&#39; en la lista de la ventana de procesamiento
* [UI] Bloqueo al mostrar el menú Nodo en el borde derecho de la pantalla (solo macOS)
* [UI] El botón de extensión del menú de la vista 3D no está visible
* [UI] El menú de extensión de la barra de herramientas Gráfico está incompleto
* [UI] Valor incorrecto del widget de parámetro después de deshacer la activación del rango duro
* [Vista 3D] La configuración de sombreado no predeterminada se pierde en Iray de una sesión a otra
* [Bakers] Bloqueo al cargar la ventana de horno con una escena sin mallas
* [Función] Bloqueo al copiar una instancia en su gráfico de referencia
* [Función] Solucionar un posible bloqueo al manipular nodos
* [Globalización] La cursiva no siempre se desactiva correctamente en japonés/coreano/chino
* [Graph] Identificador de reserva incorrecto para los nuevos gráficos de modelos MDL y de Substance
* [Graph] Los parámetros heredados gobernados por valores a veces se calculan incorrectamente
* [GraphRender] Bloqueo al cambiar de motor al calcular gráficos de alta resolución (solo macOS)

### 12.2.1

*(Lanzado: 4 de agosto de 2022)*

**Corregido:**

* [Gráfico] Resultados incorrectos al cambiar el tamaño principal del gráfico
* [Bloqueo] Bloqueo al calcular gráficos de composición de Substance con una resolución muy alta
* [Bloqueo] Bloqueo al quedarse sin memoria al cargar el paquete
* [Bloqueo] Bloqueo al utilizar corchetes en anotaciones de parámetros expuestos en un gráfico de modelo de Substance
* [Bloqueo] Mejora de la estabilidad del procesamiento de Substance de composición
* [Israel] Actualización a la versión 2021.1.6

### 12.2.0

*(Lanzado: 19 de julio de 2022)*

**Agregado:**

* [Apple] Compatibilidad nativa con Apple Silicon (M1) (solo versión de Creative Cloud)
* [Gráfico de modelo de Substance] Mostrar información sobre herramientas de nodos en la vista de gráficos
* [Gráfico de modelo de Substance] Mostrar información sobre herramientas de nodos en la biblioteca
* [Gráfico de modelo de Substance] Añadir una entrada de menú contextual a los nodos de previsualización
* [Gráfico de modelo de Substance] Permite al usuario crear accesos directos para la creación de nodos
* [UI] Añada la opción &quot;Ver salida en vista 2D&quot; en el menú contextual del gráfico de composición
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

**Corregido:**

* [Modelos de Substance] El rango definido en el parámetro expuesto se guarda al dejar de exponer
* [Modelos de Substance] El identificador no es fácil de usar en nodos constantes
* [Modelos de Substance] Mejora la búsqueda en función de la compatibilidad de nodos
* [UI] El orden del submenú &quot;Nuevo&quot; es incorrecto para los recursos de carpeta
* [UI] El tamaño predeterminado de la ventana principal es muy pequeño
* [UI] Las barras de herramientas no se ven afectadas por la opción Restablecer diseño
* [UI] Cuadrícula de transparencia visible en el icono de recurso de fuente en el Explorador
* [Cooker] Los gráficos de composición creados en un gráfico MDL siempre se vuelven a guardar por completo
* [Graph] Bloqueo al pegar un nodo copiado de un gráfico con un identificador en blanco
* [MDL] Bloqueo al cerrar un gráfico MDL específico
* [Performance] La aplicación no responde cuando se cargan paquetes muy grandes
* [Resources] Los recursos de escena 3D se pueden importar en un caso específico

### 12.1.1

*(Lanzado: 07 de junio de 2022)*

**Corregido:**

* [Content] El recurso &quot;bluenoise\_256&quot; tiene un atributo &quot;colorspace&quot; definido en algunos nodos
* [Contenido] Los nodos &quot;Obtener tamaño&quot; no aparecen en la biblioteca y la versión en escala de grises está mal etiquetada
* [Contenido] El parámetro &quot;Raíz de color aleatoria&quot; en nodos 2D Voronoi no tiene efecto
* [SBSRender] Al exportar un gráfico a EXR, no se genera el mismo bpc que en Designer
* [Modelos de Substance] El &quot;tipo gamma&quot; no debe aparecer en las propiedades del parámetro expuesto
* [Modelos de Substance] Bloqueo al utilizar corchetes en anotaciones de parámetros expuestos

### 12.1.0

*(Lanzado: 26 de abril de 2022)*

**Agregado:**

* [Principal] Nuevo contenido para gráficos de materiales
* [Principal] Enviar materiales a Stager
* [Principal] Compatibilidad con archivos USD
* [Principal] Mejorar la notificación de errores en la interfaz de usuario
* [Principal] Nodos de administración de escenas para gráficos de modelos
* [Contenido] Añadir más opciones a los sonidos de Perlin 3D (mosaico, absoluto...)
* [Contenido] Nuevo nodo Fractal de ruido revestido 3D
* [Content] Nuevo nodo Desplazamiento de textura 3D
* [Contenido] Nuevo nodo Posición de textura 3D
* [Contenido] Nuevo nodo Superficie de procesamiento de textura 3D
* [Content] Nuevo nodo Volumen de procesamiento de textura 3D
* [Content] Nuevo nodo de Campo de distancia con signo de textura 3D
* [Content] Nuevo nodo Recorte automático
* [Content] Nuevas funciones de aceleración
* [Content] Nuevos nodos de Extend Shape
* [Contenido] Nuevos mapas de Suciedad
* [Content] Nuevo nodo Rotación no uniforme
* [Contenido] Nuevo filtro Tabla de área sumada
* [Contenido] Generador de Azulejos Nuevos Aleatorios 2
* [Content] Nuevo generador de patrones de Triangle Grid
* [Content] Nueva versión del nodo Cuantificar escala de grises
* [Contenido] Nuevos ruidos fractales de Voronoi y Voronoi (2D/3D)
* [Contenido] Umbral: agregar modo de comparación &#39;Inferior&#39; e &#39;Inferior e igual&#39;
* [Contenido][Vista 3D] Añadir un ajuste de malla para mostrar estructuras a los recursos enviados
* [Modelos de Substance] Nuevo nodo Expandir instancias de grupo
* [Modelos de Substance] Nuevo nodo de Fuse
* [Modelos de Substance] Nuevo nodo Cambiar nombre
* [Modelos de Substance] Nuevo nodo Reparent
* [Modelos de Substance] Nuevo nodo Definir tabla dinámica
* [Modelos de Substance] Actualizar a SDK 1.6.0
* [UI] Mejora el comportamiento del menú Nodo al hacer clic incorrectamente
* [UI] Abrir subgráficos en la misma pestaña incluso si están anclados
* [UI] Botón Eliminar borde de la barra de título del panel Explorador
* [UI] Opción Guardar &quot;No volver a mostrar&quot; en la pantalla de bienvenida entre las distintas versiones
* [ThirdParty] Actualice Qt (y QtForPython) a 5.15.8
* [ThirdParty] Actualización de Python a 3.9.9
* [ThirdParty] Actualizar OpenSSL a 1.1.1m
* [Vista 3D] Muestra la unidad de cuadrícula en la ventana gráfica cuando se activa el ayudante &quot;Eje&quot;
* [Automatización] Proporcionar la herramienta de línea de comandos sbsbaker con Designer
* [Gestión de color] Implementación del nuevo motor de GPU para Adobe ACE
* [Cocina] Añadir una opción para cocinar un paquete sin marca de tiempo
* [Graph] Agregar insignias en el gráfico FxMap
* [Biblioteca] Añadir nuevo filtro para las funciones de aceleración
* [Player] Compatibilidad con USD
* [Propiedades] Añada un error de advertencia en el parámetro &quot;Ruta de recurso PKG&quot; de un nodo Bitmap cuando no se encuentra el recurso
* [Substance Engine] Actualización a la versión 8.4.1
* [Yebis] Advertencia al usuario de que los efectos posteriores de Yebis se eliminarán en la siguiente versión
* [Documentación] Nueva página &quot;Advertencias y errores&quot;
* [Documentación] Nueva página que describe la herencia en los Substance de composición
* [Documentación] Actualizar la sección &#39;Iray&#39;
* [Documentación] Sección Actualización de &#39;Gráficos MDL&#39;

**Corregido:**

* [UI] Problemas de recorte en la información sobre herramientas de las plantillas en la nueva ventana de gráficos
* [UI] Texto en blanco difícil de leer en nodos al utilizar el modo oscuro en macOS
* [UI] Problema de diseño en algunos cuadros de diálogo
* [UI] El mensaje de advertencia aparece truncado al crear un gráfico de funciones de Substance en el Explorador.
* [UX] El selector de color desciende en cada nueva apertura
* [UX] La ventana del editor de degradados se mueve hacia arriba cada vez que se genera
* [UX] Las propiedades de los gráficos no se muestran automáticamente para los paquetes cargados
* [Content] Asignador de Flood Fill: Selección de entrada incorrecta en un caso específico
* Flood Fill [Content]: Sangrado de texto en botones de parámetros booleanos
* [Contenido] Rango incorrecto para el parámetro Ángulo de luz de la primera muestra del nodo Multicángulo a Normal
* [Modelos de Substance] Las propiedades del nodo muestran el identificador en lugar del rótulo
* [Modelos de Substance][Vista 3D] Problema de actualización al volver a abrir un proyecto
* [Modelos de Substance][Vista en 3D] Problema de actualización al utilizar la vista previa de malla metálica
* [Parámetros] Bloqueo al eliminar entradas de gráficos en sucesión rápida en un caso específico
* [Parameters] Bloqueo al restablecer un parámetro de instancia mientras se edita la descripción de la referencia
* [Bitmap] La detección de UDIM no se activa para los archivos de mapa de bits colocados en el gráfico
* [Graph] Los nodos Bitmap/SVG no se invalidan cuando el recurso se modifica en el disco después de cargar el paquete
* [GraphRender] Pérdida de memoria cuando se cancela la evaluación de gráficos del Substance
* [Localization] La cadena &quot;Rebake all maps for this resource&quot; aparece sin localizar
* [MDL] Parámetro expuesto inicializado en 0 si la entrada está conectada a un nodo Punto no conectado
* [Preferencias] La información sobre herramientas se muestra incluso cuando el cursor está en un espacio vacío
* [Propiedades] Al deshacer un cambio de valor de espacio de color se establece el valor predeterminado en un caso específico
* [Text] No se puede deshacer el cambio de fuente al recurso de fuente que falta

## Versión 11

### 11.3.3

*(Lanzado: 01 de febrero de 2022)*

**Corregido:**

* [Modelos de Substance] En algunos casos, los rangos se pueden perder
* [Modelos de Substance] [Exportar] La escala es diferente en función del tipo de archivo
* [Modelos de Substance][Exportar] Las mallas están duplicadas

### 11.3.2

*(Lanzado: 25 de enero de 2022)*

**Agregado:**

* [Documentación] Actualizar la sección &#39;Iray&#39;

**Corregido:**

* [Modelos de Substance] No se puede publicar un paquete que contenga gráficos de modelos de Substance
* [Modelos de Substance] Imposible exportar un gráfico de modelo en algunos casos específicos
* [Modelos de Substance] Hacer más coherentes los rangos de parámetros
* [MDL] Bloqueo al exportar un archivo MDLE
* [MDL] Se genera un archivo .mdl incorrecto cuando un gráfico MDL contiene nodos Dot conectados a parámetros expuestos
* [Vista 2D] Optimizar la visualización de las herramientas de pintura
* [Contenido] Configuración incoherente del parámetro de tamaño de salida en los gráficos de origen de la plantilla
* [Propiedades] Las etiquetas de los rangos de software y hardware son incorrectas en el panel de propiedades de los nodos expuestos de los modelos MDL y Substance
* [Templates] Actualizar los valores predeterminados de las entradas en la plantilla &#39;Sampler filter&#39;

### 11.3.1

*(Lanzado: 13 de diciembre de 2021)*

**Agregado:**

* [Graph] Añada una advertencia al eliminar un gráfico utilizado en otro gráfico o paquete

**Corregido:**

* [UI] El editor de color es demasiado pequeño al utilizar un diseño de interfaz de usuario específico
* [UI] Bloqueo al actualizar la lista de plantillas usadas recientemente
* [UI] Resaltado incorrecto en las preferencias de métodos abreviados
* [UI] El tamaño de la ventana principal es demasiado pequeño después de reiniciar una sesión con ventanas (solo macOS)
* [UI] El conjunto acoplado maximizado no se minimiza al salir (solo Windows)
* [UI] Falta espacio en la información sobre el parámetro &quot;Subir de nivel&quot; [3DView] El eje en la vista 3D es demasiado pequeño cuando el cuadro delimitador de la escena es fino
* [UI] Problema de estilo en algún texto de la configuración del proyecto para el idioma francés
* [Modelos de Substance] La sujeción de los parámetros expuestos no se guarda en las sesiones
* [Modelos de Substance] El modificador Mayús sigue activado después de utilizar el método abreviado de vista previa de nodo
* [Modelos de Substance] Algunos nodos eliminados permanecen en el SBSM exportado
* [Modelos de Substance] Los nodos de destino de la evaluación se acumulan y no se eliminan. [API] Se produce un bloqueo al procesar el nodo de curva cuyas propiedades se definieron mediante la API.
* [Bakers] El widget &quot;Color de material&quot; no está visible y no funciona del modo esperado
* Nodo de Renderización PBR [Content]: cálculo interno no realizado con la resolución del nodo
* [Gráfico de funciones] Los mensajes que muestran los tipos esperados son incorrectos en algunos casos
* [Graph] Entrada relativa a la entrada: los parámetros heredados son incorrectos con instancias conectadas
* [MDL] Las instancias de gráficos de Substance no se actualizan de forma fiable en los gráficos MDL
* [Publish] Error al publicar el gráfico que contiene dependencias circulares
* [Métodos abreviados] Mayús + Espacio no debe ser un método abreviado de teclado asignable para nodos
* [Templates] Se omite el formato de salida de las plantillas personalizadas

### 11.3.0

*(Lanzado: 24 de noviembre de 2021)*

**Agregado:**

* [Modelos de Substance] Añadir información sobre herramientas para parámetros de nodos
* [Modelos de Substance] Permite mostrar en superposición en la ventana gráfica 3D el resultado de un nodo intermedio
* [Modelos de Substance] Mejorar el modo en que se visualizan los Basis
* [Modelos de Substance] Conservar la jerarquía de objetos al exportar un gráfico de modelo de Substance a .fbx
* [Modelos de Substance] Compatibilidad con varios materiales en la exportación FBX/OBJ desde el gráfico del modelo de Substance
* [Modelos de Substance][Contenido] Nodo de objeto
* [Modelos de Substance][Contenido] Nodo Transformación generativa
* [Modelos de Substance][Contenido] Nodo Organic Pattern
* [Modelos de Substance][Contenido] Partículas del nodo Instancias
* [Modelos de Substance][Contenido] Nodo de eliminación de partículas
* [Modelos de Substance][Contenido] Torno nodo
* [Substance models][Content] Nodo de shell
* [Modelos de Substance][Contenido] Nodo de proyección
* [Modelos de Substance][Contenido] Nodo de recorte de curva
* [Modelos de Substance][Contenido] Actualizar el nodo Sampler de la curva
* [Modelos de Substance][Contenido] Actualizar nodo Sampler de malla
* [Modelos de Substance][Contenido] Actualizar el nodo Variación
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
* [UI][macOS] Diseño de interfaz predeterminado incorrecto después de iniciar la aplicación
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

### 11.2.2

*(Lanzado: 28 de septiembre de 2021)*

**Agregado:**

* [Propiedades] Añadir nuevos tipos de gráficos para calcomanías, atlas, luces de entorno y texturas claras

**Corregido:**

* [UI] Diseño de interfaz incorrecto después de iniciar la aplicación
* [Estabilidad] Se bloquea al salir del modo de suspensión en Windows y al conectar o desconectar pantallas
* [Vista 3D] La creación de un recurso Escena 3D a partir del gráfico de modelo de Substance Escena no tiene efecto
* [Blend] Faltan los valores de enumeración al exponer el modo de fusión
* [Export] La exportación de escenas de modelos de Substance genera una geometría duplicada
* [MDL] Bloqueo al abrir un archivo SBS específico
* [Mesh] Bloqueo al vincular una malla específica con una geometría defectuosa
* [Modelos de Substance] La exportación falla cuando el valor predeterminado del parámetro expuesto está fuera del rango flexible

### 11.2.1

*(Lanzado: 27 de julio de 2021)*

**Agregado:**

* [Modelo de Substance] Actualizar a la versión 1.0.3
* [Modelo de Substance] Completar y mejorar la documentación de gráficos de modelos de Substance
* [Modelo de Substance] Mostrar registros en la consola
* [Modelo de Substance][ScatterOnCurves] Cambiar el valor predeterminado del espaciado
* [Modelo de Substance][ScatterOnCurves] Quitar el parámetro HalfSpaceOddEven innecesario
* [Modelo de Substance][Transformar] Actualizar rango flexible de rotación de Euler
* [Publish] Recordar la configuración en la ventana de Publish
* [Publish] Avisar al usuario cuando al menos una dependencia tenga cambios sin guardar
* [Publish] Campo Inicializar &quot;ruta de archivo&quot;
* [Publish] Añadir comentarios visuales durante la publicación
* [Interoperabilidad] Añadir el comando &quot;Enviar al reproductor&quot; al menú &quot;Enviar a&quot;
* [Interoperabilidad] Simplificar el flujo de trabajo de envío y reenvío a Sampler y Painter
* [API] Agregue SDApplication.getVersion() para permitir recuperar la versión de la aplicación host
* [Explorador] Agregar una acción Abrir a elementos de gráfico de modelo de Substance
* [Graph] Desactivar acciones &quot;Ver en vista 3d&quot; para nodos de instancia fantasma

**Corregido:**

* [Modelo de Substance] Bloqueo al eliminar una secuencia
* [Modelo de Substance] Las bases no se dibujan correctamente en algunos casos
* [Modelo de Substance] Error al exportar proyectos específicos
* [Modelo de Substance] La asignación de materiales se interrumpe al abrir un proyecto con Iray activado
* [Modelo de Substance] El rango mínimo de hardware no funciona correctamente en determinadas circunstancias
* [Modelo de Substance] [Primitivo] El primer nivel de subdivisión de la icosfera no funciona
* [Modelo de Substance][RandomFloat] Controle correctamente el caso donde Min >= Max
* [Vista 3D] Bloqueo al arrastrar y colocar mapas
* [Vista 3D] Las cadenas expuestas en materiales MDL utilizan el widget de espacio de color
* [Vista 3D] [Panaderos] Los objetos con elementos primarios no se controlan correctamente
* [Vista 3D] Mensaje de advertencia sobre el nombre de uso &quot;heightScale&quot; del archivo .glslfx heredado
* [Contenido] Advertencias de cocción en el nodo Extrusión de altura
* [Contenido] El nodo Irradiancia de RT no aparece en la biblioteca
* [Contenido] Sombras de RT: mensajes de advertencia de cocción en la consola
* [Graph] Bloqueo al abrir un archivo con algunos nodos deshabilitados
* [Graph] El nodo de puntos no funciona correctamente en MDL Graph cuando se selecciona un vínculo
* [Graph] La vista de gráficos no se vuelve a abrir automáticamente después de volver a cargar un paquete
* [Interoperabilidad] Cuadro de diálogo de error al seleccionar Descargar... al enviar al Reproductor
* [Interoperabilidad] El reenvío después de eliminar todas las salidas produce errores de API
* [Interoperabilidad] El reenvío justo después de cerrar la aplicación de destino produce errores de API
* [Explorer] [Graph] Después de volver a cargar un paquete, el primer gráfico abierto no es el primer gráfico del paquete
* [Explorer] Los nuevos gráficos de un paquete no se colocan de la misma manera en función de su tipo
* [Explorer] No se puede abrir un gráfico de modelo de Substance o un recurso de escena después de moverlo en el explorador
* [Explorer] Bloqueo al mover un gráfico de modelo de Substance a la jerarquía de paquetes
* [Biblioteca] Los archivos SBSAR permanecen en la ubicación de los archivos temporales
* [Biblioteca] Los archivos XML permanecen en la ubicación de los archivos temporales
* [Player] El material no tiene ningún impacto en la vista 3D cuando el idioma se establece en japonés
* [Player] El vínculo de descarga del Substance Player no está actualizado
* [Widget de color] La ventana del editor de color se mueve a la parte superior de la pantalla
* [IRay] Solucionar la carga del módulo IRay en Windows cuando el directorio de la aplicación contiene caracteres que no son ascii
* [Preferencias] El panel MDL se muestra dos veces en Project
* [API] Los nodos de FxMap no admiten getPropertyGraph()

### 11.2.0

*(Lanzado: 23 de junio de 2021)*

**Agregado:**

* [Marca] Substance Designer se convierte en Adobe Substance 3D Designer
* [Modelos de Substance] Nuevos gráficos de modelos de Substance para crear modelos 3D de procedimiento
* [Contenido] Añadir nuevos mapas de entorno HDR
* [Content] Nuevo nodo Normal doblado
* [Contenido] Nuevo nodo de Oclusión de ambiente de RT
* [Contenido] Nuevo nodo de RT Caustics
* [Contenido] Nuevo nodo de RT Caustics
* [Contenido] Nuevo nodo Irradiancia RT
* [Content] Nuevo nodo Sombras de RT
* [Interoperabilidad] Enviar recurso a Painter, iniciará Painter y agregará o actualizará el recurso en la biblioteca (requiere un plan Substance 3D de Adobe)
* [Interoperabilidad] Enviar recurso a Sampler, iniciará Sampler y agregará o actualizará el recurso en la biblioteca (requiere un plan Substance 3D de Adobe)
* [Interoperabilidad] Examine el recurso en Adobe Bridge y se iniciará Bridge en la ubicación del recurso (requiere un plan de Adobe Substance 3D)
* [ASM] Compatibilidad con el nuevo Adobe Standard Material (ASM) en Gráfico de Substance y MDL Graph
* [ASM] Adición de plantillas de ASM
* [ASM] Agregar sombreador de OpenGL para ASM
* [ASM] Establecer el sombreador de ASM como sombreador predeterminado
* [General] Agregar todos los archivos temporales al directorio temporal definido por el usuario
* [General] Nuevo comando &#39;Guardar una copia como&#39;
* [General] Menú Actualizar archivo
* [General] Menú Ayuda de actualización
* [Publish] Nueva ventana de publicación
* [Publish] Opción Añadir en las preferencias para no guardar el archivo SBSAR al publicar un archivo SBSAR
* [Propiedades] Agregar un campo de tipo de gráfico a las propiedades del gráfico
* [Propiedades] Reordena las propiedades de los gráficos de una forma más relevante
* [Branding] Nueva ventana Acerca de
* [Branding] Actualizar el estilo de aplicación
* [GLSLFX] Añadir una etiqueta a las técnicas
* [GLSLFX] Añada la posibilidad de establecer la etiqueta de un sombreador GLSLFX
* [Metadatos] Añadir metadatos en los recursos del paquete
* [Metadatos] Permitir la edición de metadatos para gráficos, entradas, salidas y recursos
* [Localización] Nuevas traducciones en alemán, francés y chino simplificado
* [UX] Zoom inverso en la vista 3D en el caso de arrastrar el ratón
* [AXF] Actualice a la versión 1.8.0
* [Registros] Agregar complementos instalados a los registros
* [VFX] Añadir configuración de ACES 1.2 OpenColorIO
* [API de Python] Agregue un método para consultar el directorio tmp especificado en la configuración
* [API de Python] Agregue un método isModified a SDPackage para comprobar si se ha guardado un paquete
* [API de Python] Añadir algunos métodos de conversión de color a SDColorManagementEngine
* [API de Python] Eliminación de objetos de gráficos (comentarios, ubicaciones, fotogramas, ...)
* [API de Python] Exponer la propiedad de Tamaño físico para nodos de instancias de gráficos
* [API de Python] Exponer y guardar una copia como
* [API de Python] Solucionar el método SDPackageMgr.savePackage
* [API de Python] Obtener una lista de los objetos de gráfico seleccionados
* [API de Python] Introducir nuevos nombres de método para trabajar con selecciones de gráficos
* [API de Python] Los complementos no pueden agregar acciones al primer panel del explorador creado

**Corregido:**

* [Parámetros] Los valores negativos en los parámetros Integer1 desplegables producen un comportamiento incongruente en la instancia
* [Parámetros] Problema al incrementar un valor en un widget de ángulo
* [Graph] Problemas de temporización cuando la salida se muestra en la vista 2D o 3D.
* [Internacionalización] Algunos caracteres específicos se convierten en espacios en los identificadores de archivo
* [Preferencias] La etiqueta del archivo &quot;Proyecto de usuario&quot; no se traduce del japonés
* [API de Python] Error de recursividad al ejecutar el método SDUIMgr.getCurrentGraphSelectedNodes()
* [API de Python] SDApplication.getPath(SDApplicationPath.InstallationDir) no devuelve nada
* [API de Python] SDSBSARExporter no envía notificaciones de almacenamiento de archivos

### 11.1.2 (2021.1.2)

*(Lanzado: 17 de marzo de 2021)*

**Corregido:**

* [Biblioteca] Las miniaturas no se actualizan de forma coherente
* [Contenido] La propiedad &#39;Gráficos de transformación de vectores&#39; &#39;Proporción de píxeles&#39; está establecida en &#39;Ampliación (absoluta)&#39;
* [Contenido] Los mapas de bits utilizados en las herramientas de pintura aparecen en el menú Nodo
* [Contenido] Salida NaN para entrada de color plano en el nodo Niveles automáticos con precisión de punto flotante
* [Motor][SSE2] El valor &quot;Nivel en medio&quot; distinto de 0,5 genera una salida 1,0
* [Miniatura] Los mapas de entrada se reducen a 256
* [UI] Las sugerencias de los nodos atómicos tienen un salto de línea incorrecto

### 11.1.1 (2021.1.1)

*(Lanzado: 10 de febrero de 2021)*

**Corregido:**

* [Vista 3D] Problema de procesamiento al utilizar subconjuntos que tienen altas frecuencias en el mapa normal
* [Vista 3D] Las imágenes no se aplican si la propiedad de salida &quot;Componente&quot; no está establecida en RGBA o RGB
* [Vista 3D] Las escenas no se cargan correctamente en una situación específica
* [UI] El campo de entrada &quot;Archivo de textura&quot; del Editor de pinceles se escala verticalmente
* [UI] Los botones Fijar y Acoplar desaparecen de la pestaña cuando la pestaña activa está cerrada
* [Panaderos] Resultado incorrecto cuando la caja global de mallas de poliéster altas no incluye el origen de la escena
* [Gestión de color] La propiedad de material de textura de color base sRGB no se sobrescribe en el estado de escena personalizado
* [Console] El mensaje de registro &quot;GPU disponibles&quot; no muestra las GPU y aparece de forma aleatoria
* [Console] Se registra una cadena incorrecta al utilizar la exportación por lotes
* El parámetro &quot;Formato normal de entrada&quot; del Atlas splitter [Content] afecta al canal rojo en lugar de al verde
* [Cooker] Bloqueo o salida NaN al utilizar \*.mapas de bits de superficie en SBSAR
* [Motor] Los valores de salida del mapa de degradado fuera del intervalo se ejecutan en bucle hasta 0 cuando el formato de salida tiene un intervalo de 0 a 1
* [Parámetros] Los reguladores Mín./Máx./Por defecto no se ajustan automáticamente en la ventana Exponer parámetro
* [SBSAR] Bloqueo al importar algunos SBSAR
* [SVG] Bloqueo al cancelar la importación de recursos

### 11.1.0 (2021.1.0)

*(Lanzado: 28 de enero de 2021)*

**Agregado:**

* [Manchas de color] Compatibilidad con colores de Pantone en Designer
* [Graph] Deshabilitar nodos
* [Vista 3D] Exportación de mallas teseladas desde la ventana gráfica
* [Internationalization] Actualizar versión japonesa
* [Vista 3D] Optimice el consumo de memoria cuando no utilice Iray
* [API de Python] Añadir el método SDResource.delete() para eliminar un SDResource
* [API de Python] Añadir compatibilidad con tintas planas a la API de Python
* [API de Python] Nueva devolución de llamada que se activa cuando se cierra un paquete
* [Vista 2D] Convertir la base de datos de pinceles del formato SQLite a Json
* [Vista 2D] Mejora del rendimiento y la fiabilidad del procesamiento (cálculo de CPU)
* [Biblioteca] Añadir la opción &quot;Excluir patrón&quot; en la configuración del proyecto
* [Biblioteca] Cambiar el nombre &quot;Excluir patrón&quot; a Excluir extensiones de archivo&quot; en la configuración del proyecto
* [UX] Quitar &#39;?&#39; en las barras de título de la ventana de Windows
* [UX] Mueva el método abreviado Ctrl+E a &#39;Abrir referencia&#39; cuando la edición en contexto está desactivada
* [Panaderos] Eliminación de la caché de previsualización al eliminar un panadero de la lista de pasteles
* [Rendimiento] Mejora el presupuesto de caché de imágenes en el hardware con GPU con memoria compartida
* [Preferencias] Adaptar el valor &quot;Límite de caché de GPU&quot; al grupo de memoria disponible
* [Propiedades] Mostrar atributo de Tamaño físico en instancia de nodo
* [Scripting] Marcar el sistema de scripts externo como obsoleto
* [Compartir] Quitar funciones de &quot;Exportar a Substance share&quot;

**Corregido:**

* [Contenido] Orden de E/S incoherente en nodos de material
* [Contenido] La entrada principal en los nodos de deformación es incoherente
* [Contenido] Resolver advertencias de cocina del nodo Desenfoque radial
* [Exportar] La exportación por lotes con el motor de CPU utiliza VRAM para determinar el presupuesto de memoria
* [Exportar] Al exportar a una ruta que no existe, se crean las carpetas
* [Exportar] El presupuesto de memoria es demasiado bajo al utilizar la exportación por lotes
* [Vista 2D] Artefactos/bandas al copiar imágenes HDR en el portapapeles
* [Vista 2D] Al exportar imágenes de recursos, siempre se exportan 8 bits
* [Vista 3D] Iray: cambiar el valor normal con el editor produce un resultado extraño
* [Vista 3D] Iray: la desactivación del canal normal no produce el resultado correcto
* [Biblioteca] El filtrado por URL no funciona correctamente
* [Biblioteca] Los recursos que coinciden con un patrón excluido de la biblioteca no se pueden importar manualmente
* [Bakers] Cambiar el nombre de un panadero no afecta a su entrada en la lista de vista previa de la vista 2D
* [Explorer] Pérdida de sincronización entre el Explorador y los datos del gráfico
* [Gráfico de funciones] Bloqueo al establecer un nodo de función con un tipo de salida no coincidente como salida
* [MDL] Los nodos de instancia de SBS no tienen vista previa, la salida es 0 y no activan el cálculo de gráficos
* [API de Python] La propiedad &#39;editor&#39; del parámetro de entrada no se puede modificar
* [Python] El restablecimiento del diseño no restablece correctamente los muelles creados por Python
* [Recursos] No se puede vincular o importar el documento del PSD de 32 bits

## Versión 10

### 10.2.2 (2020.2.2)

*(Lanzado: 17 de diciembre de 2020)*

**Agregado:**

* [Vista 3D] Restauración de la posición de la cámara almacenada en un recurso de escena
* [Graph] Quitar &quot;nodos de entrada&quot; en el menú contextual para FXMap y el procesador de valores

**Corregido:**

* [Contenido] Orden de E/S incoherente en nodos de material
* [Contenido] Renderización PBR: muestreo de IBL incorrecto para la aportación de specular
* [Contenido] Renderización PBR: algunos píxeles siempre son transparentes
* [Contenido] Renderización PBR: La salida UV es incorrecta para la forma del cilindro
* [Content] El parámetro &#39;Pattern Specific&#39; de Splatter Circular no tiene efecto
* [MDL] Bloqueo al crear y conectar un nodo
* [MDL] Bloqueo al duplicar un constructor de matriz de color[] con la entrada de valor expuesto conectada
* [MDL] Bloqueo al volver a conectar una conexión no válida
* [MDL] Los MDL exportados tienen parámetros duplicados
* [MDL] Los parámetros expuestos no se exportan a un archivo .mdl
* [Parámetros] Un parámetro de nodo se puede definir dos veces en el SBS en un caso específico
* [Parameters] Bloqueo al obtener el tipo de salida del gráfico de funciones de un parámetro
* [Parámetros] Bloqueo al seleccionar la opción &quot;Editar entrada de gráfico expuesta&quot; si no existe ninguna entrada coincidente.
* [Vista 3D] El procesador OpenGL no tiene correctamente en cuenta el uso de &quot;Entorno&quot;
* [Vista 3D] IOR es 0 y debe restablecerse en un caso específico
* [Vista 3D] Las UV de plano/plano de alta resolución se desplazan
* [Bitmap] Bloqueo al cancelar la importación de recursos
* [Bitmap] Bloqueo al crear un nuevo nodo de mapa de bits con un tipo de archivo no compatible
* [Dependencias] Bloqueo al deshacer &#39;Reubicar&#39; para resolver una instancia de Ghost
* [Gráfica de funciones] Bloqueo al abrir el gráfico de funciones de un parámetro
* [Editor de degradado] Al mover los reguladores y las teclas se registran demasiadas acciones en la pila de historial
* [Licencia] Bloqueo al analizar un archivo license.key no válido
* [SBSAR] Los nodos de instancia SBSAR no se pueden crear desde la biblioteca si los gráficos expuestos están en carpetas

### 10.2.1 (2020.2.1)

*(Lanzado: 4 de noviembre de 2020)*

**Corregido:**

* [General] Bloqueo al salir del modo de suspensión de Windows
* [General] Bloqueo al deshacer después de cargar un recurso de escena 3D
* [Motor] Las líneas de artefactos aparecen en la salida del nodo Distancia en Direct3D
* [Motor] Bloqueo al seleccionar el nodo Mapa de degradado en un gráfico actualizado
* [Motor] No se muestra ninguna advertencia cuando se introduce un valor predeterminado distinto de 0 en el modo de compatibilidad Motor v7
* [Vista 3D] La opción Quitar todo (Remove All) deja mallas con materiales predefinidos sin ningún material aplicado
* [Vista 3D] La opción Restablecer escena elimina todas las texturas de la malla en Irak
* [Vista 3D] OpenGL: la modificación del valor predeterminado de una muestra en un archivo .glslfx no se refleja correctamente en la interfaz de usuario
* [Vista 3D] Píxeles rojos y negros en el borde derecho de las imágenes representadas en OpenGL
* [Dependencies] No se pueden reubicar las dependencias que faltan del tipo &#39;Other&#39;
* [Dependencies] Bloqueo al salir cuando el Visor de dependencias está abierto
* [Graph] Bloqueo al duplicar un nodo de instancia Ghost
* [Graph] La edición en contexto está disponible mediante pulsación de tecla cuando está desactivada en Preferencias
* [UI] La ventana de advertencia Buscar reproductor tiene un título incorrecto
* [UI] El asistente de activación tiene un comportamiento incorrecto
* [Explorer] Los paquetes combinados siempre se pueden editar en Windows
* [MDL] Bloqueo al cargar el gráfico de la versión anterior con conexiones ahora no válidas
* [Propiedades] El color predeterminado del nodo de entrada no se actualiza al deshacer
* [SBSRender] No se utilizan perfiles ICC de mapas de bits inyectados

### 10.2.0 (2020.2.0)

*(Lanzado: 12 de octubre de 2020)*

**Agregado:**

* [Content] Añadir nodo &quot;Sección cruzada&quot;
* [Contenido] Añada la función &quot;Cross product vec2&quot; a functions.sbs
* [Contenido] Añadir nodo de valor &quot;Obtener tamaño&quot;
* [Contenido] Añada la función &quot;Orthogonal vec2&quot; a functions.sbs
* [Contenido] Añadir funciones Average a functions.sbs
* [Contenido] Añadir filtro de umbral
* [Contenido] Coincidencia de color: añadir una entrada de máscara para especificar dónde aplicar el filtro
* [Contenido] Tile Generator/Sampler: añadir nuevas opciones para controlar el tamaño del patrón
* [Contenido] Actualizar nodo de Renderización PBR con valor predeterminado para entradas de imagen
* [Parámetros] Añada iconos de advertencia para resaltar problemas en Parámetros de instancia
* [Parámetros] Ignorar instrucciones If visibles para entradas/salidas que implican parámetros que tienen una función aplicada
* [Parámetros] Mejora de la experiencia de usuario para la asociación de grupos
* [Parámetros] Repaso de la forma de exponer un solo parámetro
* [Parámetros] Resaltar parámetros expuestos
* [Parámetros] Mejorar Limpieza de parámetros no utilizados
* [Engine] Nodo de curva: nueva opción para generar la textura de la curva
* [Motor] Valores predeterminados en imágenes de entrada
* [Motor] Nodo de distancia: nuevos modos de distancia (distancias de Manhattan y Chebyshev)
* [Motor] Nodo de degradado: nuevo modo de interpolación para tener una mezcla más natural entre colores
* [UX] Algunos parámetros aparecen ahora atenuados en función de otros parámetros
* [UX] Acepte colores de RGB de 6 dígitos en el campo hexadecimal del Selector de color
* [UX] Evite mostrar las propiedades de los comentarios tan pronto como se seleccionan
* [UX] Visualización de grupos relevantes al empezar a escribir un nombre de grupo
* [UX] Acceso directo para reexportar salidas de gráficos
* [UX] Haga que todas las combinaciones de campos de texto desplegables tengan un aspecto diferente al de las combinaciones normales
* [GraphRender] Muestra las miniaturas de los nodos una a una y no sólo cuando se calculan todos
* [GraphRender] Mejora el retraso de cancelación durante el procesamiento de gráficos
* [GraphRender] Mejorar la precisión de la barra de progreso de procesamiento
* [Miniaturas] Cálculo automático de miniaturas (icono)
* [Miniaturas] Repaso de la experiencia de usuario para añadir una miniatura (icono) a un paquete
* [Preferencias] Habilitar Trazado de rayos de GPU de forma predeterminada para nuevos usuarios
* [Preferencias] 3DView / OpenGL / Calidad: reemplazar el regulador para los recuentos de muestras por una lista de opciones más intuitiva
* [Panaderos] Mejorar el rendimiento de los procesos posteriores
* [Gestión de color] Mostrar el espacio de color de trabajo actual en el cuadro de diálogo de preferencias.
* [Iray] Cambia automáticamente al modo de CPU cuando no hay GPU compatible
* [Prestaciones] Mejorar el tiempo de respuesta para calcular el nodo en el que estamos interesados (ahora calculado primero)
* [API de Python] Nuevo método addActionToExplorerToolbar para añadir iconos a la barra de herramientas del explorador
* [Resources] Actualización a FBX 2020.0.1
* [iRay] Actualización a Iray 2020.1.0
* [API] Añadir acceso de Python a la configuración y las propiedades de gestión de color

**Corregido:**

* [Gráfico] Al cambiar el tamaño principal o el mosaico uv, no se cancela el procesamiento actual
* [Graph] Bloqueo al mover una conexión de salida y pulsar Alt+LMB
* [Graph] Bloqueo al mover conexiones en modo Material o Material compacto
* [Graph] Los nodos de entrada no pueden previsualizar recursos de mapa de bits
* [Graph] Compatibilidad de nodos interrumpida en instancias
* [Graph] Se invalidan demasiados nodos al cambiar un parámetro de gráfico
* [Content] La forma de salida &quot;Shape Extrude&quot; se voltea en casos específicos: se necesita una nueva versión, la antigua ya no se usa
* [Contenido] Resultado incorrecto con la variación de color personalizada en el nodo Coincidencia de color
* [Contenido] La proporción de tamaño X/Y en Atlas scatter tiene el efecto contrario
* [Contenido] La proporción de tamaño X/Y en la salpicadura de formas tiene el efecto contrario
* [Vista 3D] Bloqueo en la operación Deshacer después de cargar un recurso de escena de un paquete
* [Vista 3D] El entorno personalizado no se guarda en SBSSCN si la ruta tiene un alias con caracteres especiales
* [Vista 3D] Al cambiar el formato normal en los ajustes de Material, se producen estados volteados
* [UI] El texto del botón Establecer como principal se desborda del área de visualización
* [UI] La posición de la ventana principal no se restaura correctamente al trabajar en modo de ventana
* [UI] El texto de la barra de estado se desplaza cuando la ventana se muestra completa o se arrastra cerca del borde de la pantalla
* [Iray] Bloqueo con el mensaje &quot;Etiqueta no válida&quot; al cambiar entre procesadores
* [Iray] Caras visibles en superficies no opacas
* [Presets] Bloqueo al aplicar ajustes preestablecidos en instancias de algunos Substance Source
* [Presets] Se muestra un nombre incorrecto después de deshacer en la instancia de SBS
* [Renderizar] Procesamiento incorrecto al ajustar un parámetro en el modo de previsualización
* [Panaderos] Actualizar varios mapas con bake provoca advertencias que bloquean algunos pasteles
* [Cooker] Al ajustar nodos SBSAR en instancias SBS, se obtiene una salida 0 de la instancia
* [Explorer] Los alias personalizados no se pasan cuando se utiliza &quot;Guardar y abrir en Substance Player&quot;
* [Editor de degradado] La selección de color absoluto no afecta a todas las teclas seleccionadas

### 10.1.3 (2020.1.3)

*(Lanzado: 11 de junio de 2020)*

**Agregado:**

* [Content] Exponer el parámetro &quot;Color mate&quot; en el nodo Escala de grises de transformación segura
* [Contenido] Renderización PBR: Añadir una opción de entrada de fondo personalizada
* [Contenido] Nodos de luz de panorama: nueva opción para probar el color de la imagen de fondo
* [Parámetros] Ocultar parámetros con el indicador &quot;no compatible&quot; de la lista de la ventana Exponer parámetros

**Corregido:**

* [Vista 3D] Bloqueo al cambiar mallas personalizadas en un caso específico
* [Vista 3D] El formato normal siempre es DirectX al inicio
* [Contenido] Ruido Worley 3D: artefacto de procesamiento al utilizar un valor de tamaño de cuadrícula alto
* [Contenido] La fusión de nodos de disolución es incorrecta
* [Contenido] Renderización PBR: quitar advertencia de cocina
* [Contenido] Renderización PBR: El resultado contiene colores negativos en algunos casos
* [Cooker] Problema de inyección de caché para nodos de instancia de varias salidas
* [Explorer] Bloqueo al cerrar un paquete que contiene un gráfico MDL mostrado
* [Graph] 2 pases de cocción: el cambio de tipo de nodo no desencadena una recuperación
* [Graph] Bloqueo al eliminar entradas mientras se utiliza la conexión
* [Graph] Los extremos del vínculo se pueden mover a un espacio vacío
* [MDL] Bloqueo al cancelar la exportación de MDL desde el gráfico de MaterialX
* [MDL] Error al cancelar la exportación a MDLE
* [Presets] Bloqueo en la pestaña Presets tras cambiar el tipo de parámetro incluido en el ajuste preestablecido
* [Resources] La lista de materiales está vacía en el menú contextual del gráfico para mallas vinculadas como no UDIM

### 10.1.2 (2020.1.2)

*(Lanzado: 27 de abril de 2020)*

**Agregado:**

* [Contenido] Agregar plantilla de filtro de Alchemist
* [Contenido] Renderización PBR: añadir parámetros para controlar las intensidades de las sombras difusas/de specular
* [Contenido] Nodos de luz de forma: añadir parámetro de posición de cámara
* [Noticias] El estilo de grupo &quot;Flecha&quot; se rompe la primera vez que se muestra la ventana
* [Bakers] Añada el método abreviado Z a la vista 2D para ver la imagen en 1:1
* [Project] Ocultar el alias $(PROJECT\_DIR) de la lista
* [Explorador] No crear recursos personalizados para recursos que no son un archivo en disco

**Corregido:**

* [Player] Informar de alias que faltan al cargar paquetes SBS
* [Player] Muestra el valor Raíz aleatoria en base decimal
* [Player] Combina todos los mapas de entorno incluidos con Substance Designer
* [Player] Bloqueo al salir de macOS High Sierra
* [Player] No se pueden cargar los paquetes que utilizan la carpeta sbs://
* [Contenido] Ruido Worley 3D: artefacto de procesamiento al utilizar un valor de tamaño de cuadrícula alto
* [Content] No se utiliza la entrada &#39;mayor que cero&#39; en el nodo &#39;Onda&#39;
* [Contenido] Luz plana: El modo de posición del espacio mundial no funciona
* [Contenido] Luz de esfera: la posición de la luz interna no funciona correctamente
* [Bakers] Bloqueo al hornear con la ventana de hornear mientras se está ejecutando la opción Actualizar todos los mapas con bake
* [Panaderos] Fallo de horneado en Optix para AO desde Mesh usando Baja como Alta con un mapa Normal
* [Bakers] La resolución de la vista previa de los archivos UVT no coincide con el tamaño de la pantalla
* [Vista 3D] El mapa de bits asignado se reemplaza al cargar un MDL si el valor predeterminado no es una textura 2d
* [Vista 3D] Los widgets de Propiedades de materiales cambian después de restablecer una propiedad
* [Vista 3D] La preferencia global de formato normal ya no funciona
* Biblioteca [MatX]: La categoría MaterialX Graph no muestra todos los nodos disponibles
* [MatX] El menú contextual de un gráfico personalizado puede contener subcarpetas vacías en la carpeta &quot;Agregar nodo&quot;
* [SBSAR] La entrada principal se vuelve a la primera entrada de la lista
* [Biblioteca] Solo se incluye el primer gráfico de SBSAR con varios gráficos
* [CustomGraph] Los nodos que no forman parte del tipo de gráfico actual se crean automáticamente en algunos casos
* [Iray] El parámetro &#39;Profundidad&#39; de proyección de cuadro no funciona correctamente
* [Preferencias] Mejora del diseño en la configuración del proyecto
* [Parámetros] Bloqueo al mover un widget de posición después de eliminar un parámetro
* [UI] Bloqueo al cambiar la jerarquía de usos en el nodo de salidas
* [Graph] Bloqueo al utilizar un cuadro de selección en un comentario y un nodo marcado

### 10.1.1 (2020.1.1)

*(Lanzado: 10 de abril de 2020)*

**Corregido:**

* [Vista 3D] El uso de memoria es demasiado alto cuando se trabaja en un gráfico de composición
* [Contenido] Formas inesperadas en la salida no cuadrada de nodos &quot;Polígono&quot;
* [Contenido] Renderización PBR: La cámara ortográfica no funciona correctamente si no se usa una resolución cuadrada
* [Contenido] Renderización PBR: El efecto bokeh con remolino aumenta el brillo del borde de la imagen
* [Gestión de color] El selector de color del cuadro de diálogo Nuevo mapa de bits no se gestiona por color.
* [Gestión de color] Los selectores de color de las herramientas de pintura y vectores en la vista 2D no se administran por color.

### 10.1.0 (2020.1.0)

*(Lanzado: 09 de abril de 2020)*

**Agregado:**

* [Atajos] Administrador de accesos directos para la creación de nodos
* [Contenido] Nuevo nodo de Renderización PBR
* [Contenido] Nuevo filtro FXAA
* [Contenido] Nuevo filtro Hald CLUT
* [Content] Exponer el filtrado en nodos &quot;Crop&quot;
* [Vista 3D] Mejora del flujo de trabajo de asignación de texturas y parámetros de sombreado
* [Vista 3D] Nuevo sombreado sin iluminar
* [Vista 3D] Agregue un &quot;Valor cero escalar&quot; a los sombreadores de desplazamiento
* [Vista 3D] Añada una opción para reducir la resolución de la ventana gráfica cuando se activa PPP altos
* [Vista 3D] GLSLFX: Permitir establecer la información de la interfaz gráfica de usuario en sampler (default, min, max, guiMin, guiMax, guiStep, guiWidget, guiName, guiGroup)
* [Vista 3D] Agregar &#39;Cargar estado con malla...&#39; en el menú Escena
* [Vista 3D] Añada la transformación de salida de ACES tonemapped en el modo de administración de color heredado
* [Panaderos] Nuevo método de muestreo en AO, Curvatura, Bent Normal, panaderos de Thickness
* [Panaderos] Nuevas opciones de normalización en panaderos de Height y Thickness
* [Gestión de color] Integración de Adobe ACE (Adobe Color Engine)
* [Gestión de color] Añadir opciones para definir el comportamiento predeterminado cuando falta el perfil ICC
* [Parámetros] Hacer que los reguladores aumenten de forma coherente con Substance Painter
* [Packaging] Agrupa tantos archivos .dll de Qt como podamos para los scripts de Python
* [Project] Desactive la configuración de los archivos de proyecto de solo lectura y comunique claramente ese estado
* [Preferencias] Ocultar opciones de configuración no claras específicas relacionadas con la capacidad de respuesta y los períodos de cálculo
* [UI] Cambiar nombre Pow2 -> 2Pow
* [Propiedades] Optimizar la visualización de propiedades de gráficos de composición
* [AXF] Actualización a AXF SDK 1.7.1

**Corregido:**

* [Vista 3D] Los parámetros de luz ambiente no son visibles aunque estén activados
* [Vista 3D] glslfx: El widget de color siempre es un vec3 sin alfa
* [Vista 3D] El conjunto de asignaciones de entorno de un recurso no se guarda en el recurso de escena
* [Vista 3D] Iray: La luz ambiente se convierte en una luz puntual en el origen de la escena
* [Vista 3D] glslfx: El widget de color siempre es un vec3 sin alfa
* [Parámetros] La URL del paquete de instancias no es correcta en el grupo de atributos.
* [Parameters] Bloqueo al exponer parámetros
* [Parámetros] Los iconos no se alinean correctamente en los parámetros de los nodos Curva
* [Parámetros] La cadena de nodo &#39;Texto&#39; solo se muestra en modo &#39;Vista previa&#39; cuando se muestra
* [Parameters] Bloqueo al cambiar el nombre de un parámetro de entrada utilizado en la instrucción &#39;Visible If&#39;
* [Parameters] Bloqueo al eliminar un nodo Levels que tiene una función definida en cualquiera de sus parámetros
* [UI] El icono de advertencia de la lista de parámetros de entrada se coloca encima de un botón existente
* [UI] Las advertencias no se borran en el elemento de parámetro de entrada correcto en un caso específico
* [UI] Impedir el &quot;¿Es UDIM de malla?&quot; que aparece cuando las UV de malla están estrictamente en el mosaico [0,1]
* [UI] Las listas desplegables de ajustes preestablecidos se pueden desplazar con la rueda del ratón con un simple desplazamiento del ratón
* [UI] La opción Cálculo de salida en atributos de gráficos se denomina incorrectamente
* [MDL] Bloqueo al colocar un recurso de gráfico SBS en un gráfico MDL
* [MDL] El nodo SBS con entrada de imagen no funciona correctamente
* [MDL] Enlaces de textura y nombres de uso incorrectos
* [Graph] El grupo de valores de entrada y el uso se omiten en el modo de creación de vínculos &quot;Material&quot;
* [Graph] Los valores de entrada utilizan el valor predeterminado en lugar de los datos de entrada para los valores booleanos
* [Panaderos] Normales incorrectas en el Panadero de Normales Espaciales Mundiales usando un mapa Normal tangente en casos específicos
* [Bakers] Uso excesivo de la memoria al hornear con la ventana de previsualización abierta
* [Presets] El ajuste preestablecido dañado hace que el procesamiento se bloquee
* [Presets] El ajuste preestablecido no afecta al parámetro booleano del SBS antiguo
* [Biblioteca] Los recursos del primer paquete abierto se muestran en el menú flotante de creación de nodos
* [Publish] La publicación en SBSAR devuelve el código de error 13 en SBSCooker en macOS
* [Publish] Advertencia de argumento obsoleto en SBSCooker al publicar en SBSAR
* [API] No se pueden obtener los metadatos de un paquete procedente de un archivo .sbsar
* [Exportar] En el modo heredado, la opción de espacio de color vuelve a los valores predeterminados para salidas específicas
* [Vista 2D] Copiar al portapapeles no tiene en cuenta el estado de Gestión de color
* [Unix] Designer ignora las señales del sistema
* [Biblioteca] Algunos filtros de la biblioteca no funcionan correctamente debido a etiquetas traducidas
* [Cocinero] La raíz cuadrada de números negativos debe devolver 0 en lugar de NaN
* [Vista 2D] Los canales rojo y azul se intercambian después de deshacer el primer trazo de pintura
* [Consola] Demasiados mensajes de advertencia en la consola &quot;QPixmap::scaled: Pixmap es un pixmap nulo&quot;
* [Contenido] &quot;Resplandor de forma&quot;: aviso cocción
* [Dependencias] Asignar un gráfico ubicado en un paquete diferente a una malla no crea dependencias
* [Iray] Las propiedades de material se vuelven inactivas después de cambiar la geometría

## Versión 9

### 9.3.3 (2019.3.3)

*(Lanzado: 14 de febrero de 2020)*

**Agregado:**

* [Batchtools] Enviar perfiles OCIO predeterminados con herramientas por lotes

**Corregido:**

* atlas scatter [Content]: problemas al utilizar color aleatorio/normal en algunas situaciones

### 9.3.2 (2019.3.2)

*(Lanzado: 04 de febrero de 2020)*

**Agregado:**

* [SBSRender] Compatibilidad con la gestión de color

**Corregido:**

* [Content] Nodo sRGB lineal a ACEScg: Las etiquetas de E/S son incorrectas
* [Content] De ACEScg a nodo sRGB: Las etiquetas de salida son incorrectas
* [Contenido] Nodos de luz de panorama: ajustar rango de temperatura
* [Gráfico] Se produce una caída grave del rendimiento y se bloquea al ajustar un gráfico anidado con la opción Edición en contexto activa.
* [Graph] Bloqueo al eliminar varios nodos en FX-Map
* [Interpretaciones] El proceso de Designer puede seguir activo después de salir

### 9.3.1 (2019.3.1)

*(Lanzado: 27 de enero de 2020)*

**Corregido:**

* [Gráfico] Se produce una caída grave del rendimiento y se bloquea al ajustar un gráfico anidado con la opción &quot;Edición en contexto&quot; activa
* [Graph] No se puede introducir el valor de enumeración de [0, 99] en el ajuste de Entero1
* [Graph] El comentario no se mueve cuando se desplaza el fotograma correspondiente
* [Graph] Faltan nombres de entrada en el nodo de instancia personalizada
* [Graph] Las miniaturas se pueden representar al cargar el gráfico aunque la opción correspondiente esté desactivada en Preferencias
* [Vista 2D] El alfa negativo muestra el comprobador independientemente de la opción de visualización
* [Vista 2D] La conversión de superficies de 32f a 8 bits falla con valores altos
* [Vista 2D] El sesgo superior/izquierdo y &#39;Hacer cuadrado&#39; establecen algunas coordenadas en valores enormes en matrices de transformación hacia delante
* [Vista 2D] Las UV de todos los objetos de malla no se muestran en conjuntos UV distintos de &quot;0&quot;
* [Contenido] Bisel: El modo de angular no funciona correctamente en la máscara de mosaico
* [Content] Flood Fill A Degradado: El valor de imagen de pendiente no se muestra en el centro de la forma
* Función [Content]; &quot;Igualdad booleana&quot; está roto
* [Panaderos] Artefactos cuando se usa el mapeo de tonos automático en el panadero &quot;Curvatura de malla&quot; en casos específicos
* [Bakers] Bloqueo en DXR al hornear sin seleccionar ningún material
* [Bakers] Problema de rendimiento en la vista 2D al activar la &quot;información&quot;
* [Motor] La función &#39;Pow&#39; emite valores enormes cuando se utiliza un valor de entrada muy bajo y un exponente alto en el motor SSE2
* [Motor] Bloqueo al utilizar una compresión jpg alta en recursos de mapa de bits
* [Motor] El procesador de valores devuelve un valor $size incorrecto cuando está dentro de un subgráfico
* [Parámetros] Aparece una ventana emergente vacía al seleccionar un nodo de instancia con un gran número de parámetros
* [Parámetros] El valor entero no se muestra en los elementos de parámetros desplegables
* El botón &quot;Editar&quot; del Transformar matriz [Parámetros] no está disponible en el modo de vista previa
* [Cooker] $size en ValueProcessor es incorrecto cuando está dentro de una instancia de gráfico
* [Cooker] El tamaño de salida es incorrecto cuando el vínculo de valor pasa a través de un nodo de punto a un nodo atómico
* [UI] El botón para mostrar todos los elementos de la barra inferior de la vista 2D no está visible
* [UI] La vista previa de los valores de RGB seleccionados muestra números incorrectos al utilizar la gestión de color
* [Exportar] Las imágenes RGBA 16f se exportan como escala de grises
* [Vista 3D] No se puede importar OBJ con varios espacios
* [Gestión de color] La configuración de OCIO no se tiene en cuenta al publicar sbsar
* [Widget de color] Los rangos de los reguladores de color pueden ampliarse exponencialmente en un caso específico
* [Doc] La sección &quot;paramValue&quot; está incompleta en la referencia de formato Sbs
* [MDL] El widget de color en instancias de sbsar no es correcto
* [Presets] Bloqueo al actualizar ajustes preestablecidos en un caso específico
* [PSD] Error de FreeImage al cargar archivos de PSD de versiones recientes de Photoshop
* [Resources] Bloqueo al deshacer la vinculación de mapa de bits directamente en el gráfico
* [SVG] Los nodos de SVG no se actualizan automáticamente cuando se utilizan las herramientas de vectores

### 9.3.0 (2019.3.0)

*(Lanzado: 19 de diciembre de 2019)*

**Agregado:**

* [General] Compatibilidad con la gestión de color mediante el archivo de configuración OpenColorIO
* [Ajustes preestablecidos] Mejorar la gestión de ajustes preestablecidos
* [Ajustes preestablecidos] Sincronizar gizmos de vista 2D y reguladores de previsualización
* [Ajustes preestablecidos] Restaurar valores de previsualización al volver al modo de previsualización
* [Ajustes preestablecidos] Mantenga activo el modo de vista previa al editar otros nodos, recursos o gráficos
* [Ajustes preestablecidos] Deshacer funciona sin problemas al navegar entre las pestañas de 3 ajustes preestablecidos
* [Ajustes preestablecidos] Permite restablecer los parámetros al valor predeterminado de Graph o del ajuste preestablecido en el modo de vista previa
* [Ajustes preestablecidos] Mejorar la fijación de parámetros
* [Ajustes preestablecidos] Importar/Exportar todos los ajustes preestablecidos de un gráfico a un archivo
* [Panaderos] Nuevo panadero &#39;Curvatura de malla&#39; basado en trazado de rayos
* [Panaderos] Añadir la opción de plano de tierra en el panadero &#39;AO de malla&#39;
* [Bakers] Añadir coincidencia por opción de nombre para ignorar la cara posterior en el panadero &#39;AO from Mesh&#39;
* [Content] Nuevo nodo de Atlas scatter
* [Contenido] Novedades en nodos y funciones de conversión de espacio de color (ACEScg)
* [Contenido] Mejora la coherencia de la nomenclatura de los nodos con las versiones en color/escala de grises
* [Graph] Mejora del rendimiento en el modo de previsualización de ajustes preestablecidos
* [Graph] Opción Añadir $(colorspace) para exportar salidas de gráficos
* [Parámetros] Cuando un parámetro se establece en invisible, oculte el gizmo correspondiente en la vista 2D
* [Parámetros] No agregue &#39;Grupo de entrada de gráficos&#39; como prefijo al exponer parámetros
* [Parámetros] Añadir información sobre herramientas para VisibleIf en parámetros de gráficos
* [AXF] Actualice AXF SDK a v1.6.

**Corregido:**

* [Linux] Designer no se inicia en CentOS 8 debido a un error de carga de la plataforma Qt.
* [Linux] ADVERTENCIA: La biblioteca Freetype se ha eliminado de la aplicación SD: Los usuarios con la versión de CentOS &lt;= 7.5 deben instalarla manualmente.
* [AxF] Bloqueo al importar archivos creados con versiones más recientes de AxF
* [2DView] Las texturas de pincel alimentadas por un recurso no se aplican
* [2DView] Bloqueo al modificar las entradas de un gráfico instanciado con el ajuste de posición
* [3DView] Bloqueo al cancelar la operación &quot;Cargar...&quot; acción
* [3DView] Opción Añadir espacio de color para las texturas de emisión en sombreadores GLSLFX
* [Panaderos] Los mapas alimentados a través de recursos se ignoran durante el procesamiento
* [Bakers] Las opciones de Dirección del espacio mundial están bloqueadas incorrectamente
* [Bitmap] Los mapas de bits EXR con valores de punto flotante se representan como una imagen en negro
* [Contenido] Flood Fill a índice: la detección de formas falla en un caso concreto
* [Contenido] Recortar: problema de muestreo cuando el nodo de recorte tiene una resolución inferior a la entrada
* [General] Bloqueo al cerrar Designer al generar la biblioteca
* [Graph] Los nodos de mapa de bits no reflejan la compresión del mapa de bits asociado
* [Graph] La caché no se borra al borrar las miniaturas de nodo después del primer procesamiento
* [Graph] Tamaño de nodo invalidado incorrectamente
* [Graph] Bloqueo en algunos casos al cambiar conexiones de entrada en un nodo de procesador de píxeles
* [Gráfico MDL] Error al restaurar un valor predeterminado de llamada de función
* [Propiedades] Los botones &quot;Editar&quot; y &quot;Matriz&quot; de los parámetros de transformar matriz son confusos

### 9.2.3 (2019.2.3)

*(Lanzado: 26 de noviembre de 2019)*

**Agregado:**

* [MacOS] Notarizar el software para seguir los nuevos requisitos de distribución de MacOS Catalina

**Corregido:**

* [Bakers] Bloqueo al realizar el procesamiento con un recurso de mapa de sesgo con un vínculo no válido
* [Panaderos] Los conjuntos de UV distintos de 0 no se tienen en cuenta en Embree
* [Bakers] &quot;Bent Normals from Mesh&quot; genera resultados incorrectos con conjuntos UV distintos de 0 en DXR
* [Bakers] Los parámetros de &#39;UV Set&#39; se restablecen a &#39;0&#39; cuando se vuelve a abrir la ventana de horneado
* [Bakers] &#39;Position&#39; genera una imagen en negro con conjuntos UV distintos de 0
* [Contenido] Mosaico automático inteligente: problema de muestreo en 8k
* atlas splitter [Content]: La detección de formas falla en algunos casos, se debe exponer el parámetro de precisión
* [Contenido] Pow no devuelve el valor correcto en algunos casos
* [Contenido] Flood Fill a índice: resultado incorrecto al publicar en sbsar
* [Biblioteca] Bloqueo al cargar el primer paquete SBS de la sesión
* [Biblioteca] La configuración &quot;Mostrar recursos en la biblioteca de forma predeterminada&quot; se omite para los recursos importados directamente en el panel Explorador
* [Console] Mensaje inesperado en la consola al utilizar el menú del nodo
* [Parámetros] No se puede quitar una sola entrada en la lista de uso de salida
* [3DView] la escena no se vuelve a cargar correctamente si el archivo de escena se modifica en el disco. El filtrado del menú Nodo [Graph] es incorrecto cuando se utilizan salidas de valor.

### 9.2.2 (2019.2.2)

*(Lanzado: 23 de octubre de 2019)*

**Corregido:**

* [Graph] El filtrado del menú de nodos es incorrecto al utilizar salidas de valor
* [Graph] Bloqueo al mostrar el menú del nodo
* [Graph] La herramienta de búsqueda aparece al utilizar el método abreviado de cambio
* [Graph] Bloqueo al generar menús de nodo consecutivamente desde el conector de entrada de valor
* [Graph] Los comentarios que contienen cadenas largas se recortan
* [Graph] El resaltado de flujo no es correcto al crear un nodo mediante la acción de arrastrar desde el menú del conector
* [Graph] Bloqueo al eliminar todos los elementos de gráfico de la escena al cargar un gráfico diferente
* [Graph] Bloqueo al utilizar para crear un nodo mientras se utiliza para hacer clic y arrastrar desde el conector
* [Graph] Bloqueo al utilizar la herramienta &quot;Buscador de nodos&quot;
* [Graph] El color del pin de salida es incorrecto en el modo &quot;Material Compact&quot;
* [Cooker] Los nodos aguas abajo de los nodos de múltiples salidas no se actualizan correctamente
* [Cooker] Problema con salidas Value y nodos passthrough
* [Cooker] El procesador de valores emite resultados incorrectos cuando solo se utiliza un nodo &#39;Get&#39;
* [Content] El nodo &#39;Contrast/Luminosity&#39; genera un valor de Alpha de 1.0
* [Contenido] La plantilla &quot;Panorama de estudio&quot; no tiene descripción
* [Contenido] Flood Fill a índice: resultado incorrecto cuando la entrada contiene una forma de ajuste
* [Content] &#39;Combinación HDR&#39;: cálculo de exposición interna incorrecto
* [Dot Node] Bloqueo al utilizar un nodo de nivel y un nodo de punto
* La acción &quot;Ir a&quot; de [Dependency Manager] ya no funciona
* [PSD] Bloqueo al deshacer la eliminación de varios nodos que se incluían en el exportador de PSD
* [UI] Bloqueo al cerrar un gráfico mediante el menú &quot;Ventana&quot; y volver a abrir uno mientras se fija uno
* [Editor de degradado] El botón Quitar clave es demasiado grande
* [Motor] Problema de precisión con sqrt() acos() y asin()
* [Panaderos] AO De Mesh: El regulador &quot;Ángulo de pliego&quot; tiene un rango de valores incorrecto al retocarlo

### 9.2.1 (2019.2.1)

*(Lanzado: 20 de septiembre de 2019)*

**Agregado:**

* [Plantillas] Añada nodos de entrada predeterminados a Specular/Brillo y a otras plantillas
* [Templates] Agregar plantilla de Anisotropía PBR
* [Vista 3D] Aumentar las distancias lejanas del plano de clip automático
* [Vista 3D] Con revestimiento PBR: cambiar el valor predeterminado de Herencia normal de capa
* atlas splitter [Content]: Opción de adición para la función Recorte automático
* [Node Menu] No filtrar nodos sin entrada

**Corregido:**

* atlas splitter [Content]: algunas salidas no se recortan correctamente cuando se utiliza la opción &quot;Recorte automático&quot;
* [Contenido] Fusión de Height de material: error de cocción relacionado con un parámetro inexistente
* [Contenido] &quot;Luz plana&quot;: El modo UV de patrón no funciona correctamente
* [Contenido] &quot;Height a la unidad del mundo normal&quot;: la entrada se fuerza a 16 bits
* [Contenido] Formas inesperadas al utilizar el nodo &quot;Bisel&quot; de angular sin mosaico en formas pequeñas
* [Biblioteca] Los iconos de sbsar no están visibles en la biblioteca
* [Biblioteca] El uso de &quot;\&quot; para filtrar la dirección URL ya no funciona
* [Biblioteca] Los valores del filtro distinguen mayúsculas de minúsculas
* [Biblioteca] El filtro de búsqueda no funciona cuando se selecciona &quot;Composición&quot;
* [Bakers] Al hacer doble clic en celdas específicas y descartar el cambio, se restablecen los valores incorrectos
* [Bakers] El texto de estado del back-end en la ventana de bakers siempre muestra &#39;Aceleración de GPU : habilitar&#39;
* [Cooker] Bloqueo al procesar una dependencia &#39;impostor&#39; en un gráfico
* [Cooker] La conversión de escala de grises tiene un tamaño de salida incorrecto al utilizar el valor
* [Explorer] Bloqueo al procesar &quot;Publish en Share&quot;
* [Graph] Bloqueo al abrir un paquete específico
* [MDL] Bloqueo al utilizar el operador de colada
* [Templates] Los identificadores de salida no son correctos en la plantilla recubierta de PBR

### 9.2.0 (2019.2.0)

*(Lanzado: 29 de agosto de 2019)*

**Agregado:**

* [Contenido] Nuevas formas de &#39;Luz de panorama&#39;
* [Contenido] Nuevo filtro de &#39;Panorama Nadir patch&#39;
* [Contenido] Nuevo filtro &quot;Nadir extract de panorama&quot;
* [Contenido] Nuevo filtro &quot;Enderezar horizonte panorámico&quot;
* [Contenido] Nuevo filtro &quot;Rotación de panorama&quot;
* [Content] Nuevo nodo &#39;Panorama Position&#39;
* [Contenido] Nuevo nodo &quot;Panorama Physical Sun and Sky&quot;
* [Contenido] Nuevos nodos &quot;Degradados de panorama&quot;
* [Contenido] Nuevo filtro &quot;Combinación HDR&quot;
* [Contenido] Nuevo filtro &quot;Previsualización HDR&quot;
* [Content] Nuevo filtro &quot;Color temperature adjustment&quot;
* [Content] Nuevo nodo &#39;Blackbody&#39;
* [Content] Nuevo filtro &#39;Exposure&#39;
* [UI] Menú de creación de nodos: mostrar y administrar Favoritos en el menú
* [UI] Agregar o quitar un nodo de favoritos desde el menú Creación de nodos
* [UI] Menú de creación de nodos: generar el menú al hacer clic o arrastrar un vínculo desde una salida
* [UI] Menú de creación de nodos: filtrar el contenido según el tipo de selección actual
* [Vista 3D] Anisotropía de soporte
* [Vista 3D] Efecto Recubrimiento de compatibilidad
* [Vista 3D] Compatibilidad con la dispersión subsuperficial
* [Graph] Nodo de puntos
* [Graph] Optimizar el procesamiento de gráficos almacenando en caché los resultados de cocción
* [Preferencias] Cambie el valor predeterminado &quot;Límite de tamaño de cocción&quot; a 8192
* [Preferencias] Añada un botón de alternancia para activar o desactivar la nueva funcionalidad de la tecla &quot;Tab&quot;
* [API] Método Add SDResource.getPackage()
* [Israel] Actualización a NVIDIA Iray RTX 2019.1.3 SDK (317500.3714)
* [Explorer] Permite vincular cualquier tipo de archivo como recurso en el paquete
* [GradientNode] Presione ESC para cancelar la selección de degradado
* [Parámetros] Quitar mayúsculas automáticas en los identificadores
* [Project] Agregue una opción para especificar si los gráficos y los recursos están &quot;visibles en la biblioteca&quot; de forma predeterminada
* [Ajustes preestablecidos] Fijar automáticamente parámetros modificados

**Corregido:**

* [MDL] No se puede exportar el módulo debido a un problema de tipo de parámetro
* [MDL] El int expuesto no es visible al cargarse
* [MDL] Bloqueo durante la exportación de MDL
* [MDL] Bloqueo al modificar el color de un nodo de superficie de material
* [MDL] void MDLGraphNodeControllerSelector::updateSelectorCurrentMember(const DataMessage&amp; msg) está dañado
* [Graph] thickness de vínculo incorrecto en la visualización del gráfico
* [Gráfico] Se activan demasiadas invalidaciones al ajustar parámetros
* [Graph] Bloqueo al cerrar un paquete con dos ventanas abiertas y al utilizar la edición en contexto
* [Gráfica de funciones] La advertencia no aparece al cerrar la vista de funciones
* [Vista 3D] Bloqueo al inicializar la vista 3D cuando la proyección de cámara se establece como ortográfica como estado de escena predeterminado
* [Vista 3D] El DOF Post-FX permanece activado en Irán
* [Vista 2D] La ventana de selección de pincel desaparece al cambiar el tamaño del pincel
* [Vista 2D] Panel de información: los valores se recortan con un diseño específico
* [Vista 2D] La imagen se desplaza al minimizar y restaurar la ventana principal
* [Panaderos] La lista de selección &quot;Desde recurso&quot; no se ha filtrado correctamente
* [Panaderos] Bloqueo al encadenar panaderos de &#39;Mapa de color desde malla&#39; y &#39;Mapa normal desde malla&#39; en Embree
* [Panaderos] La curvatura por vértice produce artefactos graves
* [Explorer] No se pueden importar recursos UDIM arrastrándolos y soltándolos en el explorador
* [Explorer] La ventana del explorador no se filtra correctamente al vincular mallas y fuentes después de vincular formatos de archivo poco habituales
* [Explorador] Los recursos son visibles cuando el gráfico tiene &#39;mostrar en biblioteca&#39; establecido en &#39;no&#39;
* [Content] Las entradas &#39;Pow&#39; y &#39;clamp&#39; no están en el orden correcto
* [Content] Las entradas del nodo &#39;Combinación RGBA&#39; no están etiquetadas
* [Cooker] De todas formas se evalúan conexiones no válidas de valores numéricos
* [Cooker] Aserción al conectar una entrada de imagen a un valor de entrada
* [UI] El cursor del ratón se bloquea en el estado &quot;redimensionar&quot; en algunos casos concretos
* [UI] Al hacer clic con el botón derecho en la vista del paquete no se muestra el menú correcto en Linux
* [Dependencias] La ruta de archivo de los recursos temporales no es correcta
* [Dependencias] La advertencia de falta de recurso de mapa de bits permanece activa después de la reubicación
* [Biblioteca] No se generan algunas miniaturas
* [Biblioteca] Los archivos MDL se muestran en la biblioteca
* [Parameters] Bloqueo al exponer parámetros
* [Parameters] Bloqueo después de volver a crear un nuevo elemento en la lista desplegable
* [Exportar] Error en la exportación de lotes 8K
* [Presets] Bloqueo al aplicar un ajuste preestablecido que implica valores booleanos en instancias de SBS
* [Scripting] La pantalla &quot;Bienvenido&quot; sigue apareciendo cuando se utiliza el argumento de línea de comandos &quot;—quit&quot;

### 9.1.3 (2019.1.3)

*(Lanzado: 19 de agosto de 2019)*

**Corregido:**

* [Bakers] Bloqueo en DXR cuando las proporciones de aspecto de la salida de la torta y el mapa de sesgo no coinciden
* [Bakers] El panadero &quot;Oclusión ambiental desde malla&quot; genera resultados incorrectos con Optix o DXR al usar un mapa normal
* [Panaderos] El panadero de curvatura genera resultados incorrectos al utilizar el ajuste Por vértice
* [Panaderos] Los mensajes de error indican el motor que ha fallado en lugar de la causa del error
* [Panaderos] Bloqueo al procesar un panadero de mapa de detalles sin una malla de poli alta
* [Bakers] El mapa de sesgo no parece afectar a toda la salida con DXR activado
* [Contenido] mg\_leaks: error tipográfico en el nombre de parámetros
* [Contenido] &quot;Forma&quot; devuelve una advertencia de cocción
* [Contenido] Los polígonos 1 y 2 no admiten funciones aleatorias
* [Contenido] Los polígonos 1 y 2 pueden tener menos de 3 lados
* [Contenido] Normal a Height HQ no funciona correctamente en formato no cuadrado
* [Parámetros] Parámetros de entrada de enteros: la lista desplegable no muestra los valores

### 9.1.2 (2019.1.2)

*(Lanzado: 2 de julio de 2019)*

**Corregido:**

* [Vista 3D] La exportación de la vista 3D con la profundidad de campo activada parece incorrecta
* [Vista 3D] El canal de Alpha de las imágenes de PSD es incorrecto al utilizar guardar procesamiento
* [Vista 3D] PNG y PSD se rompen al utilizar la opción de guardar procesamiento con Iray
* [Vista 3D] El formato dds no funciona al guardar el procesamiento
* [Graph] Los nodos se desplazan al combinar la acción de arrastrar del botón derecho y del izquierdo de formas específicas
* [Graph] La modificación de instancias de una función ya no actualiza el resultado del nodo
* [Graph] Bloqueo al mostrar el menú de la barra espaciadora
* [Content] Extrusión de forma: problema de calidad cuando la forma no tiene rotación
* [Contenido] La sombra paralela de forma (y la escala de grises) no produce sombras sin mosaicos H y V
* [Contenido] Problema normal de recorte de material
* [Bakers] Los ajustes preestablecidos de JSON Bakers no se cargan correctamente
* [Bakers] Bloqueo al hornear mallas pesadas usando Optix o DXR (ahora puede fallar debido a Vram insuficiente pero no se bloqueará)
* [Editor de mapa de bits] Las herramientas de pintura de mapa de bits desplazan los trazos y vuelven a dibujarlos en el cuadro delimitador del trazo
* [Editor de mapa de bits] Herramientas de pintura de mapa de bits rotas en OSX
* [UI] Apenas se puede acceder al menú de algunos botones
* [UI] Bloqueo al arrastrar y soltar una instancia de Baker
* [SVG] Las herramientas de edición de SVG incorporadas no son fiables
* [Parameters] Bloqueo al aplicar un ajuste preestablecido con parámetros booleanos en una instancia SBSAR
* [Red] Bloqueo a veces cuando se produce un error en una conexión cifrada SSL

### 9.1.1 (2019.1.1)

*(Lanzado: 28 de mayo de 2019)*

**Agregado:**

* [PythonIntegration] Guardar y restaurar el estado del administrador de complementos
* [Preferencias][Dependencias] Agregue una opción para determinar cómo se almacenan las rutas de acceso de los archivos de dependencias
* [Content] Asignador de Flood Fill: Añade la opción &quot;Ajustar cuadro de forma&quot;

**Corregido:**

* [Content] Asignador de Flood Fill: La &quot;Escala automática de rotación&quot; hace el efecto contrario
* [Content] &quot;luminance\_offset\_map&quot; no se utiliza en &quot;Flood Fill Mapper Color&quot;
* [Content] El nodo &quot;Flood Fill Mapper Grayscale&quot; genera artefactos de ejecución de pasos
* [Contenido] No se puede publicar la Extrusión de altura
* [Parámetros] Los ajustes preestablecidos incrustados en sbsar no se cargan en Designer
* [Panaderos] El nombre del panadero no se muestra correctamente en la lista de panaderos
* [Vista 3D] &quot;Ver resultados en vista 3D&quot; no funciona para valores
* [Cooker] Bloqueo al corregir un tipo de parámetro incorrecto
* [API] La función SDResource.setInputPropertyFromId no funciona en los parámetros de entrada de SDSBSCompGraph
* [Updater] Algunos subprogramas no se pueden actualizar en 2019
* [Explorer] Bloqueo al importar un archivo .obj específico
* [PythonIntegration] Las barras invertidas no se escapan correctamente en Windows al inicializar PYTHONPATH
* [UI] Problema de valor con algunos reguladores en panaderos
* [Linux] Designer no se puede ejecutar en CentOS &lt; 7.6

### 9.1.0 (2019.1.0)

*(Lanzado: 09 de mayo de 2019)*

**Agregado:**

* [API] Agregue el parámetro &#39;updatePackages&#39; al método SDPackageMGR.loadUserPackage() para controlar si los actualizadores se deben aplicar o no durante la carga
* [API] Añadir la capacidad de desconectar un SDConnection
* [API] Agregue la clase SDSBSARExporter para publicar un SDPackage
* [API] Agregue la clase SDHistoryUtils para administrar los comandos que se pueden deshacer
* [API] Agregar definición de nodo de entrada de escala de grises en Gráfico de composición de Substance (sbs::compositing::input\_grayscale)
* [API] Agregar definición de nodo de entrada de valor en Gráfica de composición de Substance (sbs::compositing::input\_value)
* [API] Método Add SDProperty.isFunctionOnly()
* [API] Agregar compatibilidad con parámetros de entrada personalizados en SDSBSCompNode
* [API] Agregue el parámetro &#39;reloadIfModified&#39; al método SDPackageMGR.loadUserPackage() para controlar si un paquete se ha vuelto a cargar si se ha modificado
* [API] Método Add SDPackageMgr.getPackages()
* [API] Añadir la posibilidad de obtener/añadir/eliminar rutas raíz de SDModuleMgr
* [API] Permite obtener el puntero del búfer de píxeles y el tono de una SDTexture
* [API] Permite recuperar el puntero de MainWindow
* [API] Permite crear menús personalizados en el menú principal
* [API] Permite crear DockWidgets personalizados en la ventana principal
* [API] Usar nombres de objeto para buscar menús en barras de herramientas
* [API] Proporcionar un sistema para administrar las notificaciones de la aplicación a la API
* [PythonIntegration] Agregue una variable de entorno predeterminada para buscar complementos de Python
* [PythonIntegration] Añadir búsqueda de texto y reemplazar al editor de Python
* [PythonIntegration] Instanciar complementos de Python al inicio
* [PythonIntegration] Tenga en cuenta la variable de entorno PYTHONPATH
* [PythonIntegration] Permitir la creación de barras de herramientas en widgets de gráficos
* [PythonIntegration] Compatibilidad con subprocesos de Python
* [PythonIntegration] Añadir un administrador de complementos (en el menú Herramientas)
* [Contenido] Rotación de vectores normal: añadir una entrada de imagen opcional para controlar el ángulo
* [Contenido] Nuevo filtro Mín./Máx.
* [Contenido] Nuevo filtro &quot;Flood Fill a índice&quot;
* [Contenido] Nuevo filtro &quot;Asignador de Flood Fill&quot;
* [Content] Nuevo filtro de Atlas splitter
* [Contenido] Mejora el filtro Tri Planar
* [Contenido] Nuevo filtro de Non Uniform Directional Warp
* [Contenido] Nueva deformación multidireccional
* [Contenido] Nuevo filtro de Extrusión de altura
* [Motor] Fxmap: nuevo patrón de &quot;Gradación con desplazamiento&quot;
* [Motor] Compatibilidad con el procesamiento uniforme de valores (nodo Nuevo procesador de valores)
* [Vista 3D] [Panaderos] Mejora el rendimiento de la cargadora OBJ
* [Vista 3D] Aumente las distancias del plano del clip de cámara
* [Preferencias] Añadir configuración para panaderos
* [Graph] Agiliza la invalidación evitando las comparaciones de cadenas
* [MDL] Compatibilidad con matrices MDL
* [UI] Mejoras en la IU de selección de motor
* [IRay] Actualización al SDK de IRay 2018.1.4
* [Administrador de dependencias] Usar &quot;última ruta&quot; al reubicar un recurso
* [Cocinar] Añada compatibilidad con etiquetas booleanas en la barra de base de datos
* Integrar Qt 5.12.2

**Corregido:**

* [Graph] Las conexiones se rompen al cambiar el nombre de la entrada
* [Gráfico] Se activan demasiadas invalidaciones al ajustar parámetros
* [Graph] La acción &quot;Copiar al Portapapeles&quot; no funciona si hacemos el clic derecho en una insignia
* [Graph] Mover un marco mediante Alt no se almacena en los archivos .sbs
* [MDL] El perfil de color no se actualiza automáticamente en el editor MDL
* [MDL] Bloqueo al exportar un módulo que contiene una configuración específica
* [MDL] Error al exportar un gráfico MDL que contiene un recurso LightProfile o MBSDF
* [UI] Los métodos abreviados ya no se muestran en los menús contextuales
* [UI] La ventana flotante se puede acoplar después de reiniciar
* [Scripting] La opción Cancelar no funciona en el editor de Python
* [Scripting] La opción &quot;sí a todo&quot; del menú guardar no funciona
* La lista desplegable [Parámetros] no se muestra correctamente después de la copia
* [Explorer] Al reubicar recursos, se debe abrir la última ruta reubicada de forma predeterminada
* [Biblioteca] El contenido de la biblioteca siempre se vuelve a generar al cambiar de una versión a otra
* [Biblioteca] Los mapas de bits importados se invalidan al guardar
* [IRay] El espacio de tangente no se calcula correctamente / asignación normal incorrecta
* [Función] Bloqueo o error al crear un gráfico nuevo a partir de una selección
* [API] El valor predeterminado de las propiedades no está definido

## Versión 8

### 8.3.4 (2018.3.4)

*(Lanzado: 12 de abril de 2019)*

**Agregado:**

* [Contenido] Transformación normal/Transformación de material: adición de una opción para activar la transformación Escalar y Sesgar

**Corregido:**

* [Contenido] El filtro de remolino no funciona correctamente cuando se utilizan funciones aleatorias en funciones de parámetros
* [Contenido] Transformación normal/Transformación de material: La normalidad no se normaliza después de una transformación de escala
* [Contenido] El remolino genera resultados incorrectos cuando la cantidad es aleatoria
* [Graph] Bloqueo al pulsar Mayús y arrastrar una salida y, a continuación, cambiar a Ctrl y arrastrar
* [Graph] Bloqueo al manipular puntos de división
* [Graph] Eliminación de rendimiento al mostrar insignias de nodo
* [Scripting] El uso de acciones personalizadas podría bloquearse después de 30 segundos
* [Preferencias/Proyectos] Se deben ejecutar las secuencias de comandos activadas de todos los proyectos (en la sección &quot;Secuencias de comandos&quot;)
* [MDL] Bloqueo al vincular un gráfico MDL a otro
* [Parámetros] Los nodos no se actualizan después de establecer la semilla aleatoria del gráfico en un parámetro expuesto
* [PSD] Al asignar un nodo de color se cambia el tamaño de la miniatura de la capa, pero no se asigna un nodo de escala de grises
* [API] Excepción no controlada con SDNode.getPropertyValueFromId()

### 8.3.3 (2018.3.3)

*(Lanzado: 19 de febrero de 2019)*

**Corregido:**

* [Contenido] Las salidas de Material base de PBR no tienen el nombre de grupo correcto

### 8.3.2 (2018.3.2)

*(Lanzado: 19 de febrero de 2019)*

**Agregado:**

* [Bakers] Añada una etiqueta que indique la configuración actual del sufijo &quot;Coincidir por nombre&quot;

**Corregido:**

* [Graph] Bloqueo al manipular puntos de división
* [Graph] Problema de invalidación al cambiar la profundidad de bits del nodo de entrada
* [Graph] Las opciones de cálculo de miniaturas ya no funcionan
* [Graph] Se muestra espacio vacío debajo de la ruta de exploración con un diseño de interfaz de usuario específico
* [Graph] El estilo del vínculo es incorrecto en el contexto
* [Graph] Las miniaturas no se muestran correctamente en gráficos de función/mdl en pantallas Hi DPI
* [Contenido] Color de fusión de salpicaduras de formas: ninguna opción para especificar el formato de mapa de normales
* [Contenido] Error ortográfico en la información sobre herramientas de interpolación lineal
* [Contenido] La transformación normal no gestiona correctamente la transformación de reflejo y sesgo
* [Contenido] Degradado Axial, Radial, Circular no admiten funciones aleatorias
* [Contenido] Degradado radial no funciona correctamente en formato no cuadrado
* [API] output\_exporter.sbs siempre debe actualizarse al utilizar el script export\_output
* [API] Bloqueo después de utilizar el script export\_output
* [API] No se puede establecer el valor numérico de las anotaciones en las entradas del gráfico de composición
* [Explorer] Bloqueo aleatorio al guardar un proyecto
* [Explorer] No se pueden abrir subconjuntos con extensión en mayúsculas
* [UI] El tamaño de la ventana &quot;Nuevo Substance&quot; no es persistente
* [UI] El menú contextual de la instancia de función no es coherente con el gráfico de composición
* [Panaderos] Bloqueo al abrir los panaderos en una malla específica
* [Panaderos] Cálculo incorrecto para panaderos de DXR cuando los UV tienen un valor de ordenadas 0
* [Updater] Bloqueo al cancelar el actualizador
* [Vista 3D] La esfera primitiva tiene sus UV desplazados por 1 unidad
* [Cocina] Tramado aleatorio al cocinar mapas de bits
* [Player] Los botones de control de ventana son pequeños
* [Player] Los iconos de botones están rotos

### 8.3.1 (2018.3.1)

*(Lanzado: 20 de diciembre de 2018)*

**Agregado:**

* [API] Agregue SDConnection.getOutputProperty() y SDConnection.getOutputPropertyNode()
* [API] Añadir documentación sobre todas las definiciones de recursos
* [API] Cambie la propiedad de anotación SDSBSCompNode &#39;visibleif&#39; a &#39;visible\_if&#39; para obtener coherencia

**Corregido:**

* [Graph] Pulsar la tecla TAB una segunda vez no cierra el menú Nodo
* [Graph] Las insignias de la vista 3D no funcionan correctamente en algunas situaciones
* [Graph] Los paquetes de solo lectura se pueden modificar
* [Panaderos] La barra de progreso actúa de manera extraña cuando se carga una malla de polietileno muy alta
* [Panaderos] Artefactos en malla con normales en cara
* [Bakers] El widget de parámetros y salida de Bakers no se puede descontraer
* [Explorer] Los recursos 3D se cargan cuando se abre un paquete
* [CmdLineArgs] &quot;—news hide\_changelog:true&quot; ya no funciona

### 8.3.0 (2018.3.0)

*(Lanzado: 05 de diciembre de 2019)*

**Agregado:**

* [Graph] Añadir una ruta de exploración al editar subgráficos/funciones
* [Graph] Añada TAB como método abreviado para generar el &quot;menú de nodos&quot;
* [Graph] Marcador de resaltado de nodos para nodos principales de selección
* [Graph] Añada Ctrl+E como método abreviado para abrir la función y los subgráficos de Pixel Processor
* [Graph] Conectar un nuevo nodo a la primera salida visible del nodo seleccionado
* [Graph] Añadir el nodo &quot;Insignias&quot;
* [Graph] Añadir advertencia al componer nodos mediante insignias
* [Graph] Añadir la posibilidad de buscar un nodo por su nombre, atributos o UID
* [API] Permitir la creación y modificación de datos
* [API] Permite exportar SDPackage y SDMDLGraph a módulos MDL (consulte SDMDLExporter)
* [API] Permite recuperar todos los nodos, enumeraciones y definiciones de estructura (consulte SDModuleMgr)
* [Vista 3D] Cambie a mapas de cubos para el procesador OpenGL
* [Vista 3D] Exportar imagen HDR lineal al guardar en .exr o .hdr
* [Panaderos] Integrar la tecnología de trazado de rayos DXR
* [IRay] Integrar el SDK de IRay 2018.1
* [Motor] SSE (CPU) Compatibilidad del motor para el procesamiento de imágenes de punto flotante hdr
* [Motor] Añada una opción de línea de comandos (—gpu x) para especificar el dispositivo de GPU dedicado al motor del Substance
* [Contenido] Nuevo nodo de Renderización PBR
* [UI] Fichas de repaso y barra de título
* [Administrador de dependencias] Impedir la actualización de la lista de dependencias cuando las acciones del usuario no afectan a las dependencias

**Corregido:**

* [Graph] Bloqueo al crear instancias de un gráfico en sí mismo
* [Graph] El nodo duplicado no está seleccionado
* [Graph] problema de cálculo al utilizar una misma instancia de nodo en 2 gráficas MDL diferentes
* [Graph] La tecla Z debe centrar la vista en el centro del cuadro de escena
* [Graph] Omitir el espacio de color en las reglas de conexión al utilizar el vínculo de material
* [Graph] Evite abrir salidas en la vista 3D al abrir una gráfica en conli
* [Graph] Pegar nodos es lento cuando se activa &quot;Abrir nodo recién creado&quot;
* [Vista 3D] Aserción al arrastrar y soltar una malla específica
* [Vista 3D] La opción de Escala de UV activada no funciona en el mapa de height
* [Contenido] Triplano: Diversos aspectos relacionados con el eje y las transformaciones
* [Contenido] Desenfoque de Pendiente Escala de grises: una de las muestras no tiene el modo de fusión correcto al utilizar min o max
* [Contenido] Resultado incorrecto de degradado lineal 2 a baja resolución
* [API] SDPackage.findResourceFromUrl() también podía recuperar recursos ubicados en otro SDPackage
* [API] SDPackage.getChildrenResources() siempre devuelve el primer elemento en modo no recursivo
* [API] [Documentación] Las enumeraciones, las estructuras ubicadas en la carpeta &quot;generada&quot; no se reflejan en la documentación
* [UI] La anchura de la vista 2D no debe restringirse
* [Gradient] Bloqueo al seleccionar en Mac
* [Explorer] Bloqueo al cerrar y volver a abrir un gráfico
* [Mac] El selector de color no funciona en varias pantallas
* [Parámetros] El cuadro de número en parámetros enteros no funciona
* [Cooker] Bloqueo al crear determinados nodos en OSX 10.13
* [Filtro de curva] Las teclas y los puntos de control pueden terminar con un valor -0.0 o un raro valor &quot;casi cero&quot; en el editor de curvas
* [Vista 2D] El widget de posición no está disponible para gráficos procedentes de sbsar
* [PSD] Problema de capa tras exportar con dependencias

### 8.2.2 (2018.2.2)

*(Lanzado: 04 de octubre de 2019)*

**Corregido:**

* [Contenido] La sombra de forma no funciona correctamente cuando el mosaico está desactivado
* [Contenido] El relleno de área en escala de grises o color aleatorio no funciona correctamente en algunos casos
* El Flood Fill [Content] es incorrecto en formato no cuadrado
* [Contenido] El Flood Fill a color/escala de grises está roto
* [Contenido] QuadTransform es irregular en la CPU
* [Contenido] La forma de estrella emite un modo de mosaico &quot;Sin mosaico&quot;
* [Contenido] Salida de color de mezcla de salpicaduras de formas con una profundidad de bits absoluta de 32f
* [Contenido] El color de fusión de salpicaduras de formas es largo de calcular si su formato no se establece en 32F
* [Graph] Bloqueo al vincular una imagen como entrada de un mapa FX mientras se muestran las propiedades de iteración
* [Graph] La temporización parece incorrecta al editar el gráfico en contexto
* [Graph] Bloqueo aleatorio al guardar el gráfico
* El modo de material [Graph] no funciona con sbsar
* [Vista 3D] La asignación de materiales no se restaura correctamente
* [Vista 3D] Algunos ajustes del archivo de estado de vista 3D no se cargan correctamente
* [Vista 2D] La visualización del Alpha siempre muestra negro
* [Vista 2D] El botón Mostrar imagen a escala de grises no funciona en imágenes con alfa
* [UI] el administrador de dependencias se genera al iniciarse aunque no esté activado en Mac
* [UI] Algunos botones realizan acciones incluso al soltar el ratón fuera
* [API] Bloqueo al intentar mantener un elemento de matriz fuera del ámbito de la matriz de la que procede
* [Gráfico MDL] La vista previa del nodo está invertida
* [MDL Graph] El Desplazamiento del nodo de previsualización es diferente del de la vista 3D
* [Console] El rendimiento se ralentiza cuando la consola contiene muchos mensajes
* [Console] Advertencias Qt al iniciar Designer en CentOS
* [FX-Map] Bloqueo al eliminar vínculos entre entradas y FX-map
* [Funciones] No se puede establecer un nodo de tipo de cadena como resultado en Recurso de función
* [Preferencias] No hay selección en el menú de preferencias, el usuario puede cambiar un valor accidentalmente mientras se desplaza
* [FX-Map] El cuadro combinado Input Image Index no se actualiza correctamente al añadir o quitar entradas
* [Dependencies] Bloqueo al eliminar recursos UDIM utilizados en un gráfico
* [API] SDLocationContext.getCurrentGraph() siempre devuelve null
* [Publish] URL incorrecta para la página de descarga del Substance Player

### 8.2.1 (2018.2.1)

*(Lanzado: 17 de agosto de 2018)*

**Agregado:**

* [UI] Añada un mensaje en la barra de tareas cuando la opción &quot;Edición en contexto&quot; esté activada
* [Preferencias] Vuelva a escribir la etiqueta de opción &quot;Edición en contexto&quot;

**Corregido:**

* [Gráfico] La opción Pegar sin método abreviado de vínculo no funciona en gráficos de composición
* [Graph] La invalidación es muy larga si la edición en contexto está activada
* [Graph] Bloqueo al vincular nodos
* [Graph] Bloqueo al volver a vincular nodos
* [Graph] Bloqueo al mover fotogramas
* [Graph] Bloqueo al cambiar UVTile en gráfico y malla ya no es udim
* [Graph] Bloqueo al utilizar Ctrl+Z después de pegar nodos
* [Graph] Seleccionar nodos principales es muy lento
* [Bakers] Los mapas ascendentes y descendentes permiten al usuario cambiar el tamaño de la fila
* [Bakers] La ruta para guardar o cargar el ajuste preestablecido nunca se guarda
* [Panaderos] La jaula se usa incluso cuando no está seleccionada en la ventana de cocción
* [Panaderos] La corrección de sesgo no funciona correctamente
* [Panaderos] Rendimiento muy lento cuando hay espacio UV negativo en la vista
* [Bakers] Hacer clic en el botón Cancelar no cancela la carga de la malla
* [Bakers] No se puede hornear con una jaula si el mapa de sesgo está vacío y establecido como verdadero
* [Contenido] El Flood Fill es lento en 4K
* [Contenido] La función Lineal a sRGB está dañada
* [Contenido] El fondo de escala de grises aleatorio en mosaico se controla mediante un float4 en lugar de un float, lo que impide la cocción
* [Contenido] Salpicadura de forma: El multiplicador de posición/mapa de vectores no funciona correctamente
* [Scripting] Ctrl + o no funciona en el editor de Python
* [Scripting] El editor de Python sigue preguntando incluso después de cerrar
* [Scripts] Bloqueo al crear varios scripts nuevos
* [UI] Los iconos de la biblioteca se pixelan
* [UI] Los paneles flotantes se comportan incorrectamente de forma predeterminada
* [Explorer] Bloqueo al importar una malla en CentOS
* [Explorer] La malla UDIM se carga dos veces
* [Cooker] No hay temporización para nodos en contexto
* [Cocina] Desbordamiento de la pila al cocinar
* [Licencia] Autenticación incorrecta con credenciales válidas
* [Licencia] Licencia flotante notificada más de una vez para el mismo usuario
* [Vista 3D] El valor predeterminado de V del material del azulejo UV es incorrecto
* [Vista 3D] Regresión del rendimiento en comparación con 2018.1.x
* [Preferences] Bloqueo al utilizar un archivo de configuración de un servidor
* [Biblioteca] Bloqueo al eliminar un filtro dentro de la biblioteca
* [SVG] Problema de dependencia al utilizar alias
* [Niveles] Los mapas de bits HDR de 32 bits hacen que el editor de niveles parpadee al mover la posición de los widgets
* [PSD] La ventana PSD de importación vinculada se muestra dos veces
* [Iray] La escena se actualiza cuando se modifica una luz desactivada
* [MDL] Bloqueo al eliminar todos los nodos de una plantilla MDL
* [Motor] Gran cantidad de desplazamiento en FX-Map puede congelar SD
* Crashpad se bloquea al inicio
* La variable de entorno Python hace que Designer se bloquee al iniciarse

### 8.2.0 (2018.2.0)

*(Lanzado: 19 de julio de 2018)*

**Agregado:**

* [UI] Nuevo estilo
* [UI] Nuevos reguladores
* [UI] Hacer que las ventanas flotantes realmente floten
* [UI] Cambiar el diseño de la ventana Preferencias
* [UI] Biblioteca: quitar barra de filtro
* [UI] Biblioteca: eliminar superposición de visualización de selección
* [UI] Añadir un mensaje en la barra de tareas cuando la aplicación está guardando automáticamente un paquete
* [UX] Propiedades: combinar los menús &quot;función&quot; y &quot;restablecer los valores predeterminados&quot;
* [Content] Nuevos nodos de Dispersión de forma (+ filtros complementarios)
* [Contenido] Añadir Flood Fill a los filtros de color/escala de grises
* [Contenido] Compatibilidad con nuevos Flood Fill: apoyar formas con taladros
* [Contenido] Flood Fill a degradado: Añadir entrada de imagen de Pendiente y ángulo
* [Contenido] Optimizar el filtro Nivel automático
* [Contenido] Nuevo filtro de extrusión de forma
* [Contenido] Transformación de material: agregar compatibilidad para mapas normales rotados
* [Contenido] Nuevos filtros de rotación de vector normal y transformación normal
* [Contenido] Normalización normal: mejorar la calidad de los resultados.
* [Contenido] Nuevo filtro Transformación trapezoidal
* [Contenido] Nuevo filtro de transformación cuádruple
* [Contenido] Añadir patrón de hemisferio al nodo Forma
* [Contenido] Añadir nuevos degradados con controles en la vista 2D
* [Contenido] Añadir salida UV al nodo &quot;Cube GBuffers&quot;
* [Graph] Fotograma: omitir texto de título mayor que el cuadro de marco para la selección
* [Graph] Añadir soporte para la edición en contexto de subgráficos (experimental)
* [Graph] La creación de Frame/Comment debería afectar al nodo bajo el cursor cuando se usa RMB
* [Graph] Fotograma: omitir texto de título mayor que el cuadro de marco para la selección
* [Graph] Reutilizar la ficha existente al abrir una función ya abierta
* [Graph] Crear una nueva pestaña cuando se utiliza &quot;Open Reference&quot;
* Función [Graph]: no mostrar propiedades de función al hacer clic en el fondo
* [Parámetros] Quitar el botón &quot;Exponer&quot; de los gráficos de fxmap
* Nivel [Parámetros]: Añadir un botón &quot;Invertir&quot;
* [Parámetros] Expanda el grupo &quot;Parámetros de entrada&quot; al crear un nuevo parámetro de entrada
* [Propiedades] Añada la información de la URL del paquete en los atributos del gráfico
* [Propiedades] Aumentar el tamaño del campo de descripción para los nodos de salida
* [Propiedades] Se permite introducir la función por píxel de procesador de píxeles incluso para paquetes de solo lectura.
* [Scripting] Nueva API de Python/editor de Python (primera iteración)
* [Bakers] Optimización de la transferencia de geometría durante el procesamiento
* [Vista 3D] Cambiar a perfil principal de OpenGL
* [Vista 3D] Compatibilidad con teselación/desplazamiento en Mac
* [Funciones] Recurso de función: lista de entradas de imagen en nodos de muestra

**Corregido:**

* [Graph] Bloqueo al vincular un nodo a otro
* [Graph] La obtención de variables en la función de semilla aleatoria del gráfico no funciona
* [Graph] Bloqueo al arrastrar y soltar ruido en un gráfico
* [Graph] Bloqueo al abrir un gráfico específico
* [Contenido] El resultado es diferente entre Color aleatorio del azulejo y Escala de grises
* [Contenido] Azulejo aleatorio: Cambios en los resultados al modificar el &quot;Modo aleatorio de simetría&quot;
* [Contenido] La detección de bordes no funciona con resoluciones que no son cuadradas
* [Panaderos] Artefactos al hornear curvatura usando una malla UDIM
* [Bakers] El mapa de Oclusión ambiental de la malla se invierte mientras se usa un mapa normal
* [Panaderos] La lista de conjuntos UV debe restringirse a los conjuntos UV disponibles
* [Explorer] se bloquea al eliminar recursos durante el procesamiento
* [Transform2D] Bloqueo al exponer parámetros de nivel de mapa Mip y color de fondo
* [Transform2D] Comportamiento incorrecto al exponer un Nivel de mapa MIP de transformación
* [PSDExport] El exportador de PSD no exporta correctamente la escala de grises 32F
* [Vista 2D] El cálculo del histograma no funciona con nodos 16F
* [PSD] Los PSD vinculados están dañados
* [Cooker] La función en el parámetro outputsize no se evalúa correctamente
* [Export] La ruta de exportación de los resultados debe ser la misma que la del paquete
* [Exportar] La ruta de exportación no se guarda con un patrón vacío
* [Templates] Falta el grupo para Posición en la plantilla de Painter
* [Help] la línea de comandos help no muestra —news en Mac
* [Dependencias] La exportación dos veces después de modificar el nombre de una carpeta no funciona

### 8.1.2 (2018.1.2)

*(Lanzado: 31 de mayo de 2018)*

**Agregado:**

* [Vista 3D] Permite establecer el estado de luz predeterminado en los ajustes del proyecto
* [Control de versiones] Elimine el tiempo de espera de 30 segundos al llamar a los scripts python

**Corregido:**

* Base de Suma fractal [Content]: resultado incorrecto en el tercer nivel (se ha añadido un nuevo gráfico)
* [Contenido] El fragmento de ruido de Perlin 3D se fuerza a 32 bits
* [Contenido] El degradado lineal 3 no proporciona el resultado correcto al utilizar un tamaño no uniforme
* [Contenido] Sobel normal no admite opciones de segmentación
* [Content] Checker\_1 está forzado a 8 bits
* [Contenido] Multiángulo a Normal: problema de cálculo interno
* [Contenido] El patrón de Stripe no admite valores &quot;Mayús&quot; negativos (bloqueo del motor)
* [MDL] Bloqueo al intentar abrir un proyecto MDL específico
* [MDL] El gráfico MDL no se calcula después de una operación de cierre o reapertura
* [Exportar] Las salidas de los gráficos no asignados se exportan mediante la herramienta por lotes
* [Exportar] La exportación de C16F en Exr genera una imagen en escala de grises
* [Panaderos] Las funciones de sesgo no se desactivan en la interfaz de usuario al hornear con una jaula
* [Bakers] Bloqueo cuando la jaula no tiene el conjunto UV correspondiente
* [Cocina] Subcocina: error de cocción relacionado con &quot;blend\_switch.sbs&quot;
* [Cooker] El gráfico publicado no se procesa correctamente
* [Motor] Transformación 2P: el color mate no es correcto
* [Explorer] Bloqueo al volver a importar una malla FBX
* [Widget de color] El selector de color de escala de grises solo selecciona el valor de canal rojo
* [Vista 3D] El uso &quot;textcoordN&quot; ya no funciona
* [Iray] El mapa normal se aplica dos veces para los dieléctricos

### 8.1.1 (2018.1.1)

*(Lanzado: 12 de abril de 2018)*

**Agregado:**

* [Vista 3D] Defina el rango predeterminado de &quot;Factor de teselación&quot; en [0, 16]

**Corregido:**

* [Vista 3D] Extraño artefacto visual con GPU AMD específica
* [Vista en 3D] Bloqueo con GPU AMD específicas
* [Vista 3D] [Panaderos] Las normales generadas en .obj tienen bordes duros en la costura UV
* [Vista 3D] Bloqueo al calcular armónicos esféricos
* [Bakers] No se puede establecer el recurso como &quot;incrustado&quot;
* [Bakers] bloqueo al hornear
* [Panaderos] Hornear 2 versiones diferentes de un mapa de la malla UDIM está roto
* [Bakers] Bloqueo al cambiar entre gráfico contextual y no contextual
* [Panaderos] Tener el mismo panadero dos veces los hará sincronizados
* [Bakers] al cambiar el nombre de la macro $(custom) se impide que se guarde correctamente
* [Bakers] Actualizar un mapa con bake debería bloquear la IU
* [Panaderos] Actualizar todos los mapas con bake crea recursos vacíos
* [Bakers] Al pulsar &quot;Intro&quot; para confirmar un valor de parámetro, se elimina el poli alto
* Tile Generator [Content]: Error Aleatorio de rotación cuando la cantidad X e Y son diferentes
* [Contenido] Algunos mapas de suciedades contienen instancias fantasma
* [Contenido] Cubo 3d: el uso de funciones aleatorias en parámetros no genera el resultado esperado
* [Contenido] Los ruidos fractales no se procesan correctamente cuando la Expansión no cuadrada está desactivada
* [Contenido] Las Celdas 2 y 4 no se comportan correctamente cuando la Expansión no cuadrada está desactivada
* [Graph] La actualización de una instancia sbsar crea un gráfico fantasma
* [Graph] La asignación mediante el clic derecho no debería mostrar el submenú de mosaicos UV para mallas que no sean UDIM
* [Graph] La barra de búsqueda republicada no se ha actualizado correctamente
* [Graph] Los nodos no se invalidan correctamente cuando cambia el recurso
* [Cooker] El parámetro de fusión alfa de Premult no se recupera correctamente de sbsar
* El filtro de niveles [Cocina] no fija los valores cuando se cocina en una barra lateral
* [Cooker] Las transformaciones implícitas se realizan antes de los nodos FX-Map
* [Explorer] Al pulsar la tecla Supr en un paquete, se pregunta al usuario si desea eliminarlo
* [Explorer][Bakers] Problema de reubicación
* [Curva] Bloqueo aleatorio al manipular teclas en el editor de curvas
* [MDL] El tipo de gamma no está configurado correctamente para uso personalizado
* [Parameters] Bloqueo al exponer un parámetro con el mismo identificador que una entrada existente
* [Propiedades] El uso de salida se edita sin distinción de mayúsculas y minúsculas

### 8.1.0 (2018.1.0)

*(Lanzado: 9 de marzo de 2018)*

**Agregado:**

* [Panaderos] Optimizar la cocción de alto contenido de poli
* [Panaderos] Mejorar el resultado en las costuras para el panadero Curvature
* [Panaderos] Mapas de cocción para mallas basadas en UDIM
* [Bakers] Añadir una vista 2D dedicada en la ventana de Baker
* [Graph] Compatibilidad con UDIM
* [Graph] Optimizar el rendimiento de la cocina
* [Graph] Mejora la velocidad de generación de miniaturas de nodos
* [Graph] Mantener la caché de nodos solo para gráficos abiertos
* [Graph] Añadir barra de herramientas en el gráfico de composición para controlar el modo de generación de miniaturas
* [Vista 3D] Añada una caché de geometría para optimizar la visualización de mallas de alta definición
* [Vista 3D] Compatibilidad con la visualización de UDIM (mostrar el mosaico actual)
* [Vista 3D] Actualizar cubo redondeado con topología uniforme
* [Vista 3D] Evite guardar escenas todo el tiempo
* [Contenido] Añadir nodos de ruidos 3D (Perlin, Perlin Fractal, Worley, Simplex)
* [Contenido] Nodo Agregar máscara de volumen 3D
* [Content] Añadir nodo de 3D linear gradient
* [Content] Nodo Agregar búferes de cubo 3D (útil para previsualizar nodos basados en 3D)
* [Contenido] Nodo Agregar proyección plana 3d
* [Contenido] Añadir el filtro Desenfoque radial
* [Parámetros] Visualización de las propiedades de entrada/salida de la imagen en las propiedades del gráfico
* [Parámetros] Permitir la edición de la ruta de acceso de los recursos
* [Motor] Admite hasta 8.000 texturas con el motor de CPU (SSE2)
* [Motor] Permitir que el convertidor de escala de grises utilice grosores HDR para el motor HDR
* [Preferencias] Añada una opción para desactivar la creación automática de nodos de conversión
* [Preferencias] Establecer la compresión predeterminada para png a la &quot;mejor velocidad&quot;
* [UI] vínculo html de soporte en propiedades de gráficos
* [UI] Centrar los botones &quot;Sí / No / Cancelar&quot; en el cuadro de diálogo de confirmación de guardado
* [Explorer] Visualización de la jerarquía de malla mejorada
* [IRay] Integrar el SDK de IRay 2017.1.4

**Corregido:**

* [Bakers] Al agregar una macro en el campo de nombre de salida, no se agrega en la posición del cursor
* [Bakers] No se muestra ningún material en la lista si el objeto no tiene material
* [Bakers] Al pulsar Intro para confirmar que los parámetros de baker abren un menú desplegable
* [Bakers] Las texturas al horno no deben generar comandos en la pila Deshacer
* [Bakers] Bloqueo al convertir una textura transferida de una malla sin especificar una textura
* [Explorer] &quot;Guardar como&quot; debe utilizar el nombre de archivo existente en lugar del primer nombre de recurso
* [Explorer] Comportamiento incorrecto al arrastrar y soltar un recurso de un paquete a otro
* [Explorer] Al hacer clic con el botón secundario no se deben abrir los datos de las propiedades
* [Explorer] El icono de los elementos de escena no tiene el fondo correcto
* [Graph] Ctrl+D no funciona en Linux
* [Graph] La función de revinculación múltiple a veces conecta solo un enlace
* [Gráfico] Ctrl+Mayús+D debería eliminar solo los vínculos externos, no los internos
* [Graph] El vínculo entre la escala de grises y el color no es correcto
* [Vista 3D] No se puede establecer un recurso como asignación de env
* [Vista 3D] El sombreador de información de malla no muestra los resultados en el espacio de color correcto
* [Parámetros] Los parámetros no exponibles siguen siendo exponibles mediante CTRL+P
* [Parámetros] Los campos de texto no se actualizan correctamente al deshacer o rehacer.
* [Contenido] Artefactos en Mapa de Suciedad 003
* [Contenido] La entrada principal de la escala de grises de transformación de vectores parece incorrecta
* [Cooker] sbscooker genera un error cuando falta un recurso
* [Cooking] Bloqueo con desbordamiento de pila cuando la cadena de nodos es demasiado larga
* [UI] El botón Salir de la administración de licencias no funciona

## Versión 7

### 7.2.5 (2017.2.5)

*(Lanzado: 19 de febrero de 2018)*

**Agregado:**

* [Contenido] Errores tipográficos en function.sbs
* [Contenido] Reducir el rango predeterminado de ruido de perlín y gaussiano
* [Vista 3D] Ajuste el rango predeterminado para el parámetro &quot;Escala de Height&quot;
* [AXF] Actualización de plantillas de mdl

**Corregido:**

* [Vista 3D] [Panaderos] Las normales no se vuelven a calcular si el modelo no tiene normales
* [Graph] El recurso de mapa de bits no cuadrado está vacío una vez creado una instancia
* [Contenido] El ruido de Perlin produce resultados diferentes entre la CPU y el motor de GPU

### 7.2.4 (2017.2.4)

*(Lanzado: 08 de febrero de 2018)*

**Agregado:**

* [Importación de AXF] Permite especificar el modo de filtrado en mapas de bits de entrada
* [Vista 2D] No cambiar la proporción de la imagen en la vista 2D cuando el tamaño físico está activado

**Corregido:**

* [Biblioteca] se bloquea al activar o desactivar la ruta en las preferencias
* [Baker] Buscar por nombre ignora algunas mallas con nombres específicos
* [Contenido] El filtro Premult to Straight elimina el canal alfa

### 7.2.3 (2017.2.3)

*(Lanzado: 19 de enero de 2018)*

**Corregido:**

* Error de [Content] en el nodo &quot;Validación de color base de PBR&quot;
* [Contenido] El parámetro de trastorno se rompe en la Celda 2
* [Contenido] Las Celdas 3 se invierten al utilizar valores específicos en parámetros
* [Contenido] Polígono 2: Artefactos visuales con configuraciones específicas
* [Contenido] La escala de grises del Tile Generator está en 8 bits de forma predeterminada
* [Contenido] Muestra de mosaico: el parámetro aleatorio específico del patrón no funciona
* [Content] Mapeado de formas: Las funciones aleatorias no se pueden utilizar para controlar la cantidad de motivo, el radio, la anchura, etc
* [Contenido] Polígono 2: Las funciones aleatorias no se pueden utilizar para controlar la cantidad de lados
* [Contenido] Algunos generadores de ruidos/patrones generan advertencias en la consola
* [Contenido] Non-Square-Transform-Grayscale genera un tamaño de píxel incorrecto
* [Contenido] El filtro de remolino no tiene en cuenta el modo de mosaico
* [Graph] Arrastrar y soltar un recurso de mapa de bits en el nodo Entrada de imagen ya no funciona
* [Graph] CTRL+R (recargar) ya no funciona
* [Graph] Problema al utilizar un marco en otro marco
* [Graph] Bloqueo al mover fotogramas que contienen bordes
* [Graph] La instancia &quot;Shape (Legacy)&quot; se transforma en &quot;Shape&quot; al guardar
* [Baker] Bloqueo al utilizar 2 imágenes que no funcionan
* [Panaderos] Color de la malla: Los identificadores de submalla y grupo siempre devuelven una imagen en negro
* [Panaderos] AO de Mesh: La distancia del oclusor se fija en 1 independientemente del valor de entrada
* [Iray] Bloqueo al cambiar a Iray
* [Iray] El valor de segmentación debe afectar a la intensidad de la escala alta
* [Iray] Error al cargar IRay en el equipo Windows donde VCCOMP110.dll no estaba presente
* [Vista 3D][Panaderos] Los UV no se pueden descodificar del obj exportado de Modo
* [Vista 3D] Las intensidades de Desplazamiento no son consistentes entre Opengl e Iray
* [Vista 3D] La intensidad de Oclusión de Desplazamiento/paralaje es el doble de lo que debería ser
* Desplazamiento [Vista 2D] al mostrar la imagen alfa
* [Cooker] No se encuentra el parámetro constante ($tiling) cuando se usa dentro de una instancia de gráfico
* [Cooker] Evaluación incorrecta de la variable en instancias encadenadas
* [Parámetros] La ruta del recurso PKG de mapa de bits no debe poder editarse
* [Parámetros] Los parámetros de un mismo grupo son invisibles si sólo un parámetro tiene su visibilidad en false
* [PSD] No se puede importar o vincular un archivo de PSD de una carpeta con nombres que contengan caracteres especiales
* [Funciones] Los parámetros de las funciones no deben tener una opción de visibilidad
* [LicenseService] Se produce una excepción al obtener información sobre nodos
* [UI] Al seleccionar texto en el campo de descripción, se mantiene resaltado

### 7.2.2 (2017.2.2)

*(Lanzado: 23 de noviembre de 2017)*

**Corregido:**

* [Contenido] Errores tipográficos en &quot;Direccional ...&quot; nodos
* [Contenido] Varios tipos
* [Contenido] El mosaico Sampler se define en &quot;32 bits absolutos&quot;
* [Content] Mapeado de formas: artefactos visibles en el borde de la forma en algunos casos
* Los parámetros de mosaico [Content] y &quot;Expansión no cuadrada&quot; en el polígono 1 están dañados
* [Contenido] Las opciones &quot;Raíz aleatoria&quot; y &quot;Expansión no cuadrada&quot; no funcionan con Ruido anisotrópico
* [Contenido] Instancia de &quot;forma&quot; rota en algunos mapas de Suciedad
* [Vista 3D] La escala UV no se aplica si la escala de height es 0
* [Vista 3D] El reflejo con la persiana del sombreado ya no funciona
* [Vista 2D] La ventana de información tiene el diseño roto
* [Graph] Problema al controlar el tamaño de salida con una función en un mapa de bits vinculado creado en un gráfico
* [Función] El gráfico no se invalida cuando se elimina un vínculo
* [Biblioteca] Los favoritos no funcionan
* [Exportación de PSD] El contenido del archivo de PSD cambia cada vez que se realiza una exportación
* [Gradient] Bloqueo al manipular teclas en el editor de degradados
* [Plantillas] El mapa de posición de las plantillas de Substance Painter es incorrecto
* [AxF] height físico incorrecto
* [MDL] La escala UVW del tamaño físico se invierte en los nodos MDL SBS
* [Panaderos] $custom ya no funciona
* [Preferencias] Bloqueo al iniciarse en Mac

### 7.2.1 (2017.2.1)

*(Lanzado: 20 de octubre de 2017)*

**Corregido:**

* [Motor] Bloqueo al procesar texto con el motor de GPU
* [Contenido] Mosaico en Sampler: El identificador de fila/columna no funciona correctamente si no es cuadrado
* [Contenido] Azulejo Sampler Color: La parametrización de color es incorrecta
* [Contenido] Mosaico en Sampler: valor predeterminado incorrecto para la cantidad de patrón X / Y
* [Exportar] A los PSD exportados les faltan metadatos

### 7.2.0 (2017.2.0)

*(Lanzado: 19 de octubre de 2017)*

**Agregado:**

* [Contenido] Añadir relleno de área y filtros asociados (convertir una máscara en blanco y negro en degradados, colores aleatorios, etc.)
* [Contenido] Añada nuevos ruidos, mapas de Suciedad y generadores de motivos que admitan formato no cuadrado (las versiones anteriores se marcan como &quot;Heredadas&quot;).
* [Contenido] Se ha añadido una nueva Splatter Circular con muchas más funciones
* [Content] Añadir nuevo generador de Scratches
* [Contenido] Añadir filtro de remolino
* [Contenido] Añadir selección de histograma
* [Contenido] Añadir patrón de estrella
* [Contenido] Añadir filtro de Asignador de formas
* [Contenido] Añadir filtro de transformación vectorial
* [Contenido] Añadir degradado lineal 3
* [Contenido] Azulejo Aleatorio / Tile Generator: añadir modo de simetría (h+v, h, v)
* Tile Generator [Content]: Añadir entrada de varias imágenes
* [Contenido] Cambie el nombre &quot;Combinación RGB-A&quot; por &quot;Combinación Alpha&quot;
* Visualización de la salida del nodo del conmutador [2D View] mediante la tecla C
* [Vista 2D] Optimizar el diseño de histograma/información en función de su proporción de visualización
* [Vista 2D] Añada un botón para activar o desactivar la visualización del mosaico
* [3DView] Optimización de la velocidad de cálculo de los armónicos esféricos
* [Vista 3D] Actualizar sombreadores PBR para utilizar muestreo de Fibonacci en lugar de Hammersley
* [Vista 3D] Añada una opción para guardar el estado de la escena actual como predeterminado
* [Vista 3D] [Panaderos] Serializar datos en formato legible por los seres humanos
* [Bakers] Añadir ajustes preestablecidos de exportación/importación (json)
* [Publish] Crear el archivo sbsar como no sólido
* [Publish] Almacene la imagen/miniatura del gráfico en la barra de búsqueda
* [Publish] Mostrar una barra de progreso cuando se publica un paquete
* [Dependencias] Muestra el archivo .sbs que solicita una dependencia en la &quot;Ventana de dependencias que faltan&quot;
* Ventana Informe de [Dependencias]: mostrar el icono verde cuando se haya resuelto el problema
* [Dependencias] Añada una opción para abrir las dependencias personalizadas del paquete en el explorador de paquetes
* [Preferencias] Añada una opción para establecer el estado de escena predeterminado en la configuración del proyecto
* [Preferencias] Añada una opción para activar o desactivar la ruta de la biblioteca
* [Graph] Añada una opción para realizar una captura de pantalla (a escala 1:1) del gráfico
* [Graph] Quitar información sobre herramientas del fondo de gráficos de composición
* [Scripting] Devoluciones de llamada onBeforeFileLoaded y onAfterFileLoaded
* [Motor] Añadir un parámetro base para ajustar el modo de proporción de píxeles
* [Console] Mejorar el rendimiento de la consola
* [Parámetros] Widget de nueva posición (XY)
* [Israel] Actualización al SDK de IRay 2017.1
* [PSD] Guardar el estado del widget de PSD como texto en lugar de binario
* [Biblioteca] Utilice los pulgares de sbsar si existe
* [Explorer] Cambiar nombre &quot;Dependencies..&quot; entrada a &quot;Administrador de dependencias&quot;
* Importación de archivos AXF

**Corregido:**

* [MDL] Error al exportar el módulo MDL si la textura está conectada a un parámetro expuesto
* [MDL] Intente registrar la dependencia para las variables de cadena MDL (nodo constante)
* [MDL] Bloqueo después de cerrar el paquete
* [MDL] Bloqueo al conectar un flotador 3 a un nodo de color
* [MDL] no puede abrir la biblioteca de nodos al liberar un nodo de vínculo en un marco
* [MDL] Bloqueo al utilizar una textura de archivo
* [MDL] El comportamiento de dependencia registra demasiados operandos
* [Graph] Los nombres de los conectores se desactivan tras la edición de FX-Map
* [Graph] Bloqueo al deshacer
* [Graph] Comportamiento extraño con vínculos entre nodos
* [Graph] dispersión y desconexión de nodos contraídos al deshacer
* [Graph] Las instancias de función no se actualizan cuando se cambia la referencia
* [Control de versiones] El paquete se vuelve a cargar cuando se activa una acción personalizada de Control de versiones
* [Control de versiones] Los espacios de trabajo de control de versiones deshabilitados siguen estando disponibles en el menú contextual de un paquete
* [Control de versiones] Quitar acción personalizada no quitarla del menú contextual de un paquete
* [Propiedades] La previsualización de parámetros no se actualiza al utilizar el gizmo
* [Iray] Problema de visualización de tiempo máximo
* [Iray] Problema con la opción de pausa
* [Bakers] Bloqueo al convertir UV a SVG usando la traducción al coreano o japonés
* [Panaderos] cambiar el camino después de una primera cocción no funciona
* [Exportador de PSD] deshacer el problema
* [PSD] y las capas están bloqueadas en Photoshop CS5
* El cursor de color [UI] siempre se establece en blanco cuando se crea un nodo de color uniforme
* [UI] Al abrir una ficha existente, debería mostrarse en lugar de duplicarse.
* [Presets] se bloquea al cambiar el tipo de parámetro utilizado en un ajuste preestablecido
* [Vista 3D] se combinan muestras con el mismo uso
* [Vista 2D] La información de píxeles no funciona en imágenes cuya resolución no sea una potencia de 2
* [Biblioteca] Problema al cambiar el nombre de los filtros
* [Datos] Corrección de diversos errores tipográficos en archivos SBS
* Nodo de nivel [Parameters]: problema de precisión de nivel automático
* [Preferencias] Los botones de directorios de plantillas deben desactivarse para &quot;Proyecto predeterminado&quot;

### 7.1.4 (2017.1.4)

*(Lanzado: 2 de octubre de 2017)*

**Agregado:**

* [Panaderos] Añadir la curvatura de la malla de nuevo
* [Comprobador de nueva versión] Agregar una opción de línea de comandos para deshabilitar la comprobación de la nueva versión (—news hide\_changelog:true)
* [Scripting] Deshabilitar tiempo de espera de Qprocess

**Corregido:**

* [Panaderos] no puede cambiar el color del material en UV a SVG
* [UI] no puede cerrar la vista del gráfico haciendo clic en la rueda
* [Contenido] Algunos ruidos se expresan en 8 bits en lugar de 16
* [Contenido] Curvatura suave genera un resultado incorrecto cuando el mosaico está desactivado
* [Text] se bloquea al cambiar el tamaño de fuentes específicas

### 7.1.3 (2017.1.3)

*(Lanzado: 31 de agosto de 2017)*

**Corregido:**

* [Vista 3D] bloqueo al intentar mostrar las opciones de la vista 3D en Mac 10.10.5
* [Vista 3D] La información de texto no se muestra en la vista 3D cuando se utiliza la pantalla de ppp alto
* [Vista 3D] La preferencia global para OpenGL/DirectX no se tiene en cuenta al restablecer el material
* [Contenido] Height normal: normal se invierte al utilizar el muestreo de Sobel
* [Contenido] La Oclusión ambiente (hbao\_2) no se comporta correctamente si se define como no cuadrada
* [Contenido] Las entradas de los generadores de máscaras no están en el mismo orden que &quot;Combinador de datos de malla&quot;
* [Vista 2D] Histograma: la información de selección no se actualiza al cambiar la imagen
* [Vista 2D] Histograma: La información de rango usada no se muestra para imágenes en escala de grises
* [Presets] se bloquea al cambiar el nombre de un ajuste preestablecido de un gráfico utilizado en otro gráfico
* [Graph] X e Y se invierten en la barra de herramientas Tamaño principal

### 7.1.2 (2017.1.2)

*(Lanzado: 3 de agosto de 2017)*

**Corregido:**

* [Contenido] Problema de filtrado en los filtros &quot;Smart Auto Tile&quot; y &quot;Crop Grayscale&quot;
* [Contenido] Los filtros de biblioteca no tienen en cuenta la preferencia de OpenGL/DirectX
* [Contenido] No se puede cocinar SBSAR con non\_square\_transform
* [Contenido] Forma de panorama: La zona interactiva se refleja en el canal del RGB
* [Contenido] Mosaico en Sampler: La parametrización de color de posición no está normalizada
* [Contenido] Mosaico en Sampler: Los motivos son invisibles si el mosaico está desactivado
* [Graph] El modificador $normal\_map\_format no funciona cuando se utiliza el menú de la biblioteca/barra espaciadora
* [Graph] Formato incorrecto en el nodo de mapa de bits al arrastrar y colocar un recurso RGBxxF
* [Panaderos] El color de la malla con el color del material está roto
* [Vista 3D] cada cambio en la vista 3D genera acciones en la pila Deshacer
* [Dependencias] se bloquea cuando un gráfico carece de recursos en la biblioteca personalizada
* [Iray] El bloqueo al iniciarse en la versión OSX es anterior a la 10.11

### 7.1.1 (2017.1.1)

*(Lanzado: 18 de julio de 2017)*

**Agregado:**

* [Bakers] Añadir una &quot;acción de restablecimiento&quot; en los campos de recursos
* [Panaderos] Usar color negro cuando no se encuentra color de vértice
* [Ajustes preestablecidos] Ocultar el widget de ajustes preestablecidos en instancias en las que no hay ajustes preestablecidos disponibles
* [Preferencias] Elimine la opción &quot;Calcular binormal por fragmento&quot; en la configuración del proyecto (ahora esta opción se gestiona en el complemento de fotogramas tangentes).
* ajustes de sbsupater.exe

**Corregido:**

* [Bakers] El sistema de &quot;error&quot; ya no funciona
* [Bakers] opciones de serialización: las claves antiguas permanecen
* [Bakers] se bloquea al cambiar el nombre de un panadero
* [Bakers] Problemas con la IU
* [Contenido] Filtro de coincidencia de color: diferencia entre CPU/GPU
* [Contenido] Algunos GrungeMaps generan imágenes de 8 bits en lugar de 16 bits
* [Graph] Bloqueo al utilizar el nodo X &quot;switch links&quot; en fx-map
* [Vista 3D] Bloqueo aleatorio al abrir la vista 3D
* [Vista 3D] Los binormales siempre se calculan por fragmento, independientemente del complemento de espacio tangente
* [Updater] Error XML al utilizar una fuente específica
* El módulo [Cooker] del número negativo no devuelve el mismo resultado que el motor
* [UI] problema de interfaz al utilizar el degradado de selección en la pantalla de alta PPP
* [MDL] El nodo de color no mantiene este valor
* [Packaging] Falta el plugin Mikkt Unreal tangent space

### 7.1.0 (2017.1.0)

*(Lanzado: 29 de junio de 2017)*

**Agregado:**

* [Bakers] Nueva IU
* [Panaderos] Mantenga una caché de malla de alta definición hasta que se cierre la ventana del panadero
* [Bakers] Añade una opción para corregir la deformación de sesgo usando una máscara de escala de grises
* [Panaderos] Soporte de uso-alto-poli-como-bajo-poli en panaderos de malla
* [Bakers] Hacer que la ventana Bakers no sea modal
* [Bakers] Almacenar el estado en un archivo .sbs en formato legible por humanos
* [Parámetros] Copiar/Pegar parámetros de un gráfico a otro
* [Parámetros] Añada una opción para copiar un único parámetro de entrada (y pegarlo posteriormente)
* [Parámetros] Quitar el botón de función en el parámetro &quot;Modo de color&quot;
* [Parámetros] Editar/Guardar/Mostrar ajustes preestablecidos de parámetros incrustados
* [Parámetros] Permite al usuario copiar atributos de parámetros cuando un paquete está bloqueado
* [Vista 3D] Ya no se almacena la última configuración de vista 3D de sesión en el Registro
* [Vista 3D] Crear nuevo recurso 3D a partir de la escena actual
* [Vista 3D] Ya no almacena el estado de vista 3D de una sesión a otra en el Registro
* [Vista 3D] Combine los menús &quot;Escena&quot; y &quot;Geometría&quot;
* [Vista 3D] Separe la conversión sRGB del sombreador de fragmentos (deberá actualizar los sombreadores personalizados).
* [Vista 3D] Agregue una opción para crear un nuevo recurso 3D a partir del estado actual
* [Vista 3D] Mejora el mensaje de error generado cuando #include falla en un código de sombreado
* [Vista 3D] [Explorador] Crear una escena 3D a partir de elementos primitivos
* [Vista 3D] Mostrar el número de línea correcto cuando la compilación del sombreador GLSL falló y el código contiene directivas #include
* [Gráfico] Cambiar el tamaño de un marco desde todos los vértices o bordes
* [Graph] Almacene la información de Tamaño del padre en el recurso de gráfico en lugar de en el registro local
* [Graph] optimizar la velocidad de generación de miniaturas de nodo
* [Graph] Exponga el presupuesto de caché de memoria en Preferencias
* [Graph] Añada la opción &quot;Restablecer y ver en vista 3D&quot; en los nodos
* [Content] Conversor PBR: Añadir nuevos ajustes preestablecidos de Arnold 4/5, Corona 1.6 y Renderman
* [Content] Optimización del nodo AutoLevel y compatibilidad con entrada HDR
* [Contenido] Optimizar el filtro de HBAO cuando Optimización de GPU está desactivada, añadir la versión de 16 ejemplos
* Función no compatible del SVG de salida [Cooker] en el registro
* [Cocina] No descarte todo el recurso del SVG si solo no se admite una función
* [UI] Aumentar tamaño de bloque de descripción
* [UI] Añadir información de ruta de archivo en instancias de gráficos
* [Funciones] Añadir &quot;Open Reference&quot; en instancias de función
* [Funciones] Mostrar la lista de gráficos de funciones al arrastrar y soltar .sbs en un gráfico de funciones
* [Explorador] Crear nuevo recurso 3d a partir de primitivo
* [Motor] Agregar variable $tiling
* [Curva] Añada opciones para voltear horizontal o verticalmente la curva
* [Gestión de color] Leer perfil ICC en mapas de bits
* [Export] Añada &quot;Label&quot;, &quot;Group&quot; y &quot;User Data&quot; en la lista de macros de Patrón
* [Preferencias] permite cambiar la ruta de los archivos temporales
* [Doc] Añadir formato de gráfico MDL a la documentación del formato SBS

**Corregido:**

* [Graph] Problema de caché: ver salidas en vista 3D ya no funciona
* [Graph] Borrar problema de caché
* [Graph] Las solicitudes de generación de miniaturas de nodo no se cancelan cuando se invalida el gráfico
* [Graph] Problemas de resolución después de usar F5
* Falta la vista del gráfico [Graph] al iniciarse
* [Graph] La modificación de un parámetro genera varias llamadas de procesamiento
* [Graph] Bloqueo al utilizar una plantilla personalizada que contiene mapas con bake
* [Graph] Bloqueo al vincular nodos en una función gráfica
* [Vista 3D] El problema de carga paralela con ProgressManager
* [Vista 3D] El procesamiento con iray de imágenes con resolución personalizada no está en el fotograma completo
* [Vista 3D][Iray] La definición de material no se mantiene
* [Vista 2D] El histograma está vacío en las imágenes LDR
* [Vista 2D] Problema de visualización cuando el modo de segmentación está activado
* Parámetros [MDL] no expuestos
* [MDL] Bloqueo al mover una MDL de un paquete a otro durante el procesamiento
* [MDL] No pregunte dónde asignar el MDL al hacer doble clic en el gráfico
* [Bakers] Bloqueo al bloquear un archivo .obj específico
* [Panaderos] La textura transferida de la malla / normal da un resultado incorrecto
* [Transformación 2D] No se pueden utilizar las teclas de flecha para cambiar el desplazamiento en el nodo de transformación 2D
* Problema de artefacto [Transformation 2D] con baja resolución
* [Updater] El informe de actualización no aparece al pulsar Ctrl+o/abrir
* [Propiedades][Formato] Algunos caracteres se escapan dos veces en UserTags
* [Nodo de mapa de bits] Ctrl Z no funciona en la vista 2D
* [Preferencia] Espacio en blanco inútil en la ficha Alias
* [Installer] La instalación de una versión anterior no funciona la primera vez
* Lista desplegable [Parámetros]: colocar algunos espacios en la última etiqueta de valor congela SD indefinidamente
* [UI][MAC] &quot;about Substance&quot; muestra información de Iray
* [SVG] bloqueo al importar un SVG específico
* [Contenido] Filtro de HBAO: El parámetro Radio se comporta de forma diferente en función de la resolución (se ha añadido un nuevo archivo hbao\_2.sbs, el antiguo archivo hbao.sbs ha quedado obsoleto)

## Versión 6

### 6.0.4

*(Lanzado: 21 de junio de 2017)*

**Corregido:**

* Bloqueo de [Graph] al utilizar el método abreviado X
* [Graph] se bloquea al eliminar un vínculo entre nodos
* [Graph] Si se elimina un punto de división, SD se bloquea
* [Contenido] Error en mg\_surface\_brush
* [Contenido] Calidad inferior en HBAO en comparación con 6.0.2
* [Biblioteca] Los iconos de filtros personalizados no se guardan
* [Explorer] Bloqueo al abrir un recurso 3D que hace referencia a un archivo que falta
* [Bakers] La opción Transferir textura desde malla se duplica si está activada la opción &quot;Normal&quot;

### 6.0.3

*(Lanzado: 01 de junio de 2017)*

**Agregado:**

* [Exportar] Guardar tamaño físico como ppp en texturas exportadas
* [Vista 2D] Muestra la etiqueta del parámetro de matriz en el menú Transformación

**Corregido:**

* [Contenido] Mosaico en Sampler: La parametrización de color de posición no está normalizada
* [Contenido] Recortar: Gráfico fantasma en procesador de píxeles
* [Contenido] Forma de panorama: La zona interactiva se refleja en el canal del RGB
* [Contenido] El filtro de HBAO puede generar una resolución negativa
* [Contenido] El filtro Coincidencia de color se procesa incorrectamente en algunas situaciones
* [Contenido] &quot;Premultiplicado a recto&quot; elimina el canal alfa
* [Contenido] Errores tipográficos en varias etiquetas
* [Graph] La información de Profundidad de bits se corta cuando la escala de ppp se establece en 125.1520 o 175 %
* [Graph] Cuando se pega una selección que contiene un marco, el marco no se selecciona
* [Gráfico] Cuando una selección contiene un comentario, los elementos pegados se desplazan en el gráfico
* [Graph] problema de puntos de división
* [Graph] Algunos conectores de pines no se ajustan al pasar el cursor por encima
* Falta la vista del gráfico [Graph] al iniciarse
* [Export] faltan mapas de bits tras la exportación
* [Export] No exporta las dependencias de la versión de Steam
* [Bakers] choque con la malla que tiene demasiados conjuntos UV
* [Bakers] Bloqueo de panadero de mapa UV al hornear mallas sin conjuntos UV
* [Motor] Error de Sampler con Fxmap+HDR
* [Motor] Bloqueo con imágenes JPEG de alta resolución
* [Vista 2D] Falta el widget de transformación en la vista 2D cuando el modo de vista previa de mosaico está activado
* [Vista 3D] La instancia de gráfico con uso personalizado no se envía correctamente a la vista 3D
* [Preferencias] Ruta incorrecta para mikktspace.dll
* [Explorer] al mover un recurso de mapa de bits en un paquete, aparece el menú &quot;vincular/incrustar&quot;
* [Parameters] se bloquea al utilizar &#39;tiling&#39; como nombre de parámetro
* [MDL] sin vínculos de color entre nodos
* [Linker] Procesador de píxeles: Generación incorrecta de sombreadores GLSL
* [Cooker] Problema de Profundidad de bits

### 6.0.2

*(Lanzado: 17 de marzo de 2017)*

**Agregado:**

* [Motor] Integra el último motor con optimización de descompresión jpeg

**Corregido:**

* [Contenido] El parche de clonación ya no funciona
* La salida de Height [Content] no forma parte del grupo de materiales en plantillas
* [MDL] Bloqueo al eliminar una instancia de gráfico
* [MDL] No se muestra ninguna advertencia entre nodos en conflicto
* [MDL] Mensajes de advertencia inútiles al exportar
* [Curva] La exposición de parámetros de direccionamiento no debe ser exponible
* [Motor] Bloqueo al importar una barra de búsqueda que contiene un mapa de bits HDR
* [Nodo de texto] La especificación de fuente genera un archivo XML no válido
* [Editor de degradado] Los valores no se fijan correctamente
* [Vista 3D] Bloqueo al utilizar un HDRi personalizado (alta resolución) como entorno

### 6.0.1

*(Lanzado: 3 de marzo de 2017)*

**Agregado:**

* [Panaderos] Mejorar la gestión de las tareas de progreso
* [Bakers] Cambiar la información sobre herramienta de error cuando no hay ninguna malla seleccionada
* [Propiedades] Los parámetros del efecto de postproducción 3DView deben desactivarse cuando la opción &quot;Posprocesamiento&quot; está desactivada en Preferencias
* [Licencia] Permitir la especificación de una ruta personalizada para la licencia de Substance Designer 6
* [Degradado] Desactive el regulador de &quot;precisión&quot; si no se ha realizado ninguna selección de degradado
* [Cocina] Ignorar recurso faltante en la entrada de imagen para evitar que falle la cocción
* [Vista 3D] Control de cambios en fugas de reflejos de specular
* [Graph] Añada más parámetros para la compatibilidad del motor v6

**Corregido:**

* [Panaderos] El mapa normal de la malla (espacio mundial) se voltea en el eje Y
* [Panaderos] Al hornear una malla sin UV no se informa del error
* [Panaderos] La normalidad promedio no funciona
* [Panaderos] SD se bloquea al hornear AO con una malla específica
* [Bakers] El formato de salida no se ha restaurado correctamente
* [Texto] La fuente personalizada no funciona en el reproductor
* [Text] advertencia de fuentes no válidas al abrir un paquete con fuentes en los recursos
* La entrada de texto [Text] no funciona en el modo de vista previa
* [Text] Se puede exponer el parámetro de fuente
* [Text] se bloquea al crear una función en el parámetro text
* [Text] Se bloquea al exponer el tamaño de fuente
* [Vista 2D] El porcentaje de zoom no se muestra correctamente al utilizar la tecla &quot;F&quot;
* [Vista 2D] La imagen cambia cuando se cambia el tamaño
* [Vista 2D] Discontinuidad al mostrar el mosaico
* [Vista 2D] El guizmo de transformación no se puede ver ni editar en el modo de vista previa
* [Vista 3D] Tamaño físico no tenido en cuenta por el sombreador de Parralax de PBR
* [Vista 3D] La configuración de la velocidad de actualización no se restaura correctamente de una sesión a otra
* [Graph] multiángulo\_to\_normal evitar publicación
* [Graph] El tamaño de salida del filtro pow está bloqueado
* [Graph]No se pueden crear instancias de archivos .sbsar
* [Curva] IU recortada
* [Curva] La visualización de números se recorta ligeramente
* [Curva] El widget desaparece cuando se cambia el tamaño de la barra de herramientas
* [Contenido] El nodo Resplandor está roto
* [Contenido] Mosaico en Sampler: Los motivos son invisibles si el mosaico está desactivado
* [Contenido] MG Mask Builder: parámetros de contraste de curvatura invertida
* Color Equalizer [Content]: parámetros de grupo custom\_color\_variation no conectados
* [Content] Parche de clonación: El área de parche no está visible cuando se coloca en las esquinas
* [Explorer] Al volver a cargar un paquete mientras está abierta su dependencia, se rompe el paquete de dependencias
* [Explorer] No se puede importar un recurso psd de 32 bits
* Error de cocción de [Publish] (herencia ERR:No (absoluta))
* [Degradado] El degradado debe mostrarse como Lineal cuando sRGB no está marcado
* [Transformation2D] Desplazamiento de la impresión al mover un guizmo con restricción de eje
* [Parámetros] El foco del ratón se roba mediante el menú desplegable
* [Motor] Sin segmentación no afecta al nodo de distancia en el motor de GPU
* [Export] Bloqueo al exportar salidas como TGA
* [MDL] el ajuste preestablecido de exportación no funciona

### 6.0.0

*(Lanzado: 14 de febrero de 2017)*

<b>Agregado:</b>

* [Motor] Nuevo nodo de curva
* [Engine] Nuevo nodo de texto
* [Motor] Composición de profundidad de bits 16f/32f
* [Engine] creación de instancias para mapas de efectos de GPU
* [Motor] Agregar función log2
* [Panaderos] Horneado de mapas en 8k
* [Panaderos] Hornear por material / &quot;Conjunto de texturas&quot;
* [Bakers] Mostrar el mensaje de carga cuando la salida de mapa de bits se está codificando/escribiendo en el disco
* [Panaderos] Añadir una opción de cancelación durante el horneado
* [Nodo de degradado] añadir ajustes globales para varias teclas seleccionadas
* [Nodo de degradado] Opciones de Simplificar selector de degradado
* [Graph] Añada una opción para modificar el tamaño del padre por defecto
* [Graph] Mostrar profundidad de píxeles de imagen bajo el nodo
* [Preferencias] Preferencias globales de DirectX/OpenGL
* [Preferencias] Uso de pestañas en Preferencias/IU del proyecto
* [Preferencias] elimina el parámetro MaxTextureSize que se encuentra en las preferencias de &quot;3DView&quot;
* [Preferencias] Mostrar ayuda breve sobre el autoguardado
* [Preferencias] Opciones de formato de imagen de exposición
* [Preferencias] Añada una opción para ocultar el mapa de entorno en la vista 3D de forma predeterminada
* [Preferencias] Añadir una opción para la opción alfa predeterminada del filtro de mapa normal
* [Vista 2D] Añada la posibilidad de alejarse de los límites de textura
* [Vista 2D] Interpretar la proporción X/Y del tamaño físico
* [Vista 3D] Mejorar la administración de texturas
* [Vista 3D] Desactive After Effects de forma predeterminada (para evitar el bloqueo en la GPU de gama baja)
* [Gráfico MDL] Administrar el indicador oculto en el parámetro IRay
* [MDL Graph] Se permite establecer el constructor &#39;material()&#39; como nodo raíz
* [Gráfico MDL] Crear vista previa del nodo de instancia de gráfico SBS
* [Contenido] Añadir nuevos filtros de procesamiento de digitalización
* [Contenido] Añadir nuevos filtros de ajuste (Abrazadera, Pow, Visor de rango HDR)
* [Contenido] Añadir Blue Noise (Aproximación rápida)
* [Contenido] Añadir nuevos efectos de forma (Resplandor, Sombra paralela, Trazo)
* [Publish] Añada una acción &quot;Exportar como anterior&quot; para volver a publicar el último paquete seleccionado
* [Publish] Mejora de la generación de SBSAR al utilizar mapas de bits de alta resolución
* [Publish] Advertencia al usuario sobre la configuración de gráfico no &quot;relativo a la matriz x1&quot; al publicar o cargar en Compartir
* [Propiedades] Añadir el atributo &quot;Tamaño físico&quot; en los gráficos SBS
* [Parámetros] Quitar acciones de función en rutas de recursos PKG
* [Parámetros] Quitar el elemento emergente &quot;Valores de previsualización cambiados&quot;

<b>Corregido:</b>

* [Graph] El uso de memoria aumenta con frecuencia cada vez que se abre el menú contextual
* [Graph] [En SSE2] Los nodos del polígono no muestran formas cuando el parámetro &quot;Scale&quot; está en negativo
* [Graph] Bloqueo al cambiar de &quot;Integer&quot; a &quot;Float&quot; en un parámetro expuesto
* [Graph] Si se mueven nodos mientras se selecciona un punto de división, se volverán a calcular los nodos
* [Graph] Los puntos de división no admiten &quot;Deshacer&quot;
* [Graph] Se muestra información sobre herramientas vacía cuando la descripción del gráfico contiene caracteres no imprimibles
* [MDL Graph] Bloqueo cuando se elimina el nodo actual que se muestra en la vista de propiedades
* [MDL Graph] El gráfico MDL que utiliza la función constructora material() como raíz no se procesan correctamente en la vista 3D
* [MDL] No se puede exportar el módulo MDL cuando se utiliza un operador condicional con un parámetro booleano uniforme de exposición
* [MDL] Bloqueo al cargar una plantilla de gráficos MDL dos veces
* [Archivo MDL] Los materiales que utilizan una textura no se gestionan correctamente
* [Vista 3D] El material IRay no cambia cuando cambia el nodo raíz de MDLGraph
* [Vista 3D] bloqueo aleatorio al cerrar la vista 3D mientras se está cargando una malla
* [Vista 3D] Los yebis no se reactivan después de guardar el procesamiento
* [Vista 3D] Se genera un archivo de PSD no válido al guardar el resultado de procesamiento de una escena de iray
* La luz de punto 1 de [Vista 3D] no se ilumina
* [UI] El área de detección de las casillas de verificación es demasiado ancha en los parámetros &quot;Panaderos de malla&quot;
* [UI] Problema estético en los parámetros &quot;Panaderos de malla&quot;
* [Mac] Al abrir SD haciendo doble clic en un sbs, no se envía la salida a la vista 3d
* [Mac] [Iray] El procesamiento del clúster de Fotoreal no funciona en MacOS
* [Motor] Atan2(0, 0) produce un bloqueo del motor
* [Motor] Problema de sincronización grave
* [Bakers] No se puede deshabilitar la normalización automática para el Height baker
* [Parámetros] al convertir la escala de grises a rgba, alfa debe ser 255
* [Funciones] Es posible establecer una función como nodo de salida aunque no sea compatible
* [Export] Dependencias no válidas después de exportar un paquete con recursos de PSD
* [Console] Al borrar la consola se produce un bloqueo de SD

## Versión 5

### 5.6.2

*(Lanzado: 08 de febrero de 2017)*

**Corregido:**

* [Preferencias] No se tiene en cuenta el sombreado predeterminado
* [Vista 3D] Bloqueo si se cambia el sombreado predeterminado en tiempo de ejecución
* [Engine] obtener $size problema

### 5.6.1

*(Lanzado: 17 de enero de 2017)*

**Agregado:**

* [Vista 3D] Defina el tamaño de las formas simples en 100 cm
* [Contenido] Añade &quot;Filtrado de entrada de imagen&quot; a &quot;Splatter Circular&quot; y &quot;Splatter&quot;
* [Panaderos] &quot;Curvatura de la malla&quot; Añadir advertencias de consola bajo el canal &quot;Comprobación de corrección de malla&quot;

**Corregido:**

* [Vista 3D] Desaparece cuando está desacoplado
* [Graph] Los parámetros &quot;Ruido&quot; y &quot;Precisión&quot; del mapa de degradado ya no funcionan
* [Vista 3D] ALT+R no funciona después de guardar el procesamiento
* [Bakers] &quot;Curvature From Mesh&quot; se bloquea con algunas mallas de ZBrush

### 5.6.0

*(Lanzado: 15 de diciembre de 2016)*

**Agregado:**

* [Contenido] Se ha añadido el nuevo filtro &quot;AO (Oclusión ambiental base de Horizonte)&quot;
* [Contenido] Se ha añadido el nuevo filtro &quot;Fusión de Height&quot;
* [Contenido] Se ha añadido el nuevo filtro &quot;Height a normal (unidades de mundo)&quot;.
* [Contenido] Se ha añadido el nuevo filtro &quot;Fusión de Height de material&quot;
* [Contenido] Se ha añadido el nuevo filtro &quot;Cubierta del Snow&quot;
* [Contenido] Se ha añadido el nuevo filtro &quot;Nivel de agua&quot;
* [Contenido] Se ha añadido el nuevo filtro &quot;Coincidencia de color&quot;
* [Contenido] Se ha añadido el nuevo filtro &quot;Exploración por histograma (no uniforme)&quot;
* [Preferencias] [IU] Añada una opción en Preferencias para desactivar la detección de PPP altos
* [Vista 3d] Añadir una opción para restablecer la posición de la cámara
* [Israel] Integrar el SDK de IRay 2016.2 para la compatibilidad con la arquitectura Pascal
* [Graph] Añada la opción &quot;Copiar información de nodo en el portapapeles&quot; en el menú contextual

**Corregido:**

* [MDL] La raíz de material de archivo no se elimina en el ajuste preestablecido exportado
* [Gráfico MDL] Los vínculos de recursos no disponibles no se eliminan en el gráfico MDL
* [Biblioteca] Al crear un nuevo filtro se crean dos condiciones base
* [Biblioteca] Carpetas ya no filtra el contenido de la biblioteca
* [Panaderos] La barra de progreso va y viene
* [Panaderos] El recurso de jaula inexistente impide hornear
* [Contenido] Varios errores en &quot;Functions.sbs&quot;
* [Exportar] El formato de archivo siempre se restablece en png
* [UI] Problema de escala de IU de Substance Designer
* [Graph] Bloqueo al mover el paquete original de una instancia de gráfico
* [Preferencias] si no se encuentra el sombreador/plugin tangente/.. predeterminado, utilice los definidos en el proyecto predeterminado
* [Parámetros] Los reguladores tienen demasiada precisión en Mac
* [Explorador] Mover malla 3D de una carpeta a otra daña este recurso
* Cerrar la ventana no mata el proceso SD
* El cuadro de diálogo Abrir archivo no muestra los archivos con el filtro &quot;Todos los formatos&quot;

### 5.5.3

*(Lanzado: 28 de octubre de 2016)*

**Corregido:**

* [Shelf] Bloqueo al crear la carpeta
* [Panaderos] World\_Space\_Direction ya no funciona

### 5.5.2

*(Lanzado: 18 de octubre de 2016)*

**Agregado:**

* [Gráfico MDL] Propagar valores por defecto del gráfico SBS a la instancia del nodo de gráfico SBS en el gráfico MDL
* [MDL] Compatibilidad con arrastrar y soltar del gráfico SBSAR
* [IRay] actualización a SDK 2016.1.6 (261500.16187)
* [sbsrender] Optimice la administración de memoria de sbsrender para que coincida con el rendimiento del reproductor
* [Vista 3D] Permita que el tamaño del widget sea menor que el de la barra de menús superior
* [Console] Permite copiar algunas líneas en el portapapeles

**Corregido:**

* [Player] Bloqueo al reproducir un paquete directamente en Designer mediante el &quot;botón de reproducción&quot;
* [Startup] el archivo nvcuvid.dll no se muestra en la pantalla emergente
* [Environment init] al hacer doble clic en un archivo .sbs no se carga en SD
* [Export] Bloqueo de la exportación con dependencias
* [MDL] Problema de sincronización entre un gráfico y su instancia
* [MDL] Los nodos de instancia sbsar generan textura\_retorno en lugar de valores
* [Vista 3D de IRay] En el procesador de Iray, el &quot;canal de Height&quot; no se actualiza correctamente al cambiar el mapa de height
* [Vista 3D de IRay desacoplada] &quot;Cámara>Guardar procesamiento&quot; no funciona después de ocultar la aplicación en la barra de tareas de Windows
* [Mac IRay] La GPU NVIDIA ya no se detecta con IRay
* [Panaderos] Textura transferida del bloqueo de malla al hornear texturas que no son POT
* [Bloqueo] Bloqueo al exportar un gráfico en el Substance share
* [Graph] Bloqueo al seleccionar una instancia fantasma
* [Vista 3D] No se puede aplicar el efecto de cámara Dolly (Aumentar o Reducir) a la cámara ortográfica en modo de lluvia
* [UI] El selector de color no gestiona la visualización de PPP altos
* [Graph] (MacOS 10.11.06) Cálculo infinito con nodo de mezcla de varios materiales
* [Graph] Copiar/Pegar el contenido del gráfico ==> pegar en el contenido y también una referencia a ese gráfico
* [Graph] Varias fusiones de material en escena, autoselecciona las salidas incorrectas
* [Graph] El Edge Wear de metal bloquea el PC
* [Biblioteca] Los archivos &quot;SBSAR&quot; muestran el logotipo &quot;S&quot; en lugar de las miniaturas
* [Biblioteca] Las carpetas dentro de .sbsar se muestran en la biblioteca

### 5.5.1

*(Lanzado: 08 de septiembre de 2016)*

**Agregado:**

* [Iray] Añadir el modo &quot;IQ&quot; para el renderizado en la nube
* [Iray] Actualización al SDK de Iray 2016.1.5

**Corregido:**

* [MDL] La vista en 3D no funciona correctamente la primera vez
* El degradado [MDL]\_interpolation\_linear no se exporta con la ruta completa
* [MDL] La esquina inferior derecha del marco recién creado está exactamente alineada con el nodo relacionado
* [MDL] La miniatura del material raíz no se actualiza en algunos casos
* [MDL] Bloqueo al eliminar todos los nodos y rehacer
* [MDL] Rendimiento lento en la visualización de gráficos en comparación con el Gráfico de Substance
* [MDL] No se puede exportar el módulo MDL debido al parámetro IOR
* [MDL] Los parámetros mostrados no corresponden al nodo seleccionado
* [Vista 3D] El material MDL que procede de un gráfico MDL no se restablece cuando se elimina el nodo raíz
* [Vista 3D] El encuadre de cámara predeterminado se pierde después de cargar la malla de fbx
* [Vista 3D] La asignación de texturas no se mantiene al cambiar a Iray
* [Iray] Mensaje de advertencia de IRay al mover la cámara
* [Iray] Bloqueo al cambiar a Irak
* [Iray] La contraseña de VCA no se guarda
* [Graph] Bloqueo al eliminar nodos
* [Graph] Pulsar CTRL para copiar vínculo no funciona en el modo Material
* [Graph] Bloqueo al eliminar el nodo de salida en un material de nodo de instancia
* [Panaderos][Vista 3D] No se puede cargar la malla de alta definición
* [Mac][Vista 3D] Bloqueo al intentar restaurar ventanas desconectadas en un monitor secundario
* [Parámetros] No se puede editar un valor en spinboxedit sin quitar el sufijo
* [UI] Usar &quot;Cancelar&quot; al cerrar el cuadro de mensaje SD debe detener
* Bloqueo al abrir dos vistas 3D
* Bloqueo en Alg::Scripting::Engine al utilizar mucha condición VisibleIf
* Los archivos se eliminan mediante autoguardar si existe un archivo .algautosave

### 5.5.0

*(Lanzado: 25 de agosto de 2016)*

<b>Agregado:</b>

* Substance Designer ya está disponible en Linux
* Nuevo editor MDL (Material Definition Language)
* [Panaderos] Nueva curvatura de panadero de malla
* [Biblioteca] Usar iconos de SVG en lugar de archivos de mapa de bits
* [Biblioteca] Añada una opción para filtrar el resultado para MDL, Composición, Función y Fxmap
* [Graph] Extender el &quot;Mostrar nodo recién creado&quot; para copiar/pegar/duplicar nodos
* [Nuevo documento] Crear un widget de selección de plantilla al crear un nuevo gráfico MDL
* [Vista 3D] [Israel] Muestra los nodos Modo de procesamiento + VCA junto a las iteraciones/tiempo
* [Vista 3D] Mejore el rendimiento del menú &quot;material&quot; al abrir
* [3DView][Bakers] Actualización a FBX SDK 2017
* [Vista 3D] Permite mostrar u ocultar información de procesamiento (resolución, iteraciones, etc.) en el menú de visualización de Vista 3D
* [Iray] Volver a mostrar los parámetros de teselación en la edición de escenas
* [Project] Agregar alias generado automáticamente para el directorio de archivos del proyecto
* [Proyecto] Especifique la textura de entorno predeterminada en la configuración del proyecto
* [Contenido] Se ha añadido un nuevo estudio HDRi
* [Contenido] Añadir nodo de transformación no cuadrado a la biblioteca
* Iniciar SD con un archivo .sbscfg específico

<b>Corregido:</b>

* [Graph] Las entradas no se conectan automáticamente a las salidas con el mismo uso.
* [Graph] Las entradas de nodo insertadas no están conectadas correctamente
* [Graph] Al anular la selección, también se debe seleccionar un nodo bajo el ratón
* [Graph] La inserción de nodos no se conecta a todos los vínculos
* [Panaderos] Difusión incorrecta en panadero de curvatura
* [Panaderos] &quot;Textura transferida de la malla&quot; se bloquea si la malla de alta definición no tiene UV
* [UI] El icono de función en los parámetros no se modifica cuando se define una función
* [UI] Se cortan las sugerencias de parámetros
* [Vista 3D] se muestran más de 1000 luces en la escena
* [Vista 3D] El sombreador Lambert de GLSL no administra correctamente la textura srgb
* [Vista 3D] Faltan parámetros de segmentación al conectar sustancias en Iray
* [Iray] La exportación preestablecida de mdl no funciona cuando hay espacios en el nombre
* [Israel] Los parámetros de la subdivisión no se tienen en cuenta
* [Parámetros] Ya no se muestra el identificador del parámetro
* [Parámetros] Bloqueo al cambiar la dirección URL del recurso desde &quot;De recurso...&quot; acción
* [Parámetros] Conversión incorrecta de &amp; carácter
* [Explorer] al hacer doble clic en un gráfico &#39;grande&#39; a menudo no se abre en la vista del gráfico
* [Explorer] Los SVG incrustados aparecen como ausentes en el Explorador
* [Explorer] Bloqueo al cambiar el nombre de un elemento con el carácter &quot;&amp;&quot;
* [Contenido] El mosaico del degradado 1 es incorrecto al utilizar la rotación de 90/180°
* [Perforce] La integración no parece funcionar si el espacio de trabajo se encuentra en la raíz del disco duro
* [Data] El UID generado para los nodos no es único
* [Preferencias] Al añadir un alias dirigido a la raíz del disco duro se confunden las rutas en sbsprj
* [PÉRDIDA DE MEMORIA] Algunos diálogos QD no se destruyen cuando se cierran

### 5.4.0

*(Lanzado: 29 de abril de 2016)*

**Agregado:**

* Agregar un vínculo a la Tienda de Substance
* [UI] Compatibilidad con resoluciones de alta resolución de PPP
* [UI] Permitir reordenar pestañas
* [Vista 3D] Permitir la exportación de renderizado a ArtStation
* [Vista 3D] Agregue el sombreado predeterminado a la lista de sombreados
* [Graph] Mostrar el nombre del recurso en la parte superior del nodo de mapa de bits
* [Graph] Mejorar el orden de listado del menú de búsqueda de la barra espaciadora
* [Panaderos] Nuevo panadero &quot;Posición desde malla&quot;
* [Panaderos] Nuevo ajuste de &quot;mapa normal&quot; para el panadero de transferencia de textura
* [Panaderos] Nuevo ajuste &quot;Tangent&quot; y &quot;Binormal&quot; para el panadero World Space Normal
* [Scripting] Permite ejecutar scripts durante las acciones Guardar, Exportar y Publish
* [Dependencias] Añadir una opción Contraer/Expandir según la selección
* Se ha añadido una advertencia sobre los conflictos de extensión de shell

**Corregido:**

* Bloqueo al salir
* El proceso del Substance Designer puede seguir ejecutándose después de salir
* [Iray] Las salidas no se envían a materiales mdl al cambiar de procesador
* [Contenido] Muestra de mosaico: rotación de motivo aleatorio no debe girar la forma

### 5.3.5

*(Lanzado: 6 de abril de 2016)*

**Corregido:**

* [Vista 2D] Transformación La opción de menú contextual 2D está disponible en cualquier nodo
* [Vista 2D] transformación Gizmo 2D aún editable después de eliminar el nodo de transformación
* [Vista 3D] La ruta del entorno no debe mostrarse en Parámetros de entorno
* [Vista 3D] Los parámetros de efectos posteriores no se guardan en recursos 3D
* [Vista 3D] El menú de la barra de herramientas no se comporta como un menú normal
* [Preferencias] No se puede establecer el &quot;límite de caché del motor&quot; superior a 4095
* [Preferencias] No se tiene en cuenta la configuración de un sombreado predeterminado
* [Iray] Los parámetros de color no se recuperan correctamente
* [Iray] Se restablecen los colores del material MDL
* [Iray] Los mapas de bits no se exportan junto con el ajuste preestablecido MDL
* [IRay/Mac] Cambiar el tamaño de la vista 3D hace que la estación de trabajo Mac se bloquee
* [Graph] El documento del PSD no se exporta
* [Graph] Tamaño de nodo mostrado incorrecto
* [Gráfica de funciones] La imagen de entrada de nodo de muestra no se puede editar si solo hay una imagen conectada
* [Motor] Bloqueo al calcular el gráfico de Fxmap
* [Engine OGL] Error en la generación de procesadores de píxeles
* [Degradado] El selector de degradado no funciona en Mac
* [PSD] La imagen de 8 bits no se convierte correctamente a 16 bits
* [Parámetros] El widget de histograma de nivel no tiene el mismo height en color y escala de grises
* [Console] Al hacer clic en una celda, la vista se desplaza horizontalmente
* [Explorador] Los recursos 3d reubicados no se abren correctamente en la vista 3d

### 5.3.4

*(Lanzado: 16 de enero de 2016)*

**Corregido:**

* [Iray] tangente/binormal no se tienen correctamente en cuenta
* [Explorer] El paquete se marca como guardado justo después de abrirse
* [Vista 3D] El reflejo de difusión de IBL es demasiado fuerte
* [Vista 3D] Bloqueo al arrastrar y colocar una imagen de 8 bits del explorador a la vista 3D
* La aplicación se bloquea desde el 1 de enero de 2016

### 5.3.3

*(Lanzado: 10 de noviembre de 2015)*

**Agregado:**

* [Contenido] Añada &quot;White Noise Fast&quot; (basado en el procesador de píxeles)
* [Contenido] Añada &quot;Desplazamiento horizontal/vertical global&quot; en Muestras de mosaico

**Corregido:**

* Bloqueo al crear un nuevo Substance en algunas situaciones
* [Bakers] Bloqueo cuando los mapas con bake están actualizando el gráfico
* [Panaderos] OBJ proveniente de zbrush debe usar el nombre de archivo para hacer coincidir por nombre
* [Parámetros] Bloqueo al realizar Deshacer/Rehacer/Deshacer en el gráfico de funciones
* [Gráfico] Los puntos de división no se pegan en la ubicación correcta

### 5.3.2

*(Lanzado: 30 de octubre de 2015)*

**Agregado:**

* [Contenido] Agregar control de filtrado para la entrada de patrones en Tile Generator

**Corregido:**

* [Vista 3D] El punto de enfoque no se inicializó correctamente
* [Vista 3D] Plano de clip lejano incorrecto al cambiar varias veces de recursos de malla 3D
* [Vista 3D] Breve artefacto de representación al cargar una malla
* [Vista 3D] El mapa de entorno aparece en negro cuando no se encuentra el archivo -> fallback to default envmap
* [Vista 3D] Bloqueo después de utilizar una imagen personalizada de latitud y longitud
* [Vista 3D] Bloqueo al cargar un archivo obj específico
* [Vista 3D] La carga automática de malla no funciona correctamente
* [Iray] No se puede asignar textura en un mdl externo
* [Iray] No se pueden asignar texturas al canal de anisotropía tras el restablecimiento del material
* [UI] Aparece el menú emergente de Windows cuando se suelta el botón derecho del ratón después de moverse en 3DView
* [Vista 2D] La herramienta Información no devuelve el valor de color del píxel bajo el cursor
* [Bakers] Las imágenes en escala de grises se guardan como indexadas con formato de etiqueta
* [Graph] Las salidas de la vista 3d deben restablecer los canales antes de enviar las salidas a la vista 3d
* [Parámetros] El nombre de entrada del parámetro está vacío cuando se expone desde &quot;Exponer parámetros de nodo&quot;
* [Performances] Establezca la devolución de llamada onSubstanceCallbackProfileEvent en el motor SÓLO si los intervalos están habilitados

### 5.3.1

*(Lanzado: 21 de octubre de 2015)*

**Agregado:**

* [Vista 3D] Mostrar el nombre de la malla en la escena/editar en lugar de &quot;Entidad&quot;
* [Vista 3D] Restablecer el color predeterminado cuando se abre una nueva vista 3D
* [Vista 3D] Enfoque de la cámara al cambiar de escena a simple
* [Vista 3D] Visualización de la resolución de la ventana gráfica de procesamiento cuando se utiliza una resolución personalizada
* [Iray] Ajuste de la presentación de parámetros de subdivisión
* [Iray] Enviar información de registro de IRay a registro SD
* [Bakers] Lea los archivos OBJ correctamente para que las coincidencias por nombre sean compatibles

**Corregido:**

* [Vista 3D] Visualización incorrecta de mallas con una escala diferente de 1.0
* [Vista 3D] El cálculo automático del plano cerca del clip no funciona bien con objetos grandes
* [Vista 3D] El modo de Malla metálica muestra cables demasiado gruesos
* [Vista 3D] La ventana Guardar procesamiento no se muestra si los efectos posteriores están desactivados
* [Vista 3D] Bloqueo al cambiar la geometría
* [Vista 3D] &quot;QOpenGLWidget: No se puede hacer que el widget no inicializado sea el mensaje actual en el registro
* [Vista 3D] La iluminación no se calcula si se cambia el mapa del entorno mientras Iray está en ejecución
* [Vista 3D] Bloqueo al ver malla 3D
* [Vista 3D] Muy malas actuaciones de OpenGL después de haber utilizado Iray
* [Vista 3D] Los planos de clip no se calculan correctamente
* [Vista 3D] Al cambiar el mapa de entorno, no se actualiza la vista 3D
* [Vista 3D] Las texturas no se actualizan al cambiar el gráfico
* [Vista 3D] Las muestras ocultas GLSLFX se siguen mostrando en el menú de selección
* [Vista 3D] El material no se restaura correctamente al abrir el recurso de malla
* [Vista 3D] Pérdida de memoria RAM/VRAM al abrir varias mallas y asignarles varios gráficos
* [Vista 3D] El enfoque no tiene en cuenta la distancia focal
* [Iray] nvcuvid.dll no se encuentra (desinstala la versión anterior para deshacerse del mensaje)
* [Iray] Cuadro de diálogo de exportación de ajustes preestablecidos &#39;...&#39; botón no mostrar la ventana de diálogo
* [Iray] La refracción/dispersión no funciona correctamente en el specular físico\_diffuse\
* [Iray] No se encuentra el molde predeterminado (color magenta)
* [Iray] No conecte texturas predeterminadas al material de moldeo para activar el modo de valor en el material de edición
* [Iray] La desescala no se activa cuando se actualiza una textura
* [Bakers] Worldspace normal baker muestra una imagen en negro
* [Bakers] Bloqueo al convertir un mapa normal en una vista 3D no acoplada
* [Panaderos] Si se utiliza el método &quot;incrustado&quot; mientras se establece una ruta no válida para el &quot;vínculo&quot;, no se puede guardar el recurso
* [Bakers] Al usar el método &quot;Embedded&quot; y cambiar el formato de archivo no se cambia la extensión en el disco
* [Panaderos] Los nombres aleatorios de los recursos incrustados tienen un nombre XXX..
* [Bakers] Varios objetos en .obj no se importan correctamente
* [Content] Mezcla de materiales: la salida de basecolor no se oculta cuando el canal está desactivado
* [Contenido] Blanco\_noise y los sonidos derivados no se procesan correctamente a 8k
* [Gráfico] Prestaciones lentas en el gráfico
* [Graph] Bloqueo al arrastrar y soltar elemento de función de biblioteca a gráfico de función
* [Graph] &quot;Ver salidas en vista 3d&quot; solo debe enviar la salida visible del nodo en vista 3d
* [Preferencias] El usuario predeterminado\_project tiene vacío el &quot;Sufijo de nombre&quot; para la función de coincidencia por nombre
* [Motor] La conversión de color -> escala de grises produce pérdidas de precisión
* [Console] La consola/el registro están contaminados por muchos mensajes
* [Compartir] Bloqueo al intentar compartir un paquete
* [UI] La información sobre herramientas se bloquea en la parte superior del menú Archivos recientes
* Bloqueo al salir

### 5.3.0

*(Lanzado: 01 de octubre de 2015)*

<b>Agregado:</b>

* [Vista 3D] Añadir procesador de NVIDIA Iray
* [Vista 3D] Rotar entorno mediante CTRL+Mayús+RMB
* [Vista 3D] Procese la ventana gráfica 3D con una resolución personalizada (Ogl/Iray)
* [Vista 3D] Hacer que la carga de la escena sea asincrónica
* [Vista 3D] Visualización de la escena global en el Explorador de escenas
* [Vista 3D] Desactivar la cuadrícula de forma predeterminada
* [Vista 3D] Adición de atenuación de distancia cuadrada inversa para luces puntuales
* [Vista 3D] Visualización del parámetro de color en RGB en lugar de RGBA
* [Vista 3D] Luces independientes/Cámara/Configuración del entorno
* [Compartir] Mejoras en la ventana de carga de Substances shares

<b>Corregido:</b>

* [Vista 3D] Error en la normalización de sombreadores PBR
* [Vista 3D] Bloqueo al hacer clic con el botón derecho en la raíz en el explorador de escenas
* [Vista 3D] Sombreadores PBR : conservación de energía difusa frente a especular y focos
* [Vista 3D] Hacer que &quot;Material/Reset&quot; también restablezca los canales al color predeterminado
* [Bakers] Posición con normalización de la esfera no centrada
* [UI] El estado flotante de Windows no se guarda al cerrar la aplicación
* [Cooker] No se puede publicar cuando el archivo SBS se encuentra en una ruta que contiene un carácter especial
* [Publicación] Si pulsa &quot;Intro&quot; en el campo de nombre después de publicar, se cancelará el cuadro de diálogo
* [Compartir] La exportación de subconjuntos no mantiene el alias sbs://

### 5.2.5

*(Lanzado: 15 de septiembre de 2015)*

**Agregado:**

* [Compartir] Publish envía un paquete al Substance share
* [UI] Vínculo Agregar Substance share en el menú Ayuda

**Corregido:**

* [Cocina] &quot;Tamaño fuera de los límites&quot; es un error en lugar de una advertencia
* [Cooker] &quot;No se encuentra la salida del subgráfico&quot; es un error en lugar de una advertencia
* [Vista 3D] La difusión/especificación PBR prefiere el color base en lugar de la difusión
* [Vista 3D] El mosaico no funciona correctamente con sombreadores de teselación
* [Engine] Bloqueo al crear instancias de un archivo sbsar específico
* [Motor] Las funciones Sizelog2 / pow2 no funcionan correctamente
* [Motor] El &quot;ajuste&quot; del tamaño de salida no funciona
* El Nivel de mapa MIP [del motor] no se fija para los valores negativos
* [Contenido] No se puede publicar un gráfico que contenga un filtro triplanar

### 5.2.1

*(Lanzado: 27 de agosto de 2015)*

**Corregido:**

* [Graph] Bloqueo al calcular sbsar específico
* [Graph] Bloqueo al crear instancias de fxmap con varias entradas de imagen
* [Motor] Bloqueo con sizelog2
* [Motor] El valor predeterminado del parámetro expuesto se omite con el motor DX10
* [Biblioteca] El cálculo de miniaturas se interrumpe si el proyecto contiene alias no válidos
* [Cocina] Establezca &quot;unknown\_parameter&quot; y &quot;duplicado de parámetro&quot; como advertencia en lugar de errores
* [Preferencias] El límite de caché del motor está bloqueado en 4095 Mb
* La etiqueta del parámetro de entrada [Function] se interpreta como identificador

### 5.2.0

*(Lanzado: 18 de agosto de 2015)*

**Agregado:**

* [Biblioteca] Añada una opción en las preferencias para ocultar o mostrar capas de PSD
* [Parámetros] Permitir que los datos de usuario estén en varias líneas
* [Graph] Añada una opción de preferencia para procesar comentarios a tamaño constante
* [Graph] Añada una opción de preferencia para desactivar la visualización del nuevo nodo en la vista 2D
* [Prestaciones] Mejora del rendimiento del procesador de píxeles en el motor DX10
* [Vista 3D] Agregar teselación a sombreadores PBR
* [Vista 3D] Añadir opacidad simple a los sombreadores PBR (sin ordenación de caras)
* [Contenido] Añada destinos de Vray/Corona/Redshift/Arnold al filtro de convertidor PBR (para convertir mapas para estos procesadores)
* [Contenido] Añada la técnica &quot;Orientado al detalle&quot; al filtro Combinación normal

**Corregido:**

* Bloqueo al abrir subprogramas con dependencia vacía
* El vínculo a las capas del PSD se rompe tras la recarga del paquete
* [Funciones] Las funciones anidadas rompen la seguridad de tipos
* [Funciones] No se muestran etiquetas, grupos ni descripciones
* [Funciones] Bloqueo al copiar o pegar desde una función eliminada
* [Gráfico] Vínculo de material roto con gráficos de barras
* [Graph] Al crear varios nodos de mapa de bits a partir de recursos, el nodo se apila entre sí
* [Graph] El elemento de comentario no se crea en la posición correcta cuando es hijo de un nodo
* [Graph] Selección de región de bloque de comentarios largos
* [Bakers] Tangent Space Normal map se vuelve negro en Mac
* [Parámetros] Visible Si no funciona cuando el nombre de entrada contiene &quot;-&quot;
* [Parámetros] El valor de paso en Parámetros de entrada se omite si es inferior a 0,01
* [Biblioteca] La etiqueta &quot;Visible en biblioteca&quot; no se tiene en cuenta para sbsar

### 5.1.1

*(Lanzado: 04 de junio de 2015)*

**Agregado:**

* [Graph] Reducir el espacio entre dos nodos al utilizar la conexión automática
* [Graph] Desactivar la conexión automática al utilizar arrastrar y soltar en el gráfico
* [Graph] Hacer que el marco se ajuste a la cuadrícula
* [Graph] Desactivar inserción de nodo sobre/sobre vínculo seleccionado para vínculo de material
* [Preferencias] Defina el valor máximo para Tamaño máximo de textura en 8192
* [Contenido] Añadir opciones de simetría al nodo &quot;Transformación segura&quot;

**Corregido:**

* [Graph] El nuevo nodo no está ajustado en la cuadrícula
* [Graph] El intercambio de enlaces puede generar bucles/bloqueos
* [Graph] Problemas de visualización al desactivar el tamaño de nodo y la temporización
* [Bakers] Bloqueo al realizar el procesamiento en un recurso que usa el mismo nombre que la escena
* [Bakers] El nombre de recurso predeterminado no se toma del archivo de proyecto correcto
* [Motor] Problema de función Pow2/log
* [Motor] Error en la evaluación de funciones
* [Fxmaps] Bloqueo al restablecer el parámetro al valor predeterminado
* [FxMaps] Evaluación incorrecta de la función
* [Preferencias] Al hacer clic en la pestaña del proyecto, se bloquea SD
* [Vista 3D] El uso personalizado se convierte en minúsculas
* [Parámetros] No se pueden reordenar elementos en listas desplegables
* [Explorer] Bloqueo al mover un gráfico de funciones en el explorador

### 5.1.0

*(Lanzado: 28 de mayo de 2015)*

**Agregado:**

* [Graph] Buscar/Mostrar contenido desde la biblioteca a través del menú de la barra espaciadora
* [Graph] Mostrar/abrir nodo recién creado
* [Graph] redirección de vínculos (alt+mayús)
* [Graph] seleccionar nodos primarios
* [Graph] Intercambiar 2 vínculos (X)
* [Graph] Inserte el nodo sobre un vínculo arrastrando y soltando
* [Graph] Crear un gráfico a partir de una selección de nodo
* [Graph] Eliminar vínculo al utilizar Alt + LMB en un pin de nodo
* [Graph] No conectar un nuevo nodo al anterior mediante Mayús
* [Graph] Agregar una barra de herramientas para filtros base
* [Graph] Mejora la cuadrícula (ajuste y resolución)
* [Graph] Mover el comentario/marco/pin al menú contextual
* [Graph] Crear nodo sobre un vínculo seleccionado
* [Graph] Añadir iconos a elementos de función
* [Graph] Cambiar los colores de las chinchetas en el gráfico de funciones
* [Graph] Utilice Mayús para desactivar la conexión automática del nodo
* [Graph] Hacer que el enlace seleccionado se dibuje sobre los otros enlaces
* [Graph] Añadir iconos a nodos de Fxmap
* [Graph] Agregar un modificador para dibujar vínculos curvos o rectangulares
* [Función] Haga que los distintos tipos de vectores sean más distintos en el gráfico de funciones (colores de pin/vínculo)
* [Funciones] añadir iconos en nodos y mostrar valores para constante / conjunto / obtener
* [Funciones] Añadir colores al título del nodo
* [Función] Mejorar el rendimiento para la evaluación de funciones (utilizar código generado por SSE)
* [Función] Mostrar advertencia si el nodo Establecer/Obtener está vacío
* [Bakers][Graph] Tramado de mapa de bits al convertir a 8 bpc
* [Bakers] Promedio de normales de vértices en el archivo OBJ si la malla no contiene ninguna
* [Bakers] Coincidir por nombre: usar sufijo como separador
* [Parámetros] Opción Añadir para cambiar entre RGB y HSV en el widget de color
* [Parámetros] Botón Añadir cuentagotas en el widget de color
* [Biblioteca] Agregar una categoría para contenido base (nodos de composición, fxmap, función...)
* [Vista 2D] Información: agregar pantalla en el rango [0, 1] y HSV
* [Vista 3D] Añadir compatibilidad con mipmap para el entorno
* [Dependencias] Limpiar las dependencias no utilizadas con el actualizador
* [Updater] No guardar paquetes automáticamente

**Corregido:**

* [Bloqueo] al cerrar el paquete
* [Bloqueo] al abrir el administrador de dependencias en un paquete no guardado
* [Crash] Ejemplo de error de color
* [Motor] Punto muerto de la región de segmentación FxMap
* [Motor] Problema de precisión con el motor SSE con el nodo de desenfoque o mezcla
* [Motor] El cálculo no se detiene si se divide entre 0
* [Explorer] se bloquea al exportar un paquete con dependencia si contiene ciclos de dependencia
* [Explorer] A menudo, la acción de arrastrar y soltar recursos no funciona
* [Panaderos] El valor normal al horno se vuelve negro si es superior a 256\*256
* [Bakers] Guardar un paquete en la misma ubicación que la ruta de exportación interrumpirá la ruta
* [Bakers] Ruta de destino predeterminada incorrecta cuando el paquete aún no se ha guardado
* [Motor] Se produce un resultado de tamaño de píxel incorrecto cuando se hereda de la función principal
* [Dependencias] La dependencia no utilizada no se elimina
* [Dependencies] se bloquean al abrir la ventana de dependencias del paquete que contiene ciclos de paquetes
* La selección del marco de [Graph] se cambia de escala en función del zoom
* El vínculo [Graph] no se &quot;ajusta&quot; a la entrada o salida más cercana
* [Graph] Pila de deshacer incorrecta (puede generar bloqueos)
* [Graph] La conexión múltiple con Ctrl no funciona si el pin ya está conectado
* [Vista 3D] El color de la cuadrícula se ve afectado por el color de fondo
* [Vista 3D] El nodo de salida [Graph] que contiene varios usos no se envía correctamente a la vista 3D
* [Vista 3D] Sombreado de teselación : error de compilación en GPU AMD
* [Vista 2D] Problema del sistema de patillas
* [Funciones] Error de compilación de funciones (si no)
* [Preferencias] El sufijo bajo/alto no se lee correctamente en sbsprj
* [Biblioteca] Al arrastrar y soltar una carpeta sobre otra, se elimina
* [Windows] Se pueden ejecutar varias sesiones de SD
* [Licencia] No se conserva la licencia antigua
* [Contenido] Problema con el filtro de Detección de bordes

### 5.0.3

*(Lanzado: 01 de abril de 2015)*

**Agregado:**

* [Preferencias][Panaderos] Añada una opción para calcular tbn por vértice o por píxel para que coincida con UE4
* [Biblioteca] Usar filtrado bilineal para miniaturas
* [Panaderos] Permite que la ventana se reduzca a menos de 800 px de height
* [3DView] Ecualiza la exposición del mapa del entorno/normaliza la rotación para conseguir un rayo uniforme
* Asignar nombre al método abreviado de la aplicación con versión principal

**Corregido:**

* [Graph] Bloqueo al eliminar algunos nodos fantasma
* [Graph] El nodo acoplado permanece acoplado al duplicar el nodo
* [Graph] Bloqueo al eliminar nodos
* [Graph] Los ajustes de exportación de salidas no se almacenan por gráfico
* [Graph] Estado de acoplamiento de nodo no válido al eliminar nodo
* [Bakers] Los errores ya no se muestran en un cuadro de diálogo
* [Panaderos] El recurso que falta no aparece como ausente en la ventana de panificación
* La ventana [Publicación] fallida no debe poder editarse
* [Publicar] Sbsar Resultado incorrecto
* [Vista 3D] Los materiales múltiples de las mallas FBX actualizadas no se vuelven a cargar correctamente
* [Vista 3D] La SH difusa puede producir valores negativos en algunos casos en sombreadores PBR
* [Vista 2D] La profundidad de bits mostrada para las imágenes de recursos siempre es de 8 bpc
* [Parámetros] Los parámetros no siempre se muestran en las propiedades del gráfico
* [Menú] &quot;Exportar archivo de registro..&quot; acción no consigue localizar el archivo log.txt
* [Batchtools] Error de Subsmutator
* [Explorer] Los paquetes de carga mantienen el resaltado
* [Properties] Bloqueo al borrar una función en un parámetro enum
* [Preferencias] El complemento de espacio tangente Mikkt no está establecido en el valor predeterminado en user\_project
* [Evaluación/Activación] No se puede evaluar/activar en línea en Windows
* La barra de estado de cálculo mueve la interfaz al actualizar
* Iniciar varios SD al mismo tiempo
* Actualizar la dirección URL del reproductor cuando no se encuentra el archivo .exe
* Modificación de archivo en disco no detectada correctamente

### 5.0.2

*(Lanzado: 17 de marzo de 2015)*

**Agregado:**

* [Biblioteca] Añadir control normal en material\_adjustment\_blend
* [Biblioteca] Añadir opción de fusión para normal en material\_color\_blend
* Actualización a Qt 5.4.1

**Corregido:**

* [Bloqueo] OSX 10.9 y 10.10 en FreeImage
* [Bloqueo] Al abrir un archivo fbx que contiene elementos sin vértices
* [Graph] Problemas de arrastrar y soltar
* [Graph] El método abreviado de borrar caché no funciona
* [Graph] La etiqueta TGA aparece en negro/transparente en SD
* [Biblioteca] Entrada normal TriPlanar en escala de grises incorrecta
* [Biblioteca] El nodo de detección de bordes no funciona correctamente con el motor de cpu
* [Parámetros] Rango del regulador incorrecto para float2/3/4
* [Parámetros] Al realizar la operación &quot;Exponer parámetros&quot;, Designer se bloquea dos veces
* [Console] No se redimensiona correctamente
* [Console] Duplicación en la lista de canales: View3D y 3DView
* [3DView] El orden de los parámetros definido en glslfx no se conserva en la interfaz gráfica de usuario
* [Explorer] Bloqueo al actualizar las texturas que faltan en el disco
* [Función] Cambiar el valor y editar provoca el bloqueo
* [Baker] Bloqueo al abrir la ventana de procesamiento en un recurso 3D que falta
* [PSD] Bloqueo de Psdparse (falta MSVCR120.dll)
* [Acerca de la ventana] Falta salto de línea con la versión de Steam
* [Sbs] Nuevas funciones no utilizadas del motor en SBS
* [Sbsar] Las nuevas funciones no se admiten cuando se usan en SD
* [Ui] La barra de progreso no se borra cuando finaliza una exportación con dependencias
* vcomp100.dll no se encuentra al iniciar SD en un Windows 7 recién instalado

**Problemas conocidos:**

* [Windows 8] Arrastrar y soltar no funciona la primera vez que se inicia el programa. Reiniciar SD debe resolverlo.

### 5.0.1

*(Lanzado: 5 de marzo de 2015)*

**Corregido:**

* Se ha corregido un error al exportar mapas de bits en Windows.

### 5.0.0

*(Lanzado: 4 de marzo de 2015)*

**Agregado:**

* [Exportar] descarte el canal del Alpha para TGA y BMP cuando sea completamente opaco
* [Vista 3d] Establecer el sombreador PBR de forma predeterminada
* [Vista 2D] Cambiar para ver la imagen como alfa premultiplicada
* Tamaño de [Parámetros]: Adición de un bloqueo de anchura/Height/valores de visualización en listas desplegables
* [Dependencias] Nuevo administrador de dependencias
* [Dependencies] muestra/busca la instancia de nodo correspondiente a una dependencia
* [Dependencia] Abra un paquete de dependencias en el explorador de paquetes
* [Motor] Fusión: soportar el parámetro Opacidad cuando se usa una máscara
* [Motor] Fusión: Añadir nuevos modos de fusión (superposición, pantalla, softlight, dividir)
* [Motor] Fusión: admitir fusión alfa recta
* [Engine] Nuevo nodo de degradado dinámico
* [Motor] Nuevo nodo Distancia
* [Motor] Nuevo nodo de procesador de píxeles
* [Motor] Fxmap: función dinámica de soporte para imágenes de entrada
* [Motor] Función Sampler: soportar muestreo bilineal
* [Motor] Fxmap: admite el filtrado bilineal/más cercano para imágenes de entrada
* [Motor] Fxmap: soportar imagen de entrada alfa recta/premultiplicada
* [Bakers] Añada una opción para hacer coincidir la geometría por nombre de malla entre mallas de baja y alta definición
* [Plantillas] Crear una plantilla de contenido para Substance Painter
* [Bakers] Nuevo mapa de texturas de mesh baker
* [Graph] Añada una &quot;comprobación de compatibilidad&quot; para resaltar los nodos que no son compatibles con el motor anterior
* [UI] Ajustes del menú Ayuda
* [Preferencias] establecer el complemento de espacio tangente Mikkt como predeterminado (restablecer a los valores predeterminados en las preferencias si está instalado SD4)
* [Biblioteca] Añadir nuevos mapas hdr
* Nuevo Substance a partir de plantilla
* Cambiar a Qt5
* Actualizar el sistema de licencias a SD5

**Corregido:**

* [Solo Mac] Problema del selector de color en la pantalla Retina
* [Solo Mac] Arrastrar y soltar en la vista 3D en el sistema operativo Mac también rota la vista
* [Bakers] Al hornear un mapa sin una carpeta de salida, se produce una textura vacía
* [Graph] Los nodos acoplados en el fotograma se mueven de una forma extraña
* [Parámetros] La ruta de biblioteca personalizada no se carga desde los archivos sbsprj
* [Vista 3D] Al pulsar CTRL+R para volver a cargar todos los sombreadores, también se activa el restablecimiento de la vista 3D
* [Vista 3D] Sobre. La uniformidad del height Mipmap cambia al valor predeterminado al cargar el sombreador
* [Vista 3D] Sombreado PBR : Error de Difusión frente a BaseColor
* [Biblioteca] La ruta de biblioteca no recursiva rompe texturas vinculadas en paquetes
* [Biblioteca] Los mapas de entorno no muestran el archivo .hdr
* [Explorer] &quot;Copiar/Pegar&quot; en la sustancia no debería ser posible
* [Explorer] Haga clic con el botón derecho en la opción &quot;Pegar&quot; que aún está disponible en un gráfico
* La información sobre la herramienta [Función] del muestreador es incorrecta
* [Graph] En el modo compacto, las instancias no muestran todos los nombres de vínculos cuando se expanden automáticamente para agregar un convertidor de escala de grises
