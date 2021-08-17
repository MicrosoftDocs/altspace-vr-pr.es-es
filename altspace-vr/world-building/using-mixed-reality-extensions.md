---
title: Uso de una Mixed Reality extensión
description: Obtenga información sobre cómo usar y solucionar problemas Mixed Reality extensiones para ampliar y adaptar sus mundos altspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: realidad mixta, extensiones, solución de problemas
ms.openlocfilehash: 1439ca76eaf4e0235c6552d037e55b6151e08407871bf470b3011b6cf8cbccd5
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125364"
---
# <a name="using-a-mixed-reality-extension"></a>Uso de una Mixed Reality extensión

[Mixed Reality extensions](https://developer.altvr.com/) (MREs) son aplicaciones que puede usar en sus mundos desde [cascos](https://account.altvr.com/mres/1173667287173955931) a un [Stargate en funcionamiento.](https://account.altvr.com/mres/1152987031857529562) Así es como los miembros de la comunidad con experiencia en programación pueden ampliar Altspace y los creadores de mundos un solo sentido pueden hacer que sus mundos sea más interactivo. Aunque cualquier persona de un mundo puede usar mres, solo los usuarios del Programa world building pueden examinar y generar MRE en sus mundos. 

1. Examine la sección MRE de nuestro sitio [web.](https://account.altvr.com/mres) De forma predeterminada, verá sus propios MRE, así que  seleccione **Altspace** para ver los MRE oficiales y destacados para ver los MRE de la comunidad. Familiarícese con cualquier MRE antes de usarlo en su mundo. 
2. Vaya al MRE [De cascos](https://account.altvr.com/mres/1173667287173955931) y seleccione **Copiar al Portapapeles.** 
3. Escriba su mundo y abra el Editor del mundo en **Conceptos básicos > aplicación del SDK.** Pegue la dirección URL de Los cascos en el campo URI de destino y seleccione **Confirmar**. Debe aparecer el objeto MRE e intentar conectarse al MRE que se ejecuta en la nube. Ahora debería ver algunos cascos en los que puede hacer clic.
4. Mueva, rote o escale el MRE como haría con cualquier otro objeto world.

¡Enhorabuena! Ahora usa MRE, es tan interesante.

## <a name="troubleshooting"></a>Solución de problemas

**MRE muestra un emoji desaprobado** 
    * Compruebe que la dirección URL es correcta.
    * Alterne **la opción Reproducción** en el objeto y elija **Confirmar.**
    * Pruebe a volver a escribir

**MRE está en retraso** Dependiendo de dónde se hospeda un MRE, puede experimentar cierta latencia de red.

**¿Por qué tenemos que pegar direcciones URL?**
En el futuro, puede administrar y generar MRE como lo hace Artifacts desde kits. Hasta entonces, seguiremos usando direcciones URL