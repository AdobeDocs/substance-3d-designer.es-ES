---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: Acceda a la referencia completa de la API de scripts de Substance 3D Designer Python para el desarrollo de plugins.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Referencia de API de scripts
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# Referencia de API de scripts

Esta página describe los conceptos principales de la API.

Para obtener información más detallada, consulte la documentación suministrada con la aplicación a la que se puede acceder en <b>Ayuda > Documentación de la API de Python...</b>. En esta documentación, realice una <b>búsqueda rápida</b> de los nombres de los módulos (entre paréntesis) para encontrar fácilmente su definición.

## Contexto

El objeto de contexto (*Context*) es el <b>punto de entrada principal a la API</b>. Se crea la primera vez que el usuario lo obtiene mediante el método &#39;<b>*getContext()*</b>&#39; del módulo &#39;*sd*&#39;.

Este objeto permite esencialmente <b>recuperar el objeto application</b> (*SDApplication*).

## Aplicación (SDApplication)

La aplicación (*SDApplication*) es el objeto que permite <b>acceso a los principales administradores de API</b>, como:

* el <b>Administrador del paquete </b>(*SDPackageMgr*) que administra todos los <b>paquetes</b> de la aplicación;
* el <b>Administrador del módulo </b>(*SDModuleMgr*) que administra todos los <b>módulos</b> de la aplicación;
* el <b>Administrador de </b>IU (*SDUIMgr*) que puede crear <b>menús y muelles</b> en la ventana de la aplicación.

Puede registrar <b>devoluciones de llamada</b> con la aplicación a la que se llamará cuando se produzcan ciertos eventos.

## Administrador de paquetes (SDPackageMgr)

Este objeto administra todos los <b>paquetes</b> de la aplicación. Los paquetes se muestran en el componente &#39;<b>*Explorer*</b>&#39;.

Esto le permite:

* <b>crear</b> un nuevo paquete;
* <b>cargar/descargar</b> un paquete;
* <b>guardar</b> un paquete;
* <b>buscar</b> un paquete.

## Paquete (SDPackage)

Un paquete (*SDPackage*) es una <b>colección de recursos</b> (*SDResource*).

El contenido de un paquete se puede <b>almacenar</b> en un archivo con la extensión <b>.sbs</b> mediante el objeto &#39;*SDPackageMgr*&#39;. Este objeto permite <b>recuperar </b>recursos específicos.

