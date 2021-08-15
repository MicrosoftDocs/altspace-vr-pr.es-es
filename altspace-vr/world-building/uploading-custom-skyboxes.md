---
title: Carga de skyboxes personalizados
description: Obtenga instrucciones paso a paso sobre cómo cargar y solucionar problemas de sus skybox personalizados en las experiencias altspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: skyboxes, solución de problemas
ms.openlocfilehash: 912df5a4c87b7a5817824c6ee75ec8707439636b83b4d46996bbc4129ee6e9de
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126800"
---
# <a name="uploading-custom-skyboxes"></a>Carga de skyboxes personalizados

Skybox es una manera de crear un **fondo** para su mundo que hace que la experiencia sea más envolvente. Hay diferentes tipos de skyboxes, pero actualmente se **admiten equirectangulares.** Este es un ejemplo tomado con una cámara 360 (más ejemplo [aquí):](http://moments.mankindforward.com/) 

![Vista equirectangular de 360 de una sala de estar](images/custom-skyboxes-img-01.jpeg)

También puede usar el [uploader de Unity,](world-building-toolkit-getting-started.md) pero este enfoque es más sencillo.

1. Vaya a [Worlds > Skyboxes](https://account.altvr.com/skyboxes) y presione el **botón Crear** de la derecha.

![Página del sitio web de Worlds abierta en el panel skyboxes](images/custom-skyboxes-img-02.png)

2. Rellene un nombre y especifique la imagen 360. No tiene que ser una foto, hay programas que le permiten dibujar los suyos propios o puede buscar algunos en línea. Cuando esté listo, seleccione **Crear**. 

![Formulario de creación de Skybox](images/custom-skyboxes-img-03.png)

3. Opcionalmente, puede cargar una imagen **de vista** previa para que pueda identificar fácilmente este skybox. También puede cargar audio ambiente en formato WAV. 

> [!IMPORTANT]
> Se recomienda cargar imágenes de vista previa y audio ambiente por separado, después de cargar la imagen 360. Si los carga juntos, los tamaños de archivo pueden ser lo suficientemente grandes como para detener el proceso. [Jetsons World](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) es un buen ejemplo de cómo usar skybox con audio ambiental. Observe cómo World-Builder mantiene el volumen de audio bajo y los sonidos que se escuchan son esporádicos para que la gente no se desasoye. 

4. Escriba su mundo y abra el Editor del mundo. En Skyboxes, seleccione el nuevo Skybox. En unos segundos, el cielo cambiará literalmente. Otros usuarios de su mundo también verán el cambio en el cielo. Para volver atrás, elija el **skybox** predeterminado en esa misma lista. 

## <a name="troubleshooting"></a>Solución de problemas

**Hay una siam o línea en el cielo :-(.** Es un error que corregiremos pronto.

**Upload error**
    * intente cargar solo la imagen 360 por su cuenta.
    * pruebe con otro archivo más pequeño como prueba.

**No encuentro una foto 360**
    * Noé es una buena fuente (cambie los filtros para buscar los creative commons).
    * ¡Tómese la suya propia! Hemos tenido éxito con las cámaras de Ricoh. 
**El cielo tiene un aspecto de grano o bloque** Es posible que tenga que encontrar una imagen de mayor resolución. Normalmente, alrededor de 2-5 MB y ~5000 px x 2000 px

**¡Esto daña la velocidad de fotogramas de mi mundo!**
La imagen probablemente sea demasiado grande. Algunos skyboxes generados pueden ser de 8 k. Normalmente vienen con versiones de 2k compatibles con dispositivos móviles: úsese eso.

**Help me with the ambient audio (Ayuda con el audio ambiente)**
    * Use software gratuito como Audacity para reducir el volumen o crear sus propios bucles. Recuerde que el audio se repetirá y se reproducirá en los oídos de las personas, por lo que debe mantenerlo bajo y no ser molesto.
    * [El sonido gratuito](https://freesound.org/) es una buena fuente de sonidos sin impuestos
