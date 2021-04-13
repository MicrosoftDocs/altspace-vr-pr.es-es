---
title: Carga de skyboxes personalizadas
description: Obtenga instrucciones paso a paso sobre cómo cargar y solucionar problemas de sus skyboxes personalizadas en AltspaceVR experiencias.
ms.date: 03/11/2021
ms.topic: article
keywords: Skyboxes, solución de problemas
ms.openlocfilehash: 02d5bc762dc36d4195100e8155d6250789e833f7
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213791"
---
# <a name="uploading-custom-skyboxes"></a>Carga de skyboxes personalizadas

Un SKYBOX es una forma de crear un **fondo** para su mundo que hace que la experiencia sea más envolvente. Hay diferentes tipos de Skyboxes, pero actualmente se admite **equirectangular**. A continuación se muestra un ejemplo de una cámara 360 (más información [aquí](http://moments.mankindforward.com/)): 

![360 equirectangular vista de un salón](images/custom-skyboxes-img-01.jpeg)

También puede usar el [cargador de Unity](world-building-toolkit-getting-started.md) , pero este enfoque es más sencillo.

1. Vaya a [mundos > skyboxes](https://account.altvr.com/skyboxes) y presione el botón **crear** de la derecha.

![Página de sitios web de mundos abrir en el panel de skyboxes](images/custom-skyboxes-img-02.png)

2. Rellene un nombre y especifique la imagen 360. No es necesario que sea una foto, hay programas que le permiten dibujar su propio o puede buscar algunos en línea. Cuando esté listo, seleccione **Crear**. 

![Formulario de creación de SKYBOX](images/custom-skyboxes-img-03.png)

3. Opcionalmente, puede cargar una imagen de **vista previa** para que pueda identificar fácilmente este SKYBOX. También puede cargar el audio ambiente en formato WAV. 

> [!IMPORTANT]
> Se recomienda cargar imágenes de vista previa y audio ambiente por separado, después de cargar la imagen 360. Si los carga juntos, los tamaños de archivo pueden ser lo suficientemente grandes como para detenerse el proceso. [Jetsons World](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) es un buen ejemplo de cómo usar un SKYBOX con audio ambiente. Observe cómo el generador mundial mantiene el volumen de audio bajo y los sonidos que oye son esporádicos, por lo que la gente no me molesta. 

4. Escriba su mundo y abra el editor mundial. En Skyboxes, seleccione el nuevo SKYBOX. En unos segundos, el cielo cambiará literalmente. Otros usuarios de su mundo también verán el cambio del cielo. Para volver a cambiar, elija el **valor predeterminado** SkyBOX en la misma lista. 

## <a name="troubleshooting"></a>Solución de problemas

**Hay unas costuras o una línea en el cielo:-(.** Es un error que corregiremos pronto

**Error de carga**
    * intente cargar solo la imagen de 360 por sí misma
    * Pruebe con otro archivo más pequeño como prueba

**No encuentro una foto 360**
    * Flickr es una buena fuente (cambie los filtros para buscar las de Creative Commons)
    * ¡ Tómese su propia! Hemos tenido éxito con las cámaras de Ricoh. 
**El cielo busca granulado o bloqueado** Es posible que necesite encontrar una imagen de mayor resolución. Normalmente aproximadamente 2-5 MB y ~ 5000 PX x 2000 PX

**Nos afecta a la velocidad de fotogramas del mundo.**
La imagen probablemente es demasiado grande. Algunos skyboxes generados pueden ser 8k. Normalmente se encuentran en las versiones de 2K compatibles con móviles: Úsela.

**Ayúdeme con el audio ambiente**
    * Use software gratuito como Audacity para reducir el volumen o cree sus propios bucles. Recuerde que el audio se repetirá y reproducirá en los oídos de las personas, por lo que debe mantenerse bajo y no molestar
    * El [sonido gratuito](https://freesound.org/) es una buena fuente de sonidos sin regalías
