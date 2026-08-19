---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: Obtenga información sobre los nodos de función atómica, las unidades de nodo más pequeñas de los gráficos de funciones de Substance para crear funciones personalizadas.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nodos de funciones atómicas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 16%

---


# Nodos de funciones atómicas

De forma similar a los [nodos atómicos en las gráficas de Substance](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), los nodos atómicos en las gráficas de funciones de Substance son las unidades de nodo más pequeñas en ese tipo de gráfica.

Se pueden clasificar en varias categorías de acuerdo con su propósito:

| Categoría | Nodo | Tipos de entrada | Tipo de salida | Descripción |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [Constante](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | Flotante | - | Flotante | Define un valor flotante constante, p. ej. 0,1 |
|                                                                                                                                        | Flotante 2 | - | Flotante 2 | Define un vector constante de 2 valores flotantes, p. ej. (0.1, 0.2) |
|                                                                                                                                        | Flotante 3 | - | Flotante 3 | Define un vector constante de 3 valores flotantes, p. ej. (0,1, 0,2, 0,3) |
|                                                                                                                                        | Flotante 4 | - | Flotante 4 | Define un vector constante de 4 valores flotantes, p. ej. (0,1, 0,2, 0,3, 0,4) |
|                                                                                                                                        | Entero | - | Entero | Define un valor entero constante, p. ej. 1 |
|                                                                                                                                        | Entero 2 | - | Entero 2 | Define un vector constante de 2 valores enteros, por ejemplo (1, 2) |
|                                                                                                                                        | Entero 3 | - | Entero 3 | Define un vector constante de 3 valores enteros, por ejemplo (1, 2, 3) |
|                                                                                                                                        | Entero 4 | - | Entero 4 | Define un vector constante de 4 valores enteros, por ejemplo (1, 2, 3,4) |
|                                                                                                                                        | Booleano | - | Booleano | Define un valor booleano constante, por ejemplo, True o False |
|                                                                                                                                        | Cadena | - | Cadena | Define un valor de cadena constante, por ejemplo &quot;Substance&quot; |
| [Vector](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | Flotante de vector 2 | Float1 | Float 2 | Emite 2 valores flotantes en un vector con 2 coordenadas |
|                                                                                                                                        | Flotante de vector 3 | Float1 / Float2 | Float 3 | Emite 2 valores flotantes en un vector con 3 coordenadas |
|                                                                                                                                        | Flotante de vector 4 | Float1 / 2 / 3 | Float 4 | Emite 2 valores flotantes en un vector con 4 coordenadas |
|                                                                                                                                        | Referenciar flotante 1 | Flotador vectorial | Float1 | Extrae una coordenada flotante de un vector |
|                                                                                                                                        | Referenciar flotante 2 | Flotador vectorial | Flotante 2 | Extrae 2 coordenadas flotantes de un vector |
|                                                                                                                                        | Referenciar flotante 3 | Flotador vectorial | Flotante 3 | Extrae 3 coordenadas flotantes de un vector |
|                                                                                                                                        | Referenciar flotante 4 | Flotador vectorial | Flotante 4 | Extrae 4 coordenadas flotantes de un vector |
|                                                                                                                                        | Entero de vector 2 | Entero 2 | Entero de vector 2 | Convierte 2 valores enteros en un vector con 2 coordenadas |
|                                                                                                                                        | Entero de vector 3 | Entero 3 | Entero 3 | Convierte 2 valores enteros en un vector con 3 coordenadas |
|                                                                                                                                        | Entero de vector 4 | Entero 4 | Entero 4 | Convierte 2 valores enteros en un vector con 4 coordenadas |
|                                                                                                                                        | Referenciar entero 1 | Vector Integer | Entero1 | Extrae una coordenada entera de un vector |
|                                                                                                                                        | Referenciar entero 2 | Vector Integer | Entero 2 | Extrae 2 coordenadas enteras de un vector |
|                                                                                                                                        | Referenciar entero 3 | Vector Integer | Entero 3 | Extrae 3 coordenadas enteras de un vector |
|                                                                                                                                        | Referenciar entero 4 | Vector Integer | Entero 4 | Extrae 4 coordenadas enteras de un vector |
| [Variables](../../../function-graphs/variables/variables.md) | Establecer | cualquier | tipo de entrada | Establece una variable |
|                                                                                                                                        | Obtener entero1 | - | Entero1 | Obtener una función o un gráfico Entrada de valor entero |
|                                                                                                                                        | Obtener entero 2 | - | Entero 2 | Obtener una entrada de valor Integer2 de función o gráfico |
|                                                                                                                                        | Obtener entero 3 | - | Entero 3 | Obtener una entrada de valor Integer3 de función o gráfico |
|                                                                                                                                        | Obtener entero 4 | - | Entero 4 | Obtener una entrada de valor Integer4 de función o gráfico |
|                                                                                                                                        | Obtener Float1 | - | Float1 | Obtener una entrada de función o gráfico de valor flotante |
|                                                                                                                                        | Obtener flotante 2 | - | Flotante 2 | Obtener una función o gráfico de entrada de valor Float2 |
|                                                                                                                                        | Obtener flotante 3 | - | Flotante 3 | Obtener una función o gráfico de entrada de valor Float3 |
|                                                                                                                                        | Obtener flotante 4 | - | Flotante 4 | Obtener una entrada de valor flotante4 de función o gráfico |
|                                                                                                                                        | Obtener booleano | - | Booleano | Obtener una entrada de valor booleano de función o gráfico |
| Samplers | Gris de muestra | Flotante de vector 2 | Flotante 4 | Devuelve el valor de escala de grises de una imagen de entrada en las coordenadas UV especificadas (float2) |
|                                                                                                                                        | Color de muestra | Flotante de vector 2 | Flotante 4 | Devuelve el valor de color de una imagen de entrada en las coordenadas UV especificadas (float2) |
| Proyección | A flotante | Entero1 | Float1 | Convierte un entero en un flotante |
|                                                                                                                                        | A flotante 2 | Entero 2 | Flotante 2 | Convierte un Integer2 en un Float2 |
|                                                                                                                                        | A flotante 3 | Entero 3 | Flotante 3 | Convierte un entero3 en un flotador3 |
|                                                                                                                                        | A flotante 4 | Entero 4 | Flotante 4 | Convierte un entero4 en un flotante4 |
|                                                                                                                                        | A entero | Float1 | Entero1 | Convierte un flotante en un entero |
|                                                                                                                                        | A entero 2 | Flotante 2 | Entero 2 | Convierte un objeto Float2 en un objeto Integer2 |
|                                                                                                                                        | A entero 3 | Flotante 3 | Entero 3 | Convierte un objeto Float3 en un objeto Integer3 |
|                                                                                                                                        | A entero 4 | Flotante 4 | Entero 4 | Convierte un objeto Float4 en un objeto Integer4 |
| [Operador](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | Añadir | Flotante vectorial / entero | Tipo de a &amp; b | Agrega 2 valores del mismo tipo: a + b |
|                                                                                                                                        | Resta | Flotante vectorial / entero | Tipo de a &amp; b | Resta 2 valores del mismo tipo: a - b |
|                                                                                                                                        | Multiplicación | Flotante vectorial / entero | Tipo de a &amp; b | Multiplica 2 valores del mismo tipo: a \* b |
|                                                                                                                                        | Multiplicación escalar | Flotador vectorial | Tipo de | Multiplica un valor por un valor flotante: a \* escalar |
|                                                                                                                                        | División | Float1 / Integer1 | Tipo de a &amp; b | Divide 2 valores del mismo tipo: a/b |
|                                                                                                                                        | Negación | Float1 / Integer1 | Tipo de | Devuelve el valor de negación: -a |
|                                                                                                                                        | Módulo | Float1 / Integer1 | Tipo de | Devuelve el valor del módulo: mod(a, divisor) |
|                                                                                                                                        | Producto punto | Flotador vectorial | Tipo de a &amp; b | Devuelve el producto de puntos de 2 valores del mismo tipo: punto(a, b) |
| [Lógico](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | Y | Booleano | Booleano | Devuelve verdadero si las 2 entradas booleanas son verdaderas. Devuelve false si una de las entradas es false. |
|                                                                                                                                        | O | Booleano | Booleano | Devuelve verdadero si 1 de las entradas booleanas es verdadero. Devuelve false si ambos son false. |
|                                                                                                                                        | No | Booleano | Booleano | Devuelve el valor booleano de negación de la entrada: !a |
| [Comparación](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | Igual | Float1 / Integer1 | Booleano | Devuelve verdadero si a = b |
|                                                                                                                                        | No es igual | Float1 / Integer1 | Booleano | Devuelve verdadero si a != b |
|                                                                                                                                        | Mayor | Float1 / Integer1 | Booleano | Devuelve verdadero si a > b |
|                                                                                                                                        | Mayor o igual que | Float1 / Integer1 | Booleano | Devuelve verdadero si a >= b |
|                                                                                                                                        | Menor | Float1 / Integer1 | Booleano | Devuelve verdadero si a &lt; b |
|                                                                                                                                        | Menor o igual que | Float1 / Integer1 | Booleano | Devuelve verdadero si a &lt;= b |
| Función | Absoluto | Float1 / Integer1 | Float1 | Devuelve el valor absoluto de un objeto: abs(a) |
|                                                                                                                                        | Límite mínimo | Float1 / Integer1 | Float1 | Devuelve el valor más alto inferior o igual a: piso(a) |
|                                                                                                                                        | Techo | Float1 / Integer1 | Float1 | Devuelve el valor más pequeño superior o igual a: techo(a) |
|                                                                                                                                        | Coseno | Float1 / Integer1 | Float1 | Devuelve el valor del coseno de un objeto: cos(a) |
|                                                                                                                                        | Seno | Float1 / Integer1 | Float1 | Devuelve el valor sinusoidal de: sin(a) |
|                                                                                                                                        | Tangente | Float1 / Integer1 | Float1 | Devuelve el valor de tangente de: bronceado(a) |
|                                                                                                                                        | Arcotangente 2 | Flotante de vector 2 | Float1 | Devuelve el valor arc tan 2 de una entrada vector2: arctan2(xa, ya) |
|                                                                                                                                        | Cartesiano | Float1 | Flotante 2 | Convierte 2 coordenadas polares en coordenadas cartesianas: carth(rho, theta) |
|                                                                                                                                        | Raíz cuadrada | Float1 / Integer1 | Float1 | Devuelve el valor raíz cuadrada de un |
|                                                                                                                                        | Logarítmico | Float1 / Integer1 | Float1 | Devuelve el valor logarítmico de un objeto: log(a) |
|                                                                                                                                        | Exponencial | Float1 / Integer1 | Float1 | Devuelve el valor exponencial de: exp(a) |
|                                                                                                                                        | Pow 2 | Float1 / Integer1 | Float1 | Devuelve la potencia del valor 2 de un |
|                                                                                                                                        | Interpolación lineal | Float1 / Integer1 | Float1 | Devuelve la interpolación lineal entre 2 valores, en función de un valor flotante: (1-x)a + x \* b |
|                                                                                                                                        | Mínimo | Float1 / Integer1 | Tipo de a &amp; b | Devuelve el valor mínimo entre a y b |
|                                                                                                                                        | Máximo | Float1 / Integer1 | Tipo de a &amp; b | Devuelve el valor máximo entre a y b |
| Aleatorio |                       | Float1 | Float1 | Genera un valor flotante entre 0 y a |
| [Control](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | Secuencia | cualquier | Tipo de entrada | Permite elegir qué valor calcular primero entre 2 valores. |
|                                                                                                                                        | If...Else | Booleano / a &amp; b | Tipo de a &amp; b | Devuelve verdadero si la condición de Si es verdadero. Devuelve false si es false. |
