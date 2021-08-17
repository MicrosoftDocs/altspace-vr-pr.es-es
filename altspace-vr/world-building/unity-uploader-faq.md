---
title: Ayuda del uploader de Unity
description: Manténgase al día de las últimas preguntas y soluciones más frecuentes para altspaceVR Unity Uploader.
ms.date: 02/10/2021
ms.topic: article
keywords: ayuda, preguntas más frecuentes
ms.openlocfilehash: cb983ba4e23186f7cc62043f75e7ea1b2969e92b6bd30b132f1733b5e25e92dd
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125735"
---
# <a name="unity-uploader-help"></a>Ayuda del uploader de Unity

**1. ¿Qué increíble es esta herramienta?**

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/cheyenne-mountain-gate-room-v1/player]

Esa es mi escena de Stargate Unity con una aplicación de SDK que potencia la puerta y el DND.

**2. Soy un aprendiz de vídeo, ¿dónde están mis vídeos?**

[Consulte nuestros vídeos.](https://youtu.be/km9CnVYPzoM)

**3. ¿Dónde puedo encontrar ejemplos?**

[Los mundos destacados](https://account.altvr.com/worlds/featured) [y los ejemplos de Jimmy](https://account.altvr.com/worlds/1046572460192825569) son buenos lugares para empezar

**4. ¿Funcionará con kits y el nuevo SDK?**
Sí, puede usar todas las herramientas juntas si lo desea. Estamos intentando desarrollarlos para que funcionen sin problemas juntos.

**5. ¿Admite efectos de partícula?**

![GIF de efectos de partícula de nieve](images/uploader-faq-img-01.gif)

**6. ¿Puedo obtener audio espacializado?**
No en este momento, pero puede colocar orígenes de audio para reproducir en áreas localizadas. 

**7. ¿Funciona la iluminación al día?**
Sí, pero las luces deben establecerse en "asada" y no "mixta".

**8. ¿Funciona la iluminación global?**
Sí

**9. ¿Siempre tiene que restablecer el mundo?**
Sí. Tenemos que volver a cargar los paquetes de recursos de Unity cada vez. 

**10. ¿Puedo usar mis propios materiales y sombreadores personalizados?**

![GIF de materiales y sombreadores personalizados](images/uploader-faq-img-02.gif)

**11. ¿Puedo cargar solo en una plataforma?**
Sí, mediante la herramienta Uploader. Sin embargo, las personas que están en Android no verán nada en su mundo hasta que cargue la escena para su plataforma. 

**12. ¿Se permiten scripts?**
No, por motivos de seguridad no se pueden permitir scripts ni referencias de script. Si la carga contiene scripts o referencias de script, se rechazará. Echa un vistazo al nuevo SDK si el mundo necesita scripting. 

**13. ¿Qué tamaño de una escena puedo cargar?**
Le recomendamos que empiece pequeño y tenga en cuenta a las personas de Altspace que no tienen equipos macastros. Dicho esto, hemos tenido juegos que traen sus mapas para transmisiones en vivo (por ejemplo, En adelante, un juego de realidad virtual).

![Captura de pantalla del juego vr en AltspaceVR](images/uploader-faq-img-03.png)

**14. ¿Tengo que hospedar los archivos de escena?**
No, Altspace sirve los archivos una vez cargados.

**15. ¿Se permiten sombras?**
Sí

**16. ¿Con qué rapidez puedo iterar mediante uploader?**
Si ya está en su mundo, puede presionar Upload en uploader, restablecer el mundo y ver la escena actualizada en tan solo 10 segundos. Normalmente, verá bucles de 30 segundos a unos minutos, dependiendo de la complejidad de la escena. Beba, se lo merece por ser world-builder.

**17. ¿Dónde se obtienen los modelos 3D?**
Sketchfab, Sketchup, Minecraft, Unity Asset Store, entre otros.

**18. ¿Admite animaciones?**

![GIF de animaciones personalizadas en ejecución](images/uploader-faq-img-04.gif)

**19. ¿Cómo puedo configurar el audio espacial?** Importe el archivo wav que prefiera, cree un objeto de juego vacío en la escena y seleccione este objeto. Arrastre y coloque el sonido importado en el inspector del objeto y creará un origen de audio. Después, ajuste el volumen a no más de 0,5, cambie la mezcla espacial a 3D y ajuste la distancia mínima y máxima para crear un área de sonido adecuada. Esto se muestra como esfera como colisionador de forma predeterminada. Para obtener una entrega verdadera, deberá ajustar la curva de entrega a su gusto. [(a través @IsThatToasted de )](https://www.youtube.com/watch?v=ktb2vAAwknw&list=PLGmYIROty-5bpzKQNK3mRMi4pmh_LinV4&t=642s&index=29)

**20. ¿Cómo puedo ver el desasociación con los ojos cruzados?**
A veces, uploader no invalida correctamente la configuración de representación. "Ir a Editar > Project Configuración > Player". Asegúrese de que "XR Configuración > Virtual Reality Supported" (Compatible con la realidad virtual de XR) esté activada y que el "Método de representación estéreo" sea "Single Pass" o "Single Pass (Preview)" para PC y Android (seleccione el icono de robot). Después, vuelva a compilar y cargar y restablezca el mundo. 