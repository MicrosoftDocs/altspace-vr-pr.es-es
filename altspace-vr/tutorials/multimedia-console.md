---
title: Uso de la consola multimedia
description: Aprenda a configurar, publicar y controlar la consola multimedia en sus experiencias altspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: consola, multimedia
ms.openlocfilehash: 4a51ff76e44d3870972bc17288ae77c1fa888922
ms.sourcegitcommit: 2db596ab5a1ecd4901a8c893741cc4d06f6aecea
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923012"
---
# <a name="using-the-multimedia-console"></a>Uso de la consola multimedia

La consola multimedia es una herramienta que permite compartir contenido multimedia en eventos y mundos. Puede usarlo para compartir cosas como imágenes, diapositivas de presentación, secuencias en vivo, vídeos, listas de reproducción, etc. A continuación se muestra una instrucción paso a paso sobre cómo usar la consola multimedia **v0.5.0+**. 

## <a name="getting-started"></a>Introducción

La introducción a la consola multimedia es un proceso de dos partes.  En primer lugar, está el portal web que usará para generar y publicar una configuración para la sesión de la consola multimedia que coloque en su entorno.  En segundo lugar, se coloca la aplicación de consola multimedia real en su entorno y se establece el código de configuración que debe usar.

### <a name="configuring-the-multimedia-console-with-the-web-portal"></a>Configuración de la consola multimedia con el portal web

