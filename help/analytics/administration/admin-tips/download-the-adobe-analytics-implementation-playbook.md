---
title: 'Descargar el libro de estrategias de implementación  [!DNL Adobe Analytics] '
description: Un Documento de requisitos empresariales (denominado comúnmente BRD) es una documentación muy importante en la que los principales actores, los usuarios empresariales y los usuarios tecnológicos querrán colaborar. Es un sitio para documentar todos los KPI deseados, los requisitos de creación de informes y cualquier punto de datos que desee ver cuando se complete la implementación de AA.
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10530.jpg
kt: 10530
exl-id: 42679c86-e08f-4dda-8e47-f9880409bad6
source-git-commit: cae626cb3958ebcda16ac30b0a487ebfe06d50f4
workflow-type: tm+mt
source-wordcount: '1779'
ht-degree: 0%

---

# Descargar el manual de implementación de [!DNL Adobe Analytics]

Antes de comenzar, [descargue el manual](assets/aa-implementation-playbook.xlsx).

## Pestaña Requisitos empresariales

**QUÉ:** Un Documento de requisitos empresariales (denominado comúnmente BRD) es una documentación muy importante en la que los principales actores, los usuarios empresariales y los usuarios tecnológicos querrán colaborar. Es un sitio para documentar todos los KPI deseados, los requisitos de informes y cualquier punto de datos que desee ver cuando se complete la implementación de [!DNL Adobe Analytics] (AA).

**POR QUÉ:** Esto sirve como punto de partida para la documentación siguiente (SDR, especificaciones técnicas, etc.) y es una fuente fiable común para un estado final de AA acordado. Este documento organiza las ideas entre los equipos de la organización para formar una guía que le lleve a avanzar en la creación o mejora de su implementación.

**CÓMO:** La documentación de los requisitos empresariales la suelen elaborar los usuarios empresariales finales de AA, pero es importante recibir comentarios de los usuarios tecnológicos, ya que puede haber desafíos técnicos que tener en cuenta y algunos puntos de datos pueden requerir más esfuerzo que otros, lo que influye en la priorización.

Pregúntese &quot;qué cosas queremos rastrear en nuestro sitio&quot;, &quot;qué puntos de datos serán importantes para mí en el uso de los informes&quot; y, lo más importante, &quot;cómo informarán estos puntos de datos las decisiones&quot;. Es importante asegurarse de que cada uno de los requisitos empresariales esté relacionado con un punto de datos que pueda utilizarse para informar las decisiones empresariales. Por ejemplo, puede resultar tentador querer rastrear cada clic en el sitio, pero, al final, ¿qué datos se obtienen de ese informe?

Comience por rellenar la columna C en la captura de pantalla siguiente (Requisito empresarial). Esto debería ser algo como &quot;Cuántas búsquedas internas se completan en nuestro sitio&quot; o &quot;Qué campaña interna es más efectiva en términos de impresiones&quot;. Después de completar este nivel de detalle, puede volver atrás y rellenar la columna B (Categoría) y agrupar los requisitos en categorías como &quot;Búsqueda&quot; o &quot;Promoción interna&quot;, que deben corresponder bien con sus secciones de especificaciones técnicas.

También indicará si cree que el uso de una eVar, evento, propiedad o combinación logrará lo que busca rastrear.

Y, por último, la columna Estado de implementación servirá como una comprobación de estado cuando comience a añadir cosas al sitio.

![Documento de requisitos empresariales](assets/brd-template.png)

## Pestaña Mapa de variables (documentación de etiquetado/SDR)

**QUÉ:** Un documento de etiquetado (denominado comúnmente SDR) es una documentación fundamental que resulta útil tanto para los usuarios técnicos como para los usuarios empresariales de AA. Enumera todas las variables que utilizan los grupos de informes junto con todos los detalles relevantes para la configuración de variables, cómo se implementa la variable y cuál es su propósito en la creación de informes. Al igual que el documento de propiedades, debe ser un documento de Excel activo y bien controlado, con una persona responsable de mantenerlo actualizado a medida que se introduzcan mejoras de etiquetado o cambios de implementación.

**POR QUÉ:** Este documento tendrá muchos propósitos, pero los más importantes son los siguientes:

