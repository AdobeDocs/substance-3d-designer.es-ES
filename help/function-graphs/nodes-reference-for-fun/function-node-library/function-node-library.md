---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library.html"
breadcrumb-title: ''
description: Accede a gráficos de funciones de Substance predefinidos como nodos de instancias para agilizar el flujo de trabajo y mejorar las funciones.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Biblioteca de nodos de función
user-guide-description: ''
user-guide-title: ''
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 6%

---


# Biblioteca de nodos de función

Además de [nodos atómicos](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/atomic-function-nodes.md), Designer también ofrece gráficos de funciones de Substance predefinidos como nodos de instancia. Ofrecen muchas herramientas para acelerar el flujo de trabajo y proporcionan más capacidades para trabajar con vectores o colores, reasignar valores, realizar álgebra más avanzada, ...

Estas herramientas se organizan en varias categorías:

<a name="sdf-functions"></a>

## Funciones de SDF

Estos nodos permiten crear Funciones SDF que se pueden utilizar para generar formas 3D en los nodos [Shape splatter v2](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) y [3d viewer](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md), utilizando sus parámetros **Función SDF** dedicados.

>[!INFO]
> 
> Para obtener más información sobre conceptos y flujos de trabajo que implican Funciones SDF, vaya a la página dedicada: [Trabajando con Funciones SDF](function-nodes-sdf-functions/working-with-sdf-functions.md)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Primitivos

[Cono tapado](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-capped-cone/3d-sdf-capped-cone.md)

[Cono tapado (2 puntos)](././function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-capped-cone-2-points/3d-sdf-capped-cone-2-points.md)

[Toro tapado](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-capped-torus/3d-sdf-capped-torus.md)

[Cápsula](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-capsule/3d-sdf-capsule.md)

[Cono](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-cone/3d-sdf-cone.md)

[Cubo](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-cube/3d-sdf-cube.md)

[Cilindro](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-cylinder/3d-sdf-cylinder.md)

[Cilindro (2 puntos)](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-cylinder-2-points/3d-sdf-cylinder-2-points.md)

[Elipsoide](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-ellipsoid/3d-sdf-ellipsoid.md)

[Cilindro extendido](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-elongated-cylinder/3d-sdf-elongated-cylinder.md)

[Plano de suelo](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-ground-plane/3d-sdf-ground-plane.md)

[Hélice](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-helix/3d-sdf-helix.md)

[Prisma hexagonal](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-hexagonal-prism/3d-sdf-hexagonal-prism.md)

[Plano infinito](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-infinite-plane/3d-sdf-infinite-plane.md)

[Plano](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-plane/3d-sdf-plane.md)

[Pirámide](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-pyramid/3d-sdf-pyramid.md)

[Pirámide cuadrada](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-pyramid-square/3d-sdf-pyramid-square.md)

[Roca](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-rock/3d-sdf-rock.md)

[Esfera](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-sphere/3d-sdf-sphere.md)

[Toro](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-torus/3d-sdf-torus.md)

</td>
<td style="border: 0;" valign="top">

### Operadores

[Intersección](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-intersection/3d-sdf-op-intersection.md)

[Intersección suave](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-intersection-smooth/3d-sdf-op-intersection-smooth.md)

[superficie de intersección](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-intersection-surface/3d-sdf-op-intersection-surface.md)

[Transformar](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-morph/3d-sdf-op-morph.md)

[Repetir espejo](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-repeat-mirror/3d-sdf-op-repeat-mirror.md)

[Redondeo](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-rounding/3d-sdf-op-rounding.md)

[Concha](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-shell/3d-sdf-op-shell.md)

[Resta](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-subtraction/3d-sdf-op-subtraction.md)

[Suavizado de resta](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-subtraction-smooth/3d-sdf-op-subtraction-smooth.md)

[Simetría](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-symmetry/3d-sdf-op-symmetry.md)

[Unión](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-union/3d-sdf-op-union.md)

[chaflán de unión](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-union-chamfer/3d-sdf-op-union-chamfer.md)

[Unión suave](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-union-smooth/3d-sdf-op-union-smooth.md)

</td>
<td style="border: 0;" valign="top">

### Transformaciones

[Doblar](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-bend/3d-sdf-transform-bend.md)

[Alargar](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-elongate/3d-sdf-transform-elongate.md)

[Voltear](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-flip/3d-sdf-transform-flip.md)

[Desplazamiento](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-offset/3d-sdf-transform-offset.md)

[Desplazamiento P](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-offset-p/3d-sdf-transform-offset-p.md)

[Rotar](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-rotate/3d-sdf-transform-rotate.md)

[Rotar P](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-rotate-p/3d-sdf-transform-rotate-p.md)

[Escala](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-scale/3d-sdf-transform-scale.md)

[Giro](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-twist/3d-sdf-transform-twist.md)

</td>
<td style="border: 0;" valign="top">

### Material

[Definir color](function-nodes-sdf-functions/sdf-functions-material/set-color/set-color.md)

[Definir ID de material](function-nodes-sdf-functions/sdf-functions-material/set-id/set-id.md)

[Establecer material](function-nodes-sdf-functions/sdf-functions-material/set-material/set-material.md)

[Establecer el metal](function-nodes-sdf-functions/sdf-functions-material/set-metalness/set-metalness.md)

