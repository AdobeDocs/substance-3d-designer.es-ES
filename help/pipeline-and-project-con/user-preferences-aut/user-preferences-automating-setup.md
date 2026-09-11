---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/pipeline-and-project-configuration/user-preferences-automating-setup.html"
breadcrumb-title: ''
description: Aprenda a automatizar la configuración de preferencias de usuario en Substance 3D Designer para una configuración de flujo de trabajo optimizada.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > User Preferences - Automating Setup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Preferencias del usuario: Automatizar la configuración'
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---


# Preferencias del usuario: Automatizar la configuración

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

El archivo user\_preferences.xml contiene todas las opciones de configuración específicas del usuario distintas de las definidas en [Configuración del proyecto](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md). Se relacionan principalmente con la interfaz de usuario y la configuración de rendimiento específicas.

La única configuración relevante que se debe cambiar es el [archivo de configuración](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) que contiene una lista de proyectos. Esto se puede hacer de varias maneras, como se indica a continuación.

Como alternativa, puede omitir completamente la modificación de las preferencias de usuario y realizar una anulación basada en sesión del archivo SBSCFG utilizando un argumento de la línea de comandos en el método abreviado de Designer, consulte a continuación.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Icono de archivo XML](../../assets/xml-5.png "Icono de archivo XML")

</td>
</tr>
</table>

## Permanente o basada en sesión

Hay dos formas diferentes de configurar Designer para que use otro [archivo de configuración](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) distinto del predeterminado, con ventajas e inconvenientes:

* <b>Modificando el usuario de forma permanente\_preferences.xml\
  </b>Este archivo se encuentra en *~User\AppData\Local\Adobe\Adobe Substance 3D Designer* para Windows. Si lo modifica, Designer siempre utilizará lo que se haya definido allí, independientemente de cómo, cuándo o dónde lo inicie. Para realizar cambios es necesario volver a modificar el código XML, que se describen a continuación, y suelen ser bastante complicados.
* <b>Estableciendo temporalmente la sesión mediante un argumento de línea de comandos\
  </b>Designer puede tomar un argumento de línea de comandos al inicio para invalidar el archivo SBSCFG de esa sesión (vea a continuación cómo). Es una solución sencilla y elegante que permite cambiar proyectos mucho más rápido que modificando un XML. El peligro es que si abre a través de varios accesos directos (por ejemplo, Menú Inicio y Escritorio en Windows), puede tener resultados diferentes sin que sea del todo obvio. Además, no está tan protegido contra manipulaciones, ya que los usuarios pueden eliminar, mover o modificar sus métodos abreviados de teclado mucho más fácilmente que su usuario\_preferences.xml.

## Modificación de XML

### Modificación manual de preferencias

Si no hay ninguna configuración automatizada, o con fines de prueba, se puede ir manualmente a <b>Editar > Preferencias...</b> y, a continuación, haga clic en la sección &quot;<b>Proyectos</b>&quot; de la izquierda.

![Configuración del proyecto](../../assets/preferences-ui.png "Configuración del proyecto")

El botón marcado en rojo permite al usuario elegir otro [archivo SBSCFG](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md).

### Modificar mediante script

Al igual que los archivos de proyecto y configuración, las preferencias del usuario son un XML estructurado, con la configuración pertinente claramente identificable. En lugar de modificar a través de un editor de texto como el Bloc de notas++ o Sublime Text, es muy adecuado para modificar a través de una configuración de scripts externos.

La ventaja de los scripts es que el usuario no tiene que hacer nada más que hacer clic en un botón, y si se crea un sistema lo suficientemente complicado es posible administrar e intercambiar proyectos fácilmente sin necesidad de administrar archivos y configuraciones manualmente.

La línea relevante tiene este aspecto:

```
  <configuration> 

   <configurationfile>file:///C:/Users/John/AppData/Local/Adobe/Adobe Substance 3D Designer/default_configuration.sbscfg</configurationfile> 

  </configuration>
```


#### Ejemplo de Python

A continuación se muestra una simple función de ejemplo de Python 2.7 para Windows que modifica el archivo user\_preferences.xml para otro archivo de configuración. Esto altera permanentemente el valor hasta que se vuelva a cambiar. A continuación, se puede llamar a la función SetConfigurationFile con la ruta de acceso del archivo sbscfg personalizado como parámetro.

