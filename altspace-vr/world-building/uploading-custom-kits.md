---
title: Carga de kits personalizados
description: Aprenda a configurar, generar y cargar sus propios kits personalizados en AltspaceVR, así como a solucionar problemas.
ms.date: 03/11/2021
ms.topic: article
keywords: kits, carga, solución de problemas
ms.openlocfilehash: 9a90bff2360d854dc398a35501f07cddcbce5c6c66ef8230f2e412a022f8aed0
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125565"
---
# <a name="uploading-custom-kits"></a>Carga de kits personalizados

El Editor del mundo tiene kits que contienen Artifacts que puede generar en su mundo. Por ejemplo, el [Kit de Campofire](https://account.altvr.com/kits/993516233267609824) tiene muchos tipos de árboles: cada tipo de árbol es un artefacto. Para crear su propio kit, debe crear Unity AssetBundles y cargar un archivo .zip que contenga un elemento Prefab de Unity para cada artefacto y registrar cada artefacto en nuestro sitio web. Afortunadamente, el uploader de Unity controlado por la comunidad automatiza la mayor parte del flujo de trabajo. Una vez cargado, puede generar objetos de sus propios kits en sus mundos y otros usuarios pueden verlos automáticamente. Más adelante, puede compartir el kit con sus amigos o incluso con toda la Community si se presenta.

## <a name="prerequisites"></a>Requisitos previos

1. [Instalación de Unity Hub y Unity](world-building-toolkit-getting-started.md)
2. Descarga de la versión más reciente del [carguedor de Unity](https://altvr.com/download-latest-unity-uploader/)

## <a name="setup"></a>Configuración 

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-my-own-Kits-Part-1-Setup/player]

1. Creación de un kit en nuestro sitio web en [Worlds > Kits](https://account.altvr.com/kits)
2. Copie el identificador del kit de la barra de direcciones del explorador en el Portapapeles (este paso será más fácil en las versiones 0.9 y posteriores del usuario de Uploader).
3. Creación de una nueva instancia de Unity Project
4. Importar el cargador de Unity haciendo doble clic en el paquete

![Paquete de carga de Unity importado](images/custom-kits-img-01.png)

5. Inicie sesión en uploader con el correo electrónico y la contraseña de Altspace.

![Interfaz de inicio de sesión de AltspaceVR en Unity](images/custom-kits-img-02.png)

## <a name="generate-and-upload-your-kit"></a>Generación y carga del kit

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-my-own-Kits-Part-2/player]

1. Rellene El **nombre de carpeta** del kit con el identificador del kit como prefijo y un tema (por ejemplo, **1137484494681408069_pirates)** y rellene nombre del recurso del **kit** con el identificador del kit como prefijo. Todos los recursos tendrán que tener este prefijo.

![Interfaz AltspaceVR en Unity con el nombre de carpeta del kit](images/custom-kits-img-03.png)

2. Para cada artefacto o conjunto de Artifacts:
* Arrastre los objetos Prefab(s) de origen a la pestaña Hierarchy (Jerarquía).
* Seleccione los que desea incluir en un conjunto, por su parte, cinco tipos de cilindros.
* Actualización del **nombre del recurso del kit** con el **paquete**
* Seleccione **Convert GameObject(s) to Kit Prefab (Convertir gameobjects en kit prefab)**
* Compruebe que se crearon nuevas prefabs y capturas de pantalla en la carpeta Assets/Prefabs

![Interfaz AltspaceVR en Unity con artefactos seleccionados](images/custom-kits-img-04.png)

> [!NOTE]
> Si desea realizar modificaciones en un prefab generado, arrástrelo de nuevo  a la jerarquía, realice cambios y, a continuación, haga clic en Aplicar en la pestaña Inspector para actualizar el prefab. 

3. Cuando esté listo, desplácese hacia abajo en la pestaña Uploader (Cargarr) y vamos a prepararnos para generar un archivo ZIP con el paquete de recursos.
4. Para una iteración más rápida, desactive **el Kit de compilación para Android?**. No olvide compilar y cargar una versión para Android más adelante cuando haya terminado de iterar o quiera compartir o características del kit. 
5. Seleccione **Load Kit Prefab Directories (Directorios prefab del kit de carga)**
6. Elija **Compilar** junto al que coincida con el nombre de carpeta del kit. Es habitual generar varios kits desde el mismo proyecto de Unity. Esto puede tardar un tiempo en función del tamaño del kit. Cuando haya terminado, la carpeta que contiene el archivo ZIP se abrirá automáticamente. 
7. Vaya al sitio web, edite el kit que creó anteriormente y cargue el archivo ZIP que ha generado. Esta carga puede tardar un tiempo en función del tamaño del archivo.
    * Si se realiza correctamente, verá en el lado izquierdo, en "Carga", los tamaños de archivo y para PC y Android, y cuándo se actualizaron por última vez.
    * Si no se realiza correctamente, asegúrese de que no tiene ningún script, no se admiten scripts, se comprueba la seguridad y se vuelve a intentarlo.

Enhorabuena. Ya está listo para crear mundos con su propio kit.

## <a name="troubleshooting"></a>Solución de problemas 

**¿Hay límites?**
Todavía no hay límites, pero recuerde que los usuarios deben descargar AssetBundle para su plataforma para todo el kit, aunque solo se utilice un artefacto. Intente mantener la descarga por plataforma en 5 MB o menos. Una manera de hacerlo es dividir las cosas en kits más pequeños. Por ejemplo, 200 propiedades se deben dividir a la mitad. 

**¿Ve el "ojo dividido"?**
Vuelva a importar el uploader más reciente para obtener la configuración de representación correcta.

**¿Actualizaciones o cambios no reflejados?**
    * Comprobación de la hora actualizada en la página Kit
    * Volver a escribir el mundo no funcionará: reinicie el cliente. Incluso después, puede tardar unos minutos en actualizarse.
    * Asegúrese de que no haya espacios en los nombres de carpeta o nombres prefab, por **ejemplo, "party_favors" frente a "party favors".**

**Sigue afirmando que tengo un script, pero no** AssetBundle Browser incluye automáticamente archivos a veces. Intente aislar el modelo que va a incorporar. Por ejemplo, no lo arrastre cuando ya forme parte de otro elemento Prefab.

**¿Qué sucede con los sistemas de partícula y las animaciones?**
Para ellos, a continuación, bajo un cubo 1x1x1 situado en el origen con Mesh Rendering y Collision deshabilitados. Los sistemas de partícula deben tener habilitado el bucle **y el** escalado debe establecerse en **Jerarquía** para que podamos escalarlos correctamente en Altspace. Después de generar los objetos prefab para todas las animaciones, deshabilite las colisiones en los objetos **de** colisión para cada una.

**Los Artifacts son oscuros** ¿Ha establecido el sombreador de material del modelo en Luces direccionales móviles **o de solo vértice?**

**El artefacto no está orientado a la manera correcta** Gire el **modelo** y el **colisionador** y actualice el objeto Prefab. La rotación del elemento primario no hará nada, eso se omite. Puede usar el campo **Invalidación de** rotación para hacerlo fácilmente.

**¿Pueden Artifacts usar con la función **CreateFromLibrary** del SDK?**
Sí