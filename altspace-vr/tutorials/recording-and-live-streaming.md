---
title: Grabación y streaming en vivo
description: Obtenga información sobre cómo grabar y transmitir en vivo los eventos AltspaceVR desde el equipo para promocionar y compartir con los usuarios.
ms.date: 04/26/2021
ms.topic: article
keywords: streaming, grabación, vídeo, audio, youtube, obs
ms.openlocfilehash: 95a742cb2bfe5c277e698175bd9f657fcac5923d181c3eeb6905004d25f81aa6
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126114"
---
# <a name="recording-and-live-streaming"></a>Grabación y streaming en vivo

Grabar y transmitir en vivo la experiencia altspaceVR para mostrar a otros usuarios de todo el mundo es una excelente manera de promocionar el evento, AltspaceVR y VR en general. Vea a continuación cómo empezar a trabajar:

En este artículo, aprenderá a:

* [Grabar AltspaceVR en modo 2D en pc](#recording-altspacevr-in-2d-mode-on-pc)
* [Streaming en vivo a YouTube en AltspaceVR en modo 2D en PC](#live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc)

## <a name="recording-altspacevr-in-2d-mode-on-pc"></a>Grabación de AltspaceVR en modo 2D en pc

### <a name="the-short-version"></a>La versión corta

1. Tener AltspaceVR y OBS instalados. Inicie AltspaceVR en modo 2D, inicie OBS, configure OBS para grabar AltspaceVR y grabarlo.

### <a name="the-slightly-longer-version"></a>La versión ligeramente más larga

1. Visite [https://obsproject.com/](https://obsproject.com/).
2. Seleccione **Windows** descargar OBS. Esta publicación usa **OBS v22.0.2**
3. Instalación de OBS

### <a name="have-altspacevr-running-in-2d-mode-before-you-run-obs"></a>Hacer que AltspaceVR se ejecute en modo 2D ANTES de ejecutar OBS

1. Descargue e instale AltspaceVR desde nuestro sitio web: [altvr.com/get](https://altvr.com/getaltspacevr)
2. Asegúrese de iniciar AltspaceVR en modo 2D desconéctese el cable USB de HMD del equipo o, si tiene una opción Deteniendo: Ctrl+Alt+Supr, Servicios, Servicio en tiempo de ejecución de Oculus VR, haga clic con el botón derecho y detenga. 
    * Esto deshabilitará Oculus e iniciará AltspaceVR en modo 2D, repetirá estos pasos y usará Iniciar para volver a obtener el modo VR.

Ahora, Alt-Tab a OBS:

1. En Orígenes, seleccione: **+ > Game Capture > Create New (Crear nuevo).**
2. Edite el texto a "AltspaceVR Capture", marque **Hacer que el origen sea visible** y seleccione Aceptar.
3. Haga doble clic en **Altspace CaptureVR en** Orígenes.
4. Cambiar **el modo** a La ventana específica de **captura**
5. Ventana: [AltspaceVR.exe]: AltspaceVR
6. Prioridad de coincidencia de ventana: coincide con el título; de lo contrario, busque la ventana del mismo archivo ejecutable.
7. Desplácese hacia abajo hasta El cursor de captura: desenlaza
8. Seleccione OK (Aceptar).

Esto debería hacer que AltspaceVR se muestre en OBS. Ahora, para establecer las siguientes propiedades en OBS, vaya **a Archivo > Configuración**:

|Pestaña|Configuración|
|---|---|
| **General** | Deje el valor predeterminado. |
| **Stream** | Deje el valor predeterminado. |
| Modo de salida | Cambiar a Avanzado |
| Pestaña Streaming | Pista de audio 1 <br> Codificador: x264 <br> Volver a escalar la salida: sin tics <br> Control de velocidad: CBR <br> Velocidad de bits: 6000 (6000 para 30 fps o 9000 para 60 fps) <br> Intervalo de fotogramas clave = 2 <br> Valor preestablecido de uso de CPU = muy rápido |
| Pestaña Grabación | Tipo: Estándar <br> Ruta de acceso de grabación: D:/Video (Vaya a donde desea que se guarde el archivo de vídeo) <br> Formato de grabación: mp4 (si se produce algún bloqueo durante la grabación, pruebe aquí, en lugar de mp4, si bloquea el vídeo todavía se podrá usar con el disco). <br> Pista de audio 1 <br> Codificador: Uso del codificador de secuencia |
| Pestaña Audio | Velocidad de bits de audio: 160 (para todas las pistas) |
| Pestaña Búfer de reproducción | Deje el valor predeterminado. |
| **Audio** | Frecuencia de muestreo: 48 khz <br> Canales: Estéreo <br> Dispositivo de audio de escritorio: valor predeterminado <br> Dispositivo de audio de escritorio 2: Deshabilitar <br> Dispositivo de audio micrófono/auxiliar: valor predeterminado |
| **Vídeo** | Resolución base (lienzo): 1920 x 1080 <br> Resolución de salida (escalado): 1920 x 1080 <br> Filtro de reducción vertical: biábica (escalado con aumento, 16 ejemplos) <br> Valores comunes de FPS: 30 |
| **Teclas de acceso rápido** | Deje el valor predeterminado. |
| **Avanzadas** | Prioridad del proceso: Normal | <br>

<br>Ahora, asegúrese de seleccionar **Aplicar** y, a **continuación,** aceptar para guardar toda la configuración de OBS. 

1. Alt-Tab a AltspaceVR, entra en el espacio, el mundo o el evento correctos y alinea la cámara (es decir, tu avatar), estamos a punto de grabar un vídeo.
2. Alt-Tab a OBS y, cuando esté listo, haga clic **en Iniciar grabación.**

Verá en la parte inferior derecha de OBS que REC: empezará a contar y el punto es rojo, lo que significa que está grabando.

Realice una grabación de prueba de esto: 
1. En AltspaceVR, abra, cierre o suba los menús para hacer sonidos de la interfaz de usuario.
2. Asegúrese de que no está conmutado, diga "Sibilance, Sibilance" u haga que otro usuario hable con usted en un volumen normal.
3. Consulte los niveles Audio de escritorio y Micrófono/Auxiliar mientras lo hace para ver si funciona.

Normalmente se silencia el micrófono o auxiliar al grabar. Vaya y seleccione el icono del hablante para Mic/Aux y se volverá rojo con una X.

* Es muy difícil hacer coincidir el audio y el audio del otro usuario, por lo que el micrófono se silencia mejor cuando se graba un evento.
* Otro problema con el audio es la forma en que se configura OBS. Captura TODO el audio del equipo, por lo que si está viendo YouTube en el equipo, grabará ese audio o las notificaciones de discordia.
* Para grabar solo el audio desde AltspaceVR, vaya a Volumen Mixer (haga clic con el botón derecho en el icono del hablante situado en la parte inferior derecha de Windows) y silencie los sonidos del sistema, los exploradores, y así sucesivamente, pero no mute OBS ni AltspaceVR.

> [!IMPORTANT]
> No olvide volver a activar esta configuración de Mixer volumen después de la grabación.

Ahora, vuelva a OBS y seleccione **Detener** grabación en File>Show Recordings (Mostrar **grabaciones).** Se abrirá la carpeta con los archivos de vídeo de OBS y se hace doble clic en el vídeo de prueba.

A veces, la grabación es bastante alta, por lo que reduce el control deslizante de Audio de escritorio y realiza otra grabación para probar.


## <a name="live-streaming-to-youtube-in-altspacevr-2d-mode-on-pc"></a>Streaming en vivo a YouTube en modo AltspaceVR 2D en PC

### <a name="the-short-version"></a>La versión corta

Tener AltspaceVR y OBS instalados. Inicie AltspaceVR en modo 2D, inicie OBS, ya sea en streaming en vivo o cree un "Nuevo evento en directo" en YouTube, configure OBS con la clave de secuencia de YouTube, empiece a transmitir en OBS, empiece a transmitir en YouTube y va a las carreras.

### <a name="the-slightly-longer-version"></a>La versión ligeramente más larga

1. Visite [https://obsproject.com/](https://obsproject.com/).
2. Seleccione **Windows** para descargar OBS (esta publicación usa OBS v22.0.2)
3. Instalación de OBS

Hacer que AltspaceVR se ejecute en modo 2D ANTES de ejecutar OBS
1. Descargue AltspaceVR desde nuestro sitio web: [https://account.altvr.com/downloads](https://account.altvr.com/downloads)
2. Para asegurarse de que inicia AltspaceVR en modo 2D, desconecte el cable USB de HMD del equipo o si tiene una opción Detente: Ctrl+Alt+Supr, Servicios, Servicio en tiempo de ejecución de Oculus VR, haga clic con el botón derecho en Detener. Esto deshabilitará Oculus Home e iniciará AltspaceVR en modo 2D, repetirá estos pasos e iniciará para volver a obtener el modo VR.

3. Alt-Tab a OBS

4. En Orígenes, seleccione **+** , Seleccione Game Capture, Crear nuevo, Edit text to 'AltspaceVR Capture' (Editar texto en 'AltspaceVR Capture'), marque Make source visible (Hacer visible el origen), OK (Aceptar).
5. Haga doble clic en Altspace CaptureVR
6. Modo: ventana específica de captura
7. Ventana: [AltspaceVR.exe]: AltspaceVR
8. Prioridad de coincidencia de ventana: coincide con el título; de lo contrario, busque la ventana del mismo archivo ejecutable.
9. Desplácese hacia abajo hasta El cursor de captura: desenlaza Aceptar

Esto debería hacer que AltspaceVR se muestre en OBS. ¡Perfecto!

Ahora, en OBS, va a File>Configuración:

| Pestaña | Configuración |
|---|---|
| General | Marcar Registro automático al transmitir (esto registra un archivo de vídeo en el equipo además del streaming en vivo) |
| STREAM | Tipo de secuencia: Servicios de streaming <br> Servicio: YouTube/YouTube Gaming (también se puede transmitir en streaming aTube, Mixer, Facebook Live, etc.)<br>Servidor: servidor de ingesta de YouTube principal <br>Clave de secuencia: pegue la clave de streaming desde YouTube( (consulte "Configuración del streaming en vivo en YouTube" a continuación). |
| Salida | Modo de salida: cambiar a Avanzado |
| Streaming | Pista de audio 1 <br>Codificador: x264 <br>Aplicación de la configuración del codificador del servicio de streaming: tick <br>Volver a escalar la salida: sin tics <br>Control de velocidad: CBR <br>Velocidad de bits: 6000 (6000 para 30 fps o 9000 para 60 fps) <br>Intervalo de fotogramas clave = 2 <br>Valor preestablecido de uso de CPU = muy rápido |
| Grabación | Tipo: Estándar <br>Ruta de acceso de grabación: D:/Video (vaya a donde desea que se guarde el archivo de vídeo si seleccionó "Grabar automáticamente al transmitir" anteriormente). <br>Formato de grabación: mp4 (si se produce algún bloqueo durante la grabación, pruebe aquí, en lugar de mp4, si bloquea el vídeo todavía se podrá usar con el disco). <br>Pista de audio 1 <br>Codificador: Uso del codificador de secuencia |
| Audio | Velocidad de bits de audio: 160 (para todas las pistas) Frecuencia de muestreo: 48 khz <br>Canales: Estéreo <br>Dispositivo de audio de escritorio: valor predeterminado <br>Dispositivo de audio de escritorio 2: Deshabilitar <br>Dispositivo de audio micrófono/auxiliar: valor predeterminado |
| Búfer de reproducción | Deje el valor predeterminado. |
| Vídeo | Resolución base (lienzo): 1920 x 1080 <br>Resolución de salida (escalado): 1920 x 1080 <br>Filtro de reducción vertical: biábica (escalado con aumento, 16 ejemplos) <br>Valores comunes de FPS: 30 |
| Teclas de acceso rápido | Deje el valor predeterminado. |
| Avanzado | Prioridad del proceso: Normal |
|||

<br>Ahora, asegúrese de hacer clic en Aplicar y, después, en Aceptar y, a continuación, cierre y vuelva a abrir OBS. Esto guardará toda la configuración de OBS. Se ve bien :)

Consulte la sección anterior "Cómo grabar AltspaceVR en modo 2D en PC" para obtener instrucciones sobre cómo probar la grabación mediante una grabación local en lugar de la secuencia en vivo y también cómo configurar primero la toma de cámara antes de grabar.

Otro problema con el audio es la forma en que se configura OBS. Captura TODO el audio del equipo, por lo que si está viendo YouTube, grabará ese audio, o Teams mensajes o sonidos de notificación.

Para grabar solo el audio desde AltspaceVR, vaya a Volumen Mixer (haga clic con el botón derecho en el icono del hablante situado en la parte inferior derecha de Windows) y Mute System Sounds, Browsers, and así sucesivamente, pero no mute OBS ni AltspaceVR.

No olvide volver a activar el audio después de grabar ;)

Le complace que sea una grabadora de vídeo AltspaceVR.

## <a name="setting-up-live-streaming-on-youtube"></a>Configuración del streaming en vivo en YouTube

Puede hacer que una secuencia en directo se transmita rápidamente **(Stream)** o configurar un evento de streaming en vivo futuro **(Administrar).** Podría sugerirle que lo configure de la manera "Administrar".

1. Abra el explorador, inicie sesión [https://www.youtube.com/](https://www.youtube.com/) y, a continuación, vaya a [https://www.youtube.com/my_live_events](https://www.youtube.com/my_live_events)
2. Seleccione en el icono Cuenta, en la parte superior derecha, seleccione Creator Studio en la lista desplegable.
3. STREAMING EN VIVO en el lado izquierdo de la página.

'**Stream now**' (Método):

* Seleccione EDITAR para escribir la información de streaming en vivo.<br>
* En Stream Configuración, mantenga los valores predeterminados.<br>
* Clave de secuencia (pegar en el codificador), seleccione "Reveal" y copie esta clave para que pueda pegarla en OBS.<br>
* Abrir OBS/Configuración/Stream<br>
* Pegue la clave de secuencia de YouTube en el campo Stream Key (Clave de transmisión) en OBS.<br>
* Aplicar y, a continuación, Aceptar<br>
* Seleccione Start Streaming in OBS (Iniciar streaming en OBS).<br>
* Cambie a YouTube y verá que ahora está en directo en YouTube.<br>
* Para ver la página de vídeo real de YouTube Live Stream, deberá seleccionar el icono COMPARTIR en la parte superior derecha.<br>
* Copie y pegue el "vínculo de vídeo" en una nueva pestaña del explorador; verá la página de streaming en vivo de YouTube.<br>
* Esta dirección URL es el vínculo de streaming en vivo y se puede compartir con todos los canales de redes :)<br>
* Para detener la transmisión en vivo, seleccione Detener streaming en OBS, lo que finalizará la transmisión en vivo en YouTube.<br>
* A continuación, detenga la transmisión en YouTube.<br>

'**Manage**' (Método):
* Seleccione "Schedule Stream" (Programar secuencia).
* Cree una nueva o Configuración si ya ha configurado una transmisión en vivo administrada anterior.
* Agregar título, fecha, hora de inicio, descripción, Upload miniatura y etiquetas: no olvide etiquetar AltspaceVR :)
* Elija Público en el menú desplegable (el valor predeterminado es "Unlisted")
* Usar predeterminados
* Copiar la clave stream (pegar en el codificador)
* Para ver la página de vídeo real de YouTube Live Stream, deberá seleccionar el icono COMPARTIR en la parte superior derecha. Este es el vínculo del evento de streaming en vivo de YouTube, que se puede compartir en redes sociales antes que el evento real.
* Ahora abra OBS.
* Archivo/Configuración
* STREAM
* Pegue la clave de secuencia que copió en el campo Stream Key (Clave de secuencia).
* Aplicar y, a continuación, Aceptar
* Seleccione "Iniciar streaming".
* De vuelta a YouTube, verá que la ventana "Versión preliminar" muestra la transmisión y GO LIVE ahora está encendido en la parte superior derecha.
* Selección de GO LIVE
* Ya está en directo.
* Vaya a la pestaña del explorador con el vínculo "Ver en la página de la vista" abierto para asegurarse de que el vídeo se ve bien. RECUERDE que no escuchará el audio porque ha desactivado el audio de los exploradores al silenciarlos en Windows volumen Mixer. Compruebe el audio del teléfono o pida a un amigo que compruebe el audio por usted.
* ¡Se ve bien!
* Alt-Tab a AltspaceVR para mover la cámara (es decir, su Avatar) en el evento.
* Cuando haya terminado con la transmisión en vivo, vuelva a la página "Live Control Room" de YouTube.
* Seleccione "Detener streaming".
* Se abre el cuadro de diálogo en el que se le pregunta si quiere dejar de transmitir el evento en directo, aceptar.
* Vaya a OBS y seleccione Detener streaming también.
* Gracias, ahora es un streamer AltspaceVR.

Para obtener puntos extra, comparta sus vídeos con el mundo en las redes sociales y asegúrese de @AltspaceVR etiquetarnos :)