Un script Python permite un código potente y limpio, y se puede integrar fácilmente en otro lugar, pero el inconveniente es que para que un usuario lo ejecute, debe compilarse en un ejecutable o el usuario necesita una implementación de Python.

```
import xml.etree.ElementTree as ElementTree 

import os 

 

##Example Python script for changing Substance 3D Designer user preference file## 

 

def SetConfigurationFile(p_ConfigPath): 

## Check is the path passed as parameter exists.

    if(os.path.isfile(p_ConfigPath)): 

## replace backslashes by forwardslahes to ensure consistency

        p_ConfigPath = p_ConfigPath.replace("\", "/") 

## get Local Appadata path from Environment variables, construct full path to user_preferences.xml and check if it exists.

        m_AppDataPath = os.environ.get('LOCALAPPDATA') 

        if m_AppDataPath != None: 

            m_UserPrefsPath = os.path.join(m_AppDataPath, str("Adobe/Adobe Substance 3D Designer/user_preferences.xml")) 

            if(os.path.isfile(m_UserPrefsPath)): 

## read XML elementtree from file, find correct element until we get to the actual line that defines the configurationfile path

                m_PrefsTree = ElementTree.parse(m_UserPrefsPath) 

                m_PrefsRoot = m_PrefsTree.getroot() 

                m_PrefsElement = m_PrefsRoot.find("preferences") 

                m_XMLError = True 

                if(m_PrefsElement != None): 

                    m_ConfigElement = m_PrefsElement.find("configuration") 

                    if(m_ConfigElement != None): 

                        m_ConfigFileElement = m_ConfigElement.find("configurationfile") 

                        if(m_ConfigFileElement != None): 

                            m_XMLError = False 

## Check if path is already set, to avoid double work

                            if m_ConfigFileElement.text.replace("file:///","") == p_ConfigPath: 

                                print "configurationfile is already set to desired path. Aborting." 

                                return True 

                            else: 

## construct correctly formatted path, insert into elementtree

                                m_ConfigPath = str("file:///" + p_ConfigPath) 

                                m_ConfigFileElement.text = m_ConfigPath 

 

## Write to file

                                m_XMLString = str("<?xml version="1.0" encoding="UTF-8"?>n") + ElementTree.tostring(m_PrefsRoot, 'utf-8') 

                                m_File = open(m_UserPrefsPath,'w') 

                                m_File.write(m_XMLString) 

                                m_File.close() 

                                print "configuration file path succesfully changed!" 

                                return True 

                if m_XMLError: 

## if this flag was not set to false, we can assume something was missing or went wrong when walking through the XML

                    print("Error: malformed content in user_preferences.xml!") 

                    return False 

            else: 

                print "Error: user_preferences.xml does not exist, try starting Substance 3D Designer first!" 

                return False 

        else: 

            print "Error: LocalAppData path returned None" 

            return False 

    else: 

        print "Error: Invalid Configuration File path!" 

        return False
```


## Método abreviado de argumento de línea de comandos

De una manera mucho más sencilla, se le puede indicar a Designer que use un SBSCFG específico al inicio a través del argumento &quot;—config-file&quot; (opcional).

### Configuración manual

Aunque no se recomienda utilizar un método manual en un entorno de producción, para realizar pruebas, esto se puede hacer con bastante rapidez si ya ha configurado el archivo SBSCFG.

1. Añadir un espacio
1. Agregue —config-file después de la ruta al diseñador en la sección Target.
1. Añadir otro espacio
1. Agregue su ruta de acceso *entre comillas* para evitar problemas con los espacios de la ruta
1. El resultado debería ser el siguiente:

   *&quot;C:\Program Files\Adobe\Adobe Substance 3D Designer\Adobe Substance 3D Designer.exe&quot; —config-file &quot;C:\Dev\Substance\custom\_configuration.sbscfg&quot;*

![Entrada del archivo de configuración en las propiedades del archivo ejecutable](../../assets/shortcutargument.jpg "Entrada del archivo de configuración en las propiedades del archivo ejecutable")
