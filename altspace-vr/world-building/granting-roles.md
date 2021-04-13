---
title: Conceder roles mundiales
description: Obtenga información sobre el sistema de roles y capacidades y obtenga instrucciones paso a paso para conceder a los usuarios roles en sus AltspaceVR mundos.
ms.date: 03/11/2021
ms.topic: article
keywords: roles
ms.openlocfilehash: f8cd55fbd8ede6cedd199724a3e6b2413c5bc3e6
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213690"
---
# <a name="granting-world-roles"></a><span data-ttu-id="484c6-104">Conceder roles mundiales</span><span class="sxs-lookup"><span data-stu-id="484c6-104">Granting world roles</span></span>

<span data-ttu-id="484c6-105">Altspace tiene un sistema de roles y capacidades.</span><span class="sxs-lookup"><span data-stu-id="484c6-105">Altspace has a Roles and Abilities system.</span></span> <span data-ttu-id="484c6-106">Cada persona puede tener varios roles y sus roles pueden ser diferentes en función de dónde se encuentren.</span><span class="sxs-lookup"><span data-stu-id="484c6-106">Each person can have multiple roles and their roles can be different depending on where they are.</span></span> <span data-ttu-id="484c6-107">Cada rol, a su vez, proporciona una o más capacidades.</span><span class="sxs-lookup"><span data-stu-id="484c6-107">Each role, in turn, gives you one or more abilities.</span></span> <span data-ttu-id="484c6-108">Por ejemplo, si se encuentra en su propio evento, recibirá **automáticamente los roles de** Moderador y **moderador** .</span><span class="sxs-lookup"><span data-stu-id="484c6-108">For example, when you're in your own event, you automatically receive the **presenter** and **moderator** roles.</span></span> <span data-ttu-id="484c6-109">Con esos dos roles, puede poner en marcha usuarios impropios, estar en fase y puede liberar el confeti.</span><span class="sxs-lookup"><span data-stu-id="484c6-109">With those two roles you can kick unruly users, be on stage, and maybe release the confetti.</span></span> 

1. <span data-ttu-id="484c6-110">Edite su mundo y desplácese hacia abajo hasta la sección **en VR** ([Cómo administrar mundos](managing-worlds.md))</span><span class="sxs-lookup"><span data-stu-id="484c6-110">Edit your World and scroll down to the **In VR** section ([How to manage Worlds](managing-worlds.md))</span></span>

![Cambiar roles en la sección de en la VR](images/granting-roles.png)

2. <span data-ttu-id="484c6-112">Edite el campo **roles** si desea conceder roles específicos a usuarios específicos solo para este mundo.</span><span class="sxs-lookup"><span data-stu-id="484c6-112">Edit the **Roles** field if you want to grant specific roles to specific users just for this World.</span></span> <span data-ttu-id="484c6-113">Por ejemplo, si desea que el moderador del **presentador** le proporcione el moderador de  +   un dedo, debe agregar lo siguiente y seleccionar **Guardar**. </span><span class="sxs-lookup"><span data-stu-id="484c6-113">For example, if you want to give me **presenter** + **moderator** and give Calen **moderator**, you would add the following and select **Save**.</span></span> <span data-ttu-id="484c6-114">El formato es **{role}, {username o email}** en cada línea.</span><span class="sxs-lookup"><span data-stu-id="484c6-114">The format is **{role},{username or email}** on each line.</span></span> <span data-ttu-id="484c6-115">Username no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="484c6-115">Username is case-insensitive.</span></span> 

```
presenter,jimmy
moderator,jimmy
moderator,calen
```

3. <span data-ttu-id="484c6-116">Si vuelve a seleccionar **Editar** , debería ver lo siguiente sobre el campo roles.</span><span class="sxs-lookup"><span data-stu-id="484c6-116">If you select **Edit** again, you should see the following above the Roles field.</span></span> <span data-ttu-id="484c6-117">Así es como sabe actualizar en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="484c6-117">That's how you know updated in the database.</span></span>

```
Presenters: jimmy
Moderators: jimmy,calen
```

* <span data-ttu-id="484c6-118">Para que el cambio surta efecto en Altspace, debe restablecer el mundo, de forma que todos los usuarios puedan volver a unirse.</span><span class="sxs-lookup"><span data-stu-id="484c6-118">In order for the change to take effect in Altspace, you should reset the world, forcing everyone to rejoin.</span></span> <span data-ttu-id="484c6-119">A continuación encontrará una lista completa de los roles.</span><span class="sxs-lookup"><span data-stu-id="484c6-119">There's a full list of roles below.</span></span>

