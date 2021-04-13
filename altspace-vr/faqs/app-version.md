---
title: Búsqueda de la versión de la aplicación AltspaceVR
description: Aprenda a usar la aplicación AltspaceVR, la configuración y los registros de cliente para encontrar la versión de AltspaceVR que está ejecutando actualmente.
ms.date: 02/10/2021
ms.topic: article
keywords: versión de la aplicación
ms.openlocfilehash: 5d503d3b89cd213696dd53616c5c7e3013aeef01
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213775"
---
# <a name="finding-the-altspacevr-app-version"></a><span data-ttu-id="7c100-104">Búsqueda de la versión de la aplicación AltspaceVR</span><span class="sxs-lookup"><span data-stu-id="7c100-104">Finding the AltspaceVR app version</span></span>

<span data-ttu-id="7c100-105">En el transcurso de la solución de un problema, es posible que se le pregunte qué versión de la aplicación AltspaceVR está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="7c100-105">In the course of troubleshooting an issue, you may be asked what version of the AltspaceVR app you're currently running.</span></span>

## <a name="in-altspacevr"></a><span data-ttu-id="7c100-106">En AltspaceVR</span><span class="sxs-lookup"><span data-stu-id="7c100-106">In AltspaceVR</span></span>

<span data-ttu-id="7c100-107">Para buscar la versión de la aplicación en AltspaceVR, vaya al **menú configuración** y seleccione **acerca** de en la barra de navegación izquierda.</span><span class="sxs-lookup"><span data-stu-id="7c100-107">To find the app version in AltspaceVR, navigate to the **settings menu** and select **About** in the left navigation bar.</span></span> <span data-ttu-id="7c100-108">Aquí se indica la versión de la aplicación, como se muestra en la captura de pantalla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c100-108">The 'App Version' is reported here, as shown in the screenshot below.</span></span>

![Menú de configuración abrir con el panel de información abierto](images/app-version-img-01.png)

## <a name="in-windows-system-settings"></a><span data-ttu-id="7c100-110">En configuración del sistema de Windows</span><span class="sxs-lookup"><span data-stu-id="7c100-110">In Windows System Settings</span></span>

<span data-ttu-id="7c100-111">Si instaló AltspaceVR mediante el Microsoft Store, también puede buscar la versión de la aplicación en la configuración del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c100-111">If you installed AltspaceVR via the Microsoft Store, you can additionally find the app version in the Windows system settings.</span></span>  <span data-ttu-id="7c100-112">Este escenario es una buena opción para notificar la versión de la aplicación si no puede iniciar sesión correctamente en el cliente.</span><span class="sxs-lookup"><span data-stu-id="7c100-112">This scenario is a good fit when reporting the app version if you're unable to successfully log into the client.</span></span>

<span data-ttu-id="7c100-113">Para buscar la versión de la aplicación en la configuración del sistema de Windows, abra el **menú Inicio**, escriba en **aplicaciones & características** y seleccione el resultado.</span><span class="sxs-lookup"><span data-stu-id="7c100-113">To find the app version in Windows system settings, open the **Start Menu**, type in **Apps & Features**, and select the result.</span></span> <span data-ttu-id="7c100-114">Vaya a **AltspaceVR** en la lista de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7c100-114">Navigate to **AltspaceVR** in the list of apps.</span></span> <span data-ttu-id="7c100-115">Haga clic con el botón izquierdo en AltspaceVR y seleccione **Opciones avanzadas** en el menú que aparece.</span><span class="sxs-lookup"><span data-stu-id="7c100-115">Left-click AltspaceVR and select **Advanced Options** from the menu that appears.</span></span>

![Menú Aplicaciones y características abierto con la opción Opciones avanzadas resaltada](images/app-version-img-02.png)

<span data-ttu-id="7c100-117">En las **Opciones avanzadas**, en el encabezado de **Especificaciones** , la versión de la **aplicación** debe aparecer a la derecha de la etiqueta de **versión** .</span><span class="sxs-lookup"><span data-stu-id="7c100-117">In the **Advanced Options**, under the **Specifications** header, the **App Version** should be listed to the right of the **Version** label.</span></span>

![Opciones avanzadas abiertas con la versión de la aplicación resaltada](images/app-version-img-03.png)

## <a name="in-client-logs"></a><span data-ttu-id="7c100-119">En registros de cliente</span><span class="sxs-lookup"><span data-stu-id="7c100-119">In Client Logs</span></span>

<span data-ttu-id="7c100-120">AltspaceVR informa de la versión de la aplicación en el archivo de registros de cliente como "versión de Altspace" durante el inicio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7c100-120">AltspaceVR reports the app version in the client logs file as "Altspace Version" during application startup.</span></span> <span data-ttu-id="7c100-121">Esta sería una buena opción para obtener la versión de la aplicación si no puede iniciar sesión correctamente en el cliente, pero se ha intentado iniciar antes de que se produjera un error.</span><span class="sxs-lookup"><span data-stu-id="7c100-121">This would be a good option to get the app version if you can't successfully log into the client, but it did attempt to start before failing.</span></span>

## <a name="windows"></a><span data-ttu-id="7c100-122">Windows</span><span class="sxs-lookup"><span data-stu-id="7c100-122">Windows</span></span>

<span data-ttu-id="7c100-123">En Windows, el archivo de registro de cliente se puede encontrar a través del explorador de Windows en:</span><span class="sxs-lookup"><span data-stu-id="7c100-123">On Windows, the client logs file can be found via Windows Explorer at:</span></span>

```
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player.log
%userprofile%\appdata\locallow\altspacevr\altspacevr\Player-prev.log
```

<span data-ttu-id="7c100-124">Este archivo se sobrescribe cada vez que se inicia AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="7c100-124">This file is overwritten each time you launch AltspaceVR.</span></span> <span data-ttu-id="7c100-125">' Player. log ' representa la sesión más reciente y ' Player-Prev. log ' representa la sesión anterior.</span><span class="sxs-lookup"><span data-stu-id="7c100-125">'Player.log' represents your latest session, and 'Player-prev.log' represents the previous session.</span></span>

## <a name="via-powershell"></a><span data-ttu-id="7c100-126">A través de PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c100-126">Via PowerShell</span></span>

<span data-ttu-id="7c100-127">Los usuarios avanzados pueden buscar en los registros de cliente esta cadena a través de PowerShell de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7c100-127">Advanced users can search the client logs for this string via PowerShell as follows:</span></span>

<span data-ttu-id="7c100-128">Entrada:</span><span class="sxs-lookup"><span data-stu-id="7c100-128">Input:</span></span>

```
gc $env:userprofile\appdata\locallow\altspacevr\altspacevr\Player.log | ? { $_ -match "Altspace Version" }
```

<span data-ttu-id="7c100-129">Salida:</span><span class="sxs-lookup"><span data-stu-id="7c100-129">Output:</span></span>

<span data-ttu-id="7c100-130">[2,047] versión de AltspaceVR: 3.2.23. e66c2</span><span class="sxs-lookup"><span data-stu-id="7c100-130">[2.047] AltspaceVR Version: 3.2.23.e66c2</span></span>