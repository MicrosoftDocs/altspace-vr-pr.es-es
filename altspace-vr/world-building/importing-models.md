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
# <a name="importing-gltf-models"></a>Importar modelos glTF

> [!NOTE]
> Esta característica está disponible para los usuarios seleccionados en el programa de acceso temprano en este momento.

Una manera de incluir modelos y escenas 3D en Altspace es usar el [estándar glTF](https://en.wikipedia.org/wiki/GlTF). Puede cargar un archivo. glb (glTF empaquetado) para crear un modelo que puede generar posteriormente en el editor mundial. Es una alternativa a [cargar sus propios kits](uploading-custom-kits.md). Se recomienda crear modelos para demostraciones rápidas porque no necesitará usar Unity y kits cuando quiera maximizar el rendimiento y la reutilización. 

1. Busque algunos activos de glTF 3D. Un lugar en el que buscar es Sketchfab (probar el filtrado de modelos **descargables** como [este](https://sketchfab.com/search?features=downloadable&q=low+poly+wolf&sort_by=-pertinence&type=models)). Una vez que lo encuentre, seleccione **Descargar modelo 3D**:

![modelo de perro en 3D de Sketchfab](images/importing-models-img-01.png)

2. Copie el vínculo en el modelo y lea los requisitos de licencia. 
3. Descargar la versión de **formato autoconvertido (glTF)**

![Sketchfab opciones de descarga con el formato de conversión automático resaltado](images/importing-models-img-02.png)

4. Abra el sitio de [glb Pack](https://glb-packer.glitch.me) y active la casilla **convertir PNG en JPEG (beta)** .
5. Descomprimir los archivos glTF que descargó y arrástrelos todos a la vez a la pestaña del explorador GLB Pack

![Ventana que muestra la descompresión del modelo](images/importing-models-img-03.png)

6. En función del número y el tamaño de los archivos, puede tardar un tiempo en procesarse. Una vez finalizado el procesamiento, se descargará un archivo **out. glb** . Cambie el nombre de ese archivo a algo informativo, es decir, el nombre del objeto en el mundo (por ejemplo, **Wolf. glb).**
7. Vaya a [altvr.com > más > modelos](https://account.altvr.com/users/sign_in) y seleccione **crear** .
8. Especifique la ubicación del archivo. glb y asegúrese de copiar el vínculo de Sketchfab en la descripción de atribución. Si lo desea, puede especificar una imagen de vista previa y, a continuación, seleccionar **crear modelo**:

![Vista previa del modelo en AltspaceVR](images/importing-models-img-04.png)

9. Seleccionar **copiar al portapapeles**
10. Abra el **Editor mundial > Altspace > basics > GLTF**
11. Pegue la dirección URL y seleccione **confirmar**

¡Enhorabuena! Acaba de generar su primer modelo.

## <a name="troubleshooting"></a>Solución de problemas

**Al hacer clic en **confirmar** que no se ha producido nada**
    * Actualmente tenemos un límite de 100 000 polígonos. Si se produce un error, elimine el objeto para evitar posibles problemas con los usuarios que se unen a su mundo
    * Puede haber otros problemas con el recurso. Intente usar recursos con el menor número posible de polígonos.
    * El modelo que se va a incorporar puede ser pequeño o grande. Pruebe a aumentar o reducir el tamaño de la escala o a mover el avatar en torno al modelo.

Es **lento de cargar** La rapidez con la que se cargan otros usuarios del mundo dependerá de sus velocidades de conexión. Tampoco se almacena en caché como los recursos del kit. Si coloca uno en su hogar, terminará de volver a descargar el mismo modelo cada vez que se una al unirse, lo que no es genial.

No **hay ninguna colisión** De forma predeterminada, no hay ninguna colisión en los objetos que se incorporan de esta manera

**Al generarlo, pierdo los controles en seis DOF o estoy dentro, por lo que es difícil manipularlo** . Sí, somos conscientes de estos problemas y esperamos solucionarlos pronto.  