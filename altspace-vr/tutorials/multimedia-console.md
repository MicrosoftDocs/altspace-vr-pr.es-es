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
# <a name="using-the-multimedia-console"></a><span data-ttu-id="4a724-104">Uso de la consola multimedia</span><span class="sxs-lookup"><span data-stu-id="4a724-104">Using the multimedia console</span></span>

<span data-ttu-id="4a724-105">La consola multimedia es una herramienta que permite compartir multimedia en eventos y mundos.</span><span class="sxs-lookup"><span data-stu-id="4a724-105">The Multimedia Console is a tool that enables media sharing in events and worlds.</span></span> <span data-ttu-id="4a724-106">Puede usarlo para compartir elementos como imágenes, diapositivas de presentación, livestreams, vídeos, listas de reproducción, etc.</span><span class="sxs-lookup"><span data-stu-id="4a724-106">You can use it to share things like images, presentation slides, livestreams, videos, playlists, and more.</span></span> <span data-ttu-id="4a724-107">A continuación se muestran instrucciones paso a paso sobre cómo usar la consola multimedia **v 0.5.0 +**.</span><span class="sxs-lookup"><span data-stu-id="4a724-107">Below is a step-by-step instruction on how to use the Multimedia Console **v0.5.0+**.</span></span> 

## <a name="getting-started"></a><span data-ttu-id="4a724-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="4a724-108">Getting started</span></span>

<span data-ttu-id="4a724-109">La introducción a la consola multimedia es un proceso de dos partes.</span><span class="sxs-lookup"><span data-stu-id="4a724-109">Getting started with the Multimedia Console is a two part process.</span></span>  <span data-ttu-id="4a724-110">En primer lugar, se usará el portal web para generar y publicar una configuración de la sesión de la consola multimedia que se coloca en el entorno.</span><span class="sxs-lookup"><span data-stu-id="4a724-110">First there's the web portal that you'll use to generate and publish a configuration for the Multimedia Console session you place in your environment.</span></span>  <span data-ttu-id="4a724-111">La segunda es la ubicación de la aplicación de consola multimedia real en su entorno y el establecimiento del código de configuración que debe usar.</span><span class="sxs-lookup"><span data-stu-id="4a724-111">Second is the placement of the actual Multimedia Console app in your environment and setting the configuration code it should use.</span></span>

### <a name="configuring-the-multimedia-console-with-the-web-portal"></a><span data-ttu-id="4a724-112">Configuración de la consola multimedia con el portal web</span><span class="sxs-lookup"><span data-stu-id="4a724-112">Configuring the Multimedia console with the web portal</span></span>

