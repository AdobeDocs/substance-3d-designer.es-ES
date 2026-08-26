---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: Utilice los sombreadores GLSLFX en la vista 3D de Substance 3D Designer para personalizar la representación del material y los efectos de previsualización.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombreadores GLSLFX
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 1%

---


# Sombreadores GLSLFX

Los archivos GLSLFX constituyen el puente entre la aplicación y los archivos de sombreador glsl.\
Permite utilizar cualquier sombreador glsl sin tener que modificar el código.

## Formato de archivo

El formato de archivo GLSLFX es un archivo XML. Se admiten comentarios.

### Encabezado y nodo raíz

El elemento nodo raíz XML se denomina <b>glslfx</b>.

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### Cuerpo

#### Técnica

Elemento XML que describe una técnica. Una técnica es una variación del FX actual. Un GLSLFX puede contener múltiples técnicas, pero al menos una técnica debe ser definida.

La geometría se renderizará con una de las técnicas definidas por la aplicación.

+++Definición de elemento XML
Técnica <b>Name:</b>

<b>Atributos:</b>

* nombre: Cualquier cadena utilizada para nombrar la técnica

+++

El elemento XML puede tener varios elementos secundarios. Los elementos definidos en una técnica sustituyen a los elementos definidos globalmente.

Por ejemplo, se utiliza para invalidar algunos valores de uniformes y obtener la variación de FX para esta técnica.

#### Pase de renderizado

Elemento XML que describe una pasada de procesamiento. Una pasada de procesamiento describe la representación de la geometría.

Una técnica puede contener varias pasadas de procesamiento que se ejecutarán secuencialmente. Una técnica que no contiene ninguna pasada de procesamiento es equivalente a una técnica que contiene una pasada de procesamiento en pantalla.

Los elementos definidos en una pasada de procesamiento reemplazan a los elementos definidos en la técnica principal.

+++Definición de elemento XML
<b>Nombre:</b> paso

<b>Atributos:</b>

* output

* fuera de pantalla: El procesamiento se realizará en destinos de procesamiento definidos por el usuario

* en pantalla: El procesamiento se realizará en el destino de procesamiento predeterminado

+++

#### Sombreadores

Establezca los archivos de sombreado GLSL para cada tipo.

Definición de elemento XML:

+++Definición de elemento XML
Sombreador <b>Name:</b>

<b>Atributos:</b>

* tipo: El tipo de sombreador GLSL;

* nombre de archivo: Ruta de acceso del archivo de sombreado glsl. Puede ser absoluto o relativo al archivo GLSLFX;

* primitiveType: El método para representar lo primitivo.


| Valor &#39;type&#39; | Descripción |
| --- | --- |
| punto vertical | Sombreado de vértices |
| geometría | Sombreador de geometría |
| tess\_control | Sombreador de control de teselación |
| test\_eval | Sombreador de evaluación de teselación |
| fragmento | Sombreado de fragmentos |



| Valor &#39;primitiveType&#39; | Descripción |
| --- | --- |
| punto | Procesar como puntos |
| lineloop | Procesar como bucle de línea |
| parche[1..N] | Procesar como parches con vértices [1..N] |


+++

#### Propiedades

Permita configurar alguna parte del estado de OpenGL.

+++Definición de elemento XML
Propiedad <b>Name:</b>

<b>Atributos:</b>

* nombre: Nombre de la propiedad que se va a establecer. El nombre se basa en la función OpenGL o en el nombre glEnum:
  * Sintaxis de ENUM: Sin el prefijo &#39;GL\_&#39;, en minúsculas. Ejemplos: glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;&quot;
  * Sintaxis de funciones: sin el prefijo &#39;gl&#39;, en minúsculas y con todas las palabras separadas por el carácter &#39;\_&#39;. Ejemplo: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* Sintaxis de ENUM: Sin el prefijo &#39;GL\_&#39;, en minúsculas. Ejemplos: glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;&quot;

* Sintaxis de funciones: sin el prefijo &#39;gl&#39;, en minúsculas y con todas las palabras separadas por el carácter &#39;\_&#39;. Ejemplo: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* valor: El valor de la propiedad.


