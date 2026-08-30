---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/3d-renderers.html"
breadcrumb-title: ''
description: Elija entre los procesadores rasterizador y trazador de trazados en la vista 3D para obtener una calidad de previsualización y un rendimiento diferentes.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > 3D renderers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderizadores 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1632'
ht-degree: 7%

---


# Renderizadores 3D

La Vista 3D ofrece cuatro procesadores:

* Dos versiones del procesador 3D interno de Adobe: Rasterizador para visualización en tiempo real con compatibilidad con sombras y Trazador de ruta de GPU para una representación precisa de sombras, reflejos, propiedades de materiales complejos y mucho más.
* Dos procesadores obsoletos de terceros: OpenGL y NVIDIA&#39;s Iray.

>[!NOTE]
>
> Mantenga los controladores gráficos actualizados.
> 
> Los nuevos procesadores 3D se actualizan con regularidad y algunas de estas actualizaciones requieren controladores de GPU recientes. Actualice los controladores de la GPU de su sistema a la versión más reciente para obtener la mejor fiabilidad y compatibilidad con las funciones de procesamiento.
> 
> Puede encontrar controladores aquí: [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us) [AMD](https://www.amd.com/en/support) [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

+++ Comparación de rasterizador/trazador de rutas de GPU

<table>
  <tr>
    <td>
      <img src="3d-renderers.resources/3dRendererRasterizer-2.jpg" alt="3dRendererRasterizer-2">
      <br><i>Rasterizador</i>
    </td>
    <td>
      <img src="3d-renderers.resources/3dRendererPathtracer-2.jpg" alt="3dRendererPathTracker-2">
      <br><i>Trazador de ruta de GPU</i>
    </td>
  </tr>
</table>

+++

El procesador 3D de Adobe se ha creado desde cero para admitir tecnologías modernas como el lenguaje de sombreado [MaterialX](https://materialx.org/) y la descripción de la escena [USD](https://openusd.org/release/index.html), y está preparado para ofrecer una coherencia visual completa en todo el ecosistema de Substance 3D.

Gracias a su dependencia de USD, puede aprovechar el [plugin USDFileFormat](https://github.com/adobe/USD-Fileformat-plugins) de Adobe para importar muchos formatos de escenas 3D, como FBX y GLTF, y renderizar estas escenas completamente, incluidos materiales, texturas, cámaras y luces.

+++ Importación de escenas: Rasterizador frente a OpenGL

<table>
  <tr>
    <td>
      <img src="3d-renderers.resources/3dRendererRasterizer-2.jpg" alt="3dRendererRasterizer-2">
      <br><i>Rasterizador</i>
    </td>
    <td>
      <img src="3d-renderers.resources/3dRendererOpenGL-2.jpg" alt="3dRendererOpenGL-2">
      <br><i>OpenGL</i>
    </td>
  </tr>
</table>

+++

>[!TIP]
>
> Puede seleccionar el procesador que se utiliza de forma predeterminada al iniciar una nueva Vista 3D en la sección [&#x200B; &quot;Vista 3D&quot; de la configuración del proyecto](../../../interface/preferences-window/project-settings/project-settings.md).

<a name="rasterizer"></a>

## Rasterizador

+++ Parámetros

|                                                                 |                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flotante **Samples** | Especifica el número de muestras de píxeles que se deben calcular antes de que se considere que la imagen es convergente. |
| Flotante **opacidad de Oclusión ambiental** | Especifica el valor de la opacidad de la oclusión ambiental. |
| **Habilitar desplazamiento** Boolean | Especifica si se debe habilitar el desplazamiento. |
| Flotante **umbral de Desplazamiento** | Configura un umbral para habilitar/deshabilitar la teselación de GPU. |
| **Habilitar el sacrificio posterior** Boolean | Un valor verdadero permitirá el sacrificio de mallas triangulares que tienen normales que miran hacia fuera de la cámara. Un valor falso desactivará el sacrificio de la cara posterior. |
| **Modo de diagnóstico** Entero | Dicta el modo de diagnóstico que se va a renderizar. |
| **Modo de sombra de rasterizador** Entero | Especifica la técnica que se debe utilizar para procesar sombras:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Sin sombras:</i> No se procesarán sombras.</li> <li data-preserve-html="true"><i>Voxel marchó:</i> La sombra de los rayos de marzo se transformó en una escena voxelizada.</li> </ul> |
| **Número de ejemplos de sombras rasterizadoras** Entero | Especifica cuántos rayos de sombra se trazan por píxel. |
| Flotante **Rasterizer shadow opacity** | Especifica la opacidad de las sombras, de 0,0 (sin sombras) a 1,0 (sombras completas). |
| **Transparencia independiente del orden del rasterizador habilitada** Boolean | No tiene en cuenta el orden de las superficies transparentes al procesarlas. Esto sacrifica algo de precisión para una representación más rápida de las superficies transparentes. |
| **Habilitar SSS de rasterizador** Boolean | Cambia el efecto de dispersión subsuperficial. |
| **Número de muestras de Rasterizer SSS** Entero | Especifica cuántas muestras se toman por píxel para procesar la dispersión subsuperficial. |
| **Habilitar suavizado de acumulación de rasterizador** Boolean | Cambia el suavizado de acumulación, lo que mejora el smoothness o los bordes de la imagen procesada al temblar y calcular el color medio local de cada píxel, de forma acumulativa. Es decir, acumula valores para calcular un promedio a partir de. |
| **Resolución de cuadrícula de voxel rasterizador** Entero | Dicta la resolución de la cuadrícula de voxel utilizada en el movimiento de voxel del rasterizador.   Los valores más altos dan como resultado sombras más precisas a expensas del rendimiento. |
| **Recuento de ejemplos de tiempo de ejecución de IBL de rasterizador** Entero | Especifica cuántas muestras se utilizan para calcular los reflejos de specular de IBL cuando la técnica está establecida en `runtimeSampled`. |

+++

+++ Plano de suelo

|                               |                                                                                                                                                              |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Booleano **Enabled** | Cambia el plano de tierra en la escena procesada. |
| Flotante **Height** | Controla el desplazamiento de height del plano de tierra.   Si se crea, se espera que el valor tenga el sesgo adecuado hecho un bake, en función de la escala de la escena. |
| Flotante **Intensidad de sombra** | Cuando las sombras están activadas, controla la opacidad de las sombras proyectadas en el plano del suelo, desde 0,0 (sin sombras) a 1,0 (sombras completas). |

+++

![Rasterizador - Ejemplo 1](3d-renderers.resources/3dRendererRasterizer.jpg "Rasterizador - Ejemplo 1"){zoomable="yes"}

<a name="gpu-pathtracer"></a>

## Trazador de ruta de GPU

+++ Parámetros

|                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flotante **Samples** | Especifica el número de muestras de píxeles que se deben calcular antes de que se considere que la imagen es convergente. |
| **Habilitar desplazamiento** Boolean | Especifica si se debe habilitar el desplazamiento. |
| Flotante **umbral de Desplazamiento** | Configura un umbral para habilitar/deshabilitar la teselación de GPU. |
| **Habilitar el sacrificio posterior** Boolean | Un valor verdadero permitirá el sacrificio de mallas triangulares que tienen normales que miran hacia fuera de la cámara. Un valor falso desactivará el sacrificio de la cara posterior. |
| **Tipo de ciclo de píxeles** entero | Especifica la técnica que se debe utilizar para reducir la resolución de cálculo para el procesamiento interactivo:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Sin ciclos:</i> Deshabilita el ciclo de píxeles y calcula cada muestra de píxeles completa.</li> <li data-preserve-html="true"><i>Óptimo del dispositivo:</i> Selecciona la resolución ideal de ciclo de píxeles según el dispositivo utilizado para el procesamiento.</li> <li data-preserve-html="true"><i>4x4:</i> Muestras 1/16 de los píxeles por ciclo pasado.</li> <li data-preserve-html="true"><i>8x8:</i> Muestras 1/64 de los píxeles por ciclo pasado.</li><li data-preserve-html="true"><i>Ruido azul:</i> Muestrea de forma adaptable varios píxeles y los separa para lograr una velocidad de marco objetiva.</li> </ul> |
| **Modo de diagnóstico** Entero | Dicta el modo de diagnóstico que se va a renderizar. |
| **Ver fondo a través de la transmisión** Boolean | Un valor verdadero permite ver la imagen de fondo a través de transmisivos u objetos refractivos.   Cuando esto es falso, los objetos de transmisivo mostrarán la imagen refractada del entorno de escena. |

+++

+++ Plano de suelo

|                                    |                                                                                                                                                                  |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Booleano **Enabled** | Cambia el plano de tierra en la escena procesada. |
| Flotante **Height** | Controla el desplazamiento de height del plano de tierra.   Si se crea, se espera que el valor tenga el sesgo adecuado hecho un bake, en función de la escala de la escena. |
| Flotante **Intensidad de sombra** | Cuando las sombras están activadas, controla la opacidad de las sombras proyectadas en el plano del suelo, desde 0,0 (sin sombras) a 1,0 (sombras completas). |
| **Habilitar luces locales** Boolean | Controla si la iluminación directa de las luces locales contribuye a captar sombras. |
| **Habilitar reflejos** Boolean | Controla la visibilidad de todos los reflejos en el plano del suelo. |
| Flotante **Opacidad de reflejos** | Cuando los reflejos están activados, controla la opacidad de los reflejos, entre 0,0 (sin reflejos) y 1,0 (reflejos completos). |
| Flotante de **rugosidad de reflejos** | Cuando los reflejos están activados, controla la rugosidad del material del plano del suelo que contribuye a los reflejos, desde 0,0 (totalmente brillante) a 1,0 (completamente aproximado). |

+++

![Rastreador de GPU - Ejemplo 1](3d-renderers.resources/3dRendererPathtracer.jpg "Rastreador de GPU - Ejemplo 1"){zoomable="yes"}

<a name="opengl"></a>

## OpenGL

El procesador OpenGL ofrece un procesamiento rápido en tiempo real, con algunos sombreadores disponibles de forma predeterminada en función de su caso de uso: consulte la lista siguiente.

+++ OpenPBR

Un modelo de material con un creciente apoyo respaldado por los principales actores del sector, incluido el Adobe, y con el conjunto de funciones más amplio.

Hay dos técnicas disponibles para visualizar el height:

<b>Oclusión de paralaje</b>: falsifica el desplazamiento de height sin modificar la geometría mediante la deformación y la oclusión UV localizadas.

<b>Mosaico + Desplazamiento</b>: subdivide la geometría y desplaza los vértices a lo largo de sus normales.

Obtenga más información sobre el OpenPBR en Designer [aquí](../material-properties/material-properties.md#openpbr).

+++


+++ Adobe Standard Material

sombreador estandarizado de Adobe. Garantiza un aspecto correcto entre todas las aplicaciones de Substance 3D de Adobe y admite un amplio conjunto de funciones.

Hay dos técnicas disponibles para visualizar el height:

<b>Oclusión de paralaje</b>: falsifica el desplazamiento de height sin modificar la geometría mediante la deformación y la oclusión UV localizadas.

<b>Mosaico + Desplazamiento</b>: subdivide la geometría y desplaza los vértices a lo largo de sus normales.

El Adobe Standard Material se documenta detalladamente en [esta sección](https://experienceleague.adobe.com/en/docs/substance-3d/general-knowledge/asm/adobe-standard-material) de nuestra documentación.

+++

+++ SVBRDF AxF

Un sombreador dedicado a visualizar materiales extraídos de [archivos AxF](../../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) y a usar la representación de <b>SVBRDF</b>.

Hay dos técnicas disponibles para visualizar el height:

<b>Oclusión de paralaje</b>: falsifica el desplazamiento de height sin modificar la geometría mediante la deformación y la oclusión UV localizadas.

<b>Mosaico + Desplazamiento</b>: subdivide la geometría y desplaza los vértices a lo largo de sus normales.

Este sombreador es actualmente un *trabajo en curso* y proporciona una descripción general de las características de los materiales, pero no debe usarse para realizar ajustes precisos y algunas características aún no son compatibles.

+++

+++ Blinn

sombreador de &quot;generación anterior&quot;, no correcto para PBR. Utiliza canales de Difuso, Specular y Brillo junto a canales estándar como Opacidad, Height y Normal.

Hay dos técnicas disponibles para visualizar el height:

<b>Oclusión de paralaje</b>: falsifica el desplazamiento de height sin modificar la geometría mediante la deformación y la oclusión UV localizadas.

<b>Mosaico + Desplazamiento</b>: subdivide la geometría y desplaza los vértices a lo largo de sus normales.

+++

+++ Lambert

Sombreador de iluminación lambert muy simple, solo admite el canal Diffuse. Utiliza el antiguo sistema de luces puntuales y no admite la iluminación de imágenes HDR.

+++

+++ Información de malla

Depurar sombreador no iluminado para visualizar los siguientes datos de geometría:

* Normal

* Tangente

* Binormal

* UV

* Mosaico de UV

* Color de vértice

* Posición (espacio mundial)

La visualización se fija a [0, 1]. Por lo tanto, no es posible obtener una lectura directa de valores fuera de ese rango en la pantalla.

+++

+++ Rugosidad metálica

Material PBR estándar para el modelo de rugosidad metálica. Utiliza los canales Color base, Metálico y Rugosidad.

Hay dos técnicas disponibles para visualizar el height:

<b>Oclusión de paralaje</b>: falsifica el desplazamiento de height sin modificar la geometría mediante la deformación y la oclusión UV localizadas.

<b>Mosaico + Desplazamiento</b>: subdivide la geometría y desplaza los vértices a lo largo de sus normales.

+++

+++ Rugosidad metálica - Recubierta

Material PBR recubierto para el modelo de Rugosidad metálica. Utiliza canales de color base, metálicos y de rugosidad, así como canales &quot;Coat&quot; adicionales.

Hay dos técnicas disponibles para visualizar el height:

<b>Oclusión de paralaje</b>: falsifica el desplazamiento de height sin modificar la geometría mediante la deformación y la oclusión UV localizadas.

<b>Mosaico + Desplazamiento</b>: subdivide la geometría y desplaza los vértices a lo largo de sus normales.

+++

+++ Rugosidad metálica - SSS

Material PBR de dispersión subsuperficial para el modelo de rugosidad metálica. Utiliza el color base, los canales metálicos y de rugosidad, así como un canal de dispersión adicional.

Hay dos técnicas disponibles para visualizar el height:

<b>Oclusión de paralaje</b>: falsifica el desplazamiento de height sin modificar la geometría mediante la deformación y la oclusión UV localizadas.

<b>Mosaico + Desplazamiento</b>: subdivide la geometría y desplaza los vértices a lo largo de sus normales.

+++

+++ brillo de specular

Material PBR estándar para el modelo de Brillo de Specular. Utiliza Difuso, Specular y canales de Brillo.

Hay dos técnicas disponibles para visualizar el height:

<b>Oclusión de paralaje</b>: falsifica el desplazamiento de height sin modificar la geometría mediante la deformación y la oclusión UV localizadas.

<b>Mosaico + Desplazamiento</b>: subdivide la geometría y desplaza los vértices a lo largo de sus normales.

+++

+++ No iluminado

Sombreador de depuración no iluminado para visualizar mapas de textura sin ninguna luz. Solo usa un canal de color.

+++

Designer también ofrece la posibilidad de configurar sus propios sombreadores para el procesador OpenGL [mediante archivos GLSLFX](../../../interface/3d-view/glslfx-shaders/glslfx-shaders.md).

>[!IMPORTANT]
> 
> Este procesador está **obsoleto**: No recibirá nuevas funciones y se retirará en una futura versión de Designer.

![OpenGL - Ejemplo 1](3d-renderers.resources/3dRendererOpenGL.jpg "OpenGL - Ejemplo 1"){zoomable="yes"}
