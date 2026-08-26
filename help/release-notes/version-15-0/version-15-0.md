---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/release-notes/version-15-0.html"
breadcrumb-title: ''
description: Revise las notas de la versión 15.0 de Substance 3D Designer para obtener más información sobre el nuevo procesador 3D y la compatibilidad nativa con USD.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versión 15.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1894'
ht-degree: 0%

---


# Versión 15.0

Esta actualización incluye un nuevo procesador 3D, con modos rasterizador y trazador de rutas, además de un soporte nativo de [USD](https://openusd.org/release/index.html) para permitirte editar y exportar escenas sin perder datos.

*Fecha de publicación: 15 de julio de 2025*

![Banner](../../assets/banner-47.png "Versión 15.0")

## Nuevo renderizador 3D

### Nuevo rasterizador y trazador de trazadores

Esta nueva versión te da acceso a un avanzado [procesador 3D](../../interface/3d-view/3d-renderers/3d-renderers.md), que incluye un modo de rasterizado (para tener una vista previa en tiempo real mientras trabajas en tu material) y un modo de trazador de trayectorias (un modo de trazado de rayos para obtener una representación perfecta y precisa). Este nuevo procesador mejora la funcionalidad con funciones como sombras en modo rasterizador, mejora la calidad y el rendimiento, y está diseñado para admitir tecnologías futuras como [MaterialX](https://materialx.org/). Complementa los procesadores existentes de OpenGL e Iray en Designer y se alinea con los procesadores disponibles en Substance 3D Viewer y Substance 3D Sampler, lo que garantiza una experiencia uniforme en todo el ecosistema.

![sombras y translucidez en el rasterizador](../../assets/feature_1b.png)

La [barra de herramientas de la vista 3d](../../interface/3d-view/3d-view.md) se ha actualizado para tener acceso rápido a algunas de las nuevas funciones disponibles en este procesador:

* <b>Herramienta Selección:</b> para seleccionar una submalla en la escena. Una vez seleccionada una submalla, puede centrarse en ella (F) o acceder a sus propiedades de material (clic derecho).
* <b>Habilite pathtracer:</b> para cambiar rápidamente entre los modos pathtracer y rasterizer.
* <b>Habilitar sombras:</b> para habilitar sombras en la escena, útil para ver cómo se comportan los materiales según la luz.
* <b>Habilitar plano de tierra:</b> para habilitar o no el plano de tierra en la escena.

Además, la tecla de acceso rápido para girar la luz del entorno ha cambiado para coincidir con las demás aplicaciones de Substance, por lo que ahora es *<b>mayús-clic derecho</b>* en lugar de *<b>ctrl-mayús-clic derecho</b>*.

### Efectos de posprocesamiento

[Los efectos posteriores han vuelto](../../interface/3d-view/camera/post-effects/post-effects.md). Ahora están disponibles a través del menú Cámara y ahora se desarrollan internamente.

* <b>Bloom:</b> simula el resplandor alrededor de puntos brillantes como luces y reflejos, lo que permite visualizar mejor las superficies emisoras.
* Asignación de tonos <b>: </b>Ajusta el rango de color con perfiles para obtener un efecto de rango dinámico alto (HDR).
* <b>Profundidad de campo:</b> simula las propiedades de enfoque de la lente de una cámara (solo rasterizador).

![Post FX en Designer 15.0](../../assets/postfx.gif)

## Edición de activos en contexto

Cuando trabajes en tus materiales, es posible que desees [obtener una vista previa en el contexto de una escena 3D específica](../../working-with-3d-scenes/working-with-3d-scenes.md). Por eso hemos añadido la posibilidad de importar y renderizar una escena completa, con todas sus texturas, cámaras y luces. Y, por encima de todo, si esta escena hace referencia a sombreadores de MaterialX, se procesarán correctamente con el rasterizador.

![Escena de USD cargada y representada en Designer](../../assets/feature_2.png)

Una vez importado, puedes trabajar en tu escena seleccionando una malla (con MAYÚS+Clic o gracias al explorador de escenas) y [anulando cualquiera de sus materiales](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md). En ese caso puede:

* Cree o cargue un gráfico y aplíquelo a un material de escena.
* Haz ajustes en un material existente [extrayendo sus texturas](../../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md) en un nuevo gráfico.

Por último, una vez que se edita la escena 3D, puedes [exportarla](../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md) como un nuevo archivo o como una nueva capa del archivo original, lo que te impide perder datos (solo para el formato USD).

Por último, pero no por ello menos importante, ahora se admiten más formatos 3D tanto para la importación como para la exportación: USD (+ usda, usdc, usdz), STL, PLY y GLTF, además de los formatos FBX y OBJ ya disponibles.

## Sugerencias de herramientas enriquecidas

Se han introducido sugerencias enriquecidas para demostrar mejor el propósito de cada nodo. Estas sugerencias, actualmente disponibles solo para [nodos atómicos](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), incluyen elementos visuales para demostrar el efecto del nodo y proporcionan un vínculo directo a la documentación para obtener información detallada, incluida la lista de parámetros, sugerencias y trucos.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![nodo de mezcla](../../assets/blend.gif)

</td>
<td style="border: 0;" valign="top">

![nodo de desenfoque](../../assets/blur.gif)

</td>
<td style="border: 0;" valign="top">

![nodo de distancia](../../assets/distance.gif)

</td>
</tr>
</table>

## Mejorar la compatibilidad no cuadrada

Si necesita trabajar con texturas que no sean cuadradas, esta nueva opción está diseñada para usted. En las [propiedades de material](../../interface/3d-view/material-properties/material-properties.md) de la vista 3D, en las opciones de UV para controlar el mosaico, ahora puede establecer un valor diferente para ambos ejes.

![escala de U V diferente](../../assets/nonsquare.png){zoomable="yes"}

## Bakers

Aunque la interfaz de banca solo ha recibido actualizaciones menores (consulte la lista detallada que aparece a continuación para obtener más información), la biblioteca de panaderos se ha rediseñado por completo para utilizar los panaderos basados en GPU, lo que se traduce en un rendimiento mucho mejor. Junto con los nuevos formatos de archivo compatibles mencionados anteriormente, esta actualización representa un avance sustancial para los usuarios que participan en los flujos de trabajo de banca.

Nota: si estaba utilizando sbsbaker.exe para automatizar el proceso, la herramienta ha cambiado de nombre a substance3d\_baker.exe (utilice substance3d-baker —help para obtener más información).

## Actualizaciones de requisitos de plataforma VFX

Todos los años, la [Plataforma de Referencia de VFX](https://vfxplatform.com/) publica una lista de herramientas y versiones de bibliotecas que se usarán en todos los programas para la industria de VFX con el fin de minimizar las incompatibilidades entre los programas. Como de costumbre, *actualizamos todas nuestras dependencias* para respetar todas estas recomendaciones.

## Vídeo

[![Actualización de Substance 3D Designer: Nuevo procesador, postFX y edición de contexto | Substance 3D de Adobe](../../assets/video_15.png)](https://www.youtube.com/watch?v=6EkXxu-0Q_E)

## Notas de la versión

### 15.0.0

*(Lanzado el 15 de julio de 2025)*

### Añadido

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

### Correcciones

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

### ERRORES CONOCIDOS

* [Bakers] Se bloquea al usar algunos controladores específicos de NVidia
* [Vista 3D] OpenGL: es posible que algunas escenas importadas no se procesen
* [Vista 3D] Rasterizador: artefactos de sombra al utilizar desplazamiento en una escena plana
* [Vista 3D] Buscatrazos: rendimiento lento al actualizar texturas con teselación/desplazamiento activado
* [Vista 3D] Algunas propiedades de material de color no se administran correctamente cuando se anulan
* [Vista 3D] Las escenas con animaciones simples no se admiten correctamente
* [Vista 3D] Aún no se admiten mallas con varios UDims
* [Vista 3D] Las mallas con múltiples UV no son compatibles y pueden provocar una representación de material no válida
* [Vista 3D] El trazador de trazados no es compatible con tarjetas gráficas AMD
