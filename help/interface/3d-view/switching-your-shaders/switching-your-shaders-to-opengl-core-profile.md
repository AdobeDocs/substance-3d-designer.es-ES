---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: Obtenga información sobre cómo cambiar sombreadores a OpenGL Core Profile en la vista 3D de Substance 3D Designer para obtener compatibilidad y rendimiento.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cambiar los sombreadores al perfil principal de OpenGL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# Cambiar los sombreadores al perfil principal de OpenGL

Desde la versión 2018.2.0, la ventana gráfica 3D utiliza OpenGL Core Profile.\
En esta ocasión, hemos actualizado algunos sombreadores que proporcionamos con la aplicación de GLSL versión 120 a GLSL versión 330.

Es posible que desee actualizar sus propios sombreadores para aprovechar las nuevas funciones GLSL disponibles o para hacer que su código GLSL sea más moderno. Tenga en cuenta que, en MacOS, los sombreadores antiguos pueden dejar de funcionar.\
Para obtener una visión general completa de las nuevas funciones, le recomendamos que consulte la documentación oficial de OpenGL. Por ejemplo, puede consultar la [Especificación 3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf) del lenguaje de Sombreado OpenGL.\
De lo contrario, aquí hay una guía rápida que le ayudará a convertir sus sombreadores GLSL 1.20 en GLSL 3.30:

## Actualizar el número de versión

En primer lugar, reemplaza (o añádelo en la parte superior del archivo si aún no lo tienes) tu directiva `#version` anterior por `#version 330`.

### Reemplace el &quot;atributo&quot; y &quot;variable&quot; por &quot;dentro&quot; o &quot;fuera&quot;

Ahora, las variables `attribute` y `varying` se declaran explícitamente como `in` o `out`, dependiendo de la fase del sombreador:

En el sombreador del vértice, `attribute` de los vértices se declaran como `in`, mientras que `varying` que se van a pasar al sombreador del fragmento se declaran como `out`.\
Por ejemplo:

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


se convierte en:

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


Del mismo modo, en el sombreador de fragmentos, la variación se convierte en entrada. También debe declarar una variable out que reemplace gl\_FracColor (que ya no está integrada):

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


se convierte en:

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### Usar nuevas funciones de búsqueda de textura

Con la nueva versión del lenguaje de sombreado, la API de búsqueda de textura se ha simplificado y aumentado.

Las funciones `texture1D()`, `texture2D()`, `texture3D()` y `textureCube()` se convierten en sobrecargas de `texture()`.\
Del mismo modo, `texture2DLod()` se convierte en `textureLod()`, `texture2DGrad()` se convierte en `textureGrad()`, etc.

Ahora también tiene acceso a funciones útiles como `textureSize()` (para consultar el tamaño de la muestra en texel), `textureOffset()` (para muestrear vecinos de la ubicación de destino), `textureFetch()` (para proporcionar una ubicación de muestra en píxeles) y más cosas.
