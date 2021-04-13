---
title: Ayuda del cargador de Unity
description: Manténgase al día de las últimas preguntas y soluciones más frecuentes para el cargador de Unity de AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: ayuda, preguntas más frecuentes
ms.openlocfilehash: 814ff293cb98490900cd929f33477d15d3d668ae
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213842"
---
# <a name="unity-uploader-help"></a>Ayuda del cargador de Unity

**1. ¿Cómo es increíble esta herramienta?**

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/cheyenne-mountain-gate-room-v1/player]

Esta es mi escena Stargate Unity con una aplicación de SDK que enciende la puerta y DND

**2. soy un aprendizaje en vídeo, ¿dónde están mis vídeos?**

[Consulte nuestros vídeos](https://youtu.be/km9CnVYPzoM)

**3. ¿Dónde puedo encontrar ejemplos?**

Los [mundos destacados](https://account.altvr.com/worlds/featured) y los [ejemplos de Jimmy](https://account.altvr.com/worlds/1046572460192825569) son buenos lugares para empezar

**4. ¿funcionará con kits y con el nuevo SDK?**
Sí, puede usar todas las herramientas juntas si lo desea. Estamos intentando desarrollarlos para que funcionen juntos sin problemas.

**5. ¿admite efectos de partículas?**

![GIF de efectos de partículas de nieve](images/uploader-faq-img-01.gif)

**6. ¿puedo obtener audio espacial?**
En este momento, pero puede colocar fuentes de audio para reproducirlos en áreas localizadas. 

**7. ¿funciona la iluminación?**
Sí, pero las luces tienen que establecerse en "cocida" y no en "mixta"

**8. ¿funciona la iluminación global?**
Sí

**9. ¿siempre tiene que restablecer el mundo?**
Sí. Tenemos que volver a cargar los paquetes de recursos de Unity cada vez. 

**10. ¿Puedo usar mis propios materiales y sombreadores personalizados?**

![GIF de materiales y sombreadores personalizados](images/uploader-faq-img-02.gif)

**11. ¿puedo cargar solo en una plataforma?**
Sí, con la herramienta de cargador. Sin embargo, las personas que se encuentran en Android no verán nada en su mundo hasta que cargue la escena para su plataforma. 

**12. ¿se permiten los scripts?**
No, por motivos de seguridad, no se pueden permitir scripts ni referencias de script. Si la carga contiene scripts o referencias de script, se rechazarán. Eche un vistazo al nuevo SDK si necesita crear scripts. 

**13. ¿Qué tamaño de una escena se puede cargar?**
Le recomendamos que comience a ser pequeño y tenga en cuenta las personas de Altspace que no tienen Monster PC. Dicho esto, hemos hecho que los juegos incorporen sus mapas de secuencias en directo (por ejemplo, en un juego de lanzamiento de la VR)

![Captura de pantalla del juego VR en AltspaceVR](images/uploader-faq-img-03.png)

**14. ¿tengo que hospedar los archivos de la escena?**
No, Altspace está sirviendo los archivos una vez cargados

**15. ¿se permiten las sombras?**
Sí

**16. ¿con qué rapidez puedo recorrer en iteración el uso del cargador?**
Si ya está en su mundo, puede presionar cargar en el cargador, restablecer su mundo y ver la escena actualizada en tan solo 10 segundos. Normalmente, verá bucles de 30 segundos a unos minutos según la complejidad de la escena. Tiene una bebida, se lo merece para ser un creador internacional.

**17. ¿Dónde obtengo los modelos 3D?**
Sketchfab, SketchUp, Minecraft, almacén de recursos de Unity, etc.

**18. ¿admite animaciones?**

![GIF de animaciones personalizadas en ejecución](images/uploader-faq-img-04.gif)

**19. ¿Cómo puedo configurar el audio espacial?** Importe el archivo WAV que prefiera, cree un objeto de juego vacío en la escena y seleccione este objeto. Arrastre y coloque el sonido importado en el inspector del objeto y creará un origen de audio. Después, ajuste el volumen a un máximo de 0,5, cambie la mezcla espacial a 3D y ajuste la distancia mínima y máxima para crear un área de sonido adecuada. Esto se muestra como una esfera como colisionadores de forma predeterminada. Para obtener un verdadero desactivado, deberá ajustar la curva de la lista desplegable a su gusto. [(Via @IsThatToasted )](https://www.youtube.com/watch?v=ktb2vAAwknw&list=PLGmYIROty-5bpzKQNK3mRMi4pmh_LinV4&t=642s&index=29)

**20. ¿Cómo veo Cross-Eyed/extraña?**
A veces, el cargador no invalida correctamente la configuración de representación. "Ir a editar > configuración del proyecto > Player". Asegúrese de que está activada la opción "XR Settings > realidad virtual" y "método de representación estéreo" es "Single pass" o "single Pass (Preview)" para PC y Android (seleccione el icono de robot). Después vuelva a compilar y volver a cargar y restablecer su mundo. 