* Para cualquier persona nueva en su implementación (nuevo empleado, propietario del negocio que busque comprender mejor los informes disponibles, etc.), este documento proporciona la mejor vista de todas las variables implementadas y cuál es su propósito para que las personas puedan autoabastecerse en términos de aprendizaje de la configuración de AA.
* Para el propietario/usuario técnico del producto de AA, este documento sirve como recordatorio de cómo se configuran otras variables y cuáles están disponibles para usarse al añadir una nueva dimensión.

**CÓMO:** Comience enumerando todas las [!DNL Adobe] variables predeterminadas (página, producto, ubicación geográfica, etc.), así como eVars, props, eventos y variables de lista en un documento de Excel. Debe tener una pestaña por sitio o grupo de informes.
Para cada una de estas dimensiones, añado las siguientes columnas:

* **Nombre:** Proporcione un nombre sencillo y corto que la mayoría pueda entender. Debería ser lo suficientemente intuitivo como para que un nuevo usuario pueda leerlo y comprender qué es lo que pretende capturar la variable.
* **Descripción:** más información sobre para qué se utiliza la variable y qué datos rastrea. Lo dejo corto y simple y hago que coincida con la descripción utilizada en la interfaz. Lo ideal es que mis usuarios no necesiten consultar el documento de etiquetado. Por lo tanto, cuando se configura una nueva dimensión en el servidor de administración, añado la misma descripción allí. De este modo, el usuario puede pulsar el icono de información directamente en Workspace para comprender qué es una dimensión: no es necesario ir a un documento de Excel.

![URL de página simplificada](assets/page-url-simplified.png)

* **Código:** El código del servidor que establece el valor. Puede ser el campo de la capa de datos de la página o puede llamar para que esto se haga con una regla de Launch, una regla de procesamiento, etc.
* **Informes de clasificación:** llame a cualquier informe de clasificación que se ejecute con el Importador de clasificaciones o el Generador de reglas de clasificación
* **Ámbito de la solución:** Me parece útil enumerar todas las propiedades (al menos las que usan más que variables estándar) en columnas pequeñas y agregar una marca de verificación para cada dimensión que se establezca en esa propiedad. Esto le permitirá filtrar con facilidad por una propiedad específica, así como ver rápidamente dónde se está configurando una dimensión en particular.
* **Configuración:** Configuración de la IU de administración para cada variable (es decir, para eVars: caducidad, asignación, comercialización, etc.)

Captura de pantalla de la muestra de SDR:
![Ejemplo de SDR](assets/sample-sdr.png)

También se recomienda utilizar este documento de etiquetado para realizar un seguimiento de cualquier variable gratuita y cualquiera &quot;no deseada&quot;. Cuando una dimensión ya no es útil, el desarrollador suele necesitar un tiempo para eliminarla. Incluso después de eso, puede almacenarse en caché, o puede que se dé cuenta de que la dimensión también se estaba configurando en otra parte. Limpiar las dimensiones no es fácil y, a menudo, requiere paciencia. Aquí hay algunos consejos para mantener la basura oculta bajo la alfombra para que los usuarios no se confundan y, al mismo tiempo, realizar un seguimiento de ella.

* Todas las dimensiones/eventos que no se utilizan están &quot;libres&quot; o &quot;en proceso de eliminación&quot;
   * Si la dimensión tiene valores no deseados en los últimos 90 días, está &quot;en proceso de eliminación&quot;
   * Si la dimensión está libre y limpia durante al menos los últimos 90 días, está &quot;libre&quot;
   * Márquelas como tal en &quot;Nombre&quot;, en el documento de etiquetado, para que pueda filtrarlas fácilmente. Yo tengo estas etiquetas desmarcadas en el documento de etiquetado (filtro de datos de Excel) para que los usuarios no las vean
   * Márquelas como el nombre de eVar en la interfaz para que los usuarios no las encuentren en una búsqueda (como &quot;(v6)&quot;) y elimine la descripción
* Al hacer esto, cuando se necesita una nueva dimensión, se puede filtrar fácilmente por &quot;libre&quot; en la columna Nombre para encontrar una limpia que utilizar
* Para las dimensiones y eventos &quot;en proceso de eliminación&quot;, recomiendo que realice un seguimiento de estos eventos mediante Workspace:
   * Cree un proyecto visible para los administradores solo con 3 tablas: eVars, props y eventos. Utilizo &quot;instancias&quot; para eVars específicos y, para las props, creo segmentos VISITA con &quot;prop5 existe&quot;, por ejemplo.
   * Establecer fecha en Últimos 90 días
   * Utilice lo anterior como filas en las 3 tablas, junto con ocurrencias
   * Tan pronto como algo llega a &quot;0&quot;, lo marco como &quot;libre&quot; en el documento de etiquetado y lo elimino del proyecto de Workspace