| Valores &#39;name&#39; | Valores &#39;value&#39; | Descripción |
| --- | --- | --- |
| blend\_enabled | booleano | Activar o desactivar el modo de fusión |
|  | true |  |
|  | falso |  |
| blend\_func | cadena, cadena | Definición de las funciones de fusión de origen y destino |
|  | cero | para OpenGL enum GL\_ZERO |
|  | uno | para OpenGL enum GL\_ONE |
|  | src\_color | para OpenGL enum GL\_SRC\_COLOR |
|  | one\_minus\_src\_color | para enumeración de OpenGL GL\_ONE\_MINUS\_SRC\_COLOR |
|  | dst\_color | para OpenGL enum GL\_DST\_COLOR |
|  | one\_minus\_dst\_color | para enumeración de OpenGL GL\_ONE\_MINUS\_DST\_COLOR |
|  | src\_alpha | para OpenGL enum GL\_SRC\_ALPHA |
|  | one\_minus\_src\_alpha | para enumeración de OpenGL GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | dst\_alpha | para OpenGL enum GL\_DST\_ALPHA |
|  | one\_minus\_dst\_alpha | para enumeración de OpenGL GL\_ONE\_MINUS\_DST\_ALPHA |
|  | constante\_color | para OpenGL enum GL\_CONSTANT\_COLOR |
|  | one\_minus\_constant\_color | para enumeración de OpenGL GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | constante\_alfa | para OpenGL enum GL\_CONSTANT\_ALPHA |
|  | one\_minus\_constant\_alpha | para enumeración de OpenGL GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | src\_alpha\_saturate | para enumeración de OpenGL GL\_SRC\_ALPHA\_SATURATE |
|  | src1\_color | para OpenGL enum GL\_SRC1\_COLOR |
|  | one\_minus\_src1\_color | para enumeración de OpenGL GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | src1\_alpha | para OpenGL enum GL\_SRC1\_ALPHA |
|  | one\_minus\_src1\_alpha | para enumeración de OpenGL GL\_ONE\_MINUS\_SRC1\_ALPHA |
| cull\_face\_enabled | booleano | Activar o desactivar el sacrificio de caras |
|  | true |  |
|  | falso |  |
| cull\_face\_mode | cadena | Definir el modo de sacrificio de caras |
|  | frente | para OpenGL enum GL\_FRONT |
|  | posterior | para OpenGL enum GL\_BACK |
|  | front\_and\_back | para enumeración de OpenGL GL\_FRONT\_AND\_BACK |
| profundidad\_func | cadena | Definir la función de comparación de profundidad |
|  | nunca | para OpenGL enum GL\_NEVER |
|  | menos | para OpenGL enum GL\_LESS |
|  | lequial | para OpenGL enum GL\_LEQUAL |
|  | igual | para OpenGL enum GL\_EQUAL |
|  | notable | para OpenGL enum GL\_NOTEQUAL |
|  | gequal | para OpenGL enum GL\_GEQUAL |
|  | mayor | para OpenGL enum GL\_GREATER |
|  | siempre | para OpenGL enum GL\_ALWAYS |


+++

#### Uniformes

Permite anular algunos uniformes definidos globalmente o en la técnica principal. Esto permite cambiar el comportamiento del sombreado para esta técnica o pasada de procesamiento.

Consulte la sección <b>Uniformes</b> a continuación para obtener más detalles sobre su definición.

+++Ejemplo


+++

## Destinos de procesamiento

Para las pasadas de procesamiento &#39;fuera de la pantalla&#39;, los destinos de procesamiento deben definirse en la pasada de procesamiento.

+++Definición de elemento XML
Salida de <b>Nombre:</b>

<b>Atributos:</b>

* archivo adjunto: El punto de conexión de OpenGL, inspirado en los nombres de OpenGL:\
  GL\_COLOR\_ATTACHMENT[0.3] => &#39;color[0.3]&#39;\
  GL\_PROFUNDIDAD\_ATTACHMENT => &#39;profundidad&#39;

archivo adjunto: El punto de conexión de OpenGL, inspirado en los nombres de OpenGL:\
GL\_COLOR\_ATTACHMENT[0.3] => &#39;color[0.3]&#39;\
GL\_PROFUNDIDAD\_ATTACHMENT => &#39;profundidad&#39;

