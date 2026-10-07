---
title: Registrar errores de sincronización de CRM para facilitar la resolución de problemas
description: Aprenda a utilizar un registro de errores de sincronización de CRM para investigar los problemas de sincronización de CRM y mantenerla en funcionamiento sin problemas.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00.000Z
jira: KT-13875
thumbnail: KT-13875.jpeg
exl-id: 6a38f5dd-5d25-43d8-a1d3-e75ab396e555
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: c68cd75e-5bca-4bc3-a60e-9e183f816441
    internal-label: Experience Manager Cloud Manager
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: d1d0a9cd-295d-4976-8c39-ddae266f240e
    internal-label: Administration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 749b293ab38b8ea5a5f72517bd5c3455399137c2
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%
---
# Registrar errores de sincronización de CRM para solucionar problemas

Como administrador de [!DNL Marketo Engage], comprobar si la instancia está sincronizada con su CRM debería ser una parte clave de su [rutina diaria](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. Aunque la sección [Notificaciones](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html?lang=es){target="_blank"} (que se encuentra en la esquina superior derecha de la interfaz [!DNL Marketo Engage]) es donde empezará a buscar e investigar los problemas de sincronización frecuentes, hay una sugerencia profesional que puede ayudarle a administrar el estado de la instancia de forma organizada. [!DNL Adobe] Campeona de Marketo (2019-2022), Amy Goldfine recomienda que los usuarios administradores mantengan un registro de los errores de sincronización de CRM para facilitar la resolución de problemas.

![Captura de pantalla de la ficha Errores de sincronización](/help/marketo-tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## ¿Por qué mantener un registro de los errores de sincronización de CRM?

Al registrar los errores de sincronización de CRM, los administradores de [!DNL Marketo Engage] pueden revisar los problemas y tendencias con los administradores de CRM para corregir la causa raíz. Siga los pasos a continuación para documentar los problemas de sincronización de CRM para su instancia.

## Cómo mantener un registro de los errores de sincronización de CRM

Antes de comenzar, descargue la [plantilla Registro de errores de sincronización con CRM](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Paso 1:** Vaya a la sección *[!UICONTROL Administrador]* en [!DNL Marketo Engage]. En *[!UICONTROL Integración]*, haga clic en *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]* o *[!DNL Veeva]*, dependiendo de qué [!DNL CRM] utilice, y luego en la ficha *[!UICONTROL Errores de sincronización]*.

**Paso 2:** Puede elegir [exportar los registros de errores como  [!DNL CSV] archivo a través del panel [!UICONTROL Filtro]](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html?lang=es#filter-sync-errors){target="_blank"}. Si solo tiene unas pocas horas, copiar y pegar directamente desde la ficha *[!UICONTROL Errores de sincronización]* sería la mejor opción.

**Paso 3:** Tenga en cuenta la fecha en la que se produjo el error.

**Paso 4:** Escriba el número de registros de persona afectados por ese error. (A veces, su CRM solo generará un error para una persona. A veces habrá muchas personas con el mismo error a la vez).

**Paso 5:** Tenga en cuenta la dirección de correo electrónico de una persona afectada por el error. Esto facilita la referencia y la conversación de los errores con el administrador de CRM.

**Paso 6:** Pegue vínculos al registro de persona en [!DNL Marketo Engage] y al registro de [!UICONTROL contacto o posible cliente de CRM] de esa persona.

**Paso 7:** En la última columna, pegue el texto real del error.

## ¿Cuál es el siguiente paso?

**Identificar códigos de error:** Para comprender los códigos de error, busque las descripciones en la documentación de desarrolladores [Tabla de códigos de error de nivel de respuesta](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} y busque los pasos siguientes habituales para resolver los errores.

## Autores

**Amy Goldfine**\
[!DNL Adobe] campeón de Marketo (2019-2022)
*Fundador, MarketingOpsAdvice.com*

![Amy Goldfine](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Administrador de marketing de adopción y retención en[!DNL Adobe]*

![Amy Chiu](/help/marketo-tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
