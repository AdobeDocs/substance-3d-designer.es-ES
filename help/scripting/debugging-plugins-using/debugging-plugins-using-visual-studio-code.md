---
helpx_url: "https://helpx.adobe.com/es/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: Obtenga información sobre cómo depurar complementos de Substance 3D Designer Python mediante Visual Studio Code para un desarrollo eficaz.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Depurar complementos mediante código de Visual Studio
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Depurar complementos mediante código de Visual Studio

Como estándar de flujo de trabajo para muchos desarrolladores, el **IDE de código de Visual Studio** está disponible para depurar complementos de Python.

>[!WARNING]
>
> El método <b>debugpy.listen()</b> puede permitir que cualquier persona que pueda conectarse al puerto especificado ejecute código arbitrario dentro del proceso depurado.
> 
> Por lo tanto, la depuración debe *<b>sólo</b>* configurarse y realizarse en *redes seguras*.

Para configurar la sinergia entre Visual Studio Code y Substance 3D Designer, siga estos pasos:

1. Instale **[Visual Studio Code](https://code.visualstudio.com/)** y la **[extensión de Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**.
1. Instale el **[módulo Python de depuración](https://github.com/microsoft/debugpy)**.

   >[!NOTE]
   >
   > Asegúrese de que el intérprete de Python en Designer pueda encontrar el módulo &#39;*debugpy*&#39;. La forma más sencilla de hacerlo es agregar el directorio donde se encuentra el módulo &#39;*debug*&#39; a la variable de entorno **PYTHONPATH**. Una alternativa podría ser modificar sys.path en el script para agregar la ruta de acceso al módulo de depuración.
1. Inicie la aplicación, abra el Editor de Python y **ejecute el siguiente código**:

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. En Visual Studio Code, abra el proyecto y cree un archivo **launch.json**. Añada lo siguiente al archivo:

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. Haga clic en el icono <b>Debug</b> y, si es necesario, cree o edite la configuración del depurador.
1. Seleccione **Python: Adjunte a la configuración de Designer** y haga clic en **Iniciar depuración**.

   Ahora debería poder establecer puntos de interrupción, recorrer paso a paso el código y utilizar todas las demás características del depurador de código de Visual Studio.
