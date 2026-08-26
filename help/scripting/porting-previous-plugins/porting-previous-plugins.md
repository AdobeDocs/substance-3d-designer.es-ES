---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: Obtenga información sobre cómo trasladar complementos de versiones anteriores de Substance Designer a la API de Python actual.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasladar plugins anteriores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Trasladar plugins anteriores

Debido a los cambios realizados para admitir Qt en Python, **los complementos anteriores ya no funcionarán**.\
En particular, tenga en cuenta lo siguiente:

## Carga y descarga de complementos

Los complementos se cargan ahora cuando se inicia <b>la aplicación</b> y se descargan cuando <b>se cierra</b>.\
Por lo tanto, *ya no es necesario* que los complementos hereden de &#39;*sdplugins.Plugin*&#39;.

Para obtener más información, consulte la sección [Conceptos básicos del complemento](../../scripting/plugin-basics/plugin-basics.md).

## Creación de elementos de interfaz de usuario

Los complementos *ya no necesitan* para definir &#39;*sdplugins.PluginDesc*&#39;.\
En su lugar, los complementos pueden usar el <b>nuevo objeto [administrador de IU](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)</b> y <b>Qt para Python</b> para crear cualquier elemento de interfaz de usuario que necesiten.

Encontrará pequeños ejemplos de código en la sección [Creación de elementos de interfaz de usuario](../../scripting/creating-user-interface/creating-user-interface-elements.md).

## Reemplazar usos del contexto de ubicación

La clase &#39;*SDLocationContext*&#39; se ha *quitado* de la API de Python.\
Los complementos pueden usar el objeto <b>[UI manager](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)</b> para tener acceso al gráfico y a la selección activos actualmente.

Puede encontrar algunos ejemplos en la sección [Acceso a gráficos y selecciones](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md).