* nombre: el nombre del destino de procesamiento.\
  Se puede utilizar en una pasada de procesamiento posterior para enlazar este destino de procesamiento como un muestreador.

nombre: el nombre del destino de procesamiento.\
Se puede utilizar en una pasada de procesamiento posterior para enlazar este destino de procesamiento como un muestreador.

* formato: el formato interno del destino de procesamiento.

formato: el formato interno del destino de procesamiento.

* claro: atributo opcional que define un valor claro.\
  Si está presente, el destino de procesamiento se borrará hasta este valor al principio de la pasada de procesamiento.\
  Si falta, el destino de procesamiento mantendrá su contenido anterior.

+++

>[!NOTE]
>
> Los destinos de procesamiento de color están prohibidos en una pasada de procesamiento &quot;en pantalla&quot;, pero un destino de procesamiento de profundidad se puede compartir con cualquier pasada de procesamiento (pero es probable que se interrumpa el procesamiento al mezclar varios materiales en la escena).

<b>Acerca de los formatos</b>

Para los formatos de profundidad, se admiten todos los formatos OpenGL de solo profundidad (sin galería de símbolos):

* GL\_PROFUNDIDAD\_COMPONENT16 => &#39;profundidad26&#39;
* GL\_PROFUNDIDAD\_COMPONENT24 => &#39;profundidad34&#39;
* GL\_PROFUNDIDAD\_COMPONENT32 => &#39;profundidad42&#39;
* GL\_PROFUNDIDAD\_COMPONENT32F => &#39;profundidad42f&#39;

Para los formatos de color, el nombre se basa en nombres de enumeración de OpenGL, sin el prefijo &#39;GL\_&#39;, en minúsculas.\
No se admiten tres formatos de canal (RGB); en su lugar, utilice un formato RGBA.\
Profundidad de bits por canal admitida:

* Entero sin signo normalizado: 8, 16
* Punto flotante: 16, 32

Una excepción a estas reglas es el formato GL\_R11F\_G11F\_B10F que se admite.:

* GL\_RGBA8 => &#39;rgba8&#39;
* GL\_RGBA16F => &#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => &quot;rg16&quot;

### Samplers

Si se permite reemplazar algunos muestreadores definidos globalmente, no se pueden definir en una técnica. Esto permite definir un uso de muestra para esta pasada de procesamiento o leer desde un destino de procesamiento de una pasada de procesamiento anterior.

Consulte la sección <b>Samplers</b> para obtener más detalles sobre su definición.

+++Ejemplo


+++

## Formato de vértice de entrada

Esto permite definir la semántica de cada atributo definido en el sombreador de vértices.

<b>Definición de elemento XML:</b>

Nombre: &#39;vertexformat&#39;

Atributos:

* &#39;nombre&#39;: El nombre del atributo tal como se define en el sombreador de vértices.
* &#39;semántico&#39;: Semántica del atributo.

| Valor &#39;semántico&#39; | Descripción |
| --- | --- |
| posición | Posición del vértice (float3) |
| normal | Vértice normal (float3) |
| texcoord[0..N] | Búfer de coordenadas de textura de vértice N (float2) |
| tangente[0..N] | Tampón de tangentes de vértices N (float4) |
| binormal[0..N] | Búfer binormal del vértice N (float4) |

Ejemplo:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## Samplers

Esto permite definir el uso de cada muestreador.\
Lo utiliza la aplicación para saber qué textura se va a establecer en los muestreadores especificados.

<b>Definición de elemento XML:</b>

Nombre: &#39;sampler&#39;

Atributos:

* &#39;nombre&#39;: Nombre de la variable de muestra en el archivo de sombreado.
* &#39;uso&#39;: El uso del muestreador. Coincide con el uso especificado en el nodo Salida del gráfico.

