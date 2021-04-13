---
title: Presentación del kit de herramientas de creación mundial
description: Aprenda a configurar y cargar los mundos de AltspaceVR con las plantillas de escenas de Unity con el kit de herramientas de creación mundial.
ms.date: 03/11/2021
ms.topic: article
keywords: halla
ms.openlocfilehash: cf4660f46d93ca5c5f23de3f567ff04b12519617
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213649"
---
# <a name="introducing-the-world-building-toolkit"></a>Presentación del kit de herramientas de creación mundial

> [!NOTE]
> El kit de herramientas de creación mundial es un proyecto de la comunidad que ejecuta nuestro fantástico amigo, [Anthony Madden](https://twitter.com/chigamesstudio), con soporte técnico de EE. UU. Si le interesa, únase al descodificador [oficial de AltspaceVR](https://discordapp.com/invite/altspacevr) y visite el canal de creación de #world. Actualmente tenemos una versión beta de prueba de Mac en este momento, [más detalles](https://altvr.com/altspacevr-mac)

El cargador le permite usar una escena de Unity como plantilla para sus mundos. Puede incluir una Haunted House para Halloween o su creación favorita desde Minecraft. Si puede importarlo en Unity, probablemente puede obtenerlo en Altspace de esta manera. Estos son algunos [mundos de ejemplo](https://account.altvr.com/worlds/1046572460192825569).

![Mundos de ejemplo](images/unity-uploader-img-01.png)

## <a name="setup"></a>Configurar

1. Únase al descodificador [oficial de AltspaceVR](https://discordapp.com/invite/altspacevr) y visite el canal de creación de #world-los amigos no permiten a los amigos crear solo mundos.
2. Lea nuestra [Guía de introducción de creación mundial](world-building-getting-started.md) para obtener los conceptos básicos
3. [Instale Unity Hub](https://blogs.unity3d.com/2018/01/24/streamline-your-workflow-introducing-unity-hub-beta) e instale **Unity 2019.4.2 F1**. El cargador no funcionará a menos que coincida exactamente con esta versión. Necesitará una cuenta de Unity gratuita si no tiene una y elige **personal** , ya que está haciendo esto por diversión. Durante la instalación, asegúrese de activar la opción **compilaciones de Android** y deshabilitar la actualización automática.
4. [Descarga del cargador de Unity más reciente](https://aka.ms/AsvrCommunityUploader)
5. [Cree una plantilla](https://account.altvr.com/space_templates/new) en nuestro sitio Web. Asígnele el nombre **Hola mundo plantilla**.
6. [Cree un mundo](https://account.altvr.com/worlds/my) y asígnele el nombre **Hola mundo**. Seleccione **Hola mundo plantilla** como plantilla.

![Pantalla mundial creada](images/unity-uploader-img-02.png)

## <a name="upload-your-scene"></a>Carga de la escena

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-a-Template/player]

1. Abra Unity Hub y cree un nuevo proyecto de Unity 2019.4.2 F1.
2. Con el proyecto abierto, importe el cargador haciendo doble clic en el archivo que ha descargado (es un paquete de Unity). Ahora debería ver una nueva pestaña denominada **AltspaceVR**. Deberá importar el paquete para cada proyecto de Unity que quiera usar con Altspace
3. Abrir **menú > configuración de compilación de AltspaceVR >**
4. Inicio de sesión con las credenciales de la cuenta de Altspace
5. Seleccione **cargar plantillas** y, a continuación, seleccione **Hola mundo plantilla** .
6. Agregue un cubo a la escena y guárdelo.
7. ¿Comprobar **compilar para Windows?** y desactivar la **compilación de Android?**
8. Seleccione **Cargar**. En un minuto aproximadamente, debería ver **carga** completada.
9. Para unirse **Hola mundo** , inicie Altspace y escriba desde **el menú > mundos > mis mundos**
10. Restablecer el mundo desde la **configuración del > de menús > moderado > restablecer espacio**
11. Debería ver el cubo. Si lo hace rápidamente en el vídeo anterior, puede ver los cambios en tan solo 10 segundos.

## <a name="whats-supported"></a>Lo que se admite

* Sí: modelos, colisiones, animaciones, efectos de partículas, audio, Skyboxes, etc.
* No: scripts. Por motivos de seguridad, las cargas que contienen scripts se rechazarán.
* Quizás: cosas sofisticadas como la iluminación global dinámica
* Cargar escenas para distintas plataformas por separado o juntas
* Vea los [mundos destacados](https://account.altvr.com/worlds/featured)y muchos se crearon con el cargador

## <a name="tips"></a>Sugerencias

* Únase al descodificador [oficial de AltspaceVR](https://discordapp.com/invite/altspacevr).
* En la página de la plantilla en el lado izquierdo, se muestran las cargas más recientes por plataforma. Si se realiza correctamente, vería **1-2 minutos**. Screen_Shot_2019-01-11 _at_1.21.04_AM.png

![Panel Plantillas abierto con cargas resaltadas](images/unity-uploader-img-03.png)

* Puede ser en el mundo al actualizar. En el momento en que el cargador dice que la carga se ha **completado** , puede restablecer el mundo para ver los cambios.
* La compilación para PC solo con una escena simple debe tardar menos de 1 minuto en ver un cambio en Altspace
* Establezca su mundo en privado y que no esté en la lista para evitar distracciones.
* Coloque un cubo en el origen para que pueda ver dónde se generarán los usuarios de forma predeterminada. Oculte el cubo al cargar.

## <a name="troubleshooting"></a>Solución de problemas

**Estoy caer o no se puede transportar a nada** Debe agregar colisiones a los objetos para transportarlos.

**No se ha cambiado nada**
    * ¿Guardó la escena en Unity?
    * ¿Eligió la plataforma en la que está probando?
    * ¿Está en el mundo adecuado? ¿Eligió la plantilla correcta en el cargador y en el formulario del mundo?
    * ¿Ha activado las estadísticas de la página de plantillas?

**Se produce un error de carga o se agota el tiempo**
    * El error de carga más común tiene la versión de Unity equivocada. Debe coincidir exactamente con la versión necesaria.
    * Es posible que la carga sea demasiado grande. Intente mantener las escenas de PC < 100 MB. Empiece a ser pequeño y compilar. Optimizar, optimizar y optimizar.
    * Pruebe con un proyecto nuevo con un cubo simple.
    * No fuerce la salida durante una compilación, ya que puede dañar la escena. Intente volver a cargar.

**Es un proceso lento.**
    * Se recomienda compilar solo para PC durante la iteración y para Android más adelante.
    * Intente quitar los archivos no usados. Por cualquier motivo, Unity obtiene overzealous a veces.

**No puedo iniciar sesión con mis credenciales de Altspace**
    * Los mensajes de correo electrónico distinguen mayúsculas de minúsculas.
    * Pruebe con un nuevo proyecto.
    * Asegúrese de que su cuenta de Altspace está en buen estado.

## <a name="see-also"></a>Vea también

* [Aprendizaje de Unity](https://unity3d.com/learn)
* [Foros de Unity](https://forum.unity.com)
