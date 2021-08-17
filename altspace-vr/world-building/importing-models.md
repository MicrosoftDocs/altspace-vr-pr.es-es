---
title: Importación de modelos glTF
description: Aprenda a importar correctamente modelos glTF 3D en las experiencias de AltspaceVR y a solucionar cualquier problema.
ms.date: 03/11/2021
ms.topic: article
keywords: models, glTF, importing, sketchfab, troubleshooting
ms.openlocfilehash: 527c38fc49028258fa432445fe14a355710a18be65ee74252a8c39bc1bfe5190
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127093"
---
# <a name="importing-gltf-models"></a>Importación de modelos glTF

> [!NOTE]
> Esta característica está disponible para usuarios seleccionados en el programa acceso anticipado en este momento.

Una manera de traer modelos y escenas 3D a Altspace es usar el [estándar glTF](https://en.wikipedia.org/wiki/GlTF). Puede cargar un archivo .glb (glTF empaquetado) para crear un modelo que puede generar más adelante en el Editor del mundo. Es una alternativa a cargar [sus propios kits.](uploading-custom-kits.md) Se recomienda crear modelos para demostraciones rápidas, ya que no es necesario usar Unity y kits cuando quiera maximizar el rendimiento y la reusabilidad. 

1. Busque algunos recursos glTF 3D. Un lugar donde buscar es Sketchfab (pruebe a filtrar por **modelos descargables** como [este](https://sketchfab.com/search?features=downloadable&q=low+poly+wolf&sort_by=-pertinence&type=models)). Una vez que lo encuentre, **seleccione Download 3D Model (Descargar modelo 3D):**

![Modelo de perro 3D de Sketchfab](images/importing-models-img-01.png)

2. Copie el vínculo al modelo y lea los requisitos de licencia. 
3. Descargar la **versión del formato autoconvertido (glTF)**

![Opciones de descarga de Sketchfab con el formato convertido automáticamente resaltado](images/importing-models-img-02.png)

4. Abra el [sitio de GLB Packer](https://glb-packer.glitch.me) y active la casilla **Convertir PNG a JPEG (beta)**
5. Descomprima los archivos glTF que descargó y arrástrelos todos a la vez a la pestaña del explorador GLB Packer.

![Ventana que muestra la descompresión del modelo](images/importing-models-img-03.png)

6. Según el número y el tamaño de los archivos, puede tardar un tiempo en procesarse. Cuando se realiza el procesamiento, se descarga un archivo **out.glb.** Cambie el nombre de ese archivo a algo informativo: este será el nombre del objeto en el mundo (por **ejemplo, Low Poly Wolf.glb).**
7. Vaya a [altvr.com > Más > modelos y](https://account.altvr.com/users/sign_in) seleccione **Crear.**
8. Especifique la ubicación del archivo .glb y asegúrese de copiar el vínculo Sketchfab en la descripción para la atribución. Puede especificar una imagen de vista previa si lo desea y, a continuación, **seleccionar Crear modelo:**

![Vista previa del modelo en AltspaceVR](images/importing-models-img-04.png)

9. Seleccione **Copiar en el Portapapeles.**
10. Abra el **Editor del mundo > Altspace > Basics > GLTF**
11. Pegue la dirección URL y seleccione **Confirmar.**

¡Enhorabuena! Acaba de generar su primer modelo.

## <a name="troubleshooting"></a>Solución de problemas

**Al hacer clic en Confirmar **que no** ha ocurrido nada**
    * Actualmente tenemos un límite de polígono de 100 000. Si se produce un error, elimine el objeto para evitar posibles problemas con los usuarios que se unen a su mundo.
    * Puede haber otros problemas con el recurso. Intente usar recursos con el menor número de polígonos posible.
    * El modelo que va a incorporar puede ser pequeño o grande. Pruebe a aumentar o reducir la escala o mueva el avatar, es posible que esté de pie dentro del modelo.

**La carga es lenta** La rapidez con la que otros usuarios del mundo la cargan dependerá de sus velocidades de conexión. Tampoco se almacena en caché como recursos de Kit. Si coloca uno en su página principal, terminará por volver a descargar el mismo modelo cada vez que se una, lo que no es excelente.

**No hay ninguna colisión** De forma predeterminada, no hay ninguna colisión en los objetos que se traen de esta manera.

**Al generarlo, se pierden los controles** en seis DOF o estoy dentro, por lo que es difícil manipularlo. Sí, somos conscientes de estos problemas y esperamos solucionarlos pronto.  