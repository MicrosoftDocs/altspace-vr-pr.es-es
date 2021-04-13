---
title: Usar una extensión de realidad mixta
description: Obtenga información sobre cómo usar y solucionar problemas de las extensiones de la realidad mixta para extender y adaptar sus mundos de AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: realidad mixta, extensiones, solución de problemas
ms.openlocfilehash: 498e71c48f7c67abc40ce4f4667c9eeac4c4e73b
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213653"
---
# <a name="using-a-mixed-reality-extension"></a>Usar una extensión de realidad mixta

[Las extensiones de realidad mixta](https://developer.altvr.com/) (MREs) son aplicaciones que se pueden usar en los mundos desde [cascos](https://account.altvr.com/mres/1173667287173955931) a un [Stargate](https://account.altvr.com/mres/1152987031857529562)de trabajo. Este es el modo en que los miembros de la comunidad con experiencia de programación pueden extender Altspace y los creadores del mundo unidireccional pueden hacer que sus mundos sean más interactivos. Aunque MREs puede ser usado por cualquier persona de un mundo, solo las personas del programa de creación mundial pueden examinar y generar MREs en sus mundos. 

1. Examine la sección MRE de nuestro [sitio web](https://account.altvr.com/mres). De forma predeterminada, verá su propio MREs, así que seleccione en **Altspace** para ver MREs oficiales y **destacados** para ver MREs de la comunidad. Familiarícese con cualquier MRE antes de usarlo en su mundo. 
2. Vaya a la MRE [cascos](https://account.altvr.com/mres/1173667287173955931) y seleccione **copiar al portapapeles**. 
3. Escriba su mundo y abra el editor mundial en **basics > aplicación SDK**. Pegue la dirección URL de los cascos en el campo URI de destino y seleccione **confirmar**. El objeto MRE debe aparecer e intentar conectarse a la MRE que se ejecuta en la nube. Ahora debería ver algunos cascos en los que puede hacer clic.
4. Mueva/rote/escale el MRE igual que haría con cualquier otro objeto del mundo.

¡Enhorabuena! Está usando MREs Now (ya está tan divertido).

## <a name="troubleshooting"></a>Solución de problemas

**MRE muestra un Emoji desenfadado** 
    * Compruebe que la dirección URL es correcta
    * Alternar la opción de **reproducción** en el objeto y elegir **confirmar**
    * Intente volver a escribir

**MRE está retrasado** Dependiendo de dónde se hospede un MRE, puede experimentar una latencia de red

**¿Por qué es necesario pegar las direcciones URL?**
En el futuro, puede administrar y generar MREs como si se tratara de los artefactos de los kits. Hasta entonces, seguiremos usando las direcciones URL