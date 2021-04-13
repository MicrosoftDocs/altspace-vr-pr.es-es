---
title: Uso del Interactables
description: Aprenda a crear, usar y personalizar el generador de interactables para colocar elementos en los espacios de AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: generación, interacciones, personalizaciones
ms.openlocfilehash: 7f4b87591b2e11b2084af4d2bf83748ed51fd193
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213923"
---
# <a name="using-the-interactables-spawner"></a><span data-ttu-id="7e588-104">Uso del Interactables</span><span class="sxs-lookup"><span data-stu-id="7e588-104">Using the Interactables Spawner</span></span>

<span data-ttu-id="7e588-105">El Interactables generador permite colocar los elementos interactivos en el evento, el mundo o el espacio de inicio.</span><span class="sxs-lookup"><span data-stu-id="7e588-105">The Interactables Spawner allows you to place interactable items in your event, world, or home-space.</span></span> <span data-ttu-id="7e588-106">Actualmente, esta característica forma parte de nuestro [programa de acceso temprano](../world-building/early-access.md) y no estará disponible a menos que haya participado en el menú principal.</span><span class="sxs-lookup"><span data-stu-id="7e588-106">This feature is currently part of our [Early Access Program](../world-building/early-access.md) and won't be available unless you've opted in through your Main Menu.</span></span>

> [!NOTE]
> <span data-ttu-id="7e588-107">Aunque seguimos realizando una prueba piloto de esta característica, tenga en cuenta que la generación de demasiadas interactables puede afectar al rendimiento de su entorno o evento.</span><span class="sxs-lookup"><span data-stu-id="7e588-107">While we continue to pilot this feature please be aware that spawning too many interactables may affect the performance of your environment or event.</span></span> 

## <a name="creating-an-interactable"></a><span data-ttu-id="7e588-108">Crear un interactuable</span><span class="sxs-lookup"><span data-stu-id="7e588-108">Creating an interactable</span></span>

<span data-ttu-id="7e588-109">Para convertir el objeto en un objeto interactuable:</span><span class="sxs-lookup"><span data-stu-id="7e588-109">To turn your object into an interactable object:</span></span>

1. <span data-ttu-id="7e588-110">Coloque el objeto en el espacio.</span><span class="sxs-lookup"><span data-stu-id="7e588-110">Place the object in your space.</span></span>
2. <span data-ttu-id="7e588-111">A continuación, busque la entrada en la lista de objetos y seleccione el **icono de engranaje** situado junto a ella para abrir su configuración:</span><span class="sxs-lookup"><span data-stu-id="7e588-111">Then, find the entry in the object list, and select the **gear icon** next to it to open its settings:</span></span>

![Editor mundial abierto con la lista de objetos resaltada](images/interactables-spawner-img-01.png)

<span data-ttu-id="7e588-113">En la página Configuración encontrará una nueva casilla **"objeto de generación de objetos"**, que se usa para convertirla en un objeto interactuable.</span><span class="sxs-lookup"><span data-stu-id="7e588-113">On the settings page you’ll find a new checkbox **“Object spawner“**, which is used to make it an interactable object.</span></span>

1. <span data-ttu-id="7e588-114">Active la casilla y seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="7e588-114">Check the box and select **confirm**.</span></span>
2. <span data-ttu-id="7e588-115">En el modo de edición, puede desplazarse por la ubicación de generación del objeto en el espacio.</span><span class="sxs-lookup"><span data-stu-id="7e588-115">While in edit mode, you can move around the object’s spawn location in the space.</span></span>
3. <span data-ttu-id="7e588-116">**Salga del modo de edición** para habilitar la interacción del elemento.</span><span class="sxs-lookup"><span data-stu-id="7e588-116">**Exit edit mode** to enable item interaction.</span></span>

![Ventana actualizar artefacto abierta en la aplicación AltspaceVR](images/interactables-spawner-img-02.png)

## <a name="other-customizations"></a><span data-ttu-id="7e588-118">Otras personalizaciones</span><span class="sxs-lookup"><span data-stu-id="7e588-118">Other customizations</span></span>

<span data-ttu-id="7e588-119">Después de habilitar **"objeto de generación de objetos"** cuando vuelva a las propiedades de ese objeto, habrá una configuración adicional que se puede aplicar a la forma en que se comporta el objeto generado.</span><span class="sxs-lookup"><span data-stu-id="7e588-119">After enabling **“Object spawner”** when you go back into the properties for that object, there will be an extra setting you can apply to how the spawned object behaves.</span></span>

> [!NOTE]
> <span data-ttu-id="7e588-120">Escala de objetos interactivos: Esto establece la escala del objeto cuando se selecciona, en comparación con "escala", que es la escala de cómo aparece el objeto en el mundo antes de seleccionarlo por primera vez.</span><span class="sxs-lookup"><span data-stu-id="7e588-120">Interactable object scale: This sets the scale of the object when it gets picked up, compared to “Scale” which is the scale of how the object appears in the world prior to picking it up for the first time.</span></span>

<span data-ttu-id="7e588-121">Los responsables del kit pueden observar que los cambios en el kit mientras AltspaceVR se está ejecutando no surtirán efecto hasta que reinicie AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="7e588-121">Kit makers may notice that changes to your Kit while AltspaceVR is running won't take effect until you restart AltspaceVR.</span></span>

<span data-ttu-id="7e588-122">Recientemente hemos agregado un botón en la pestaña **configuración moderada** denominada **recargar los kits de mundos**.</span><span class="sxs-lookup"><span data-stu-id="7e588-122">Recently we’ve added a button under the **Moderate Settings** tab called **Reload Worlds Kits**.</span></span> <span data-ttu-id="7e588-123">Al hacer clic en este botón, se hace que (solo usted) vuelva a escribir el espacio y vuelva a cargar todos los kits, lo que descargará solo las nuevas versiones de los kits que se han actualizado mientras estaba en AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="7e588-123">Clicking this button causes (just you) to reenter the space, reloading all Kits again, which will download only new versions of the Kits that have been updated while you were in AltspaceVR.</span></span>

![Panel de configuración moderada abierto en la aplicación AltspaceVR](images/interactables-spawner-img-03.png)