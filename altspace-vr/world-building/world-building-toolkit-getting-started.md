---
title: Presentación de world building Toolkit
description: Obtenga información sobre cómo configurar y cargar los mundos altspaceVR mediante plantillas de escena de Unity con el servicio World Building Toolkit.
ms.date: 03/11/2021
ms.topic: article
keywords: Toolkit
ms.openlocfilehash: 8b66e35509060e00b2e52d3770380d009d7060339003f534d23fdd47372a57f0
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125413"
---
# <a name="introducing-the-world-building-toolkit"></a>Presentación de world building Toolkit

> [!NOTE]
> The World Building Toolkit es un proyecto de la comunidad ejecutado por nuestro fantástico [amigo, Antonio Madden,](https://twitter.com/chigamesstudio)con el soporte de nosotros. Si está interesado, únase a la discordia [oficial de AltspaceVR](https://discordapp.com/invite/altspacevr) y visite el canal #world creación. Actualmente tenemos una versión beta de prueba de Mac en este momento, [más detalles](https://altvr.com/altspacevr-mac)

El uploader le permite usar una escena de Unity como plantilla para sus mundos. Puede traer una casa en desa desarrollo para Asíns o su creación favorita desde Minecraft. Si puede importarlo en Unity, probablemente pueda acceder a Altspace de esta manera. Estos son algunos ejemplos [de Worlds.](https://account.altvr.com/worlds/1046572460192825569)

![Mundos de ejemplo](images/unity-uploader-img-01.png)

## <a name="setup"></a>Configuración

1. Únase a la discordia oficial [altspaceVR](https://discordapp.com/invite/altspacevr) y visite el canal #world creación de aplicaciones: los amigos no permiten que los amigos compilen mundos por sí solos.
2. Lea nuestra [Guía de desarrollo Tareas iniciales de creación](world-building-getting-started.md) mundial para ver los conceptos básicos
3. [Instale Unity Hub](https://blogs.unity3d.com/2018/01/24/streamline-your-workflow-introducing-unity-hub-beta) e instale **Unity 2020.3.9.** El uploader no funcionará a menos que coincida exactamente con esta versión. Necesitará una cuenta gratuita de Unity si no tiene una y elija **Personal,** ya que lo está haciendo de forma divertida. Durante la instalación, asegúrese de activar la opción **Compilaciones de Android** y de deshabilitar la actualización automática.
4. [Descarga del uploader de Unity más reciente](upgrading-content-to-the-latest-unity.md#altspacevr-uploader-v090-upgrade-guide)
5. [Cree una plantilla en](https://account.altvr.com/space_templates/new) nuestro sitio web. Así **mismo, Hola mundo plantilla**.
6. [Cree un mundo](https://account.altvr.com/worlds/my) y asízcór **Hola mundo**. Seleccione **Hola mundo plantilla como** plantilla.

![Pantalla del mundo creado](images/unity-uploader-img-02.png)

## <a name="upload-your-scene"></a>Upload la escena

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-a-Template/player]

1. Abra Unity Hub y cree un nuevo proyecto de Unity 2020.3.9.
2. Con el proyecto abierto, importe el uploader haciendo doble clic en el archivo que descargó (es un paquete de Unity). Ahora debería ver una nueva pestaña denominada **AltspaceVR.** Deberá importar el paquete para cada proyecto de Unity que quiera usar con Altspace.
3. Abrir **menú > AltspaceVR > compilación Configuración**
4. Inicio de sesión con las credenciales de la cuenta de Altspace
5. Seleccione **Cargar plantillas y,** a continuación, **Hola mundo plantilla**
6. Agregue un cubo a la escena y guárdelo.
7. Active **Build for Windows?** (¿Compilar para Windows? y desactive Build for **Android? (¿Compilar para Android?)**
8. Haga clic en **Cargar**. En aproximadamente un minuto, debería **ver** Upload completo.
9. Unirse **Hola mundo** iniciando Altspace y especificando en **Menú > Mundos > Mis mundos**
10. Restablecer el mundo desde el **menú > Configuración > moderar > restablecer espacio**
11. Debería ver el cubo. Si lo hace rápidamente como en el vídeo anterior, puede ver los cambios en tan solo 10 segundos.

## <a name="whats-supported"></a>Lo que se admite

* Sí: modelos, colisión, animaciones, efectos de partícula, audio, skyboxes, y así sucesivamente
* No: scripts. Por motivos de seguridad, se rechazarán las cargas que contienen scripts.
* Quizás: cosas muy interesantes, como la iluminación global dinámica
* Upload escenas para distintas plataformas por separado o juntos
* Consulte Featured Worlds , many were built using the Uploader [(Mundos destacados,](https://account.altvr.com/worlds/featured)muchos se han creado mediante el uploader).

## <a name="tips"></a>Sugerencias

* Únase a [la discordia oficial de AltspaceVR.](https://discordapp.com/invite/altspacevr)
* En la página Plantilla del lado izquierdo, se muestran las cargas más recientes por plataforma. Si se ha realizado correctamente, verá hace **entre 1 y 2 minutos.** Screen_Shot_2019-01-11 _at_1.21.04_AM.png

![Panel Plantillas abierto con las cargas resaltadas](images/unity-uploader-img-03.png)

* Puede estar en el mundo al actualizar. En el momento en que el Upload **indica complete,** puede restablecer el mundo para ver los cambios.
* La creación solo para PC con una escena simple debe tardar menos de 1 minuto en ver un cambio en Altspace
* Establezca su mundo en Privado y Sin lista para evitar distracciones.
* Coloque un cubo en el origen para que pueda ver dónde se generarán las personas de forma predeterminada. Oculte el cubo al cargarlo.

## <a name="troubleshooting"></a>Solución de problemas

**Estoy caiendo o no puedo teleportar a nada** Debe agregar colisión a objetos para teleportarlos.

**No ha cambiado nada**
    * ¿Ha guardado la escena en Unity?
    * ¿Ha elegido la plataforma en la que está probando?
    * ¿Está en el mundo correcto? ¿Ha elegido la plantilla correcta en el formulario Uploader AND en el formulario World?
    * ¿Ha compruebe las estadísticas de la página Plantilla?

**Upload error o se ha pasado el tiempo de espera**
    * El error de carga más común es tener una versión incorrecta de Unity. Debe coincidir exactamente con la versión necesaria.
    * La carga puede ser demasiado grande. Intente mantener las escenas de PC < 100 MB. Empiece a ser pequeño y se compile. Optimice, optimice, optimice.
    * Pruebe con un proyecto nuevo con un cubo simple.
    * No fuerce la salida durante una compilación, ya que puede dañar la escena. Intente volver a cargar.

**Es un proceso lento**
    * Se recomienda compilar solo para PC mientras se itera y para Android más adelante.
    * Intente quitar los archivos no usados. Por cualquier razón, Unity se vuelve sobresalida a veces.

**No puedo iniciar sesión con mis credenciales de Altspace**
    * Los correos electrónicos distinguen mayúsculas de minúsculas.
    * Pruebe con un nuevo proyecto.
    * Asegúrese de que la cuenta de Altspace está en buen estado.

## <a name="see-also"></a>Consulte también

* [Unity Learn](https://unity3d.com/learn)
* [Foros de Unity](https://forum.unity.com)