1. <span data-ttu-id="4a724-113">En primer lugar, debe asegurarse de que el contenido está hospedado en línea porque necesitará una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="4a724-113">First, you'll need to make sure your content is hosted online because you'll need a URL.</span></span> <span data-ttu-id="4a724-114">(Puede cargar fotografías en altvr.com, hospedar un archivo. MP4 en línea o usar Twitch live stream link: https://www.twitch.tv/ninja)</span><span class="sxs-lookup"><span data-stu-id="4a724-114">(You can upload photos to altvr.com, host a video .mp4 file online or use Twitch live stream link: https://www.twitch.tv/ninja)</span></span> 
2. <span data-ttu-id="4a724-115">Vaya al portal web de la consola multimedia en [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)</span><span class="sxs-lookup"><span data-stu-id="4a724-115">Navigate to the web portal for the Multimedia Console at [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)</span></span>
3. <span data-ttu-id="4a724-116">En el portal web, puede generar y publicar una configuración para la consola multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-116">From the web portal, you can generate and publish a configuration for the Multimedia Console.</span></span>  <span data-ttu-id="4a724-117">(Consulte a continuación para obtener más información sobre las distintas propiedades).</span><span class="sxs-lookup"><span data-stu-id="4a724-117">(See below for details about the various properties).</span></span>
4. <span data-ttu-id="4a724-118">Una vez que haya escrito el medio en la lista de medios y haya configurado la configuración general, seleccione el botón publicar en la parte superior derecha de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4a724-118">Once you've entered the media into the media list and have configured the general settings, select the publish button in the top-right part of the app.</span></span>
5. <span data-ttu-id="4a724-119">Una vez completada la publicación, aparecerá un cuadro de diálogo con un código de dos palabras para que pueda escribir en la consola multimedia que ha colocado.</span><span class="sxs-lookup"><span data-stu-id="4a724-119">Once the publish has completed, a dialog will pop up with a two word code for you to enter in to the Multimedia Console you placed.</span></span>
  
### <a name="placing-the-multimedia-console-in-your-environment"></a><span data-ttu-id="4a724-120">Colocación de la consola multimedia en el entorno</span><span class="sxs-lookup"><span data-stu-id="4a724-120">Placing the Multimedia console in your environment</span></span>

1. <span data-ttu-id="4a724-121">Seleccione en el **Editor mundial > panel del editor > aplicaciones SDK > consola multimedia**.</span><span class="sxs-lookup"><span data-stu-id="4a724-121">Select on **World Editor > Editor Panel > SDK Apps > Multimedia Console**.</span></span> <span data-ttu-id="4a724-122">(No vaya al **Editor mundial > basics > aplicación de SDK**, que es para aplicaciones no registradas).</span><span class="sxs-lookup"><span data-stu-id="4a724-122">(Don't go to **World Editor > Basics > SDK App**--that's for unregistered apps.)</span></span>  
2. <span data-ttu-id="4a724-123">Coloque la consola multimedia para el mejor conjunto de su espacio y audiencia.</span><span class="sxs-lookup"><span data-stu-id="4a724-123">Position the Multimedia Console to best suite your space and audience.</span></span>
3. <span data-ttu-id="4a724-124">Para salir del modo de edición, haga clic en el botón modo de edición naranja.</span><span class="sxs-lookup"><span data-stu-id="4a724-124">Get out of Edit Mode by clicking the orange Edit Mode button.</span></span>
4. <span data-ttu-id="4a724-125">¿Se le solicitará **el propietario del reproductor de media?**</span><span class="sxs-lookup"><span data-stu-id="4a724-125">You'll be prompted **Are you the media player owner?**</span></span> <span data-ttu-id="4a724-126">Si es la persona que debe ser la propietaria oficial de esta sesión de la consola multimedia, confirme y continúe.</span><span class="sxs-lookup"><span data-stu-id="4a724-126">If you're the person who should be the official owner of this Multimedia Console session, confirm and continue.</span></span> <span data-ttu-id="4a724-127">(También están disponibles otros roles con permisos.</span><span class="sxs-lookup"><span data-stu-id="4a724-127">(Other permissioned roles are available as well.</span></span> <span data-ttu-id="4a724-128">A continuación se muestra una lista detallada).</span><span class="sxs-lookup"><span data-stu-id="4a724-128">See below for a detailed list.)</span></span>
5. <span data-ttu-id="4a724-129">Seleccione Sí para confirmar que es el host principal.</span><span class="sxs-lookup"><span data-stu-id="4a724-129">Select Yes to confirm that you are the primary host.</span></span>  
6. <span data-ttu-id="4a724-130">Aparecerá un cuadro de diálogo que le pide que escriba un código desde el portal web o un archivo JSON válido.</span><span class="sxs-lookup"><span data-stu-id="4a724-130">A dialog should pop up that asks you to enter a code from the web portal or valid JSON.</span></span>  <span data-ttu-id="4a724-131">Escriba el código de dos palabras del portal web, incluido el guión y presione Aceptar.</span><span class="sxs-lookup"><span data-stu-id="4a724-131">Enter the two word code from the web portal including the dash and hit OK.</span></span> <span data-ttu-id="4a724-132">(JSON es una configuración avanzada que se describe a continuación).</span><span class="sxs-lookup"><span data-stu-id="4a724-132">(JSON is an advanced configuration described below)</span></span>
7. <span data-ttu-id="4a724-133">La consola multimedia debe cargarse después de unos segundos con la configuración generada en el portal web.</span><span class="sxs-lookup"><span data-stu-id="4a724-133">The Multimedia Console should load after a few seconds with the configuration you built in the web portal.</span></span>

### <a name="controlling-the-multimedia-console"></a><span data-ttu-id="4a724-134">Controlar la consola multimedia</span><span class="sxs-lookup"><span data-stu-id="4a724-134">Controlling the Multimedia console</span></span>

1. <span data-ttu-id="4a724-135">Después de escribir el código y completar el proceso de configuración, verá que aparecen botones de control debajo de una pantalla de medios.</span><span class="sxs-lookup"><span data-stu-id="4a724-135">After you input your code and complete the configuration process, you'll see control buttons appear below a media display.</span></span> 
    * <span data-ttu-id="4a724-136">**Play** inicia el visor de medios (o se reinicia en la entrada actual, si se detuvo previamente)</span><span class="sxs-lookup"><span data-stu-id="4a724-136">**Play** starts the media viewer (or restarts at current entry, if previously stopped)</span></span> 
    * <span data-ttu-id="4a724-137">**Detener** detiene el visor multimedia y oculta los medios actuales.</span><span class="sxs-lookup"><span data-stu-id="4a724-137">**Stop** stops the media viewer, and hides current media.</span></span>  
    * <span data-ttu-id="4a724-138">**Siguiente/anterior** omite el siguiente o el medio anterior</span><span class="sxs-lookup"><span data-stu-id="4a724-138">**Next/Prev** skips to next or previous media</span></span> 
    * <span data-ttu-id="4a724-139">**x/x**   muestra el índice actual en la lista de medios y le permite saltar a cualquier punto de la lista.</span><span class="sxs-lookup"><span data-stu-id="4a724-139">**x/x** shows the current index into the media list, and allows you to jump to any point in the list</span></span>
    * <span data-ttu-id="4a724-140">La **configuración** permite volver a escribir un nuevo código desde el portal web para establecer una nueva configuración en la consola.</span><span class="sxs-lookup"><span data-stu-id="4a724-140">**Config** allows reentering a new code from the web portal to set a new configuration in the console.</span></span> 

<span data-ttu-id="4a724-141">Ahora está listo para empezar a compartir a través de la consola multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-141">Now you're set to begin sharing via the Multimedia Console!</span></span>  
 
## <a name="working-with-the-web-portal"></a><span data-ttu-id="4a724-142">Trabajar con el portal web</span><span class="sxs-lookup"><span data-stu-id="4a724-142">Working with the web portal</span></span>

<span data-ttu-id="4a724-143">El portal web es una aplicación web que permite configurar las distintas características de la consola multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-143">The web portal is a web app that enables configuring the various features of the Multimedia Console.</span></span>  <span data-ttu-id="4a724-144">Estas características se dividen en dos categorías: configuración general de la consola de medios y la lista de reproducción de medios.</span><span class="sxs-lookup"><span data-stu-id="4a724-144">These features fall in to two categories; general media console settings, and the media play list.</span></span>

### <a name="multimedia-console-general-settings"></a><span data-ttu-id="4a724-145">Configuración general de la consola multimedia</span><span class="sxs-lookup"><span data-stu-id="4a724-145">Multimedia console general settings</span></span>

<span data-ttu-id="4a724-146">**Configuración de reproducción**</span><span class="sxs-lookup"><span data-stu-id="4a724-146">**Playback Settings**</span></span>

<span data-ttu-id="4a724-147">Configuración de reproducción general para la lista de medios</span><span class="sxs-lookup"><span data-stu-id="4a724-147">General playback settings for the media list</span></span>

* <span data-ttu-id="4a724-148">**Lista de medios de bucle**: determina si la lista de medios debe repetirse una vez que llegue al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="4a724-148">**Loop Media List**- Determines whether the media list should loop around once you reach the end of the list.</span></span>
* <span data-ttu-id="4a724-149">**Método de inicio** : selecciona el método por el que debe comenzar la consola multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-149">**Start Method** - Selects the method by which the multimedia console should start.</span></span>
    * <span data-ttu-id="4a724-150">Manual: espera a que se presione el botón de reproducción antes de iniciar el medio</span><span class="sxs-lookup"><span data-stu-id="4a724-150">Manual - Waits for the play button to be pressed before starting the media</span></span>
    * <span data-ttu-id="4a724-151">Inicio automático desde Inicio: inicia automáticamente la lista de medios desde el principio de la lista.</span><span class="sxs-lookup"><span data-stu-id="4a724-151">Auto Start from Beginning - Auto start the media list from the beginning of the list</span></span>
    * <span data-ttu-id="4a724-152">Inicio automático automático: inicia el medio automáticamente desde un punto de Inicio aleatorio de la lista.</span><span class="sxs-lookup"><span data-stu-id="4a724-152">Auto Start Random - Auto starts the media from a random starting point in the list</span></span>

<span data-ttu-id="4a724-153">**Roles**</span><span class="sxs-lookup"><span data-stu-id="4a724-153">**Roles**</span></span>

<span data-ttu-id="4a724-154">Asignaciones de roles para controlar y configurar la consola multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-154">Role assignments for controlling and configuring the Multimedia Console.</span></span>    <span data-ttu-id="4a724-155">Estos roles se dividen en el siguiente conjunto:</span><span class="sxs-lookup"><span data-stu-id="4a724-155">These roles are broken down in to the following set:</span></span>

* <span data-ttu-id="4a724-156">**Solo propietario** : el usuario que es el propietario de la sesión de la consola multimedia</span><span class="sxs-lookup"><span data-stu-id="4a724-156">**Owner Only** - The user that is the owner of the Multimedia Console Session</span></span>
* <span data-ttu-id="4a724-157">**Usuarios con privilegios elevados** : los usuarios que tienen roles de moderador, host o moderador en el espacio en el que está configurada originalmente la consola multimedia</span><span class="sxs-lookup"><span data-stu-id="4a724-157">**Elevated Users** - Users that have moderator, host, or presenter roles in the space that the Multimedia Console is configured in originally</span></span>
* <span data-ttu-id="4a724-158">**Todos los usuarios** -todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="4a724-158">**All Users** - All users</span></span>

<span data-ttu-id="4a724-159">Estos roles se apilan en el sentido de que a todos los roles por encima del que se elija en esta lista también se les concederá permiso para usar esa característica.</span><span class="sxs-lookup"><span data-stu-id="4a724-159">These roles stack in the sense that all roles above the one chosen in this list will also be granted permission to use that feature.</span></span>  <span data-ttu-id="4a724-160">Ejemplo: **usuarios con privilegios elevados** incluye el **propietario** aunque no sea un moderador, un host o un presentador \* \* en AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="4a724-160">Example: **Elevated Users** includes the **Owner** even if they aren't a moderator, host, or presenter\*\* in AltspaceVR.</span></span> <span data-ttu-id="4a724-161">Las características que se controlan mediante asignaciones de roles son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="4a724-161">Features that are controlled by role assignments are as follows</span></span>

* <span data-ttu-id="4a724-162">**Puede controlar el reproductor de media** : determina qué roles pueden controlar los botones de reproducción multimedia para la consola multimedia</span><span class="sxs-lookup"><span data-stu-id="4a724-162">**Can control media player** - Determines what roles can control the media playback buttons for the Multimedia Console</span></span>
* <span data-ttu-id="4a724-163">**Puede configurar el reproductor de media** : determina qué roles pueden configurar la consola multimedia mediante el acceso al botón **config** .</span><span class="sxs-lookup"><span data-stu-id="4a724-163">**Can configure the media player** - Determines what roles can configure the Multimedia Console by being granted access to the **Config** button</span></span>

### <a name="adding-photos-and-videos-to-the-media-list"></a><span data-ttu-id="4a724-164">Agregar fotos y vídeos a la lista de medios</span><span class="sxs-lookup"><span data-stu-id="4a724-164">Adding photos and videos to the media list</span></span>

<span data-ttu-id="4a724-165">El medio es el corazón de la consola multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-165">Media is the heart of the Multimedia Console.</span></span>  <span data-ttu-id="4a724-166">Las imágenes y los vínculos de vídeo se admiten como tipos de medios en la consola multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-166">Images and video links are supported as media types within the Multimedia Console.</span></span>  <span data-ttu-id="4a724-167">Para agregar nuevos medios, seleccione los iconos **Agregar imagen** o **Agregar vídeo** para que aparezca un cuadro de diálogo para especificar la configuración y la información multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-167">To add new media, select either the **Add Image** or **Add Video** icons to have a dialog pop up to enter the media information and settings.</span></span>  <span data-ttu-id="4a724-168">A continuación se muestra el desglose de los tipos de medios y la configuración asociada</span><span class="sxs-lookup"><span data-stu-id="4a724-168">Below is the breakdown of the media types and associated settings</span></span>

<span data-ttu-id="4a724-169">**Imagen**</span><span class="sxs-lookup"><span data-stu-id="4a724-169">**Image**</span></span>

<span data-ttu-id="4a724-170">Las imágenes deben ser un tipo de imagen estándar, como JPEG, PNG y hijo.</span><span class="sxs-lookup"><span data-stu-id="4a724-170">Images should be a standard image type such as jpeg, png, and son on.</span></span> <span data-ttu-id="4a724-171">Deben hospedarse en algún lugar con un vínculo público.</span><span class="sxs-lookup"><span data-stu-id="4a724-171">They need to be hosted somewhere with a public link.</span></span>

* <span data-ttu-id="4a724-172">**Nombre** : (obligatorio) nombre con el que desea identificar la imagen.</span><span class="sxs-lookup"><span data-stu-id="4a724-172">**Name** - (Required) Name that you wish to identify the image with.</span></span>
* <span data-ttu-id="4a724-173">**URL** de la imagen: (obligatorio) dirección URL pública de la imagen</span><span class="sxs-lookup"><span data-stu-id="4a724-173">**Image URL** - (Required) The public url of the image</span></span>
* <span data-ttu-id="4a724-174">**Omitir después** del número de segundos que se debe omitir la imagen después de</span><span class="sxs-lookup"><span data-stu-id="4a724-174">**Skip After** - The number of seconds that the image should be skipped after</span></span>

<span data-ttu-id="4a724-175">**Vídeo**</span><span class="sxs-lookup"><span data-stu-id="4a724-175">**Video**</span></span>

<span data-ttu-id="4a724-176">Los vídeos pueden ser vídeos hospedados o secuencias en directo a través de Twitch y DLive.</span><span class="sxs-lookup"><span data-stu-id="4a724-176">Videos can be hosted videos or live streams through Twitch and DLive.</span></span>  <span data-ttu-id="4a724-177">(Otra compatibilidad puede funcionar con el trabajo adicional para obtener la dirección URL de flujo adecuada, pero no es totalmente compatible con la consola multimedia).</span><span class="sxs-lookup"><span data-stu-id="4a724-177">(Other support may function with extra work to get the proper stream url, but aren't fully supported within the Multimedia Console)</span></span>

* <span data-ttu-id="4a724-178">**Nombre** : (obligatorio) nombre con el que desea identificar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="4a724-178">**Name** - (Required) Name that you wish to identify the video with.</span></span>
* <span data-ttu-id="4a724-179">**URL de vídeo** : (obligatorio) dirección URL pública a la que se hospeda el vídeo o desde la que se sirve la secuencia en directo.</span><span class="sxs-lookup"><span data-stu-id="4a724-179">**Video URL** - (Required) The public url that the video is hosted at or the live stream is served from.</span></span>
* <span data-ttu-id="4a724-180">**Omitir después** del número de segundos que se debe omitir el vídeo después</span><span class="sxs-lookup"><span data-stu-id="4a724-180">**Skip After** - The number of seconds that the video should be skipped after</span></span>
* <span data-ttu-id="4a724-181">**Volumen** : el volumen del vídeo con valores 0 (min)-1 (máx.).</span><span class="sxs-lookup"><span data-stu-id="4a724-181">**Volume** - The volume of the video from 0 (min) - 1 (max) values.</span></span>
* <span data-ttu-id="4a724-182">**Hora de inicio** : el número de segundos desde el principio del vídeo comienza desde.</span><span class="sxs-lookup"><span data-stu-id="4a724-182">**Start Time** - The number of seconds from the beginning of the video start from.</span></span>
* <span data-ttu-id="4a724-183">Poner al **día la distancia de inicio** : la distancia en metros en que el volumen comienza a pasar a medida que sale de la consola multimedia</span><span class="sxs-lookup"><span data-stu-id="4a724-183">**Roll Off Start Distance** - The distance in meters in world that the volume begins to fall off at as you move away from the Multimedia Console</span></span>
* <span data-ttu-id="4a724-184">**Acción de fin de vídeo** : la acción que se realizará una vez que se alcance el final del vídeo.</span><span class="sxs-lookup"><span data-stu-id="4a724-184">**End of Video Action** - The action to take once the end of the video is reached.</span></span>
    * <span data-ttu-id="4a724-185">Detener: la lista de medios se detiene una vez finalizado el vídeo</span><span class="sxs-lookup"><span data-stu-id="4a724-185">Stop - The media list stops after the video has ended</span></span>
    * <span data-ttu-id="4a724-186">Loop: el vídeo se repetirá hasta que se omita manualmente</span><span class="sxs-lookup"><span data-stu-id="4a724-186">Loop - The video will loop until manually skipped</span></span>
    * <span data-ttu-id="4a724-187">Reproducir siguiente: el siguiente medio en la lista de medios se iniciará después de que finalice el vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="4a724-187">Play Next - The next media in the media list will be started after the current video ends.</span></span>

## <a name="working-with-json-directly-advancedoptional"></a><span data-ttu-id="4a724-188">Trabajar directamente con JSON (avanzado/opcional)</span><span class="sxs-lookup"><span data-stu-id="4a724-188">Working with JSON directly (advanced/optional)</span></span>

<span data-ttu-id="4a724-189">La consola multimedia permite escribir JSON directamente en el símbolo del sistema de la consola de AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="4a724-189">The Multimedia Console supports entering JSON directly in to the prompt of the console in AltspaceVR.</span></span>  <span data-ttu-id="4a724-190">JSON es el mecanismo interno con el que se habilitan las configuraciones del reproductor de media.</span><span class="sxs-lookup"><span data-stu-id="4a724-190">JSON is the internal mechanism with which we enable media player configurations.</span></span> <span data-ttu-id="4a724-191">Exponer la capacidad de establecer directamente JSON es algo que permite a los usuarios más avanzados crear sus propios flujos de trabajo que se adapten a sus necesidades y que estén familiarizados con JSON.</span><span class="sxs-lookup"><span data-stu-id="4a724-191">Exposing the ability to set JSON directly is something that allows for more advanced users to build their own workflows that suites their needs and familiarity with JSON.</span></span>  <span data-ttu-id="4a724-192">A continuación se describe una breve descripción de la estructura JSON y el esquema por el que se valida el JSON.</span><span class="sxs-lookup"><span data-stu-id="4a724-192">The following is a brief description of the JSON structure and the schema by which the JSON is validated.</span></span> <span data-ttu-id="4a724-193">Para obtener descripciones más detalladas de las propiedades siguientes, vea las secciones anteriores que tratan sobre la configuración de la consola multimedia.</span><span class="sxs-lookup"><span data-stu-id="4a724-193">For more detailed descriptions of the properties below, see the above sections that talk about configuring the Multimedia Console.</span></span>  <span data-ttu-id="4a724-194">Esta sección se centra principalmente en los ejemplos de esquema y la estructura de los datos JSON.</span><span class="sxs-lookup"><span data-stu-id="4a724-194">This section is focused primarily on the schema examples and structuring for the JSON data.</span></span>

### <a name="global-media-settings"></a><span data-ttu-id="4a724-195">Configuración de medios globales</span><span class="sxs-lookup"><span data-stu-id="4a724-195">Global media settings</span></span>

```json
{
  "loopMediaList": true | false
  "startMethod": "manual" | "autostart-beginning" | "autostart-random"
  "controlMediaPlayer": "everyone" | "elevated" | "owner"
  "configureMediaPlayer": "elevated" | "owner"
  ...
}
```

### <a name="media-list"></a><span data-ttu-id="4a724-196">Lista de medios</span><span class="sxs-lookup"><span data-stu-id="4a724-196">Media list</span></span>

<span data-ttu-id="4a724-197">La lista de medios es una propiedad establecida en la raíz de la estructura JSON, como los roles y la configuración de reproducción.</span><span class="sxs-lookup"><span data-stu-id="4a724-197">The media list is a property set at the root of the JSON structure like the Roles and Playback Settings.</span></span>  <span data-ttu-id="4a724-198">Es una matriz simple que puede contener una de las siguientes estructuras de configuración de medios.</span><span class="sxs-lookup"><span data-stu-id="4a724-198">It's a simple array that can contain one of the following media configuration structures.</span></span> <span data-ttu-id="4a724-199">(Consulte las descripciones de propiedades anteriores para obtener más información sobre lo que hace cada uno).</span><span class="sxs-lookup"><span data-stu-id="4a724-199">(See property descriptions above for details on what each does.)</span></span>

<span data-ttu-id="4a724-200">**Ejemplo de imagen**</span><span class="sxs-lookup"><span data-stu-id="4a724-200">**Image example**</span></span>

<span data-ttu-id="4a724-201">*Campos obligatorios: "Name" y "imageUrl"*</span><span class="sxs-lookup"><span data-stu-id="4a724-201">*Required fields: "name" and "imageUrl"*</span></span>

```json
{
    "name": "Altspace Screenshot",
    "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
    "skipAfter": 10
}
```

<span data-ttu-id="4a724-202">**Ejemplo de vídeo**</span><span class="sxs-lookup"><span data-stu-id="4a724-202">**Video example**</span></span>

<span data-ttu-id="4a724-203">*Campos obligatorios: "Name" y "videoUrl"*</span><span class="sxs-lookup"><span data-stu-id="4a724-203">*Required fields: "name" and "videoUrl"*</span></span>

```json
{
    "name": "Ninja Twitch Live Stream",
    "videoUrl":"https://www.twitch.tv/ninja",
    "volume":0.2,
    "startTime":0,
    "endOfVideoAction":"play-next"
}
```

### <a name="example-json"></a><span data-ttu-id="4a724-204">Ejemplo de JSON</span><span class="sxs-lookup"><span data-stu-id="4a724-204">Example JSON</span></span>

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

### <a name="schema"></a><span data-ttu-id="4a724-205">Schema</span><span class="sxs-lookup"><span data-stu-id="4a724-205">Schema</span></span>

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
> <span data-ttu-id="4a724-206">Actualizado con la consola multimedia v 0.5.0</span><span class="sxs-lookup"><span data-stu-id="4a724-206">Up to date with Multimedia Console v0.5.0</span></span>