---
title: Agregar puntos de generación personalizados
description: Aprenda a crear, agregar y solucionar problemas de los puntos de generación personalizados a AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: Spawnpoint, solución de problemas
ms.openlocfilehash: 0f53bdc229eb21e50edef34981c592556236fc55
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213697"
---
# <a name="adding-custom-spawn-points"></a>Agregar puntos de generación personalizados

Los usuarios que escriban su mundo se **generarán** o aparecerán en el origen, en la posición (0,0), cuando entren en su mundo. Sin embargo, puede agregar uno o más puntos de generación si desea, por ejemplo, que los usuarios comiencen en la entrada a su. Si especifica varios puntos de generación, se elegirá uno aleatoriamente cada vez que alguien entre en él y el origen no se incluirá. Puede administrar puntos de generación a cualquier mundo o evento en el que esté habilitado su editor mundial. Puede controlar el lugar en el que se generan (posición) y la dirección a la que se enfrentarán (giro). Los puntos de generación solo estarán visibles en el modo de edición. 

1. Vaya cerca del lugar donde desea que se generen los usuarios. Abra el **Editor mundial > aspectos básicos** y asegúrese de que la opción **bloquear rotación** está activada. Seleccione el **punto de generación** para crear uno. Muévalo a la posición exacta que desee:

![Ventana de conceptos básicos del editor mundial abierta](images/spawn-points-img-01.png)

2. Seleccione en el icono de configuración para el punto de generación y asegúrese de que la **rotación > X** y la **rotación > Z** son **0**. Si son números pequeños como **8.537777745 e-07**, eso es bien. Esta es una peculiaridad de cómo se controlan los números de punto flotante:

![Actualizar puntos de generación en la configuración del editor World](images/spawn-points-img-02.png)

3. Vuelva a escribir el mundo a través de la **configuración del > de menús > General > volver a escribir espacio > volver a escribir**
4. Debe generar el nuevo punto de reproducción.
5. Si desea que los usuarios se encuentren en una dirección diferente, seleccione la configuración del punto de generación y establezca la **rotación solo > y** . Intente establecer Y en 180 y tanto X como Z en 0 (ADVERTENCIA: X y Z son avanzadas, por lo que las personas se enferman). Después, seleccione **confirmar** y volver a escribir el mundo. Eso debe generar una dirección opuesta. 

## <a name="troubleshooting"></a>Solución de problemas

**¿La gente todavía está generando en el origen?**
    * Asegúrese de que los puntos de generación están ligeramente por encima del suelo o la superficie. Si el punto de generación se superpone a otros objetos, los usuarios se crean en la ubicación predeterminada, el origen. Esto puede ocurrir si el punto de generación dentro de un objeto y el alto de la persona varía. 
    * Intente restablecer el mundo a través de la **configuración del > de menús > moderada > el espacio de restablecimiento**

**¿Tiene varios puntos de generación pero sigue generando en el mismo lugar?**
Es posible que no esté de suerte: es aleatorio después de todo. Intente realizar una serie de reentrada al menos cinco veces antes de suponer que hay un error. 

**La gente está inestable o su cabeza está inclinada** Es posible que haya olvidado comprobar la **rotación de bloqueos** o establecer el valor X y Z para la rotación. Normalmente, se deben establecer en 0 a menos que esté creando un mundo exótico. 

**¿Las personas que caen al generar?**
No establezca una posición de punto de generación demasiado alta sobre un objeto. Si están demasiado lejos, se regenerarán en el origen.