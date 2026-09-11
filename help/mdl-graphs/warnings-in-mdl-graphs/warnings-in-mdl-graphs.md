---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/warnings-in-mdl-graphs.html"
breadcrumb-title: ''
description: Comprende y resuelve las advertencias en los gráficos MDL para garantizar una definición y representación adecuadas del material.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Warnings in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Advertencias en gráficos MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---


# Advertencias en gráficos MDL

Esta página muestra mensajes de advertencias y errores que pueden activarse mediante gráficos MDL en [Substance 3D Designer](https://www.adobe.com/es/products/substance3d-designer.html), y ofrece pasos comunes de solución de problemas para cada uno.

Las advertencias se muestran en la información sobre herramientas del icono de advertencia para el recurso de gráfico en el panel [Explorador](../../interface/the-explorer-window/the-explorer-window.md), así como en la esquina inferior izquierda de la [vista de gráfico](../../interface/the-graph-view/the-graph-view.md) si el gráfico está cargado.

>[!NOTE]
>
> Las ilustraciones de esta sección se registraron en <b>gráficos de modelos de Substance</b>, que se *retiraron* en la versión <b>13.0.0</b> de Substance 3D Designer. Sin embargo, también se aplican a los gráficos MDL.

## ![(error)](../../assets/error.svg) No se ha definido ningún nodo de salida

El gráfico no tiene definido ningún nodo de salida.

<b>![(tick)](../../assets/check.svg) Solución</b>

Seleccione cualquier nodo del gráfico que genere un valor cuyo tipo coincida con el tipo esperado para esta función, si lo hubiera, y luego haga clic en RMB y seleccione la opción <b>Establecer como raíz</b> en el menú contextual o haga doble clic en LMB en el nodo.\
El nodo de salida de un gráfico de modelo de Substance tiene el color *naranja*.

![&#39;Solución no definida de nodo de salida&#39;](../../assets/warnings-model-output.gif "&#39;Solución no definida de nodo de salida&#39;")

### ![(error)](../../assets/error.svg) Se rechazó al menos un valor de entrada

El valor proporcionado para un parámetro no genera un cálculo válido del nodo.

<b>![(tick)](../../assets/check.svg) Solución</b>

Ajuste el valor para que tenga sentido para el parámetro de destino.

![&#39;Se rechazó al menos un valor de entrada&#39; solución](../../assets/warnings-model-rejected-value.gif "&#39;Se rechazó al menos un valor de entrada&#39; solución")

### ![(error)](../../assets/error.svg) No hay valor de entrada

No se proporciona un valor de entrada esperado por un nodo para realizar su cálculo.

<b>![(tick)](../../assets/check.svg) Solución</b>

Algunos parámetros de nodo no pueden recaer en un valor predeterminado cuando no se proporcionan datos a su conector de entrada. A menudo, este es el caso de las entradas de escena.

Conecte las entradas de nodo al conector de salida de otro nodo de tipo coincidente.

![&#39;Solución sin valor de entrada&#39;](../../assets/warnings-model-no-input-value.gif "&#39;Solución sin valor de entrada&#39;")

### ![(error)](../../assets/error.svg) No se calculó el nodo

La información proporcionada al nodo está incompleta o no es válida, por lo que el nodo no pudo realizar sus cálculos.

<b>![(tick)](../../assets/check.svg) Solución</b>

Suba al gráfico y compruebe si hay advertencias desencadenadas por problemas que impiden que los nodos proporcionen una salida válida.

![&#39;No se calculó el nodo&#39; solución](../../assets/warnings-model-no-input-value.gif "&#39;No se calculó el nodo&#39; solución")

### ![(error)](../../assets/error.svg) Los datos a los que se hace referencia tienen algunas advertencias

El recurso al que hace referencia un nodo tiene una o más advertencias. Estos son algunos nodos que hacen referencia a un recurso:

* Un nodo de instancia de gráfico hace referencia a un gráfico
* Un nodo de recursos de escena hace referencia a un recurso de escena 3D de mapa de bits

<b>![(tick)](../../assets/check.svg) Solución</b>

En el panel Explorador, busque el recurso al que se hace referencia y solucione todas las advertencias que provoca el recurso:

* Para gráficos, consulte otros elementos de esta página
* Para cualquier otro tipo de recurso, consulte la página Advertencias de dependencias

![&#39;Los datos a los que se hace referencia tienen algunas advertencias&#39; solución](../../assets/warnings-model-referenced-data.gif "&#39;Los datos a los que se hace referencia tienen algunas advertencias&#39; solución")

### ![(error)](../../assets/error.svg) Recurso de referencia no encontrado

No se encontró el recurso al que hace referencia un nodo en la ruta guardada en el archivo Substance 3D (SBS). Estos son algunos nodos que hacen referencia a un recurso:

* Un nodo de instancia de gráfico hace referencia a un gráfico
* Un nodo de recursos de escena hace referencia a un recurso de escena 3D de mapa de bits

<b>![(tick)](../../assets/check.svg) Solución</b>

Para nodos de instancia de gráfico

Compruebe que el gráfico de origen existe en el paquete ubicado en la ruta guardada en su atributo <b>Package</b>.\
Si no es así, elimine el nodo de instancia y sustitúyalo por un nodo de instancia que haga referencia a un paquete válido. Como alternativa, puede volver a crear el paquete y el gráfico al que hace referencia el nodo de la instancia y luego volver a cargar el paquete host haciendo clic en *RMB* en él en el panel [Explorador](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion) y seleccionando la opción <b>Volver a cargar</b> en el menú contextual.

Para nodos de recursos de escena

Busque los recursos a los que se hace referencia en el panel [Explorador](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion) y compruebe que existen en la ubicación guardada en su atributo <b>Ruta de archivo</b>.\
Si no es así, haz clic en *RMB* en el elemento de recurso en el Explorador y selecciona <b>Reubicar...Opción </b> en el menú contextual para establecer un nuevo archivo de destino válido para ese recurso.

![&#39;Recurso de referencia no encontrado&#39; solución](../../assets/warnings-model-referenced-resource.gif "&#39;Recurso de referencia no encontrado&#39; solución")

### ![(error)](../../assets/error.svg) El intervalo de software no contiene el valor

El valor por defecto de un parámetro expuesto no se incluye en el rango flexible definido para dicho parámetro.

<b>![(tick)](../../assets/check.svg) Solución</b>

Ajuste el valor por defecto o el rango flexible para que el primero se incluya en el segundo.

>[!NOTE]
>
> Esta advertencia no se puede desencadenar a través de la interfaz de usuario, ya que *ajusta automáticamente* el intervalo flexible para incluir el valor predeterminado. Solo modificar los datos del archivo Substance 3D (SBS) *directamente* puede provocar esta advertencia.

El intervalo flexible de ![ no contiene la solución de valor &#39;](../../assets/warnings-model-ranges.gif "&#39; El intervalo flexible no contiene la solución de valor &#39;")

### ![(error)](../../assets/error.svg) El intervalo de software está fuera del intervalo de hardware

El rango flexible de los parámetros expuestos y no está totalmente incluido en el rango definido para ese parámetro.

<b>![(tick)](../../assets/check.svg) Solución</b>

Ajuste el rango suave o el rango duro para que el primero se incluya por completo en el segundo.

>[!NOTE]
>
> Esta advertencia no se puede desencadenar a través de la interfaz de usuario, ya que *ajusta automáticamente* el rango flexible para que se incluya completamente en el rango duro. Solo modificar los datos del archivo Substance 3D (SBS) *directamente* puede provocar esta advertencia.

![&#39;El intervalo suave está fuera del intervalo duro&#39; solución](../../assets/warnings-model-ranges.gif "&#39;El intervalo suave está fuera del intervalo duro&#39; solución")

### ![(error)](../../assets/error.svg) El valor está fuera del intervalo de hardware

El valor predeterminado de un parámetro expuesto no se incluye en el intervalo definido para ese parámetro.

<b>![(tick)](../../assets/check.svg) Solución</b>

Ajuste el valor predeterminado o el intervalo de hardware para que el primero se incluya en el segundo.

>[!NOTE]
>
> Esta advertencia no se puede desencadenar a través de la interfaz de usuario, ya que *ajusta automáticamente* el valor predeterminado que se va a incluir en el intervalo de hardware. Solo modificar los datos del archivo Substance 3D (SBS) *directamente* puede provocar esta advertencia.

![&#39;El valor está fuera del rango duro&#39; solución](../../assets/warnings-model-ranges.gif "&#39;El valor está fuera del rango duro&#39; solución")