| Valor de &#39;uso&#39; | Descripción |
| --- | --- |
| difundir | Mapa de difusión |
| opacidad | Mapa de opacidad |
| emisivo | Mapa emisivo |
| oclusión ambiental | Mapa de oclusión ambiental |
| ambiente | Mapa ambiental |
| máscara | Mapa de máscara |
| detallado normal | Mapa normal de detalle |
| normal | Mapa de normales |
| bache | Mapa de relieve |
| height | mapa de height |
| desplazamiento | mapa de desplazamiento |
| nivel especular | mapa de specular level |
| color especular | Mapa de colores del specular |
| specular | mapa de speculares |
| brillo | Mapa de brillo |
| rugosidad | Mapa de rugosidad |
| anisotropinivel | Mapa de nivel de anisotropía |
| anisotropiángulo | Mapa de ángulo de anisotropía |
| transmisivo | Mapa transmisivo |
| reflexión | Mapa de reflejos |
| refracción | Mapa de refracción |
| entorno | Mapa de entorno (mapa de cubos) |
| panorama | El mapa panorámico (mapa de latitud/longitud) |
| máscara de azul | Una textura de tramado de 256x256 |

* Se admiten varios usos.
  * Ejemplo:

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


&#39;isHidden&#39;: Booleano que indica si el muestreador debe aparecer en la GUI

* Ejemplo:

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


Modo de ajuste:

<table data-preserve-html="true"><tbody><tr><th>Nombre</th><th>Valor</th></tr><tr><td rowspan="4">texture_wrap_s, texture_wrap_t, texture_wrap_r<br/><br/><br/></td><td>clamp_to_edge</td></tr><tr><td>clamp_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">repetir<br/><br/></td></tr></tbody></table>

Filtro de textura

<table data-preserve-html="true"><tbody><tr><th>Nombre</th><th>Valor</th></tr><tr><td rowspan="6">texture_min_filter, texture_mag_filter<br/><br/><br/></td><td>más cercano</td></tr><tr><td>lineal</td></tr><tr><td colspan="1">nearest_mipmap_nearest</td></tr><tr><td colspan="1">linear_mipmap_nearest</td></tr><tr><td colspan="1">nearest_mipmap_linear</td></tr><tr><td colspan="1">linear_mipmap_linear</td></tr></tbody></table>

Ejemplo:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## Uniformes

Esto le permite agregar información adicional sobre los uniformes de cada sombreador.

<b>Definición de elemento XML:</b>

Nombre: &#39;uniforme&#39;

Atributos:

&#39;nombre&#39;: El nombre del uniforme en el archivo de sombreado.

| Valor &#39;semántico&#39; | Descripción |
| --- | --- |
| mundo | Matriz mundial (float16) |
| worldinversetranspose | Matriz de transposición inversa mundial (float16) |
| worldviewprojection | Matriz de proyección de la vista mundial (float16) |
| view inverso | Matriz inversa mundial (float16) |
| visión del mundo | Matriz de vista del mundo (float16) |
| modelview | Matriz de vista de modelo (float16) |
| proyección | Matriz de proyección (float16) |
| ambiente | Color ambiente de la escena (float3) |
| lightposition[0.N] | Posición de la luz n de la escena (float3) |
| lightcolor[0..N] | Color de la luz n de la escena (float3) |
| intensidad de luz[0..N] | Intensidad de la luz n de la escena (flotante) |
| tiempo global | Hora actual en segundos (float) |
| resolución | Resolución de ventana gráfica (int2) |
| ratón | Posición del ratón (int2) |
| samplespostablesize | Número de muestras que se utilizarán para calcular la iluminación ambiental (int) |
| irradianceschcoefs | El conjunto de vectores de armónicos esféricos (float3[10]) |
| panoramamipmapheight | Número de niveles de mapa MIP en el mapa panorámico (float) |
| panorámica | Ángulo Ángulo de rotación del mapa panorámico (flotante) |
| panoramaintensity | Intensidad del mapa panorámico (float) |
| computebinormalinfragmentshader | ¿Se calcula el binormal por fragmento? (si no es así, por vértice) (bool) |
| isdirectxnormal | ¿Es el DirectX del formato de mapa de normales? (bool) |
| uvwscale | Valores de escala de u, v, w (float3) |
| renderuvitil | ¿Renderizar solo 1 mosaico UV? (bool) |
| uvtilecoords | Coordenada del mosaico UV que se va a procesar (int2) |

&#39;semántico&#39;: La semántica del uniforme. (Todas las matrices son float16).

Ejemplo:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


Ejemplo:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### Otros parámetros

Se puede añadir información adicional a cada uniforme para:

