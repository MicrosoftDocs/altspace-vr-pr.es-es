---
title: Usar el proyector web para transmitir un explorador
description: Aprenda a usar el proyector web para transmitir contenido desde un explorador designado a experiencias de AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: proyector Web, Stream, browser
ms.openlocfilehash: 4f89757a572ae3d77a7b11f068760268a4089ddd
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213703"
---
# <a name="using-the-web-projector-to-stream-a-browser"></a>Usar el proyector web para transmitir un explorador

El proyector web AltspaceVR es una sólida solución de uso compartido de medios que le permite transmitir por secuencias una pestaña de explorador designada desde su PC de escritorio directamente a AltspaceVR. Se puede usar para compartir diapositivas, vídeos, fotos y todo lo que se puede abrir desde un explorador. * el proyector Web requiere descargar una extensión del explorador y actualmente está disponible exclusivamente a través del editor mundial. A continuación se muestra una introducción completa de la característica y cómo usarla:

## <a name="requirements"></a>Requisitos

1. Debe usar un equipo PC o Mac para transmitir el explorador.
2. La extensión del explorador necesaria es compatible actualmente con el explorador Edge. (Estamos trabajando para expandir esta lista).
3. Aunque puede transmitir desde un equipo Mac, el proyector web todavía no está disponible en el cliente Mac de AltspaceVR.

> [!NOTE]
> Esta característica está pensada principalmente para transmitir por secuencias una pestaña del explorador de su elección. Si está intentando transmitir por secuencias su aplicación de escritorio, el proyector web transmitirá por secuencias todo el audio del equipo (incluido AltspaceVR), lo que puede dar lugar a eco y comentarios. Tendrá que silenciar AltspaceVR para evitar que esto suceda. También puede usar un dispositivo independiente para ejecutar AltspaceVR mientras realiza la transmisión desde su PC.

## <a name="getting-started"></a>Introducción

1. Para empezar, deberá descargar e instalar la extensión del explorador, que se puede encontrar [aquí](https://account.altvr.com/web_projector).
2. A continuación, [transfiera localmente su extensión en el explorador Edge](https://docs.microsoft.com/microsoft-edge/extensions-chromium/getting-started/extension-sideloading).
    * Una vez completada la descarga, vaya a la sección de **extensiones** del explorador. (Se encuentra en **configuración**)
    * Descomprima el archivo. zip.
    * Alternar en el **modo de desarrollador** y seleccionar **cargar desempaquetado**
    * Elija la carpeta que acaba de descomprimir. Esta es la extensión del proyector Web.
    * Una vez agregada la extensión, puede entrar en **detalles** para establecer la configuración.

## <a name="setting-up-a-shareable-browser"></a>Configuración de un explorador que se pueden compartir

Una vez que la extensión se haya descargado e instalado, ya está listo para usarse.

1. Abra una pestaña en el explorador Edge y navegue hasta el medio que desea compartir.
2. Configure la ventana para que esté listo para compartir. (Nota: toda la ventana del explorador se proyectará en el mundo)
3. Busque la extensión recién instalada (que se muestra como un icono de AltspaceVR cerca de la barra de direcciones URL en el explorador). Seleccione AltspaceVR. Se le pedirá que inicie sesión en su cuenta. (* Nota: es importante que inicie sesión en la misma cuenta que usará para configurar el proyector Web).
4. Una vez que haya iniciado sesión, debería ver la pantalla de extensión que le ofrece una opción **iniciar streaming** . Selecciónela.

## <a name="projecting-your-browser-in-world"></a>Proyectar el explorador en todo el mundo

1. Una vez que el explorador está configurado para la proyección y se ha iniciado el streaming a través de la extensión, abra AltspaceVR.
2. Configure el proyector Web en el entorno que desee abriendo su editor mundial > Basics > proyector Web
3. Una vez hecho esto, puede usar los controles del editor mundial para cambiar el tamaño del proyector Web. (También incluirá instrucciones, en la pantalla).
4. Seleccione el botón **conectar** para iniciar la transmisión por secuencias del explorador de Edge.
5. Recuerde hacer clic en **difundir** para empezar a compartir con todos los invitados en el espacio.
6. No olvide **detener el streaming.** La sesión agotará el tiempo de espera, pero hasta entonces seguirá teniendo el proyecto en vivo en el explorador. Es mejor finalizar la sesión en cuanto termine.

![Explorador previsto en AltspaceVR World](images/web-project-img-01.png)

**Vídeo: sugerencia de streaming:** Si el vídeo se repite, detenga la transmisión por secuencias, ajuste la calidad del vídeo en 480p o 360p y, a continuación, reinicie la transmisión y difusión. Las resoluciones más altas pueden agotar la CPU y cargar el ancho de banda.

> [!NOTE]
> En este momento, los botones de control adicionales en la parte superior del proyector web todavía no están activos. Permanecerán atenuados y no se pueden hacer clic en ellos. Esto no es un error, sino por diseño (por ahora).

> [!IMPORTANT]
> Declinación de responsabilidades: Nota: el uso del proyector Web, al igual que todas las demás características de AltspaceVR, está sujeto a los [términos de servicio](../community/terms-of-service.md) y a nuestros estándares de la [comunidad](../community/community-standards.md). Como tal, el proyector web no se puede usar para transmitir contenido que infringe cualquiera de los dos acuerdos. Si lo hace, se producirán acciones de moderación tomadas por AltspaceVR. No se garantiza el acceso al proyector web Open Beta y solo se puede conceder para una versión de prueba temporal. La duración de la versión beta y la duración de su participación son a la discreción del equipo de AltspaceVR. No es necesario usar la versión beta del proyector web y la participación en la versión beta es voluntaria. Se anima a los participantes a ofrecer comentarios sobre el proyector web que le ayudarán a dar forma a la funcionalidad y la facilidad de uso de la característica a medida que continúe el desarrollo. La versión beta del proyector web puede tener una funcionalidad limitada y puede estar sujeta a errores inesperados. Gracias por adelantado a su participación.
