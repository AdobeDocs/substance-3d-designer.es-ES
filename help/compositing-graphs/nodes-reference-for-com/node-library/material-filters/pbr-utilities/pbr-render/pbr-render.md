---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: Utilice el nodo Renderización PBR para procesar materiales basados en la física con iluminación realista para previsualizar la apariencia del material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderización PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 6%

---


# Renderización PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render.resources/pbr-render.png){width="250px"}

<b>En:</b> Filtros de material > Utilidades de PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descripción

Procesa un material PBR en una esfera, plano o cilindro mediante Iluminación basada en imagen (IBL). Se trata de un motor de procesamiento dentro de un nodo, que puede resultar muy útil para generar miniaturas, previsualizaciones o recursos 2D. No es una representación como la vista 3D, sino una textura real que se genera en el gráfico.

Este nodo requiere al menos un material PBR completo para ser conectado. Lo ideal es utilizar los modos de creación de vínculos para conectar el material a la Renderización PBR. Además, necesitará un entorno HDRI desenvuelto esféricamente para que el renderizado calcule la iluminación. Los materiales para pruebas se encuentran en Materiales PBR, los mapas de entorno se encuentran en [Vista 3D en la biblioteca.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> Motor **CPU (SSE2)**
> 
> El nodo Renderización PBR es muy pesado y no funciona bien con el motor de CPU SSE2. Cambie a otro motor presionando F9, si el nodo funciona muy mal.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entradas de canal de materiales</b> | Se utilizan varias entradas de material para representar el material en la geometría:<br><br>- Color base<br>- Normal<br>- Emisivo<br>- Rugosidad<br>- Metálico<br>- Specular level<br>- Height<br>- Oclusión ambiental<br>- Máscara de opacidad<br>- Nivel de anisotropía<br>- Ángulo de anisotropía<br>- Translucidez<br>- Escala de distancia de dispersión |
| <b>Mapa de Dirt de lente</b> <i>Entrada en escala de grises</i> | Mapa personalizado del dirt en la lente que aparece cuando se ven destellos de lente. |
| <b>Mapa de apertura de lente</b> <i>Entrada en escala de grises</i> | Se puede utilizar para anular el efecto bokeh (desenfoque). Cuanto más contrastado, más visible es. Tenga en cuenta que solo se muestra un círculo dentro de la textura, por lo que cualquier forma debe encajar dentro de un círculo. |
| <b>Entrada en segundo plano</b> <i>Entrada de color</i> | La asignación personalizada se usa como fondo cuando el parámetro <b>Background Mode</b> está establecido en <i>Background Input</i> |
| <b>Mapa de entorno</b> <i>Entrada de color</i> | Mapa del entorno utilizado para calcular la iluminación. Se debe asignar esféricamente y en HDR |

<a name="outputs"></a>

## Salidas

|  |  |
|:---|:---|
| <b>Belleza</b> | El renderizado final |
| <b>Irradiancia cruda</b> | Los datos de irradiancia del procesamiento final <br><br><i>Alpha:</i> Mapa de opacidad |
| <b>Specular sin procesar</b> | Los datos de specular del renderizado final <br><br><i>Alpha:</i> mapa de sombras de Specular |
| <b>Espacio normal</b> | El espacio mundial normaliza los datos del renderizado final <br><br><i>Alpha:</i> Mapa de altura del espacio mundial |
| <b>Espacio Tangente Normal</b> | El espacio tangente normaliza los datos del renderizado final <br><br><i>Alpha:</i> Mapa de altura del espacio tangente |
| <b>UV</b> | Los datos UV del procesamiento final <br><br><i>Alpha:</i> Mapa de opacidad |

<a name="parameters"></a>

## Parámetros

|  |  |
|:---|:---|
| <b>Forma</b> <i>Esfera, Plano, Cilindro</i> | Define la forma utilizada para el procesamiento. Las formas personalizadas no son posibles. |
| <b>Intensidad de Desplazamiento</b> <i>0.0 - 0.5</i> | Establezca la intensidad del desplazamiento desde el height. |
| <b>Rotación de entorno</b> <i>0.0 - 1.0</i> | Rota el entorno de iluminación. Gira previamente en comparación con mover la cámara. |
| <b>Modo en segundo plano</b> <i>Color, Entorno, Ambiente, Entrada De Fondo</i> | Establezca lo que se muestra en el fondo. Color es un color sólido, Entorno es el mapa que ha conectado con un desenfoque opcional. Ambient es una versión muy borrosa del entorno. |
| <b>Color de fondo</b> <i>(Valor de color)</i> | Solo está disponible cuando el modo Fondo está establecido en Color. |
| <b>Desenfoque de fondo del entorno</b> <i>0.0 - 1.0</i> | Solo está disponible cuando el modo de fondo está establecido en Entorno. |
| <b>Forma</b> |  |
| <b>Escala</b> <i>0.0 - 2.0</i> | Ajuste la escala de la esfera. |
| <b>Tamaño de plano</b> <i>0.0 - 1.0</i> | Ajuste la escala del plano. |
| <b>Radio del cilindro</b> <i>0.0 - 1.0</i> | Ajuste el radio del cilindro. |
| <b>Longitud del cilindro</b> <i>0.0 - 1.0</i> | Establezca la longitud del cilindro. |
| <b>Rotación</b> <i>0.0 - 1.0</i> | Gira la forma sin girar la iluminación. |
| <b>Dirección de rotación</b> <i>0.0 - 1.0</i> | Define el eje de rotación en 2D. |
| <b>Giro en la dirección</b> <i>0.0 - 1.0</i> | Gira la forma en el eje de rotación. |
| <b>Posición de forma</b> <i>-1.0 - 1.0</i> | Mueve formas. |
| <b>Mosaico UV</b> <i>1.0 - 6.0</i> | Define la cantidad de mosaico UV. |
| <b>Escala de UV de esfera</b> <i>0.0 - 4.0</i> | Define la escala de los UV en la esfera. |
| <b>Escala de UV de plano</b> <i>1.0 - 4.0</i> | Define la escala de los UV en el plano. |
| <b>Escala de UV del cilindro</b> <i>1.0 - 6.0</i> | Establece la escala de UV en el cilindro. |
| <b>Desplazamiento de UV</b> <i>0.0 - 1.0</i> | Desplazamientos de UV |
| <b>UV de inclinación</b> <i>Falso/Verdadero</i> | Inclina los rayos UV 45 grados para la esfera. |
| <b>Cámara</b> |  |
| <b>Exposición</b> <i>-4.0 - 4.0</i> | Ajusta la exposición de la cámara |
| <b>Asignador de tonos</b> <i>Hejl lineal, ACE y fílmico</i> | Defina la solución de asignación de tonos que se utilizará para la imagen final. |
| <b>Modo de cámara</b> <i>Perspectiva, Ortográfica</i> | Cambiar la cámara entre dos modos de proyección. |
| <b>Campo de visión</b> <i>0.01 - 100.0</i> | Ajuste el ángulo FOV de la cámara. |
| <b>Distancia</b> <i>0.0 - 4.0</i> | Establezca la distancia de la cámara desde el centro del objeto. |
| <b>Intensidad de viñeta</b> <i>0.0 - 1.0</i> | Defina la intensidad del efecto de viñeta. |
| <b>Radio de viñeta</b> <i>0.0 - 1.0</i> | Defina el radio del efecto de viñeta. |
| <b>Posición de la pantalla</b> | Mueve la cámara alrededor del objeto, que también se puede cambiar con un gizmo en la vista 2D. |
| <b>Profundidad de campo</b> |  |
| <b>Radio de apertura</b> <i>0.0 - 0.1</i> | Define el radio de la apertura. Los valores más altos significan que las áreas desenfocadas se vuelven más borrosas (bokeh). |
| <b>Hojas de apertura</b> <i>3 - 9</i> | Define la forma del desenfoque bokeh. |
| <b>Anillo de apertura</b> <i>0.0 - 1.0</i> | Añade un degradado interior a la forma bokeh. |
| <b>Difracción de apertura</b> <i>0.0 - 2.0</i> | Añade aberración cromática al efecto bokeh. |
| <b>Swirly Bokeh</b> <i>0.0 - 1.0</i> | Añade un efecto de giro o giro a las áreas de desenfoque desenfocado. |
| <b>Modo de enfoque</b> <i>Automático, punto</i> | Establecer si el foco está predeterminado o definido por el usuario. El enfoque de puntos le permite mover un punto en la vista 2D para determinar la distancia de enfoque. |
| <b>Punto de enfoque</b> | Si el foco se establece en Punto, podrá mover ese punto. tiene un gizmo de vista 2D. |
| <b>Desplazamiento de enfoque</b> <i>-0.5 - 0.5</i> | Si el foco está establecido en Automático, le permite cambiarlo de un lado a otro. |
| <b>Usar mapa de apertura personalizado</b> <i>Falso/Verdadero</i> | Reemplaza la configuración de apertura anterior y utiliza la entrada del mapa de apertura para determinar la forma bokeh. Requiere una entrada. |
| <b>Efectos posteriores</b> |  |
| <b>Habilitar Efectos de posprocesamiento</b> <i>Falso/Verdadero</i> | Alterna <i>todos los</i> efectos posteriores en el procesamiento final. |
| <b>Intensidad de floración</b> <i>0.0 - 2.0</i> | Define la intensidad del efecto de floración. |
| <b>Umbral de floración</b> <i>0.0 - 2.0</i> | Define el umbral bajo para que aparezca la floración. |
| <b>Cambio de croma de floración</b> <i>0.0 - 1.0</i> |  |
| <b>Intensidad de halo de lente</b> <i>0.0 - 1.0</i> | Define la intensidad del efecto de halo de lente. |
| <b>Intensidad de destellos de lente</b> <i>0.0 - 1.0</i> | Define la intensidad del destello de lente. Asegúrate de que la luz del fondo de tu entorno esté visible para poder ver correctamente este efecto. |
| <b>Intensidad de Dirt de la lente</b> <i>0.0 - 1.0</i> | Define el efecto del mapa de dirt de lente en los destellos de lente. |
| <b>Configuración de procesamiento</b> |  |
| <b>Calidad de Difuso</b> <i>16 Muestras, 32 Muestras, 64 Muestras, 128 Muestras</i> | Cambiar entre niveles de calidad para el mapa difuso. |
| <b>Multiplicador de Emisivos de Difuso</b> <i>0.0 - 1.0</i> | Controla en qué medida las partes emisoras contribuyen a la irradiancia. |
| <b>Intensidad de sombra de Difuso</b> <i>0.0 - 1.0</i> | Controla la intensidad de las sombras difusas. |
| <b>Tramado de Specular</b> <i>0.0 - 1.0</i> | Establezca la cantidad de tramado para el specular. |
| <b>Multiplicador de sombras de Specular</b> <i>0.0 - 1.0</i> | Controla la intensidad de las sombras en los reflejos del specular. |
| <b>Modo de opacidad</b> <i>Prueba de Alpha tramado, Fusión de Alpha simple</i> | Controla el método de aplicación de transparencia. El modo <i>Fusión simple de Alpha</i> es más visible en fondos uniformes. |
| <b>Intensidad de Oclusión ambiental</b> <i>0.0 - 1.0</i> | Define la intensidad de las sombras de la oclusión ambiente. |
| <b>Ajustes de material</b> |  |
| <b>Actualizar normales</b> <i>Falso/Verdadero</i> | Las normales se calcularán de nuevo a partir del mapa de height según la intensidad del desplazamiento. |
| <b>Formato normal</b> <i>DirectX, OpenGL</i> | Cambiar entre diferentes Formatos de mapa de normales (invierte el canal verde) |
| <b>Entrada F0 dieléctrica</b> <i>Valor constante, entrada de Specular level</i> | Establecer qué controla los valores F0. La entrada de specular level significa que estará gobernada por un mapa de entrada. |
| <b>Dielectric F0</b> <i>0.0 - 0.08</i> | Si se elige Valor constante para la entrada F0 dieléctrica, este regulador le permite definir el valor global. |
| <b>Abrigo transparente</b> |  |
| <b>Habilitar capa transparente</b> <i>Falso/Verdadero</i> | Permite añadir una capa transparente y simple sobre el material de entrada. |
| <b>Peso de la capa transparente</b> <i>0.0 - 1.0</i> | Establece la intensidad o intensidad de la capa de capa transparente. |
| <b>Borrar Nivel especular de capa</b> <i>0.0 - 1.0</i> | Define la rugosidad de la capa de capa transparente. |
| <b>Heredar normal de la capa base</b> <i>Falso/Verdadero</i> | Defina si la capa de borrado ignora o utiliza los valores normales del material base. |
| <b>Emissive</b> |  |
| <b>Habilitar iluminación de Emisivo</b> <i>Verdadero/Falso</i> | Activa o desactiva la contribución difusa de la iluminación del emisivo. |
| <b>Intensidad del Emisivo</b> <i>0.0 - 10.0</i> | Define el multiplicador global para el mapa de emisiones. |
| <b>Dispersión subsuperficial</b> |  |
| <b>Habilitar dispersión subsuperficial</b> <i>Verdadero/Falso</i> | Alterna la dispersión subsuperficial en el procesamiento final.<br><br><i>Nota:</i> La dispersión subsuperficial requiere que el valor de entrada <b>Translucidez</b> sea <i>superior a 0.0</i> |
| <b>Distancia de dispersión</b> <i>0.0 - 1.0</i> | Ajusta la distancia máxima del efecto de dispersión.<br><br><i>Nota:</i> Este valor se multiplica por el valor de entrada <b>Escala de distancia de dispersión</b> <i>por canal de color</i>. |
| <b>Cambio de color rojo</b> <i>0.0 - 1.0</i> | Ajusta la intensidad del efecto Cambio de color rojo en la dispersión. |
| <b>Rayleigh</b> <i>0.0 - 1.0</i> | Ajusta la intensidad del efecto Rayleigh en la dispersión. |

## Ejemplos

Todas las imágenes se generaron directamente dentro de Designer, en la ventana gráfica 2D, utilizando materiales de la biblioteca [Substance 3D Assets](https://substance3d.adobe.com/assets).

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/pbr-render-v2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-thermal-insulation-panel.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-ominous-obsidian.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-forest-gravel-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-chesterfield-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-carbon-fiber.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/plane-inclined-lumber-tiles.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/cylinder-medieval-leaded-glass-window.jpg" />
        </td>
    </tr>
</table>
