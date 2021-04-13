---
title: Uso de la consola multimedia
description: Obtenga información sobre cómo empezar a configurar, publicar y controlar la consola multimedia en sus experiencias de AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: consola, multimedia
ms.openlocfilehash: 601328eb6f266dbcfc9d81fc4f1c2d09ac62b318
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213702"
---
# <a name="using-the-multimedia-console"></a>Uso de la consola multimedia

La consola multimedia es una herramienta que permite compartir multimedia en eventos y mundos. Puede usarlo para compartir elementos como imágenes, diapositivas de presentación, livestreams, vídeos, listas de reproducción, etc. A continuación se muestran instrucciones paso a paso sobre cómo usar la consola multimedia **v 0.5.0 +**. 

## <a name="getting-started"></a>Introducción

La introducción a la consola multimedia es un proceso de dos partes.  En primer lugar, se usará el portal web para generar y publicar una configuración de la sesión de la consola multimedia que se coloca en el entorno.  La segunda es la ubicación de la aplicación de consola multimedia real en su entorno y el establecimiento del código de configuración que debe usar.

### <a name="configuring-the-multimedia-console-with-the-web-portal"></a>Configuración de la consola multimedia con el portal web

1. En primer lugar, debe asegurarse de que el contenido está hospedado en línea porque necesitará una dirección URL. (Puede cargar fotografías en altvr.com, hospedar un archivo. MP4 en línea o usar Twitch live stream link: https://www.twitch.tv/ninja) 
2. Vaya al portal web de la consola multimedia en [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)
3. En el portal web, puede generar y publicar una configuración para la consola multimedia.  (Consulte a continuación para obtener más información sobre las distintas propiedades).
4. Una vez que haya escrito el medio en la lista de medios y haya configurado la configuración general, seleccione el botón publicar en la parte superior derecha de la aplicación.
5. Una vez completada la publicación, aparecerá un cuadro de diálogo con un código de dos palabras para que pueda escribir en la consola multimedia que ha colocado.
  
### <a name="placing-the-multimedia-console-in-your-environment"></a>Colocación de la consola multimedia en el entorno

1. Seleccione en el **Editor mundial > panel del editor > aplicaciones SDK > consola multimedia**. (No vaya al **Editor mundial > basics > aplicación de SDK**, que es para aplicaciones no registradas).  
2. Coloque la consola multimedia para el mejor conjunto de su espacio y audiencia.
3. Para salir del modo de edición, haga clic en el botón modo de edición naranja.
4. ¿Se le solicitará **el propietario del reproductor de media?** Si es la persona que debe ser la propietaria oficial de esta sesión de la consola multimedia, confirme y continúe. (También están disponibles otros roles con permisos. A continuación se muestra una lista detallada).
5. Seleccione Sí para confirmar que es el host principal.  
6. Aparecerá un cuadro de diálogo que le pide que escriba un código desde el portal web o un archivo JSON válido.  Escriba el código de dos palabras del portal web, incluido el guión y presione Aceptar. (JSON es una configuración avanzada que se describe a continuación).
7. La consola multimedia debe cargarse después de unos segundos con la configuración generada en el portal web.

### <a name="controlling-the-multimedia-console"></a>Controlar la consola multimedia

1. Después de escribir el código y completar el proceso de configuración, verá que aparecen botones de control debajo de una pantalla de medios. 
    * **Play** inicia el visor de medios (o se reinicia en la entrada actual, si se detuvo previamente) 
    * **Detener** detiene el visor multimedia y oculta los medios actuales.  
    * **Siguiente/anterior** omite el siguiente o el medio anterior 
    * **x/x**   muestra el índice actual en la lista de medios y le permite saltar a cualquier punto de la lista.
    * La **configuración** permite volver a escribir un nuevo código desde el portal web para establecer una nueva configuración en la consola. 

Ahora está listo para empezar a compartir a través de la consola multimedia.  
 
## <a name="working-with-the-web-portal"></a>Trabajar con el portal web

El portal web es una aplicación web que permite configurar las distintas características de la consola multimedia.  Estas características se dividen en dos categorías: configuración general de la consola de medios y la lista de reproducción de medios.

### <a name="multimedia-console-general-settings"></a>Configuración general de la consola multimedia

**Configuración de reproducción**

Configuración de reproducción general para la lista de medios

* **Lista de medios de bucle**: determina si la lista de medios debe repetirse una vez que llegue al final de la lista.
* **Método de inicio** : selecciona el método por el que debe comenzar la consola multimedia.
    * Manual: espera a que se presione el botón de reproducción antes de iniciar el medio
    * Inicio automático desde Inicio: inicia automáticamente la lista de medios desde el principio de la lista.
    * Inicio automático automático: inicia el medio automáticamente desde un punto de Inicio aleatorio de la lista.

**Roles**

Asignaciones de roles para controlar y configurar la consola multimedia.    Estos roles se dividen en el siguiente conjunto:

* **Solo propietario** : el usuario que es el propietario de la sesión de la consola multimedia
* **Usuarios con privilegios elevados** : los usuarios que tienen roles de moderador, host o moderador en el espacio en el que está configurada originalmente la consola multimedia
* **Todos los usuarios** -todos los usuarios

Estos roles se apilan en el sentido de que a todos los roles por encima del que se elija en esta lista también se les concederá permiso para usar esa característica.  Ejemplo: **usuarios con privilegios elevados** incluye el **propietario** aunque no sea un moderador, un host o un presentador * * en AltspaceVR. Las características que se controlan mediante asignaciones de roles son las siguientes:

* **Puede controlar el reproductor de media** : determina qué roles pueden controlar los botones de reproducción multimedia para la consola multimedia
* **Puede configurar el reproductor de media** : determina qué roles pueden configurar la consola multimedia mediante el acceso al botón **config** .

### <a name="adding-photos-and-videos-to-the-media-list"></a>Agregar fotos y vídeos a la lista de medios

El medio es el corazón de la consola multimedia.  Las imágenes y los vínculos de vídeo se admiten como tipos de medios en la consola multimedia.  Para agregar nuevos medios, seleccione los iconos **Agregar imagen** o **Agregar vídeo** para que aparezca un cuadro de diálogo para especificar la configuración y la información multimedia.  A continuación se muestra el desglose de los tipos de medios y la configuración asociada

**Imagen**

Las imágenes deben ser un tipo de imagen estándar, como JPEG, PNG y hijo. Deben hospedarse en algún lugar con un vínculo público.

* **Nombre** : (obligatorio) nombre con el que desea identificar la imagen.
* **URL** de la imagen: (obligatorio) dirección URL pública de la imagen
* **Omitir después** del número de segundos que se debe omitir la imagen después de

**Vídeo**

Los vídeos pueden ser vídeos hospedados o secuencias en directo a través de Twitch y DLive.  (Otra compatibilidad puede funcionar con el trabajo adicional para obtener la dirección URL de flujo adecuada, pero no es totalmente compatible con la consola multimedia).

* **Nombre** : (obligatorio) nombre con el que desea identificar el vídeo.
* **URL de vídeo** : (obligatorio) dirección URL pública a la que se hospeda el vídeo o desde la que se sirve la secuencia en directo.
* **Omitir después** del número de segundos que se debe omitir el vídeo después
* **Volumen** : el volumen del vídeo con valores 0 (min)-1 (máx.).
* **Hora de inicio** : el número de segundos desde el principio del vídeo comienza desde.
* Poner al **día la distancia de inicio** : la distancia en metros en que el volumen comienza a pasar a medida que sale de la consola multimedia
* **Acción de fin de vídeo** : la acción que se realizará una vez que se alcance el final del vídeo.
    * Detener: la lista de medios se detiene una vez finalizado el vídeo
    * Loop: el vídeo se repetirá hasta que se omita manualmente
    * Reproducir siguiente: el siguiente medio en la lista de medios se iniciará después de que finalice el vídeo actual.

## <a name="working-with-json-directly-advancedoptional"></a>Trabajar directamente con JSON (avanzado/opcional)

La consola multimedia permite escribir JSON directamente en el símbolo del sistema de la consola de AltspaceVR.  JSON es el mecanismo interno con el que se habilitan las configuraciones del reproductor de media. Exponer la capacidad de establecer directamente JSON es algo que permite a los usuarios más avanzados crear sus propios flujos de trabajo que se adapten a sus necesidades y que estén familiarizados con JSON.  A continuación se describe una breve descripción de la estructura JSON y el esquema por el que se valida el JSON. Para obtener descripciones más detalladas de las propiedades siguientes, vea las secciones anteriores que tratan sobre la configuración de la consola multimedia.  Esta sección se centra principalmente en los ejemplos de esquema y la estructura de los datos JSON.

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

### <a name="media-list"></a>Lista de medios

La lista de medios es una propiedad establecida en la raíz de la estructura JSON, como los roles y la configuración de reproducción.  Es una matriz simple que puede contener una de las siguientes estructuras de configuración de medios. (Consulte las descripciones de propiedades anteriores para obtener más información sobre lo que hace cada uno).

**Ejemplo de imagen**

*Campos obligatorios: "Name" y "imageUrl"*

```json
{
    "name": "Altspace Screenshot",
    "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
    "skipAfter": 10
}
```

**Ejemplo de vídeo**

*Campos obligatorios: "Name" y "videoUrl"*

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
> Actualizado con la consola multimedia v 0.5.0