---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/function-nodes.html"
breadcrumb-title: ''
description: Acceda a nodos de función en gráficas de funciones de Substance 3D Designer para llamar y ejecutar gráficas de funciones personalizadas.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Función
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 5%

---


# Nodos de función

Los nodos Function transforman el valor de entrada de acuerdo con la función matemática que representan.

Aunque sus conectores de entrada no suelen estar escritos, no admiten todos los tipos de valor.

## Lista de nodos

+++Pow
![Icono de nodo Pow](function-nodes.resources/function-nodes-01.jpg "Icono de nodo Pow")



Devuelve la primera entrada elevada a la potencia de la segunda entrada: <b>X^Y</b>.

+++

+++2Pow
![2Icono de nodo Pow](function-nodes.resources/function-nodes-02.jpg "Icono de nodo 2Pow")



Devuelve 2 a la potencia de su valor de entrada: <b>2^X</b>.

+++

+++Raíz cuadrada
![Icono de nodo raíz cuadrado](function-nodes.resources/function-nodes-03.jpg "Icono de nodo raíz cuadrado")



Devuelve la raíz cuadrada de su valor de entrada: <b>√X</b>.

+++

+++Exponencial
![Icono de nodo exponencial](function-nodes.resources/function-nodes-04.jpg "Icono de nodo exponencial")



Devuelve el valor exponencial de su valor de entrada: <b>e^X</b>

<b>e</b> es aproximadamente igual a 2,7182818.

+++

+++Logaritmo
![Icono de nodo de logaritmo](function-nodes.resources/function-nodes-05.jpg "Icono de nodo de logaritmo")



Devuelve el logaritmo natural de su valor de entrada: <b>ln(X)</b>.

+++

+++Base logarítmica 2
![Icono de nodo de base de logaritmo 2](function-nodes.resources/function-nodes-06.jpg "Icono de nodo de base de logaritmo 2")



Devuelve el logaritmo base 2 de su valor de entrada: <b>log2(X)</b>.

+++

+++Absoluto
![Icono de nodo absoluto](function-nodes.resources/function-nodes-07.jpg "Icono de nodo absoluto")



Devuelve el valor absoluto de su entrada: <b>abs(X)</b>.

+++

+++Techo
![Icono de nodo de celda](function-nodes.resources/function-nodes-08.jpg "Icono de nodo de celda")



Redondea su valor de entrada hacia arriba. Devuelve el valor entero más pequeño no menos que X: <b>ceil(X)</b>.

+++

+++Límite mínimo
![icono de nodo de Suelo](function-nodes.resources/function-nodes-09.jpg "icono de nodo de Suelo")



Redondea su valor de entrada hacia abajo. Devuelve el mayor valor entero no mayor que X: <b>floor(X)</b>.

+++

+++Interpolación lineal
![Icono de nodo de interpolación lineal](function-nodes.resources/function-nodes-10.jpg "Icono de nodo de interpolación lineal")



Devuelve la interpolación lineal entre dos valores en función de un valor flotante: <b>(1 - X)\*A + X\*B</b>.

+++

+++Mínimo
![Icono de nodo mínimo](function-nodes.resources/function-nodes-11.jpg "Icono de nodo mínimo")



Devuelve el valor más bajo de los dos valores de entrada: <b>min(A, B)</b>.

+++

+++Máximo
![Icono de nodo máximo](function-nodes.resources/function-nodes-12.jpg "Icono de nodo máximo")



Devuelve el mayor de los dos valores de entrada: <b>max(A, B)</b>.

+++

+++Coseno
![Icono de nodo coseno](function-nodes.resources/function-nodes-13.jpg "Icono de nodo coseno")



Devuelve el coseno de su valor de entrada en radianes: <b>cos(X)</b>.

+++

+++Seno
![Icono de nodo sinusoidal](function-nodes.resources/function-nodes-14.jpg "Icono de nodo sinusoidal")



Devuelve el seno de su valor de entrada en radianes: <b>sin(X)</b>.

+++

+++Tangente
![Icono de nodo de tangente](function-nodes.resources/function-nodes-15.jpg "Icono de nodo de tangente")



Devuelve la tangente de su valor de entrada en radianes: <b>tan(X)</b>.

+++

+++Arco tangente 2
![icono de nodo de Arco tangente 2](function-nodes.resources/function-nodes-16.jpg "icono de nodo de Arco tangente 2")



Devuelve el ángulo entre el vector 2D de entrada y la horizontal.

Es el recíproco de la función <b>Cartesian</b>.

No es necesario cambiar el componente X e Y del vector de entrada como en la función <b>atan2</b> habitual.

+++

+++Cartesiano
![Icono de nodo absoluto](function-nodes.resources/function-nodes-07.jpg "Icono de nodo absoluto")



Convierte las coordenadas polares en coordenadas cartesianas.

Es el recíproco de la función <b>Arc tangent 2 </b>: <b>Longitud \* Float2(cos(Ángulo), sin(Ángulo).</b>

Las coordenadas polares son una distancia desde el origen y un ángulo en radianes desde la horizontal.

+++

+++Aleatorio
![Icono de nodo aleatorio](function-nodes.resources/function-nodes-17.jpg "Icono de nodo aleatorio")



Devuelve un valor aleatorio entre 0 y el valor de entrada <b>X</b>.

+++
