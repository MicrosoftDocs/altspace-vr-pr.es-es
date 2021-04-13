---
title: Importar modelos glTF
description: Obtenga información sobre cómo importar correctamente modelos de glTF 3D en sus experiencias de AltspaceVR y solucionar cualquier problema.
ms.date: 03/11/2021
ms.topic: article
keywords: modelos, glTF, importación, sketchfab, solución de problemas
ms.openlocfilehash: 4489f90832bd1cf85ff161caed11684257cce6ab
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213790"
---
# <a name="importing-gltf-models"></a><span data-ttu-id="4057c-104">Importar modelos glTF</span><span class="sxs-lookup"><span data-stu-id="4057c-104">Importing glTF models</span></span>

> [!NOTE]
> <span data-ttu-id="4057c-105">Esta característica está disponible para los usuarios seleccionados en el programa de acceso temprano en este momento.</span><span class="sxs-lookup"><span data-stu-id="4057c-105">This feature is available for select users in the Early Access program at this time.</span></span>

<span data-ttu-id="4057c-106">Una manera de incluir modelos y escenas 3D en Altspace es usar el [estándar glTF](https://en.wikipedia.org/wiki/GlTF).</span><span class="sxs-lookup"><span data-stu-id="4057c-106">One way to bring 3D models and scenes into Altspace is using the [glTF standard](https://en.wikipedia.org/wiki/GlTF).</span></span> <span data-ttu-id="4057c-107">Puede cargar un archivo. glb (glTF empaquetado) para crear un modelo que puede generar posteriormente en el editor mundial.</span><span class="sxs-lookup"><span data-stu-id="4057c-107">You can upload a .glb file (packed glTF) to create a Model that you can later spawn in the World Editor.</span></span> <span data-ttu-id="4057c-108">Es una alternativa a [cargar sus propios kits](uploading-custom-kits.md).</span><span class="sxs-lookup"><span data-stu-id="4057c-108">It's an alternative to [uploading your own Kits](uploading-custom-kits.md).</span></span> <span data-ttu-id="4057c-109">Se recomienda crear modelos para demostraciones rápidas porque no necesitará usar Unity y kits cuando quiera maximizar el rendimiento y la reutilización.</span><span class="sxs-lookup"><span data-stu-id="4057c-109">We recommend creating Models for quick demonstrations because you won't need to use Unity, and Kits when you want to maximize performance and reusability.</span></span> 

1. <span data-ttu-id="4057c-110">Busque algunos activos de glTF 3D.</span><span class="sxs-lookup"><span data-stu-id="4057c-110">Find some glTF 3D assets.</span></span> <span data-ttu-id="4057c-111">Un lugar en el que buscar es Sketchfab (probar el filtrado de modelos **descargables** como [este](https://sketchfab.com/search?features=downloadable&q=low+poly+wolf&sort_by=-pertinence&type=models)).</span><span class="sxs-lookup"><span data-stu-id="4057c-111">One place to search is Sketchfab (try filtering for **Downloadable** models like [this](https://sketchfab.com/search?features=downloadable&q=low+poly+wolf&sort_by=-pertinence&type=models)).</span></span> <span data-ttu-id="4057c-112">Una vez que lo encuentre, seleccione **Descargar modelo 3D**:</span><span class="sxs-lookup"><span data-stu-id="4057c-112">Once you find it, select **Download 3D Model**:</span></span>

![modelo de perro en 3D de Sketchfab](images/importing-models-img-01.png)

2. <span data-ttu-id="4057c-114">Copie el vínculo en el modelo y lea los requisitos de licencia.</span><span class="sxs-lookup"><span data-stu-id="4057c-114">Copy the link to the model and read the licensing requirements.</span></span> 
3. <span data-ttu-id="4057c-115">Descargar la versión de **formato autoconvertido (glTF)**</span><span class="sxs-lookup"><span data-stu-id="4057c-115">Download the **Autoconverted Format (glTF)** version</span></span>

![Sketchfab opciones de descarga con el formato de conversión automático resaltado](images/importing-models-img-02.png)

4. <span data-ttu-id="4057c-117">Abra el sitio de [glb Pack](https://glb-packer.glitch.me) y active la casilla **convertir PNG en JPEG (beta)** .</span><span class="sxs-lookup"><span data-stu-id="4057c-117">Open the [GLB Packer](https://glb-packer.glitch.me) site and check the box **Convert PNG to JPEG (beta)**</span></span>
5. <span data-ttu-id="4057c-118">Descomprimir los archivos glTF que descargó y arrástrelos todos a la vez a la pestaña del explorador GLB Pack</span><span class="sxs-lookup"><span data-stu-id="4057c-118">Uncompress the glTF files you downloaded and drag them all at once into the GLB Packer browser tab</span></span>

![Ventana que muestra la descompresión del modelo](images/importing-models-img-03.png)

6. <span data-ttu-id="4057c-120">En función del número y el tamaño de los archivos, puede tardar un tiempo en procesarse.</span><span class="sxs-lookup"><span data-stu-id="4057c-120">Depending on the number and size of the files, it may take a while to process.</span></span> <span data-ttu-id="4057c-121">Una vez finalizado el procesamiento, se descargará un archivo **out. glb** .</span><span class="sxs-lookup"><span data-stu-id="4057c-121">When processing is done, an **out.glb** file will be downloaded.</span></span> <span data-ttu-id="4057c-122">Cambie el nombre de ese archivo a algo informativo, es decir, el nombre del objeto en el mundo (por ejemplo, **Wolf. glb).**</span><span class="sxs-lookup"><span data-stu-id="4057c-122">Rename that file to something informative--this will be the name of the object in the world (e.g **Low Poly Wolf.glb**)</span></span>
7. <span data-ttu-id="4057c-123">Vaya a [altvr.com > más > modelos](https://account.altvr.com/users/sign_in) y seleccione **crear** .</span><span class="sxs-lookup"><span data-stu-id="4057c-123">Navigate to [altvr.com > More > Models](https://account.altvr.com/users/sign_in) and select **Create**</span></span>
8. <span data-ttu-id="4057c-124">Especifique la ubicación del archivo. glb y asegúrese de copiar el vínculo de Sketchfab en la descripción de atribución.</span><span class="sxs-lookup"><span data-stu-id="4057c-124">Specify the location of the .glb file and make sure you copy the Sketchfab link into the description for attribution.</span></span> <span data-ttu-id="4057c-125">Si lo desea, puede especificar una imagen de vista previa y, a continuación, seleccionar **crear modelo**:</span><span class="sxs-lookup"><span data-stu-id="4057c-125">You can specify a preview image if you want, then select **Create Model**:</span></span>

![Vista previa del modelo en AltspaceVR](images/importing-models-img-04.png)

9. <span data-ttu-id="4057c-127">Seleccionar **copiar al portapapeles**</span><span class="sxs-lookup"><span data-stu-id="4057c-127">Select **Copy to Clipboard**</span></span>
10. <span data-ttu-id="4057c-128">Abra el **Editor mundial > Altspace > basics > GLTF**</span><span class="sxs-lookup"><span data-stu-id="4057c-128">Open the **World Editor > Altspace > Basics > GLTF**</span></span>
11. <span data-ttu-id="4057c-129">Pegue la dirección URL y seleccione **confirmar**</span><span class="sxs-lookup"><span data-stu-id="4057c-129">Paste in your url and select **Confirm**</span></span>

<span data-ttu-id="4057c-130">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="4057c-130">Congrats!</span></span> <span data-ttu-id="4057c-131">Acaba de generar su primer modelo.</span><span class="sxs-lookup"><span data-stu-id="4057c-131">You just spawned your first Model.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="4057c-132">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="4057c-132">Troubleshooting</span></span>

<span data-ttu-id="4057c-133">**Al hacer clic en **confirmar** que no se ha producido nada**</span><span class="sxs-lookup"><span data-stu-id="4057c-133">**When I clicked **Confirm** nothing happened**</span></span>
    * <span data-ttu-id="4057c-134">Actualmente tenemos un límite de 100 000 polígonos.</span><span class="sxs-lookup"><span data-stu-id="4057c-134">We currently have a 100k polygon limit.</span></span> <span data-ttu-id="4057c-135">Si se produce un error, elimine el objeto para evitar posibles problemas con los usuarios que se unen a su mundo</span><span class="sxs-lookup"><span data-stu-id="4057c-135">If it fails, delete the Object to avoid potential problems with users joining your World</span></span>
    * <span data-ttu-id="4057c-136">Puede haber otros problemas con el recurso.</span><span class="sxs-lookup"><span data-stu-id="4057c-136">There may be other problems with the asset.</span></span> <span data-ttu-id="4057c-137">Intente usar recursos con el menor número posible de polígonos.</span><span class="sxs-lookup"><span data-stu-id="4057c-137">Try to use assets with as few polygons as possible.</span></span>
    * <span data-ttu-id="4057c-138">El modelo que se va a incorporar puede ser pequeño o grande.</span><span class="sxs-lookup"><span data-stu-id="4057c-138">The model you're bringing in may be small or large.</span></span> <span data-ttu-id="4057c-139">Pruebe a aumentar o reducir el tamaño de la escala o a mover el avatar en torno al modelo.</span><span class="sxs-lookup"><span data-stu-id="4057c-139">Try increasing/decreasing the Scale or move your avatar around, you might be standing inside the model!</span></span>

<span data-ttu-id="4057c-140">Es **lento de cargar** La rapidez con la que se cargan otros usuarios del mundo dependerá de sus velocidades de conexión.</span><span class="sxs-lookup"><span data-stu-id="4057c-140">**It's slow to load** How quickly other users in the World load it will depend on their connection speeds.</span></span> <span data-ttu-id="4057c-141">Tampoco se almacena en caché como los recursos del kit.</span><span class="sxs-lookup"><span data-stu-id="4057c-141">It's also not cached like Kit assets.</span></span> <span data-ttu-id="4057c-142">Si coloca uno en su hogar, terminará de volver a descargar el mismo modelo cada vez que se una al unirse, lo que no es genial.</span><span class="sxs-lookup"><span data-stu-id="4057c-142">If you place one in your Home, you'll end up redownloading the same Model every time you join, which isn't great.</span></span>

<span data-ttu-id="4057c-143">No **hay ninguna colisión** De forma predeterminada, no hay ninguna colisión en los objetos que se incorporan de esta manera</span><span class="sxs-lookup"><span data-stu-id="4057c-143">**There's no collision** By default there's no collision on the objects that are brought in this way</span></span>

<span data-ttu-id="4057c-144">**Al generarlo, pierdo los controles en seis DOF o estoy dentro, por lo que es difícil manipularlo** . Sí, somos conscientes de estos problemas y esperamos solucionarlos pronto.</span><span class="sxs-lookup"><span data-stu-id="4057c-144">**When I spawn it, I lose my controls on six DOF or I'm inside so it's hard to manipulate it** Yes, we're aware of these issues and hope to address them soon.</span></span>  