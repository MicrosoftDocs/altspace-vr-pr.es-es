---
title: Uso del proyector web para transmitir un explorador
description: Aprenda a usar el proyector web para transmitir contenido desde un explorador designado a las experiencias altspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: proyector web, flujo, explorador
ms.openlocfilehash: 2c5cb6ef917b7e799b8da3f1a769d77258866992
ms.sourcegitcommit: 2db596ab5a1ecd4901a8c893741cc4d06f6aecea
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923002"
---
# <a name="using-the-web-projector-to-stream-a-browser"></a>Uso del proyector web para transmitir un explorador

AltspaceVR Web Projector es una sólida solución de uso compartido de medios que permite transmitir una pestaña del explorador designada desde el equipo de escritorio directamente a AltspaceVR. Se puede usar para compartir diapositivas, vídeos, fotos y prácticamente cualquier otra cosa que pueda abrir desde un explorador.* El proyector web requiere la descarga de una extensión de explorador y actualmente está disponible exclusivamente a través del Editor del mundo. A continuación se muestra una introducción completa de la característica y cómo usarla:

## <a name="requirements"></a>Requisitos

1. Debe usar un equipo PC o Mac para transmitir el explorador.
2. La extensión de explorador necesaria es compatible actualmente con el explorador Edge. (Estamos trabajando para expandir esta lista).
3. Aunque puede transmitir desde un equipo Mac, el proyector web aún no está disponible en el cliente AltspaceVR Mac.
4. Si tiene todo configurado correctamente (ha iniciado sesión en la extensión del explorador/AltspaceVR con la misma cuenta, conectado o difundiendo con Web Proyector en AltspaceVR) y sigue viendo una pantalla verde, WebProjector necesita el puerto TCP 443 abierto y el intervalo de puertos UDP 20000-20400.

> [!NOTE]
> Esta característica está diseñada principalmente para transmitir una pestaña del explorador de su elección. Si en su lugar intenta transmitir la aplicación de escritorio, el proyector web transmitirá todo el audio del equipo (incluido AltspaceVR), lo que puede dar lugar a eco o comentarios. Tendrá que silenciar AltspaceVR para evitar que esto suceda. Como alternativa, también puede usar un dispositivo independiente para ejecutar AltspaceVR mientras transmite desde el equipo.

## <a name="getting-started"></a>Introducción

1. Para empezar, deberá descargar e instalar la extensión del explorador, que se puede encontrar [AQUÍ.](https://account.altvr.com/web_projector)
2. A continuación, [haga una instalación local de la extensión en el explorador Edge.](https://docs.microsoft.com/microsoft-edge/extensions-chromium/getting-started/extension-sideloading)
    * Una vez completada la descarga, vaya a la **sección Extensiones** del explorador. (Se encuentra en **Configuración**)
    * Descomprima el .zip archivo.
    * Activar el modo **de desarrollador y** seleccionar Cargar **desempaquetar**
    * Elija la carpeta que acaba de descomprimir. Se trata de la extensión Web Projector.
    * Una vez agregada la extensión, puede ir a **Detalles** para configurar la configuración.

## <a name="setting-up-a-shareable-browser"></a>Configuración de un explorador que se puede compartir

Una vez que la extensión se haya descargado e instalado, estará listo para usarla.

1. Abra una pestaña en el explorador Edge y vaya a los medios que quiera compartir.
2. Configure la ventana para que esté listo para compartirla. (Nota: Toda la ventana del explorador se proyectará en el mundo)
3. Busque la extensión recién instalada (que se muestra como un icono altspaceVR cerca de la barra de direcciones URL en el explorador). Seleccione AltspaceVR. Se le pedirá que inicie sesión en su cuenta. (*Nota: Es importante que inicie sesión en la misma cuenta que usará para configurar el proyector web).
4. Una vez que haya iniciado sesión, debería ver que la pantalla de extensión le ofrece la **opción Iniciar** streaming. Selecciónela.

## <a name="projecting-your-browser-in-world"></a>Proyección del explorador en el mundo

1. Una vez que el explorador esté configurado para la proyección y haya empezado a transmitir por secuencias a través de la extensión, abra AltspaceVR.
2. Para configurar el proyector web en el entorno que prefiera, abra el editor del mundo > Basics > Web Projector
3. Una vez colocado, puede usar los controles del Editor del mundo para cambiar el tamaño del proyector web. (También incluirá instrucciones, en pantalla).
4. Seleccione el **botón Conectar** para empezar a transmitir el explorador Edge.
5. No olvide hacer clic **en Difusión** para empezar a compartir con todos los invitados del espacio.
6. No olvide detener **streaming.** La sesión se terminará finalmente, pero hasta entonces seguirá proyectando en directo el explorador. Es mejor finalizar la sesión en cuanto haya terminado.

![Explorador proyectado en AltspaceVR world](images/web-project-img-01.png)

**Sugerencia de streaming de vídeo:** Si el vídeo se atascada, detenga el streaming, ajuste la calidad del vídeo a 480p o 360p y reinicie la transmisión y difusión. Las resoluciones más altas pueden sobrecargar la CPU y cargar el ancho de banda.

> [!NOTE]
> En este momento, los botones de control adicionales situados en la parte superior del proyector web aún no están en directo. Seguirán siendo grises y no se pueden hacer clic en ellos. Esto no es un error, es por diseño (por ahora).

> [!IMPORTANT]
> DECLINACIÓN DE RESPONSABILIDADES: El uso del proyector web, como todas las demás características de AltspaceVR, está sujeto a nuestros términos de servicio [y](../community/terms-of-service.md) a nuestros [estándares de la comunidad.](../community/community-standards.md) Por lo tanto, el proyector web no se puede usar para transmitir contenido que infracción de ninguno de los contratos. Esto dará lugar a acciones de moderación realizadas por AltspaceVR. No se garantiza el acceso a Web Projector Open Beta y solo se puede conceder para una evaluación temporal. La longitud de la versión beta y la duración de la participación están a discreción del equipo de AltspaceVR. No es necesario usar la versión beta del proyector web y la participación en la versión beta es puramente voluntaria. Se anima a los participantes a ofrecer comentarios sobre el proyector web que ayudarán a dar forma a la funcionalidad y facilidad de uso de la característica a medida que el desarrollo continúa. La versión beta del proyector web puede tener una funcionalidad limitada y puede estar sujeta a errores inesperados. Gracias, de antemano, por su participación.
