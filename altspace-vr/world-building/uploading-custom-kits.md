---
title: Carga de kits personalizados
description: Obtenga información sobre cómo configurar, generar y cargar sus propios kits personalizados en AltspaceVR, así como ayuda para la solución de problemas.
ms.date: 03/11/2021
ms.topic: article
keywords: kits, carga, solución de problemas
ms.openlocfilehash: e5a1b9c2ef5339db0cb821cb6f7d21a930416451
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213902"
---
# <a name="uploading-custom-kits"></a>Carga de kits personalizados

El editor mundial tiene kits que contienen artefactos que puede generar en su mundo. Por ejemplo, el [Kit de Campfire](https://account.altvr.com/kits/993516233267609824) tiene muchos tipos de árboles: cada tipo de árbol es un artefacto. Para crear su propio Kit, debe crear Unity AssetBundles y cargar un archivo. zip que contenga un recurso prefabricado de Unity para cada artefacto y registrar cada artefacto en nuestro sitio Web. Afortunadamente, el cargador de Unity controlado por la comunidad automatiza la mayor parte del flujo de trabajo. Una vez cargados, puede generar objetos de sus propios kits en sus mundos y otros usuarios pueden verlos automáticamente. Más adelante, podrá compartir su kit con sus amigos o incluso con toda la comunidad.

## <a name="prerequisites"></a>Requisitos previos

1. [Instalación de Unity Hub y Unity](world-building-toolkit-getting-started.md)
2. Descargar la versión más reciente del [cargador de Unity](https://altvr.com/download-latest-unity-uploader/)

## <a name="setup"></a>Configurar 

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-my-own-Kits-Part-1-Setup/player]

1. Cree un kit en nuestro sitio web en [mundos > kits](https://account.altvr.com/kits)
2. Copie el identificador del kit de la barra de direcciones del explorador en el portapapeles (este paso será más sencillo en las versiones 0.9 de la
3. Creación de un nuevo proyecto de Unity
4. Importar el cargador de Unity haciendo doble clic en el paquete

![Paquete de cargador de Unity importado](images/custom-kits-img-01.png)

5. Inicie sesión en el cargador con el correo electrónico y la contraseña de Altspace

![Interfaz de inicio de sesión de AltspaceVR en Unity](images/custom-kits-img-02.png)

## <a name="generate-and-upload-your-kit"></a>Generar y cargar el kit

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-my-own-Kits-Part-2/player]

1. Rellene el nombre de la **carpeta del kit** con el identificador del kit como prefijo y un tema (por ejemplo, **1137484494681408069_pirates**) y rellene el nombre del **recurso del kit** con el identificador del kit como prefijo. Todos los recursos deberán tener este prefijo.

![Interfaz AltspaceVR en Unity con el nombre de la carpeta kit](images/custom-kits-img-03.png)

2. Para cada artefacto o conjunto de artefactos:
* Arrastre los recurso prefabricado de origen a la pestaña jerarquía
* Seleccione los que desea incluir en un conjunto, por ejemplo, cinco tipos de barriles.
* Actualizar el **nombre del recurso del kit** con el **barril**
* Seleccione **convertir GameObject (s) en kit recurso prefabricado**
* Compruebe que se han creado nuevas Prefabs y capturas de pantallas en la carpeta assets/Prefabs

![Interfaz AltspaceVR en Unity con artefactos seleccionados](images/custom-kits-img-04.png)

> [!NOTE]
> Si desea realizar modificaciones en un recurso prefabricado generado, vuelva a arrastrarlo a la jerarquía, realice los cambios y, a continuación, haga clic en **aplicar** en la pestaña inspector para actualizar el recurso prefabricado. 

3. Cuando esté listo, desplácese hacia abajo en la pestaña del cargador y prepárese para generar un archivo zip con el paquete de activos.
4. Para una iteración más rápida, desactive el **Kit de compilación para Android?**. Recuerde compilar y cargar una versión para Android más adelante cuando haya terminado la iteración o desee compartir o incluir su kit. 
5. Selección de **directorios recurso prefabricado del kit de carga**
6. Elija **compilar** junto a la que coincida con el nombre de la carpeta del kit. Es habitual generar varios kits desde el mismo proyecto de Unity. Esto puede tardar unos minutos en función del tamaño del kit. Cuando haya terminado, se abrirá automáticamente la carpeta que contiene el archivo. zip. 
7. Vaya al sitio web, edite el kit que creó anteriormente y cargue el archivo zip que ha generado. Esta carga puede tardar unos minutos en función del tamaño del archivo.
    * Si se realiza correctamente, verá en el lado izquierdo "cargas" los tamaños de archivo y para PC y Android, y cuándo se actualizaron por última vez.
    * Si no se ha realizado correctamente, asegúrese de que no tiene ningún script, no se admiten scripts, por lo que comprobamos la seguridad e inténtelo de nuevo.

¡Enhorabuena! Está listo para crear mundos con su propio Kit.

## <a name="troubleshooting"></a>Solución de problemas 

**¿Hay límites?**
Todavía no hay límites fuertes, pero recuerde que los usuarios deben descargar el AssetBundle para su plataforma para todo el kit, incluso si solo se usa un artefacto. Intente mantener la descarga por plataforma en 5 MB o menos. Una forma de hacerlo es dividir las cosas en kits más pequeños. Por ejemplo, 200 props debe dividirse en la mitad. 

**¿Ve "vista en dos paneles"?**
Volver a importar el cargador más reciente para obtener la configuración de representación correcta

**¿Las actualizaciones y los cambios no se reflejan?**
    * Comprobar la hora actualizada en la página del kit
    * Volver a escribir el mundo no funcionará: reinicie el cliente. Incluso puede tardar unos minutos en actualizarse
    * Asegúrese de que no hay espacios en los nombres de carpeta o recurso prefabricado **, por ejemplo, "party_favors" frente a la entidad favorece "**

**Sigue diciendo que tengo un script pero no** El explorador de AssetBundle incluye automáticamente los archivos a veces. Intente aislar el modelo que está incorporando. Por ejemplo, no lo arrastre cuando ya forme parte de otro recurso prefabricado

**¿Qué ocurre con los sistemas de partículas y las animaciones?**
Para ellos, próximos en un cubo 1x1x1 situado en el origen con la representación en malla y la colisión deshabilitada. Los sistemas de partículas deben tener habilitada la opción de bucle y el **ajuste de escala** se debe establecer en **jerarquía** para que podamos escalarlos correctamente en Altspace. Después de generar el Prefabs para todas las animaciones, deshabilite las colisiones en los objetos de **colisión** para cada una de ellas.

**Los artefactos son oscuros** ¿Estableció el sombreador de material del modelo en las **luces direccionales solo de dispositivo móvil/vértice iluminado**?

**El artefacto no está orientado a la manera correcta** Gire el **modelo** y el **Colisionador** y actualice el recurso prefabricado. La rotación del elemento primario no hará nada, lo que se pasa por alto. Puede usar el campo de **invalidación de giro** para hacerlo fácilmente.

**¿Estos artefactos se pueden usar con la función **CreateFromLibrary** del SDK?**
Sí