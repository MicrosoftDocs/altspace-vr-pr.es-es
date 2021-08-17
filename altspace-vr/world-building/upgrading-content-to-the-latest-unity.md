---
title: Actualización del contenido a la versión más reciente de Unity
description: Obtenga información sobre cómo actualizar el contenido a la versión más reciente de Unity.
ms.date: 06/4/2021
ms.topic: article
keywords: kits, worlds, unity, updating, shaders, uploader, troubleshooting
ms.openlocfilehash: a10e64b4dc19e256dcae9d61620de0140db60ccc0bf2a10dc864313f139bbd10
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126768"
---
# <a name="updating-content-to-the-latest-unity-version"></a>Actualización del contenido a la versión más reciente de Unity

## <a name="moving-to-unity-202039"></a>Traslado a Unity 2020.3.9

A partir de hoy, AltspaceVR se ha actualizado a una versión reciente de Unity (2020.3.9). Además de algunas mejoras de rendimiento, esta actualización nos probará en el futuro para las próximas características que nos complace incorporar. Este cambio debe ser compatible con todo el contenido existente. Si no es así, no dude en ponerse en contacto con el soporte técnico: altvr.com/support

Aunque este cambio a 2020.3.9 no ha afectado al contenido generado por el usuario, en unas semanas realizaremos un cambio en el modo de representación estéreo de AltspaceVR que requerirá que los usuarios actualicen su [contenido.]( https://docs.unity3d.com/Manual/SinglePassStereoRendering.html) Esta actualización a [la creación de instancias de paso](https://docs.unity3d.com/Manual/SinglePassInstancing.html) único permitirá importantes mejoras de rendimiento en sus mundos. Tenga en cuenta que esta nueva compilación ya no admitirá la compatibilidad con versiones anteriores con contenido de 2019.4 y versiones anteriores. Es urgente que todo el contenido propiedad del creador se actualice lo antes posible para evitar cambios importantes. Siga la guía siguiente para actualizar el contenido y garantizar una transición sin problemas a la creación de instancias de paso único en Unity 2020.3.9.

> [!NOTE]
> Si usa con regularidad contenido que es propiedad de otra persona y se ha compartido con usted, póngase en contacto con el propietario del world/kit y asegúrese de que planea actualizar su contenido.

> Si es un creador de contenido y tiene preguntas o necesita ayuda, póngase en contacto con nuestro equipo de soporte técnico para obtener ayuda: altvr.com/support

## <a name="testing-your-spi-content"></a>Prueba del contenido spi

Use las siguientes versiones preliminares de AltspaceVR para probar el contenido recién actualizado en VR. Las versiones preliminares son solo con fines de prueba y no deben usarse para un uso general de la plataforma.

* [AltspaceVR SPI Preview para Windows Mixed Reality](https://aka.ms/AvrSpiMr)
* [AltspaceVR SPI Preview para SteamVR](https://aka.ms/AvrSpiSteam)
* [AltspaceVR SPI Preview for Oculus Dimensional](https://aka.ms/AvrSpiRift)

> Nota: Solo se han proporcionado vistas previas de VR de PC. La representación con instancia de paso único no está disponible en Android y no es necesaria en plataformas que no son de realidad virtual como Mac. Por lo tanto, puede usar la versión de lanzamiento general para probar estos dispositivos.


## <a name="storecompatibilitycheck"></a>Comprobación de compatibilidad del almacén

La actualización a Unity 2020.3.9 también afectará a la compatibilidad de cascos y compilación de tienda. Ahora es un requisito que descargue AltspaceVR desde la tienda que sea compatible con el casco. Por ejemplo: para un casco de WinMR o Oculus, descargue AltspaceVR desde Windows Store o Oculus Store, respectivamente. Windows Mixed Reality usuarios deben descargar AltspaceVR desde Windows Store, los usuarios de SteamVR de Steam y los usuarios de Oculus Dimensional desde Oculus Store.

## <a name="altspacevr-uploader-v090-upgrade-guide"></a>AltspaceVR Uploader v0.9.0 Upgrade Guide 

Uploader 0.9 se empaqueta de forma diferente a las versiones anteriores del uploader. Al mismo tiempo que este cambio de empaquetado, el nuevo uploader requiere una nueva versión de Unity. Esta guía está pensada para que este proceso de actualización sea más fácil y seguro para todos los implicados.

1. **COPIA DE SEGURIDAD DEL PROYECTO:** cree una copia de todo el directorio del proyecto y pónla en algún lugar seguro. Esta actualización es una actualización destructiva, por lo que no podrá crear ni cargar paquetes para Unity 2019.4 después de completarla. Si se encuentra con algún problema durante esta actualización, necesitará una copia limpia del proyecto en la que resalte. También lo necesitará para actualizar los kits o plantillas en directo antes de que AltspaceVR se actualice oficialmente a Unity 2020.3.9.

2. **REMOVE OLD UPLOADER:** con Unity cerrado, elimine los siguientes archivos o carpetas y sus archivos .meta correspondientes:

    ```console
    * Assets/Altspace

    * Assets/Plugins

    * Assets/Prefabs/test-folder, Readme.txt

    * Assets/Resources/bg.jpeg, bg2.jpeg, logo.png, UserPreferences.asset

    * Assets/DFloor_v004.fbx

    * Library (This is a Unity system folder, not an Uploader folder. Delete it anyway, and let it be rebuilt during the upgrade.)
    ```

3. **DESCARGAR VERSIÓN DEL MOTOR:** abra Unity Hub e instale Unity 2020.3.9 (o haga [clic](https://unity3d.com/ru/unity/whats-new/2020.3.9) aquí para instalar directamente).

4. **ACTUALIZAR PROYECTO:** abra el proyecto limpio en Unity 2020.3.9 y permita que Unity actualice el proyecto.

5. (Solo PC) **DESCARGAR MIXED REALITY FEATURE TOOL:** siga las instrucciones para descargar Mixed Reality [Feature Tool,](/windows/mixed-reality/develop/unity/welcome-to-mr-feature-tool)que usará para administrar la instalación del paquete uploader.

6. **INSTALL THE UPLOADER** : use la herramienta de características de MR para seleccionar el proyecto de Unity y agregue la característica AltspaceVR Uploader (En el encabezado AltspaceVR). Siga las instrucciones de la herramienta.

En macOS, descargue manualmente la [](https://dev.azure.com/aipmr/MixedReality-Unity-Packages/_packaging?_a=package&feed=Unity-packages&package=com.microsoft.altspacevr_uploader&protocolType=Npm&version=0.9.0&view=versions)versión más reciente del Registro e instálla desde el administrador de paquetes del editor de Unity (Windows > Administrador de paquetes > + > Agregar paquete desde tarball).

Una vez que el paquete termina de importarse, la conocida ventana Uploader debe estar disponible en el elemento de menú AltspaceVR.

## <a name="troubleshooting-tips"></a>Sugerencias para la solución de problemas

1. Si tienes problemas de controlador o entrada en el casco de WinMR, asegúrate de que está situado en la cabeza para activar correctamente el sensor de presencia. Se trata de un problema conocido y Microsoft está trabajando activamente para resolverlo.

2. Compruebe la compatibilidad con los cascos y la compilación de la tienda. Si usa un casco WinMR, por ejemplo, asegúrese de que la compilación altspaceVR se adquirió a través de Windows Store.

3. Si durante las pruebas descubre que el contenido solo aparece en un ojo en modo VR, es probable que los sombreadores personalizados que use no admitan la representación SPI. Deberá elegir un sombreador diferente o seguir la guía de actualización spi de [Unity](https://docs.unity3d.com/Manual/SinglePassInstancing.html) para editar manualmente el sombreador y agregar compatibilidad.

4. Para los usuarios de WinMR, recuerde que antes de poder acceder al modo VR en AltspaceVR, debe: 
    1. Descargue e instale OpenXR para Windows Mixed Reality desde el Microsoft Store.
        1. Apertura de la Portal de realidad mixta aplicación
        2. En la esquina inferior izquierda de la aplicación, seleccione "Ver más".
        3. En el menú que aparece, seleccione Set Up OpenXR (Configurar OpenXR). Al hacerlo, se iniciará Windows Store desde donde puede instalar el entorno de ejecución. Si este elemento de menú no aparece, es posible que OpenXR ya esté instalado en el equipo.