[Definir rugosidad](function-nodes-sdf-functions/sdf-functions-material/set-roughness/set-roughness.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<a name="comparison"></a>

## Comparación

Igualdad booleana

Equidad float2

Equidad float3

Equidad float4

No igual a booleano

No es igual a float2

No es igual a float3

No es igual a float4

</td>
<td style="border: 0;" valign="top">

<a name="conversion"></a>

## Conversión

[-1, 1] a [0, 1]

[0, 1] a [0, 1, 0]

[0, 1] a [-1, 1]

[0, 1] a [1, 0]

[a, b] a [0, 1]

Boolean a float1

Grados a radianes

Grados a turnos

balance de heightes

Onda de diente de sierra

Onda triangular

Se convierte en grados

</td>
<td style="border: 0;" valign="top">

<a name="constant"></a>

## Constante

2 Pi

Pi

<a name="parity"></a>

## Paridad

Cuenta par

Recuento impar

Prueba de paridad

</td>
</tr>
</table>

<a name="maths"></a>

## Matemáticas

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

acos

asin

Flotador medio

Promedio float2

Promedio de flotador3

Promedio flotante4

Ajustar

Producto cruz

vec2 de productos cruzados

Distancia flotante2

Distancia flotante3

</td>
<td style="border: 0;" valign="top">

División escalar float2

Flotador de división escalar3

Flotador de división escalar4

Fmod

Frac

Longitud flotante2

Longitud flotante3

Combinar flotante3

Combinar flotante4

Normalizar vec2

Normalizar vec3

Normalizar vec4

</td>
<td style="border: 0;" valign="top">

Un signo menos

vec2 ortogonal

Reflejar

Flotador redondo1

Saturar

Saturar flotante2

Firmar

Smoothstep

Paso

Truncar flotador

</td>
</tr>
</table>

<a name="color"></a>

## Color

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

ACEScg a sRGB lineal

Dirección a normal

HCL a RGB

HSI a RGB

Desplazamiento de HSL

HSL a RGB

HSV a RGB

sRGB lineal a ACEScg

Lineal a sRGB (luminancia)

Lineal a sRGB

Color aleatorio

Luminosidad aleatoria

</td>
<td style="border: 0;" valign="top">

RGB croma 2 polar

RGB croma hexagonal

Tono RGB 2 polar

Tono RGB hexagonal

Media de ligereza RGB

RGB ligereza bi-hexcone

hexcona de ligereza RGB

Luminosidad RGB Rec.601

Luminosidad RGB Rec.709

Saturación del RGB HSI

Saturación del RGB HSL

Saturación del RGB HSV

</td>
<td style="border: 0;" valign="top">

RGB a HCL

RGB a HSI

RGB a HSL

RGB a HSV

sRGB a lineal (luminancia)

sRGB a lineal

Temperatura del RGB

Asignador de tonos ACES

Tono Agx (aprox.)

Hejl tonemapper

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<a name="transformation"></a>

## Transformación

Cartesiano a polar

Desplazamiento direccional

Matriz invertida

Multiplicar matriz

Polar a cartesiano

Rotar vec2

Rotar vec2 (Radian)

Matriz de rotación

Matriz de escala

Matriz de mosaicos

</td>
<td width="66.67%" style="border: 0;" valign="top">

<a name="random"></a>

## Aleatorio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Aleatorio discreto [a, b]

Aleatorio global

[Hash 11](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[Hash 14](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[Hash 21](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[Hash 2](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[Hash 24](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[Hash 31](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[Hash 32](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

</td>
<td style="border: 0;" valign="top">

Distribución normal

Uniforme aleatorio [-1, 1[

Uniforme aleatorio [a, b[

Float2 uniforme al azar [a, b[

Flotador uniforme aleatorio3 [a, b[

Flotador uniforme al azar4 [a, b[

</td>
</tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<a name="easings"></a>

## Aceleraciones

Suavizar en círculo

Suavizado en cúbico

Facilidad en expo

Suavizar círculo de entrada

Suavizar entrada salida cúbica

Exposición de entrada fácil

Cuadrante de entrada lenta

Suavizar el cuarto de galón

Suavizar el quint de entrada

Suavizado de entrada desde

Aceleración en quad

Suavizado en el cuarto de galón

Suavizado en quinta

Suavizado del seno

Círculo de salida lenta

Suavizar salida cúbica

Exposición de salida lenta

Cuadrante de salida lenta

Suavizar cuarto de galón

Suavizar salida quint

Suavizar salida desde

</td>
<td width="66.67%" style="border: 0;" valign="top">

<a name="various"></a>

## Diversos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Curva

Escala de UV de expansión no cuadrada

Tamaño de salida no cuadrado

Rugosidad

Interruptor flotante 2 entradas

Interruptor flotante2 2 entradas

Interruptor flotante2 4 entradas

Interruptor flotante2 8 entradas

Interruptor flotante3 2 entradas

Interruptor flotante3 4 entradas

Interruptor flotante3 8 entradas

Interruptor flotante3 8 entradas

Interruptor flotante4 2 entradas

Interruptor flotante4 4 entradas

Interruptor flotante4 8 entradas

</td>
<td style="border: 0;" valign="top">

Cambiar entradas de entero 2

Cambiar entradas de entero 4

Cambiar entradas de entero 8

Conmutador entero2 2 entradas

Conmutador entero2 4 entradas

Conmutador entero2 8 entradas

Conmutador entero3 2 entradas

Conmutador entero3 4 entradas

Conmutador entero3 8 entradas

Conmutador entero4 2 entradas

Conmutador entero4 4 entradas

Conmutador entero4 8 entradas

</td>
</tr>
</table>

</td>
</tr>
</table>