Para <b>crear</b> un recurso específico, vea los métodos estáticos de objeto relacionados (p. ej.: &#39;*SDSBSCompGraph.sNew()*&#39;).

Un paquete también contiene un diccionario de metadatos (SDMetadataDict). Puede encontrar más información sobre los metadatos [aquí](../../package-metadata/package-metadata.md).

## Recurso (SDResource)

Un recurso (*SDResource*) es un objeto al que otro recurso puede <b>hacer referencia</b>.

Hay varios recursos <b>tipos</b>:

* Carpetas (*SDResourceFolder*);
* Gráficos (*SDGraph*);
* Bitmaps (*SDResourceBitmap*);
* Imágenes de SVG (*SDResourceSVG*);
* Fuentes (*SDResourceFont*);
* Escenas (*SDResourceScene*);
* Medidas BSDF (*SDResourceBSDFMeasurement*);
* Perfiles ligeros (*SDResourceLightProfile*).

Se puede <b>crear</b> un recurso a partir del método estático &#39;*sNew()*&#39; en:

* un bulto;
* una carpeta.

Un recurso puede tener varias <b>propiedades</b> (*SDProperty*).

## Administrador de IU (SDUIMgr)

El administrador de interfaz de usuario permite <b>crear elementos de interfaz de usuario</b> en la ventana principal de Substance Designer, como <b>menus</b>, <b>docks</b> y permite registrar <b>devoluciones de llamada</b> cuando se producen eventos relacionados con la interfaz de usuario.

Además, el administrador de IU tiene acceso al <b>gráfico activo actual</b> y a la <b>selección</b> del gráfico activo.

## Gráficos (SDGraph)

Un gráfico (*SDGraph*) es un objeto que contiene:

* <b>nodos </b>(*SDNode*);
* <b>objetos de gráfico</b> (*SDGraphObjects*);
* <b>propiedades </b>(*SDProperty*).

Hay 4 tipos de gráficas diferentes:

* Gráfico del Substance (*SDSBSCompGraph*)
* Gráfico de funciones del Substance (*SDSBSFunctionGraph*)
* Gráfico de Substance FXMap (*SDSBSFxMapGraph*)

Un gráfico puede tener uno o varios nodos <b>output</b>. Los nodos de salida representan los <b>resultados</b> del gráfico.

Se pueden <b>recuperar</b> todos los nodos disponibles para un gráfico con el método &#39;*getNodeDefinitions()*&#39;.

Se puede <b>crear</b> un nuevo nodo con el método &#39;*newNode()*&#39;.

Se puede crear un nuevo nodo <b>instance</b> a partir de un recurso (*SDResource*) con el método &#39;*newInstanceNode()*&#39;.

## Nodo (SDNode)

Un nodo (*SDNode*) representa una <b>operación</b> realizada en un objeto.

Se puede crear a partir de:

* una <b>definición</b> (*SDDefinition*) (consulte &#39;*SDGraph.newNode()&#39;*);
* un <b>recurso</b> (*SDResource*) (consulte &#39;*SDGraph.newInstanceNode()&#39;*).

Un nodo puede tener varias <b>propiedades</b>.

Hay varios <b>tipos</b> de nodo:

* *<b>SDSBSCompNode</b>*: Un nodo del Gráfico de Substance (*SDSBSCompGraph*);
* *<b>SDSBSFunctionNode</b>*: Un nodo del Gráfico de función de Substance (*SDSBSFunctionGraph*);
* *<b>SDSBSFxMapNode</b>*: Un nodo del Substance FXMap Graph (*SDSBSFxMapGraph*);

## Objetos de gráficos (SDGraphObjects)

Un objeto de gráfico (*SDGraphObject*) es un objeto que <b>agrega información adicional</b> al gráfico, pero que <b>*no* se tiene en cuenta</b> durante el proceso de evaluación del gráfico.

Hay <b>3 tipos</b> de objetos gráficos:

* <b>Pin</b> (*SDGraphObjectPin*)
* <b>Comentario</b> (*SDGraphObjectComment*)
* <b>Marco</b> (*SDGraphObjectFrame*)

Consulte el método estático &#39;*sNew()*&#39; en estos objetos para obtener más información sobre cómo <b>crearlos</b>.

## Propiedades (SDProperty)

Una propiedad (*SDProperty*) es un objeto que <b>describe</b> una propiedad de <b>otro objeto</b> (un gráfico, un nodo, un recurso, etc.).

Pertenece a una <b>categoría</b> específica (*SDPropertyCategory*):

* <b>Entrada</b>: clasifica las propiedades de entrada de un objeto, que normalmente <b> afectan a la operación </b> realizada por el objeto actual;
  * Por ejemplo: la propiedad &#39;*color*&#39; de un nodo de Color uniforme en un gráfico de Substance es una propiedad de entrada;
* <b>Salida</b>: clasifica las propiedades de salida de un objeto. Se utiliza para identificar un <b>resultado</b> de un objeto;
* <b>Anotación</b>: clasifica las propiedades que <b>*no* afectan a la operación</b> realizada por un objeto;
  * Por ejemplo: la &#39;*etiqueta*&#39; de un gráfico es una propiedad de anotación porque no afecta al cálculo del gráfico.

Contiene los siguientes <b>miembros</b>:

* <b>Id</b>: El identificador de los bienes en el contexto de esta categoría;
* <b>Tipos</b>: Los tipos admitidos por la propiedad actual. Algunas propiedades pueden admitir *varios* tipos: &#39;*int*&#39;, &#39;*float*&#39;, etc.;
  * Por ejemplo: las propiedades de entrada de un nodo &#39;*sbs::function::add*&#39; pueden admitir diferentes tipos: &#39;*int&#39;*, &#39;*int2&#39;*, &#39;*int3&#39;*, &#39;*int4&#39;*, &#39;*float&#39;*, &#39;*float2&#39;*, &#39;*float3&#39;*, &#39;*float4&#39;, etc.;*
* <b>Categoría</b>: La categoría a la que pertenece la propiedad (entrada, salida, anotación);
* <b>Etiqueta</b>: La etiqueta de la propiedad, utilizada para mostrar *only*;
* <b>Descripción</b>: La descripción de la propiedad;
* <b>ValorPredeterminado</b>: El valor predeterminado;
* <b>EsConectable</b>: Indica si se puede *realizar una conexión (* SDConnection *) en esta propiedad;*
* <b>isReadyOnly</b>: Indica si la propiedad es de sólo lectura. Si es true, el valor asociado *no* se puede modificar;
* <b>isVariadic</b>: Si es true, esta propiedad se representará como *varias* propiedades en el objeto;
* <b>isPrimary</b>: Indica si la propiedad especificada es la propiedad *principal* que controla otras propiedades. *Nota:* esto es específico para el Substance *Composición* nodos (*SDSBSCompNode*).

Ejemplos:

* Propiedades del nodo &#39;*sbs::compositing::input*&#39;:

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::entrada</th></tr><tr><td style="text-align: left;"><strong>Entrada</strong></td><td style="text-align: left;"><strong>Anotación</strong></td><td style="text-align: left;"><strong>Salida</strong></td></tr><tr><td>$outputsize</td><td>etiqueta</td><td><p>unique_filter_output (CONECTABLE)</p></td></tr><tr><td>$format</td><td>descripción</td><td><br/></td></tr><tr><td>$pixelsize</td><td>identificador</td><td><br/></td></tr><tr><td>$pixelratio</td><td>userdata</td><td><br/></td></tr><tr><td>$mosaico</td><td>grupo</td><td><br/></td></tr><tr><td>$aleatorio</td><td>visible si</td><td><br/></td></tr><tr><td><p>bitmapresourcepath</p></td><td>usos</td><td><br/></td></tr></tbody></table>

* Propiedades del nodo &#39;*sbs::compositing::blend*&#39;:

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::blend</th></tr><tr><td style="text-align: left;"><strong>Entrada</strong></td><td style="text-align: left;"><strong>Anotación</strong></td><td style="text-align: left;"><strong>Salida</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output (CONECTABLE)</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelratio</td><td><br/></td><td><br/></td></tr><tr><td>$mosaico</td><td><br/></td><td><br/></td></tr><tr><td>$aleatorio</td><td><br/></td><td><br/></td></tr><tr><td>source.connector (CONECTABLE)</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.connector (CONECTABLE)</p></td><td><br/></td><td><br/></td></tr><tr><td>opacity.connector (CONECTABLE)</td><td><br/></td><td><br/></td></tr><tr><td>opacitimulto</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">blendingmode</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">mezcla de colores</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">maskrectangle</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## Tipo (SDType)

Un tipo (*SDType*) contiene información de un valor <b>type</b>, como:

* <b>Id</b>: El identificador del tipo;
* <b>Modificador</b>: El modificador de tipo que puede ser uno de los valores <b>enum</b> de &#39;*SDTypeModifier&#39;*&#39;:
  * *Automático*;
  * *Uniforme*: El valor se evalúa *una vez* por operación;
  * *Variación*: El valor se evalúa *varias veces* por operación (por ejemplo: para cada texel).

Se definen varios tipos, como:

* <b>enumeraciones</b> (*SDTypeEnum*): describe un tipo <b>enumeration</b> con todas sus propiedades;
* <b>estructuras</b> (*SDTypeStruct*): describe un tipo <b>structure</b> con todas sus propiedades;
* <b>matriz</b> (*SDTypeArray*): describe una <b>matriz</b>.
* etc.

Consulte la *Documentación de la API de Python* del Substance Designer para obtener una lista exhaustiva.

## Valores (SDValue)

Un valor (*SDValue*) es un objeto que <b>encapsula</b> un valor de *tipo base*.

Por ejemplo:

* un objeto &#39;<b>*SDValueInt*</b>&#39; encapsula un valor &#39;*int*&#39;;
* un objeto &#39;<b>*SDValueFloat4*</b>&#39; encapsula un valor &#39;*float4*&#39;;
* etc.

El valor del tipo base normalmente se puede <b>recuperar</b> con el método &#39;<b>get()</b>&#39;, pero esto puede depender del *tipo* de &#39;*SDValue&#39;* que se haya devuelto.

## Conexión (SDConnection)

Una conexión (*SDConnection*) representa un <b>vínculo</b> entre dos propiedades<b> diferentes</b> de dos <b>nodos</b> diferentes.

Contiene:

* El <b>nodo de destino</b>;
* La <b>propiedad de destino</b> del nodo de destino;

Todas las <b>operaciones de conexión</b> se llevan a cabo en un nodo:

* <b>creando</b> una nueva conexión, consulte &#39;*SDNode.newPropertyConnection()*&#39;
* <b>eliminando</b> una conexión existente, consulte &#39;*SDNode.deletePropertyConnection()*&#39;
* <b>Recuperando</b> las conexiones de una propiedad, consulte &#39;*SDNode.getPropertyConnections()*&#39;

## Módulo (SDModule)

Un módulo es una <b>colección de definiciones y tipos</b>.

Permite recuperar fácilmente toda la información sobre los nodos que se pueden crear, así como sobre enumeraciones y estructuras.

Contiene:

* un <b>identificador</b> (*Id*) que es único en el contexto del administrador de módulos (*SDModuleMgr*);
* una lista de <b>definiciones</b> (*SDDefinition*);
* una lista de <b>tipos</b> (*SDType*).

## Definición (Definición SD)

Un objeto de definición (*SDDefinition*) contiene información sobre la definición de un <b>objeto</b> determinado basado en <b>propiedades</b> (&#39;*SDNode&#39;*, etc.).

Contiene:

* <b>Id</b>: el identificador de la definición;
* <b>Etiqueta</b>: La etiqueta de la definición;
* <b>Descripción</b>: La descripción de la definición;
* <b>Propiedades</b>: Las propiedades de todas las propiedades disponibles *categorías* (*SDPropertyCategory*).