De este modo, los datos siempre están limpios y tiene una idea clara de qué es basura.

![Resumen de variables y eventos](assets/variables-and-events-overview.png)

## Pestaña Propiedades

**QUÉ:** Un documento de propiedades debe enumerar todas sus propiedades digitales: sitios web, aplicaciones móviles, otras herramientas (chat, comentarios, etc.), estén o no etiquetadas con [!DNL Adobe Analytics]. Esto debería servir como un documento centralizado y vivo entre los usuarios empresariales y tecnológicos.

**POR QUÉ:** Esto le proporcionará una visión clara del recorrido del usuario en todas sus propiedades digitales, así como lo que [!DNL Adobe Analytics] cubre y no cubre, para que pueda empezar a priorizar la adición de etiquetado a cualquier propiedad donde falte. Al presentar el ecosistema digital de esta manera, puede identificar posibles oportunidades en la estrategia de etiquetado para obtener una visión completa del recorrido del usuario. Por ejemplo: ¿necesita un grupo de informes globales para seguir varios dominios o sitios? ¿Se necesita un traspaso de ID de visitante entre dominios o aplicaciones para una experiencia híbrida? ¿Es necesario actualizar los filtros de URL internos para el seguimiento entre dominios?

**CÓMO:** Identifique a un propietario del documento para proporcionar el control y una única fuente de responsabilidad para administrar las actualizaciones.
Enumere lo siguiente en la pestaña Propiedades:

* **Nombre de propiedad:** Puede ser un dominio, subdominio, nombre de aplicación, etc. Incluso dentro del mismo dominio, si algunas partes se administran por separado (como, por ejemplo, por un equipo o una tecnología diferentes), deberían separarse.
* **Vínculo (URL)** a la propiedad donde esté disponible
* **Propietario y contactos:** Enumerar el propietario principal o los contactos de la propiedad
* **Método de etiqueta:** Muchos tenemos diferentes métodos e implementaciones de código (Launch, archivos JS, AEP, etc.). Puede desglosar esto más si es necesario (por ejemplo, por versión de código o sistema de administración de etiquetas), pero está pensado para realizar un seguimiento de todos los métodos y versiones de código diferentes, dónde debe actualizarse el código y cómo debe mantenerse. Si utiliza [!DNL Adobe] Launch, indique el nombre de la propiedad de Launch.

Recuerde incluir todas las propiedades digitales, aunque no estén etiquetadas con [!DNL Adobe Analytics]. Esto le ayudará a comprender su entorno digital y cómo sus usuarios interactúan con todas las propiedades.

Se recomienda mantener este documento lo más simple posible y no saturarlo con demasiada información para que sea fácil de interpretar por diferentes partes de la organización. Los equipos de [!DNL Analytics], a menudo, comprenden mejor el panorama digital que cualquier otro equipo, por lo que otros equipos y ejecutivos suelen utilizar este documento para ofrecer una descripción general exhaustiva.

>[!TIP]
>
>Cree una dimensión de nombre/propiedad de sitio en [!DNL Adobe Analytics]. Tener una dimensión específica (normalmente un eVar) en [!DNL Adobe Analytics] que identifique el nombre del sitio o la aplicación permitirá la segmentación, la resolución de problemas, la creación de grupos de informes virtuales, etc. Las ventajas son infinitas, especialmente cuando se combinan varios sitios en un grupo de informes (global). La clave es garantizar que los equipos de desarrollo siempre fijen este valor en la dimensión de propiedades, incluidas todas las cargas de página (llamadas s.t/trackState) y todos los eventos personalizados (llamadas s.tl/trackAction). Las reglas de procesamiento pueden ser una herramienta útil para configurar estos valores de forma correcta y coherente.

[Vea este vídeo de Doug Moore](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=es){target="_blank"} para obtener más información sobre cómo rellenar el manual de implementación.

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataforma digital [!DNL Analytics] en NortonLifeLock
[!DNL Adobe Analytics] campeón

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en [!DNL Adobe]