* definir el valor predeterminado
* valores de sujeción
* controlar la forma en que se mostrará el uniforme en la aplicación:
* establecer la etiqueta
* establezca la información del widget utilizada para editar el valor en la aplicación:
* nombre del widget, min, max, increment/decrement step
* uniformes de grupo en widgets de grupo

Como los Uniformes pueden ser reemplazados para cada técnica, permite mostrar una configuración de interfaz de usuario específica para cada técnica.

<b>Definición de elemento XML:</b>

Nombre: &#39;uniforme&#39;

Atributos:

* &#39;nombre&#39;: El nombre del uniforme en el archivo de sombreado.
* &#39;predeterminado&#39;: El valor predeterminado uniforme
* &#39;min&#39;: El valor mínimo del intervalo de validez
* &#39;max&#39;: El valor máximo del intervalo de validez
* &#39;guiName&#39;: El nombre del uniforme en la GUI de la aplicación
* &#39;guiGroup&#39;: El nombre del grupo para poner el uniforme en la GUI de la aplicación
* &#39;guiWidget&#39;: El nombre del widget utilizado para editar el valor uniforme en la GUI de la aplicación

| Valor &#39;guiWidget&#39; | Descripción |
| --- | --- |
| regulador | Widget de regulador para floatN |
| ángulo | Widget de ángulo para flotador |
| color | Widget de color para float3, float4 color |
| casilla de verificación | Widget de CheckBox para bool |

* &#39;guiMin&#39;: El valor mínimo del widget
* &#39;guiMax&#39;: El valor máximo del widget

## Ejemplo: Teselación/paralaje

### Archivo de sombreador de vértices de paralaje

Se encuentra en .\tessellation\_parallax\parallax\vs.glsl

Contenido:

> #version 120

attribute vec4 iVS\_Position;\
atributo vec4 iVS\_Normal;\
attribute vec2 iVS\_UV;\
attribute vec4 iVS\_Tangent;\
attribute vec4 iVS\_Binormal;

variar vec3 iFS\_Normal;\
variar vec2 iFS\_UV;\
variar vec3 iFS\_Tangent;\
variar vec3 iFS\_Binormal;\
variar vec3 iFS\_PointWS;

worldMatrix uniforme mat4;\
mat4 worldViewProjMatrix uniforme;

void main()\
&lbrace;\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position;\
iFS\_Normal = iVS\_Normal.xyz;\
iFS\_UV = iVS\_UV;\
iFS\_Tangent = iVS\_Tangent.xyz;\
iFS\_Binormal = iVS\_Binormal.xyz;\
iFS\_PointWS = (worldMatrix \&#42; iVS\_Position).xyz;\
&rbrace;

### Archivo de sombreador de vértices de teselación

Se encuentra en .\tessellation\_parallax\tessellation\vs.glsl

Contenido:

&#x200B;>> 

&#x200B;#version 120

attribute vec4 iVS\_Position;\
atributo vec4 iVS\_Normal;\
attribute vec2 iVS\_UV;\
attribute vec4 iVS\_Tangent;\
attribute vec4 iVS\_Binormal;

variación de vec4 oVS\_Normal;\
variar vec2 oVS\_UV;\
variar vec4 oVS\_Tangent;\
variar vec4 oVS\_Binormal;

void main()\
&lbrace;\
gl\_Position = iVS\_Position;\
oVS\_Normal = iVS\_Normal;\
oVS\_UV = iVS\_UV;\
oVS\_Tangent = iVS\_Tangent;\
oVS\_Binormal = iVS\_Binormal;\
&rbrace;

### Archivo de sombreador de control de teselación

Se encuentra en .\tessellation\_parallax\tessellation\tcs.glsl

Contenido:

&#x200B;>> 

&#x200B;#version 400 core\
&#x200B;#extension GL\_ARB\_tessellation\_shader : permitir

layout(vertices = 3) out;

en vec4 oVS\_Normal[];\
en vec2 oVS\_UV[];\
en vec4 oVS\_Tangent[];\
en vec4 oVS\_Binormal[];

out vec4 oTCS\_Normal[];\
out vec2 oTCS\_UV[];\
out vec4 oTCS\_Tangent[];\
out vec4 oTCS\_Binormal[];

teselación de flotador uniformeFactor;

void main()\
&lbrace;\
gl\_TestLevelOuter[0] = tessellationFactor;\
gl\_TestLevelOuter[1] = tessellationFactor;\
gl\_TestLevelOuter[2] = tessellationFactor;\
gl\_TestLevelInner[0] = tessellationFactor;\
gl\_out[gl\_InvocationID].gl\_Position = gl\_in[gl\_InvocationID].gl\_Position;

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID];\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID];\
oTCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID];\
oTCS\_Binormal[gl\_InvocationID] = oVS\_Binormal[gl\_InvocationID];\
&rbrace;

