---
title: Introducción al uploader de Altspace
description: Aprenda a configurar y cargar sus mundos AltspaceVR mediante plantillas de escena de Unity con altspace Uploader.
ms.date: 09/29/2021
ms.author: v-vtieto
ms.topic: article
keywords: toolkit, Altspace, uploader
ms.openlocfilehash: 8d71551fe552159c0078105307802774f44c0d47
ms.sourcegitcommit: 8c58f9f9ad1a3f9534141dee2c78e32792d0db7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2021
ms.locfileid: "130298839"
---
# <a name="introducing-the-altspace-uploader"></a>Introducción al uploader de Altspace

> [!NOTE]
> - Si está interesado, únase al canal oficial [AltspaceVR Discord](https://discordapp.com/invite/altspacevr) y visite el canal #world creación.  
> - Si está intentando recuperar un espacio antiguo, consulte la guía [de actualización](upgrading-old-unity-projects.md). 

El uploader le permite usar una escena de Unity como plantilla para sus mundos. Puede traer una casa de Campoo o su creación favorita desde Minecraft. Si puede importarlo en Unity, probablemente pueda acceder a Altspace de esta manera. Estos son algunos ejemplos [de Worlds.](https://account.altvr.com/worlds/1046572460192825569)

![Mundos de ejemplo](images/unity-uploader-img-01.png)

## <a name="setup"></a>Configurar

1. Únase al [espacio oficial Desacepto de AltspaceVR](https://discordapp.com/invite/altspacevr) y visite el canal #world creación. Los amigos no permiten que los amigos compilen mundos por sí solos.
2. Lea nuestra [guía de Tareas iniciales world-building](world-building-getting-started.md) para ver los aspectos básicos.
3. [Instale Unity Hub](https://unity3d.com/get-unity/download) y **Unity 2020.3.9.** El uploader no funcionará a menos que coincida exactamente con esta versión. Necesitará una cuenta gratuita de Unity si no tiene una. Durante la instalación, elija la **versión personal** (ya que lo está haciendo para disfrutar) y asegúrese de hacer lo siguiente:
    * Incluya el **módulo Compatibilidad con compilación de Android.**
    * En Windows, incluya el **módulo Compatibilidad con compilación de Mac (Mono).**
    * En Mac, incluya el **módulo Windows build support (Mono) (Compatibilidad con la compilación** de compilación [Mono]).
4. [Descarga del carguedor AltspaceVR](https://aka.ms/AvrUrpUploader)
5. [Cree una plantilla en](https://account.altvr.com/space_templates/new) nuestro sitio web. Así **mismo, Hola mundo plantilla**.
6. [Cree un mundo](https://account.altvr.com/worlds/my) y asíéeno **Hola mundo**. Seleccione **Hola mundo plantilla como** plantilla.

![Pantalla del mundo creado](images/unity-uploader-img-02.png)

## <a name="upload-your-scene"></a>Upload la escena

> [!NOTE]
> Puede encontrar una guía paso a paso más detallada [aquí.](https://buildingthemetaverse.medium.com/how-to-make-your-own-altspace-templates-and-kits-unity-2020-3-9-uploader-2-x-5b40e92bb759)

1. Abra Unity Hub y cree un nuevo proyecto de Unity 2020.3.9. Para la plantilla, seleccione **Canalización de representación universal.**

    ![Elección de la plantilla de Unity de URP](images/001-unity-templates.png)

1. Vaya a la carpeta en la que descargó altspace Uploader y, a continuación, cópiela o muévela de esa carpeta a la carpeta raíz del nuevo proyecto de Unity.
1. En Unity, en la barra de menús, **seleccione Ventana**  >  **Administrador de paquetes.**
1. En la Administrador de paquetes menú desplegable, seleccione el signo más desplegable ("+") y, a continuación, seleccione **Agregar paquete desde tarball**.
1. Vaya a la carpeta que contiene altspace Uploader, seleccione uploader y, a continuación, haga clic **en Abrir.**  Una vez cargado el paquete, **AltspaceVR** aparece en la barra de menús:

    ![AltspaceVR en la barra de menús](images/002-altspacevr-on-menu-bar.png)

> [!NOTE]
> Deberá importar el paquete Altspace Uploader en todos los proyectos de Unity que quiera usar con Altspace.
1. En la barra de menús, **seleccione AltspaceVR > templates**.
1. En el cuadro **de diálogo Altspace VR Templates (Plantillas de ALTSPACE VR),** inicie sesión con las credenciales de la cuenta de Altspace. (El inicio de sesión de MSA estará disponible pronto. Si solo ha iniciado sesión en Altspace con su cuenta Microsoft, deberá crear una contraseña con la opción "Olvidó su contraseña" en el sitio web).
1. Haga clic **en la lista desplegable Seleccionar** una plantilla y, a continuación, seleccione Hola mundo **plantilla.**
1. Elija una escena: haga clic en el botón de puntos suspensivos Choose a .unity file (Elegir un archivo **.unity)** (tres puntos), vaya a la carpeta **Assets** Scenes (Escenas de recursos) del proyecto y  >   seleccione **SampleScene.unity** y ábrala.
1. En **Compilar para plataformas:**, asegúrese de **Windows** está seleccionado. Por ahora, no se deben seleccionar las otras dos opciones, **Android** **y** **Mac.** Una vez que quiera que los usuarios lo visiten, debe compilar y cargar para todas las plataformas".
1. Seleccione el **botón Build & Upload (Compilar).** Este proceso puede tardar uno o dos minutos.
1. Inicie Altspace, seleccione **Menú principal** y, a continuación, en la barra de **menús, seleccione Mis mundos.**
1. Vaya a **Hola mundo** y ábralo.

    La escena debe ser similar a la que vio en el editor de Unity.

## <a name="whats-supported"></a>Lo que se admite

* Sí: modelos, colisiones, animaciones, efectos de partícula, audio, skyboxes, y así sucesivamente.
* No: scripts. Por motivos de seguridad, se rechazarán las cargas que contienen scripts.
* Quizás: cosas muy interesantes, como la iluminación global dinámica.
* Upload escenas para distintas plataformas por separado o juntas.
* Consulte [Mundos destacados.](https://account.altvr.com/worlds/featured) Muchas se han creado mediante uploader.

## <a name="tips"></a>Sugerencias

* Únase al [altspacevr discord oficial.](https://discordapp.com/invite/altspacevr)
* En la página Plantilla del lado izquierdo, se muestran las cargas más recientes por plataforma. Si se realiza correctamente, verá hace **entre 1 y 2 minutos.** 

![El panel plantillas se abre con las cargas resaltadas](images/template-upload-list.png)

* Puede estar en el mundo al actualizar. En el momento en que el Upload **indica complete,** puede restablecer el mundo para ver los cambios.
* Al compilar solo para PC con una escena simple, debería tardar menos de un minuto en ver un cambio en Altspace.
* Establezca su mundo en Privado y No está en la lista para evitar distracciones.
* Coloque un cubo en el origen para que pueda ver dónde se generan las personas de forma predeterminada. Oculte el cubo al cargarlo.

## <a name="troubleshooting"></a>Solución de problemas

**Estoy caiendo o no puedo teleportar a nada** Debe agregar colisión a los objetos para teleportarlos.

**No ha cambiado nada**
    * ¿Ha guardado la escena en Unity?
    * ¿Ha elegido la plataforma en la que está probando?
    * ¿Está en el mundo correcto? ¿Ha elegido la plantilla adecuada en el formulario Uploader AND en el formato World?
    * ¿Ha compruebe las estadísticas de la página Plantilla?

**Upload error o se ha pasado el tiempo de espera**
    * El error de carga más común se produce al tener una versión incorrecta de Unity. Debe coincidir exactamente con la versión necesaria.
    * La carga puede ser demasiado grande. Intente mantener las escenas de PC < 100 MB. Empiece a ser pequeño y a compilar. Optimización, optimización y optimización.
    * Pruebe con un proyecto nuevo que contenga un cubo simple.
    * No fuerce la salida durante una compilación, ya que puede dañar la escena. Intente volver a cargar.

**Es un proceso lento**
    * Se recomienda compilar para PC solo durante la iteración y para Android más adelante.
    * Intente quitar archivos no usados. Por cualquier razón, Unity a veces se vuelve sobresalida.

**No puedo iniciar sesión con mis credenciales de Altspace**
    * Los correos electrónicos distinguen mayúsculas de minúsculas.
    * Pruebe con un nuevo proyecto.
    * Asegúrese de que la cuenta de Altspace está en buen estado.

## <a name="see-also"></a>Consulte también

* [Unity Learn](https://unity3d.com/learn)
* [Foros de Unity](https://forum.unity.com)  
