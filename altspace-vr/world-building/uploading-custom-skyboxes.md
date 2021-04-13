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
# <a name="uploading-custom-skyboxes"></a><span data-ttu-id="a2f1c-104">Carga de skyboxes personalizadas</span><span class="sxs-lookup"><span data-stu-id="a2f1c-104">Uploading custom Skyboxes</span></span>

<span data-ttu-id="a2f1c-105">Un SKYBOX es una forma de crear un **fondo** para su mundo que hace que la experiencia sea más envolvente.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-105">A Skybox is a way to create a **background** for your World that makes the experience more immersive.</span></span> <span data-ttu-id="a2f1c-106">Hay diferentes tipos de Skyboxes, pero actualmente se admite **equirectangular**.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-106">There are different kinds of Skyboxes but we currently support **equirectangular**.</span></span> <span data-ttu-id="a2f1c-107">A continuación se muestra un ejemplo de una cámara 360 (más información [aquí](http://moments.mankindforward.com/)):</span><span class="sxs-lookup"><span data-stu-id="a2f1c-107">Here's an example taken with a 360 camera (more example [here](http://moments.mankindforward.com/)):</span></span> 

![360 equirectangular vista de un salón](images/custom-skyboxes-img-01.jpeg)

<span data-ttu-id="a2f1c-109">También puede usar el [cargador de Unity](world-building-toolkit-getting-started.md) , pero este enfoque es más sencillo.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-109">You can also use the [Unity Uploader](world-building-toolkit-getting-started.md) but this approach is simpler.</span></span>

1. <span data-ttu-id="a2f1c-110">Vaya a [mundos > skyboxes](https://account.altvr.com/skyboxes) y presione el botón **crear** de la derecha.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-110">Navigate to [Worlds > Skyboxes](https://account.altvr.com/skyboxes) and press the **Create** button on the right</span></span>

![Página de sitios web de mundos abrir en el panel de skyboxes](images/custom-skyboxes-img-02.png)

2. <span data-ttu-id="a2f1c-112">Rellene un nombre y especifique la imagen 360.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-112">Fill in a name and specify your 360 image.</span></span> <span data-ttu-id="a2f1c-113">No es necesario que sea una foto, hay programas que le permiten dibujar su propio o puede buscar algunos en línea.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-113">It doesn't have to be a photo, there are programs that let you draw your own or you can search for some online.</span></span> <span data-ttu-id="a2f1c-114">Cuando esté listo, seleccione **Crear**.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-114">When you're ready, select **Create**.</span></span> 

![Formulario de creación de SKYBOX](images/custom-skyboxes-img-03.png)

3. <span data-ttu-id="a2f1c-116">Opcionalmente, puede cargar una imagen de **vista previa** para que pueda identificar fácilmente este SKYBOX.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-116">You can optionally upload a **preview** image so you can easily identify this skybox.</span></span> <span data-ttu-id="a2f1c-117">También puede cargar el audio ambiente en formato WAV.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-117">You can also upload ambient audio in WAV format.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="a2f1c-118">Se recomienda cargar imágenes de vista previa y audio ambiente por separado, después de cargar la imagen 360.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-118">We recommend you upload preview images and ambient audio separately, after you upload the 360 image.</span></span> <span data-ttu-id="a2f1c-119">Si los carga juntos, los tamaños de archivo pueden ser lo suficientemente grandes como para detenerse el proceso.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-119">If you upload them together the file sizes can be large enough to stall the process.</span></span> <span data-ttu-id="a2f1c-120">[Jetsons World](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) es un buen ejemplo de cómo usar un SKYBOX con audio ambiente.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-120">[Jetsons World](https://account.altvr.com/worlds/1004174988393054363/spaces/1084431533181240311) is a great example of how to use a Skybox with ambient audio.</span></span> <span data-ttu-id="a2f1c-121">Observe cómo el generador mundial mantiene el volumen de audio bajo y los sonidos que oye son esporádicos, por lo que la gente no me molesta.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-121">Notice how the World-Builder kept the audio volume low and sounds you hear are sporadic so people don't get annoyed.</span></span> 

4. <span data-ttu-id="a2f1c-122">Escriba su mundo y abra el editor mundial.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-122">Enter your World and open the World Editor.</span></span> <span data-ttu-id="a2f1c-123">En Skyboxes, seleccione el nuevo SKYBOX.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-123">Under Skyboxes, select your new Skybox.</span></span> <span data-ttu-id="a2f1c-124">En unos segundos, el cielo cambiará literalmente.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-124">In a few seconds, the sky will literally change.</span></span> <span data-ttu-id="a2f1c-125">Otros usuarios de su mundo también verán el cambio del cielo.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-125">Others in your World will also see the sky change.</span></span> <span data-ttu-id="a2f1c-126">Para volver a cambiar, elija el **valor predeterminado** SkyBOX en la misma lista.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-126">To switch back, choose the **default** skybox in that same list.</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="a2f1c-127">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="a2f1c-127">Troubleshooting</span></span>

<span data-ttu-id="a2f1c-128">**Hay unas costuras o una línea en el cielo:-(.**</span><span class="sxs-lookup"><span data-stu-id="a2f1c-128">**There's a seam or line in the sky :-(.**</span></span> <span data-ttu-id="a2f1c-129">Es un error que corregiremos pronto</span><span class="sxs-lookup"><span data-stu-id="a2f1c-129">It's a bug that we'll fix soon</span></span>

<span data-ttu-id="a2f1c-130">**Error de carga**</span><span class="sxs-lookup"><span data-stu-id="a2f1c-130">**Upload failed**</span></span>
    * <span data-ttu-id="a2f1c-131">intente cargar solo la imagen de 360 por sí misma</span><span class="sxs-lookup"><span data-stu-id="a2f1c-131">try uploading just the 360 image on its own</span></span>
    * <span data-ttu-id="a2f1c-132">Pruebe con otro archivo más pequeño como prueba</span><span class="sxs-lookup"><span data-stu-id="a2f1c-132">try with another, smaller file as a test</span></span>

<span data-ttu-id="a2f1c-133">**No encuentro una foto 360**</span><span class="sxs-lookup"><span data-stu-id="a2f1c-133">**I can't find a 360 photo**</span></span>
    * <span data-ttu-id="a2f1c-134">Flickr es una buena fuente (cambie los filtros para buscar las de Creative Commons)</span><span class="sxs-lookup"><span data-stu-id="a2f1c-134">Flickr is a good source (change the filters to find creative commons ones)</span></span>
    * <span data-ttu-id="a2f1c-135">¡ Tómese su propia!</span><span class="sxs-lookup"><span data-stu-id="a2f1c-135">Take your own!</span></span> <span data-ttu-id="a2f1c-136">Hemos tenido éxito con las cámaras de Ricoh.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-136">We've had success with Ricoh's cameras.</span></span> 
<span data-ttu-id="a2f1c-137">**El cielo busca granulado o bloqueado** Es posible que necesite encontrar una imagen de mayor resolución.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-137">**The sky looks grainy or blocky** You may need to find a higher-resolution image.</span></span> <span data-ttu-id="a2f1c-138">Normalmente aproximadamente 2-5 MB y ~ 5000 PX x 2000 PX</span><span class="sxs-lookup"><span data-stu-id="a2f1c-138">Typically around 2-5 MB and ~5000 px x 2000 px</span></span>

<span data-ttu-id="a2f1c-139">**Nos afecta a la velocidad de fotogramas del mundo.**</span><span class="sxs-lookup"><span data-stu-id="a2f1c-139">**It hurts my World's framerate!**</span></span>
<span data-ttu-id="a2f1c-140">La imagen probablemente es demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-140">The image is probably too large.</span></span> <span data-ttu-id="a2f1c-141">Algunos skyboxes generados pueden ser 8k.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-141">Some generated skyboxes can be 8k.</span></span> <span data-ttu-id="a2f1c-142">Normalmente se encuentran en las versiones de 2K compatibles con móviles: Úsela.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-142">They usually come with mobile-friendly 2k versions--use that.</span></span>

<span data-ttu-id="a2f1c-143">**Ayúdeme con el audio ambiente**</span><span class="sxs-lookup"><span data-stu-id="a2f1c-143">**Help me with the ambient audio**</span></span>
    * <span data-ttu-id="a2f1c-144">Use software gratuito como Audacity para reducir el volumen o cree sus propios bucles.</span><span class="sxs-lookup"><span data-stu-id="a2f1c-144">Use free software like Audacity to lower the volume or create your own loops.</span></span> <span data-ttu-id="a2f1c-145">Recuerde que el audio se repetirá y reproducirá en los oídos de las personas, por lo que debe mantenerse bajo y no molestar</span><span class="sxs-lookup"><span data-stu-id="a2f1c-145">Remember that the audio will be repeated and playing in people's ears so keep it low and not annoying</span></span>
    * <span data-ttu-id="a2f1c-146">El [sonido gratuito](https://freesound.org/) es una buena fuente de sonidos sin regalías</span><span class="sxs-lookup"><span data-stu-id="a2f1c-146">[Free Sound](https://freesound.org/) is a good source of royalty-free sounds</span></span>