### Archivo sombreador de evaluación de teselación

Se encuentra en .\tessellation\_parallax\tessellation\tcs.glsl

Contenido:

&#x200B;>> 

&#x200B;#version 400 core

layout(triangles, equal\_spacing, ccw) in;

en vec4 oTCS\_Normal[];\
en vec2 oTCS\_UV[];\
en vec4 oTCS\_Tangent[];\
en vec4 oTCS\_Binormal[];

worldMatrix uniforme mat4;\
mat4 worldViewProjMatrix uniforme;

muestra uniforme 2D heightMap;

baldosas flotantes uniformes = 1,0f;\
altura de flotador uniformeMapScale = 1,0f;

out vec3 iFS\_Normal;\
out vec2 iFS\_UV;\
out vec3 iFS\_Tangent;\
out vec3 iFS\_Binormal;\
out vec3 iFS\_PointWS;

vec3 interpolate3D(vec3 v0, vec3 v1, vec3 v2, vec3 uvw)\
&lbrace;\
devuelve uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
&rbrace;

vec2 interpolate2D(vec2 v0, vec2 v1, vec2 v2, vec3 uvw)\
&lbrace;\
devuelve uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
&rbrace;

void main()\
&lbrace;\
vec3 uvw = gl\_TessCoord.xyz;