1. En primer lugar, deberá asegurarse de que el contenido se hospeda en línea porque necesitará una dirección URL. (Puede cargar fotos en altvr.com, hospedar un archivo de .mp4 en línea o usar un vínculo de streaming en vivo de Dlive: https://dlive.tv/yourlivestream) 
2. Vaya al portal web de la consola multimedia en [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)
3. Desde el portal web, puede generar y publicar una configuración para la consola multimedia.  (Consulte a continuación para obtener más información sobre las distintas propiedades).
4. Una vez que haya escrito los medios en la lista de medios y haya configurado la configuración general, seleccione el botón Publicar en la parte superior derecha de la aplicación.
5. Una vez completada la publicación, aparecerá un cuadro de diálogo con un código de dos palabras para que escriba en la consola multimedia que ha colocado.
  
### <a name="placing-the-multimedia-console-in-your-environment"></a>Colocación de la consola multimedia en su entorno

1. Seleccione en World Editor > Editor Panel > SDK Apps > Multimedia Console (Aplicaciones **> multimedia).** (No vaya a World **Editor > Basics > SDK App**,es decir, para las aplicaciones no registradas).  
2. Coloque la consola multimedia en el mejor conjunto de su espacio y audiencia.
3. Salga del modo de edición haciendo clic en el botón naranja Modo de edición.
4. Se le preguntará **¿Es el propietario del reproductor multimedia?** Si es la persona que debe ser el propietario oficial de esta sesión de consola multimedia, confirme y continúe. (También hay otros roles con permisos disponibles. Consulte a continuación una lista detallada).
5. Seleccione Sí para confirmar que es el host principal.  
6. Debería abrirse un cuadro de diálogo que le pide que escriba un código desde el portal web o UN JSON válido.  Escriba el código de dos palabras desde el portal web, incluido el guion, y presione Aceptar. (JSON es una configuración avanzada que se describe a continuación)
7. La consola multimedia debe cargarse después de unos segundos con la configuración que creó en el portal web.

### <a name="controlling-the-multimedia-console"></a>Control de la consola multimedia

1. Después de introducir el código y completar el proceso de configuración, verá que los botones de control aparecen debajo de una pantalla multimedia. 
    * **La reproducción** inicia el visor multimedia (o se reinicia en la entrada actual, si se ha detenido previamente). 
    * **Detener** detiene el visor multimedia y oculta los medios actuales.  
    * **Next/Prev** omite los medios siguientes o anteriores 
    * **x/x**   muestra el índice actual en la lista de medios y le permite saltar a cualquier punto de la lista.
    * **La** configuración permite volver a escribir un nuevo código desde el portal web para establecer una nueva configuración en la consola. 

Ahora está listo para empezar a compartir a través de la consola multimedia.  
 
## <a name="working-with-the-web-portal"></a>Trabajo con el portal web

El portal web es una aplicación web que permite configurar las distintas características de la consola multimedia.  Estas características se incluyen en dos categorías: configuración general de la consola multimedia y la lista de reproducción multimedia.

### <a name="multimedia-console-general-settings"></a>Configuración general de la consola multimedia

**Configuración de reproducción**

Configuración general de reproducción para la lista de elementos multimedia

* **Lista de medios de** bucle: determina si la lista de elementos multimedia debe recorrerse en bucle una vez que llegue al final de la lista.
* **Método Start:** selecciona el método por el que se debe iniciar la consola multimedia.
    * Manual: espera a que se presione el botón de reproducción antes de iniciar el medio.
    * Inicio automático desde el principio: inicio automático de la lista de medios desde el principio de la lista
    * Inicio automático aleatorio: inicia automáticamente el medio desde un punto inicial aleatorio de la lista.

**Roles**

Asignaciones de roles para controlar y configurar la consola multimedia.    Estos roles se desglosan en el siguiente conjunto:

* **Solo propietario:** el usuario que es el propietario de la sesión de consola multimedia
* **Usuarios con privilegios** elevados: usuarios que tienen roles de moderador o host en el espacio en el que se configuró originalmente la consola multimedia
* **Todos los usuarios:** todos los usuarios

Estos roles se apilan en el sentido de que todos los roles por encima del elegido en esta lista también tendrán permiso para usar esa característica.  Ejemplo: **Los usuarios con** privilegios elevados incluyen el propietario incluso si no son un moderador o host** en AltspaceVR.  Las características controladas por asignaciones de roles son las siguientes:

* **Puede controlar el reproductor multimedia:** determina qué roles pueden controlar los botones de reproducción multimedia de la consola multimedia.
* **Puede configurar el reproductor multimedia:** determina qué roles pueden configurar la consola multimedia con el acceso al **botón Config (Configuración).**

### <a name="adding-photos-and-videos-to-the-media-list"></a>Adición de fotos y vídeos a la lista de medios

Los medios son el núcleo de la consola multimedia.  Las imágenes y los vínculos de vídeo se admiten como tipos de medios en la consola multimedia.  Para agregar nuevos medios,  seleccione  los iconos Agregar imagen o Agregar vídeo para que se haga emergente un cuadro de diálogo para especificar la información y la configuración multimedia.  A continuación se muestra el desglose de los tipos de medios y la configuración asociada.

**Image**

Las imágenes deben ser un tipo de imagen estándar, como jpeg, png e son on. Deben hospedarse en algún lugar con un vínculo público.

* **Nombre:** nombre (obligatorio) con el que desea identificar la imagen.
* **Dirección URL de** la imagen: (obligatorio) La dirección URL pública de la imagen
* **Omitir después:** número de segundos después de los que se debe omitir la imagen

**Vídeo**

Los vídeos se pueden hospedar en vídeos o transmisiones en vivo a través de La tracción y DLive.  (Otra compatibilidad puede funcionar con trabajo adicional para obtener la dirección URL de secuencia adecuada, pero no es totalmente compatible en la consola multimedia)

* **Nombre:** nombre (obligatorio) con el que desea identificar el vídeo.
* **Dirección URL del** vídeo: (obligatorio) Dirección URL pública en la que se hospeda el vídeo o desde la que se sirve el streaming en vivo.
* **Omitir después:** número de segundos después del que se debe omitir el vídeo

> [!NOTE]
> OBLIGATORIO: coloque el tiempo que coincida con la longitud del vídeo para permitir que los vídeos se reenván correctamente. Por ejemplo, si el vídeo tiene una duración de 5 minutos, ponga 300 segundos, de lo contrario, el vídeo no saltará al siguiente fragmento de contenido.

* **Volumen:** el volumen del vídeo de 0 (min) a 1 (máx.) valores.
* **Hora de** inicio: número de segundos a partir del principio del vídeo.
* **Roll Off Start Distance :la** distancia en metros del mundo en la que el volumen comienza a despegar cuando se aleja de la consola multimedia
* **Final de la acción de vídeo:** la acción que se debe realizar una vez que se alcanza el final del vídeo.
    * Detener: la lista de elementos multimedia se detiene una vez finalizado el vídeo
    * Bucle: el vídeo se recorrerá en bucle hasta que se omita manualmente.
    * Reproducir siguiente: el siguiente medio de la lista de elementos multimedia se inicia una vez que finaliza el vídeo actual.

## <a name="working-with-json-directly-advancedoptional"></a>Trabajar directamente con JSON (avanzado/opcional)

La consola multimedia admite la introducción de JSON directamente en el símbolo del sistema de la consola en AltspaceVR.  JSON es el mecanismo interno con el que se habilitan las configuraciones del reproductor multimedia. Exponer la capacidad de establecer JSON directamente es algo que permite a los usuarios más avanzados crear sus propios flujos de trabajo que se ajusten a sus necesidades y familiaridad con JSON.  A continuación se muestra una breve descripción de la estructura JSON y el esquema por el que se valida el JSON. Para obtener descripciones más detalladas de las propiedades siguientes, consulte las secciones anteriores en las que se explica cómo configurar la consola multimedia.  Esta sección se centra principalmente en los ejemplos de esquema y la estructuración de los datos JSON.

### <a name="global-media-settings"></a>Configuración de medios globales

```json
{
  "loopMediaList": true | false
  "startMethod": "manual" | "autostart-beginning" | "autostart-random"
  "controlMediaPlayer": "everyone" | "elevated" | "owner"
  "configureMediaPlayer": "elevated" | "owner"
  ...
}
```

### <a name="media-list"></a>Lista de elementos multimedia

La lista de elementos multimedia es una propiedad establecida en la raíz de la estructura JSON, como roles y configuración de reproducción.  Se trata de una matriz simple que puede contener una de las siguientes estructuras de configuración de medios. (Consulte las descripciones de propiedades anteriores para obtener más información sobre lo que hace cada uno).

**Ejemplo de imagen**

*Campos obligatorios: "name" e "imageUrl"*

```json
{
    "name": "Altspace Screenshot",
    "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
    "skipAfter": 10
}
```

**Ejemplo de vídeo**

*Campos obligatorios: "name" y "videoUrl"*

```json
{
    "name": "Ninja Twitch Live Stream",
    "videoUrl":"https://www.twitch.tv/ninja",
    "volume":0.2,
    "startTime":0,
    "endOfVideoAction":"play-next"
}
```

### <a name="example-json"></a>Ejemplo de JSON

```json
{
  "loopMediaList": false,
  "startMethod": "autostart-beginning",
  "controlMediaPlayer": "everyone",
  "configureMediaPlayer": "elevated",
  "mediaList": [
    {
      "videoUrl": "https://www.twitch.tv/ninja",
      "volume": 0.2,
      "startTime": 0,
      "endOfVideoAction": "play-next"
    },
    {
      "imageUrl": "http://www.hypergridbusiness.com/wp-content/uploads/2016/09/AltspaceVR-highrise.jpg",
      "skipAfter": 10
    },
    {
      "imageUrl": "https://d1qb2nb5cznatu.cloudfront.net/startups/i/333629-6ffd7199b9bcf34d8957e8e09d974a38-medium_jpg.jpg?buster=1423092095",
      "skipAfter": 5
    },
    {
      "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
      "skipAfter": 10
    },
    {
      "imageUrl": "https://altvr-wpengine.netdna-ssl.com/wp-content/uploads/2019/05/Educators-in-VR-Social-VR-AltspaceVR.png",
      "skipAfter": 10
    },
    {
      "videoUrl": "https://www.twitch.tv/shroud",
      "volume": 1,
      "startTime": 0,
      "endOfVideoAction": "stop"
    }
  ]
}
```

### <a name="schema"></a>Schema

```json
{
  "$schema": "https://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": [
    "mediaList"
  ],
  "properties": {
    "loopMediaList": {
      "type": "boolean",
      "description": "Whether to loop through the media list when reaching the beginning or end of the list."
    },
    "controlMediaPlayer": {
      "type": "string",
      "enum": [
        "everyone",
        "elevated",
        "owner"
      ],
      "default": "owner",
      "description": "What roles are able to control the media player. (Owner can always control player)"
    },
    "configureMediaPlayer": {
      "type": "string",
      "enum": [
        "elevated",
        "owner"
      ],
      "default": "owner",
      "description": "What roles are allowed to configure the media play list.  Note: This role needs to be able to control the media player in order to configure it. (Owner can always configure media)"
    },
    "startMethod": {
      "type": "string",
      "enum": [
        "manual",
        "autostart-beginning",
        "autostart-random"
      ],
      "default": "manual",
      "description": "The method by which the media player should start"
    },
    "mediaList": {
      "description": "A list of images or videos to configure the media player to operate on.",
      "type": "array",
      "items": {
        "oneOf": [
          {
            "title": "Image",
            "type": "object",
            "description": "Configuration for an image media.",
            "properties": {
              "imageUrl": {
                "type": "string",
                "description": "The url for the image to load."
              },
              "skipAfter": {
                "type": "number",
                "minimum": 5,
                "default": null,
                "description": "The number of seconds that should pass before skipping to the next media. (Minimum 5)."
              }
            },
            "required": [
              "imageUrl"
            ]
          },
          {
            "title": "Video",
            "type": "object",
            "description": "Configuration for a video media.",
            "properties": {
              "videoUrl": {
                "type": "string",
                "description": "The url of the video to load."
              },
              "skipAfter": {
                "type": "number",
                "minimum": 5,
                "default": null,
                "description": "The number of seconds that should pass before skipping to the next media. (Minimum 5)."
              },
              "volume": {
                "type": "number",
                "minimum": 0,
                "maximum": 1,
                "default": null,
                "description": "The volume to play the video at. (Minimum 0, maximum 1)"
              },
              "startTime": {
                "type": "number",
                "minimum": 0,
                "default": null,
                "description": "The time in seconds from the start of the video to begin playing the video at. (Minimum of 0)"
              },
              "rolloffStartDistance": {
                "type": "number",
                "minimum": 0,
                "default": null,
                "description": "The distance in meters away from the media player that the volume will begin to fall off. (Minimum 0)"
              },
              "endOfVideoAction": {
                "type": "string",
                "enum": [
                  "stop",
                  "loop",
                  "play-next"
                ],
                "default": null,
                "description": "The type of action to take at the end of the video."
              }
            },
            "required": [
              "videoUrl"
            ]
          }
        ]
      }
    }
  }
}
```

> [!NOTE]
> Actualizado con la consola multimedia v0.5.0