4. <span data-ttu-id="484c6-120">Edite el campo **roles contextuales** si desea conceder un rol a cada uno de ellos que se una a su mundo.</span><span class="sxs-lookup"><span data-stu-id="484c6-120">Edit the **Contextual Roles** field if you want to grant a role to every one that joins your World.</span></span> <span data-ttu-id="484c6-121">Por ejemplo, si desea permitir que las personas vuelen y usen el megaphone para que puedan escucharse entre sí mientras están en parte, agregue lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="484c6-121">For example, if you want to let people fly and use the megaphone so they can hear each other while far part, add the following:</span></span>

```
pilot,megaphone_only
```

<span data-ttu-id="484c6-122">Después de seleccionar **Actualizar**, restablezca el mundo.</span><span class="sxs-lookup"><span data-stu-id="484c6-122">After you select **Update**, reset the World.</span></span> <span data-ttu-id="484c6-123">Esto solo afectará a este mundo.</span><span class="sxs-lookup"><span data-stu-id="484c6-123">This will only affect this World.</span></span> <span data-ttu-id="484c6-124">Si desea conceder roles a un universo completo, edite los mismos campos en el universo.</span><span class="sxs-lookup"><span data-stu-id="484c6-124">If you want to grant roles to an entire Universe, edit the same fields on the Universe.</span></span> 

## <a name="roles"></a><span data-ttu-id="484c6-125">Roles</span><span class="sxs-lookup"><span data-stu-id="484c6-125">Roles</span></span> 

* <span data-ttu-id="484c6-126">**Presentador** : capacidades como poder estar en fase</span><span class="sxs-lookup"><span data-stu-id="484c6-126">**Presenter** - abilities like being able to be on stage</span></span>
* <span data-ttu-id="484c6-127">**Moderador** : capacidades como **Kick** to maintain Decorum</span><span class="sxs-lookup"><span data-stu-id="484c6-127">**Moderator** - abilities like **kick** to maintain decorum</span></span>
* <span data-ttu-id="484c6-128">**Terraformer** : capacidad de usar el editor mundial</span><span class="sxs-lookup"><span data-stu-id="484c6-128">**Terraformer** - ability to use the World Editor</span></span>
* <span data-ttu-id="484c6-129">**Piloto** : capacidad para alternar el modo de vuelo y generar la herramienta 6DOF Flight</span><span class="sxs-lookup"><span data-stu-id="484c6-129">**Pilot** - ability to toggle fly mode and spawn the 6DOF flight tool</span></span>
* <span data-ttu-id="484c6-130">**Megaphone_only** : capacidad de hablar con los oídos de los usuarios dondequiera que se encuentren en el mundo.</span><span class="sxs-lookup"><span data-stu-id="484c6-130">**Megaphone_only** - ability to speak into users' ears wherever they are in the World</span></span>
* <span data-ttu-id="484c6-131">**Showcase_new_sdk** : capacidad de generar aplicaciones de SDK de MRE</span><span class="sxs-lookup"><span data-stu-id="484c6-131">**Showcase_new_sdk** - ability to spawn MRE SDK apps</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="484c6-132">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="484c6-132">Troubleshooting</span></span>

<span data-ttu-id="484c6-133">**¿Puedo eliminar roles?**</span><span class="sxs-lookup"><span data-stu-id="484c6-133">**Can I delete roles?**</span></span>
<span data-ttu-id="484c6-134">No desde el formulario ahora mismo para que el archivo a Support Request en help.altvr.com y nos encargaremos de ello.</span><span class="sxs-lookup"><span data-stu-id="484c6-134">Not from the form right now so file a Support request at help.altvr.com and we'll take care of it for you</span></span>

<span data-ttu-id="484c6-135">**¿Se copian roles cuando un mundo importa desde otro?**</span><span class="sxs-lookup"><span data-stu-id="484c6-135">**Are roles copied when a World is importing from another?**</span></span>
<span data-ttu-id="484c6-136">No, los roles no se copian</span><span class="sxs-lookup"><span data-stu-id="484c6-136">No, roles aren't copied</span></span>