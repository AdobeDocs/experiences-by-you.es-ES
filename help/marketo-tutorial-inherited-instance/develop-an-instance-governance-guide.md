---
title: Desarrollar una guía de gobernanza de instancias con documentación
description: Aprenda a establecer un procedimiento sólido para crear y mantener la documentación y el registro de cambios para su [!DNL Marketo Engage] ejemplo. Esto no solo ahorrará tiempo para el intercambio de conocimientos de su equipo, sino que también mejorará la salud y la eficacia de su instancia.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-14103
thumbnail: KT-14103.jpeg
hide: false
exl-id: e127b84d-ef92-4527-a0e6-a36af35b7ee0
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 1%

---

# Desarrollar una guía de gobernanza de instancias con documentación

A medida que avanza hacia un [!DNL heredado [!DNL Marketo Engage]] por ejemplo, a menudo conlleva el desafío de carecer de documentación técnica y funcional actualizada. Como administrador, establecer directrices para garantizar un control adecuado de las instancias es una responsabilidad central que no se puede pasar por alto. Es una de las estrategias críticas para [aumente la eficacia mientras trabaja en un [!DNL Marketo Engage] instancia](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

Este tutorial paso a paso procede de [!DNL [!DNL Adobe] Nick Hajdin, campeón de Marketo (2018), le guiará a través de este proceso para esbozar la configuración de la instancia, documentar los programas operativos principales y mantener un [!DNL changelog] para aplicar una política de gobernanza estricta.

## ¿Por qué desarrollar una guía y documentación de gobernanza de instancias para su instancia heredada?

Documentación detallada y una [!DNL changelog] son vitales para una gestión eficiente y la transferencia de conocimientos dentro de su [!DNL [!DNL Marketo Engage]] instancia. Realizar un seguimiento de los cambios y las decisiones que ha realizado durante la configuración de la instancia puede ayudarle a lo siguiente:

1. Capacite a los usuarios internos de forma más sencilla y escalable.
2. Generar de forma más eficaz en [!DNL [!DNL Marketo Engage]] a largo plazo.
3. Mantenga el estado y la higiene de su instancia en adelante para evitar que pase horas investigando correos electrónicos, [pista de auditoría](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html), y [registro de actividad](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) para obtener el contexto.
4. Ahorrar tiempo al transferir [!DNL [!DNL Marketo Engage]] conocimientos a un nuevo [!DNL [!DNL Marketo Engage]] administrador si su equipo experimenta algún cambio.

## [!DNL [!DNL Marketo Engage]] guía de gobernanza 101

Una guía de gobernanza sirve como fuente fiable para la configuración de la instancia y los requisitos de diseño del sistema. La información clave que se recomienda incluir en este documento es:

* Estructuras de programa/carpeta
* Permiso de usuario y función
* Límites de comunicación
* Normas de gobernanza
* Formación interna del usuario antes de concederle acceso a la plataforma

## Cómo desarrollar y mantener una guía de gobernanza para su [!DNL [!DNL Marketo Engage]] instancia

### Paso 1: Identifique el estado actual de la guía y documentación de gobernanza

* **No puedo encontrar ninguna documentación para mi instancia heredada:** Si ha iniciado recientemente una función nueva y no puede encontrar ninguna documentación para la instancia heredada, **vaya al paso 2** y comience con una plantilla descargable que proporcionamos.
* **Tengo la documentación registrada:** ¡Felicidades, es una buena señal! Asegúrese de revisar su relevancia para ver cuándo se realiza el último cambio. Si los integrantes del equipo no la mantienen activamente, se recomienda actualizarla e informar a los usuarios internos sobre cómo mantenerla actualizada.

### Paso 2: Identificar los elementos que se incluirán en [!DNL [!DNL Marketo Engage]] Documentación &amp; [!DNL Changelogs]

El formato varía de una plataforma basada en la nube a un documento compartido. Puede diseñar el formato que se adapte a las necesidades de su organización. [Esta es una sencilla documentación y plantilla de Excel changelog](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx), que cubre los elementos importantes con los que puede empezar. Se incluyen:

* Documentación
   * Nombre de plantilla de programa
   * Canal
   * Fecha de creación
   * Creado por
   * Finalidad del programa
   * Estado
   * Vínculo a plantilla de programa
   * Nota
* Changelog
   * Nombre de plantilla de programa
   * Fecha del cambio
   * Actualizado por
   * Propósito de la actualización
   * Experiencia antes del cambio (incluir vínculos/capturas de pantalla)
   * Experiencia tras el cambio (incluir vínculos/capturas de pantalla)
   * URL del programa

### Paso 3: Identificar y documentar el estado actual de los programas operativos primarios

Comience por identificar los programas operativos clave con impactos en el nivel de suscripción. Algunos ejemplos son Administración de datos [!DNL Campaign]s, ciclo de vida del posible cliente, puntuación del posible cliente, [!DNL CRM] Sincronización y capacidad de entrega.

Para cada programa operativo identificado, documente su estado actual. Esto incluye detalles sobre el propósito del programa, la configuración, las campañas inteligentes asociadas y la integración con otras herramientas (si corresponde).

### Paso 4: Aplicar [!DNL Changelog] Mantenimiento

El siguiente paso es establecer una directiva de gobernanza estricta para [!DNL [!DNL Marketo Engage]] instancia que exige &quot;[!DNL Changelog] mantenimiento&quot;. Esta política garantiza que cualquier actualización realizada en los programas operativos en toda la instancia esté documentada exhaustivamente.

Informe a su equipo de la importancia de estos documentos y de cómo acceder a ellos y actualizarlos correctamente. Podría resultar útil asignar responsabilidades para mantener el registro de cambios, por lo que algunos miembros o administradores designados del equipo de operaciones de marketing registran los cambios de forma coherente y proporcionan firmas.

### Paso 5: Centralización de la documentación

Establezca una ubicación o repositorio central para almacenar toda la documentación relacionada con su [!DNL [!DNL Marketo Engage]] instancia. Podría ser una unidad compartida, una carpeta dedicada o un sistema basado en la nube.

### Paso 6: Revisión y actualización periódicas

Programe revisiones periódicas de la documentación para asegurarse de que es precisa y está actualizada. Se puede pasar por alto fácilmente durante las horas de mayor afluencia. Configure recordatorios de forma proactiva en el calendario para asegurarse de que su equipo realiza actualizaciones con regularidad y reflejen los cambios o las optimizaciones en los programas operativos.

## Novedades 

Comience descargando esto [plantilla simple](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

Siga los pasos anteriores para desarrollar la guía y la documentación de gobernanza. A medida que avance en el proceso, tenga en cuenta las siguientes reglas:

**Actualice la documentación existente:**
Es crucial mantener la documentación actualizada. Si no se ha modificado en los últimos 3 años, dedique tiempo a revisar la documentación a medida que audite la instancia.

**Compartir y entrenar:**
Comparta su documentación y [!DNL changelog] Póngase en contacto con los miembros relevantes del equipo y edúquelos sobre cómo actualizar estos registros.

**Revisión periódica:** preprograme el tiempo para revisarlos y mantenerlos durante todo el año para incluir cualquier cambio, optimización o ajuste nuevo a medida que se produzca.

Mantenimiento de una documentación completa y actualizada para su [!DNL Marketo Engage] La instancia de le ahorrará tiempo y esfuerzo a largo plazo y facilitará la administración eficaz de instancias.

### Autores

**Nick Hajdin**
[!DNL [!DNL Adobe] Campeón de Marketo] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![Nick Hajdin](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**Amy Chiu**
*Administrador de marketing de adopción y retención,[!DNL Adobe]*

![Amy Chiu](/help/marketo-tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
