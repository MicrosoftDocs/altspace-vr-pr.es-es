---
title: Actualización de proyectos antiguos de Unity
description: Aprenda a actualizar el contenido a la versión más reciente de Unity.
ms.date: 10/19/2021
ms.topic: article
keywords: kits, mundos, unity, actualización, sombreadores, uploader, solución de problemas
ms.openlocfilehash: 06af70164e5bf870a10bf1ee9e949e09dfa69fd2
ms.sourcegitcommit: 8c58f9f9ad1a3f9534141dee2c78e32792d0db7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2021
ms.locfileid: "130302409"
---
<a name="upgrading-old-unity-projects"></a>Actualización de proyectos antiguos de Unity
=============================

A lo largo de los años, AltspaceVR ha experimentado varias actualizaciones poco frecuentes que requieren que los usuarios cambien su contenido. Si ve que una plantilla o kit que ha cargado en el pasado no es accesible en la versión más reciente de AltspaceVR, siga esta guía para volver a ejecutar el contenido.

> [!NOTE]
> Antes de seguir los pasos de esta guía, debe crear una copia de seguridad completa del proyecto en caso de que la actualización no se realice sin problemas. La manera más sencilla es crear una segunda copia de toda la carpeta del proyecto. Para obtener una solución más avanzada, considere la posibilidad de usar un sistema de control de versiones como Git y GitHub.

<a name="overview"></a>Información general
---------

En el momento de redactar este artículo, la versión actual de AltspaceVR usa la configuración siguiente:

* Motor de juegos: Unity 2020.3.18f1 (también aceptable: Unity 2020.3.9f1)
* Upload Herramienta: Uploader 2.2
* Representación: Canalización de representación universal (URP)
* Modo estéreo: Single-Pass de creación de instancias (SPI) o multivista en la misión

Si la versión de Unity del proyecto es anterior a la 2020.3, probablemente deba realizar todas estas actualizaciones a la vez, así que siga esta guía desde el principio. Si ya está en Unity 2020.3, pero con Uploader 0.9, comience desde el paso 6.

1. **COPIA DE SEGURIDAD DEL PROYECTO:** cree una copia de todo el directorio del proyecto y pónla en un lugar seguro. Esta actualización es una actualización destructiva, por lo que perderá los archivos de proyecto originales después de completarla.
    Si encuentra algún problema durante esta actualización, necesitará una copia limpia del proyecto para volver a usar.

2. **REMOVE OLD UPLOADER:** realice este paso si el proyecto usa AltspaceVR Uploader 0.8 o una versión anterior. Con Unity cerrado, elimine los siguientes archivos o carpetas y sus archivos .meta correspondientes. Si el archivo o la carpeta no existen, simplemente omita el archivo.

    * Assets/Altspace
    * Recursos/complementos
    * Assets/Prefabs/test-folder
    * Assets/Prefabs/Readme.txt
    * Assets/Resources/bg.jpeg
    * Assets/Resources/bg2.jpeg
    * Recursos/Recursos/logo.png
    * Assets/Resources/UserPreferences.asset
    * Assets/DFloor_v004.fbx

3. **QUITAR RECURSOS PROCESADOS:** realice este paso si va a actualizar a una nueva versión de Unity. Con Unity cerrado, elimine la carpeta Biblioteca del proyecto. Se trata de una carpeta del sistema de Unity que contiene archivos y recursos específicos del motor que se generan automáticamente a partir del contenido de la carpeta Assets (entre otras cosas).

4. **DESCARGAR VERSIÓN DEL MOTOR:** realice este paso si va a actualizar a una nueva versión de Unity. Abra el centro de Unity e instale Unity 2020.3.18f1 desde el archivo de descarga (vínculo a la instalación[del motor).](unityhub://2020.3.18f1/a7d1c678663c)
    * Si se compila en un Windows, active las casillas compatibilidad con la compilación de Android y Mac.
    * Si se compila en un equipo Mac, active las casillas android y Windows build support (Compatibilidad con la compilación).

5. **ACTUALIZAR PROYECTO:** abra el proyecto limpio en Unity 2020.3.18f1 y permita que Unity actualice el proyecto.
    Esto puede tardar algún tiempo.

6. **DOWNLOAD THE UPLOADER:** descargue la versión más reciente del uploader [aquí](https://aka.ms/AvrUrpUploader)y guárdelo en la carpeta Packages del proyecto. Este archivo debe tener una extensión de archivo ".tgz".
    > [!NOTE]
    > Si usa el explorador Safari para descargarlo, se extraerá automáticamente en un archivo ".tar", que Unity no puede usar. Puede usar un explorador diferente para descargar o usar la utilidad del sistema "gzip" para volver a comprimirlo.
    
7. **INSTALL THE UPLOADER** : instale uploader desde el administrador de paquetes del editor de Unity:
    1. Abra la ventana Administrador de paquetes Unity: Windows > Administrador de paquetes
    2. En la parte superior izquierda de la ventana, haga clic en el icono "+" y seleccione "Agregar paquete desde tarball".
    3. Seleccione el archivo tgz que descargó en el último paso.
    4. Espere a que Unity desempaquete el paquete.

8. **ABRIR EL CARGUEDOR:** si la instalación se ha realizado correctamente, habrá un menú "AltspaceVR" disponible en la barra superior.
    Este menú contiene ventanas independientes para kits y plantillas. Abra el más adecuado para el proyecto.
    La primera vez que se abra la ventana, configurará los valores del proyecto para que coincidan con el cliente de juego de Altspace: habilitar la canalización de representación universal y Single-Pass creación de instancias

9. **CORREGIR SOMBREADORES:** mientras se ejecuta la configuración por primera vez, puede aparecer temporalmente una ventana de PowerShell.
    Es posible que se le pida que actualice algunos de los sombreadores personalizados o descargados. Si aprueba el mensaje, el script de PowerShell intentará actualizar los sombreadores automáticamente, pero las probabilidades de éxito son bajas. Deberá comprobar manualmente si el sombreador sigue funcionando correctamente en URP.

10. **CORRECCIÓN DE** MATERIALES: algunos o todos los materiales se pueden convertir en color rojo/rojo durante el proceso de actualización. Esto indica un error en el sombreador utilizado por ese material. Si usó los sombreadores integrados de Unity, normalmente puede migrarlos automáticamente a sombreadores compatibles con URP desde el menú: Editar canalización de representación > > Canalización de representación universal > Actualizar materiales Project materiales a materiales universales de UniversalRP.

11. **COMPILACIÓN Y CARGA:** en este momento, el proyecto debe actualizarse por completo. Siga las instrucciones de la guía [de Tareas iniciales](world-building-toolkit-getting-started.md) para compilar y cargar el kit o plantilla.

<a name="troubleshooting-tips"></a>Sugerencias para la solución de problemas
---------------------

1. Si detecta que el contenido solo aparece en un ojo en modo VR, es probable que los sombreadores personalizados que use no admitan la representación SPI. Deberá elegir otro sombreador o seguir la guía de actualización [de SPI](https://docs.unity3d.com/Manual/SinglePassInstancing.html) de Unity para editar manualmente el sombreador y agregar compatibilidad.

2. Si descubre que parte del contenido es de color rojo o rojo-rojo en el juego o es totalmente invisible, esto puede deberse a que un sombreador no es compatible con URP. Deberá reemplazar el sombreador o actualizarlo usted mismo.