vec3 newPos = interpolate3D(gl\_in[0].gl\_Position.xyz, gl\_in[1].gl\_Position.xyz, gl\_in[2].gl\_Position.xyz, uvw);\
vec3 newNormal = normalize(interpolate3D(oTCS\_Normal[0].xyz, oTCS\_Normal[1].xyz, oTCS\_Normal[2].xyz, uvw);\
vec3 newTangent = normalize(interpolate3D(oTCS\_Tangent[0].xyz, oTCS\_Tangent[1].xyz, oTCS\_Tangent[2].xyz, uvw));\
vec3 newBinormal = normalize(interpolate3D(oTCS\_Binormal[0].xyz, oTCS\_Binormal[1].xyz, oTCS\_Binormal[2].xyz, uvw);\
vec2 newUV = interpolate2D(oTCS\_UV[0], oTCS\_UV[1], oTCS\_UV[2], uvw);

float heightTextSample = texture(heightMap, newUV \&#42; tiling).x \&#42; 2.0 - 1.0;\
newPos += newNormal \&#42; heightTextSample \&#42; heightMapScale;

vec4 obj\_pos = vec4(newPos, 1);\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos;

iFS\_UV = newUV \&#42; mosaico;\
iFS\_Tangent = newTangent;\
iFS\_Binormal = newBinormal;\
iFS\_Normal = newNormal;\
iFS\_PointWS = (worldMatrix \&#42; obj\_pos).xyz;\
&rbrace;

### Archivo de sombreador de fragmentos

Se encuentra en .\tessellation\_parallax\fs.glsl

Contenido:

&#x200B;>> 

&#x200B;#version 120

// #define ALG\_NORMAL\_DIRECTX\
&#x200B;#define ALG\_NORMAL\_OPENGL

&#x200B;#ifdef ALG\_NORMAL\_DIRECTX\
// #define VOLTEAR\_NORMAL\_X\
&#x200B;#define VOLTEAR\_NORMAL\_Y\
// #define VOLTEAR\_NORMAL\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_DIRECTX

&#x200B;#ifdef ALG\_NORMAL\_OPENGL\
// #define VOLTEAR\_NORMAL\_X\
&#x200B;#define VOLTEAR\_NORMAL\_Y\
// #define VOLTEAR\_NORMAL\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_OPENGL

variar vec3 iFS\_Normal;\
variar vec2 iFS\_UV;\
variar vec3 iFS\_Tangent;\
variar vec3 iFS\_Binormal;\
variar vec3 iFS\_PointWS;

vec3 uniforme Lamp0Pos = vec3(0,0f,0,0f,70,0f);\
vec3 uniforme Lamp0Color = vec3(1,0f,1,0f,1,0f);\
vec3 uniforme Lamp1Pos = vec3(70,0f,0,0f,0,0f);\
vec3 uniforme Lamp1Color = vec3(0,198f,0,198f,0,198f);\
uniforme bool flipNormal = true;\
piso uniforme TilingDetail = 3.0f;\
Float uniforme SpecExpon = 50.0;\
flotador uniforme Ks = 1,0;\
uniforme int parallax\_mode = 0;\
teselación de flotador uniformeFactor = 4.0;\
altura de flotador uniformeMapScale = 1,0f;\
profundidad de flotador uniforme\_detail = 0,5f;\
Kr = 0.5f;\
uniforme int KF\_on = 1;\
KFs de flotador uniforme = 1.0f;\
vec3 AmbiColor uniforme = vec3(0,07f,0,07f,0,07f);\
baldosas flotantes uniformes = 1,0f;\
uniforme int enableTilingInFS = 0;

muestra uniforme 2D heightMap;\
muestra uniforme2D normalMap;\
muestra uniforme 2D detailNormalMap;\
muestreador uniforme 2D emissiveMap;\
muestra uniforme 2D diffuseMap;\
muestra uniforme 2D specularMap;\
muestra uniforme 2D opacityMap;\
muestra uniformeEntorno de cuboMapa;

worldMatrix uniforme mat4;\
uniforme mat4 worldInverseTransposeMatrix;\
uniforme mat4 viewInverseMatrix;

vec4 litFct(float NdotL, float NdotH, float specExp)\
&lbrace;\
float ambient = 1.0;\
float diffuse = max(NdotL, 0.0);\
specular float = step(0.0, NdotL) \&#42; pow(max(0.0, NdotH), specExp);\
vec4 de retorno (ambiente, difuso, specular, 1.0);\
&rbrace;

vec3 lerpFct(vec3 v0, vec3 v1, porcentaje flotante)\
&lbrace;\
valor devuelto v0 + (v1-v0) \&#42; por ciento;\
&rbrace;

// Sombreado de Phong\
void phong\_sombreado(\
en vec3 LightColor,\
en vec3 normalWS,\
en vec3 pointToLightDirWS,\
en vec3 pointToCameraDirWS,\
inout vec3 DiffuseContrib,\
inout vec3 SpecularContrib)\
&lbrace;\
vec3 Hn = normalize(pointToCameraDirWS + pointToLightDirWS);\
vec4 litV = litFct(dot(normalWS, pointToLightDirWS), dot(normalWS, Hn), SpecExpon);\
DiffuseContrib = litV.y \&#42; LightColor;\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor;\
&rbrace;

vec3 fixNormalSample(vec3 v)\
&lbrace;\
resultado vec3 = v - vec3(0,5,0,5,0,5);

&#x200B;#ifdef FLIP\_NORMAL\_X\
result.x = -result.x;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_X\
&#x200B;#ifdef FLIP\_NORMAL\_Y\
result.y = -result.y;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_Y\
&#x200B;#ifdef FLIP\_NORMAL\_Z\
result.z = -result.z;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_Z

resultado de retorno;\
&rbrace;

vec3 normalVecOSToWS(vec3 normal)\
&lbrace;\
retorno normal;\
&rbrace;

void main()\
&lbrace;\
vec3 cameraPosWS = viewInverseMatrix[3].xyz;\
vec3 pointToLight0DirWS = normalize(Lamp0Pos - iFS\_PointWS);\
vec3 pointToLight1DirWS = normalize(Lamp1Pos - iFS\_PointWS);\
vec3 pointToCameraDirWS = normalize(cameraPosWS);\
vec3 normalOS = normalize(iFS\_Normal);\
vec3 tangentOS = normalize(iFS\_Tangent);\
vec3 binormalOS = normalize(iFS\_Binormal);

// ------------------------------------------\
// Asegúrese de que la TBN esté normalizada Orthon\
binormalOS = normalize(cross(normalOS, tangentOS));\
tangentOS = normalize(cross(binormalOS, normalOS));

vec3 cumulatedNormalOS = normalOS;

// ------------------------------------------\
// Actualizar UV\
float a = dot(normalOS,-pointToCameraDirWS);\
vec3 s = vec3(dot(pointToCameraDirWS,tangentOS), dot(pointToCameraDirWS,binormalOS), a);\
vec2 uv = enableTilingInFS == 0 ? iFS\_UV : (mosaico iFS\_UV \&#42;);\
height flotante = texture2D(heightMap,uv).x \&#42; 2.0 - 1.0 ;\
float parallax = parallax\_mode == 0 ? (tessellationFactor / 100000.f + heightMapScale / 500.f) : (heightMapScale / 50.f);\
uv += (height \&#42; s.xy \&#42; paralaje) ;

// ------------------------------------------\
// Agregar normal desde normalMap\
vec3 normalTS = texture2D(normalMap,uv).xyz;\
normalTS = fixNormalSample(normalTS);\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalMapOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

// ------------------------------------------\
// Agregar mapa normal de detalles\
vec3 normalDetailTS = texture2D(detailNormalMap,uv\&#42;TilingDetail).xyz;\
normalDetailTS = fixNormalSample(normalDetailTS);\
vec3 variableNormalDetailTS = lerpFct(vec3(0.0,0.0,0.5),normalDetailTS,Profundidad\_detail);\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalDetailOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

if (length(normalTS)&lt;0.0001)\
cumulatedNormalOS = normalOS;

vec3 cumulatedNormalWS = normalVecOSToWS(cumulatedNormalOS);

// ------------------------------------------\
// Computar difusión y Specular

// Contribución de Light 0\
vec3 diffContrib = vec3(0, 0, 0);\
vec3 specContrib = vec3(0, 0, 0);\
phong\_sombreado(Lamp0Color, cumulatedNormalWS, pointToLight0DirWS, pointToCameraDirWS, diffContrib, specContrib);

// Contribución de Light 1\
vec3 diffContrib2 = vec3(0, 0, 0);\
vec3 specContrib2 = vec3(0, 0, 0);\
phong\_sombreado(Lamp1Color, cumulatedNormalWS, pointToLight1DirWS, pointToCameraDirWS, diffContrib2, specContrib2);

diffContrib += diffContrib2;\
specContrib += specContrib2;

vec4 diffuseColor = texture2D(diffuseMap,uv);

vec3 specularColor = texture2D(specularMap,uv).rgb;\
vec3 R = reflejo(pointToCameraDirWS,cumulatedNormalWS);\
vec3 reflColor = Kr \&#42; textureCube(environmentMap,R.xyz).bgr;

float FallofRefl;

if (KFs >= 0.0)\
FallofRefl = max((1-dot(pointToCameraDirWS/(KFs),cumulatedNormalWS),0)\&#42;KF\_on;\
else\
FalseRefl = (1-max((1-dot(pointToCameraDirWS/(-KFs),cumulatedNormalWS)),0))\&#42;KF\_on;

if (KF\_on == 0)\
FallofRefl=1.0;

vec3 Ambiant\_final = diffuseColor.rgb\&#42;AmbiColor;

// ------------------------------------------\
vec3 emissive = texture2D(emissiveMap,uv).xyz;

vec3 finalcolor = Ambiant\_final\
&#x200B;+ specularColor\&#42;specContrib\
&#x200B;+ diffuseColor.rgb\&#42;diffContrib\
&#x200B;+ (reflColor\&#42;specularColor\&#42;FallofRefl)\
&#x200B;+ emisivo;

// Color final\
vec4 finalColor4 = vec4(final, color, textura2D(opacityMap,uv));

gl\_FragColor = finalColor4;\
&rbrace;

### Archivo GLSLFX

El fichero glslfx define dos técnicas para procesar la geometría:

* Uno usa la técnica de teselación de hardware
* El otro se basa en un efecto de paralaje que se utilizará como retroceso si el hardware del usuario no admite la teselación.

Se encuentra en .\tessellation\_parallax\fs.glsl

Contenido:

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```
