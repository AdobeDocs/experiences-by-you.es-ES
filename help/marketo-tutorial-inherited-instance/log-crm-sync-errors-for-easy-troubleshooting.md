---
title: Registrar errores de sincronización de CRM para facilitar la resolución de problemas
description: Aprenda a utilizar un registro de errores de sincronización de CRM para investigar los problemas de sincronización de CRM y mantenerla en funcionamiento sin problemas.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13875
thumbnail: KT-13875.jpeg
hide: false
exl-id: 6a38f5dd-5d25-43d8-a1d3-e75ab396e555
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Registrar errores de sincronización de CRM para facilitar la resolución de problemas

As a [!DNL Marketo Engage] administrador, comprobar si la instancia está sincronizada con su CRM debe ser una parte clave de su [rutina diaria](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. While the [Notifications section](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html){target="_blank"} (lo encontrará en la esquina superior derecha de su [!DNL Marketo Engage] interfaz) es donde empezará a buscar e investigar problemas de sincronización frecuentes, hay una sugerencia profesional que podría ayudarle a administrar el estado de la instancia de forma organizada. [!DNL Adobe] Campeona de Marketo (2019-2022), Amy Goldfine recomienda que los usuarios administradores mantengan un registro de los errores de sincronización de CRM para facilitar la resolución de problemas.

![Captura de pantalla de la pestaña Errores de sincronización](/help/marketo-tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## ¿Por qué mantener un registro de los errores de sincronización de CRM?

Registrando los errores de sincronización de CRM, [!DNL Marketo Engage] Los administradores pueden revisar los problemas y las tendencias con los administradores de CRM para solucionar la causa raíz. Siga los pasos a continuación para documentar los problemas de sincronización de CRM para su instancia.

## Cómo mantener un registro de los errores de sincronización de CRM

Antes de empezar, descargue [Plantilla de registro de errores de sincronización CRM](/help/marketo-tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Paso 1:** Vaya a la *[!UICONTROL Administrador] sección* in [!DNL Marketo Engage]. En *[!UICONTROL Integración]*, haga clic en *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]*, o *[!DNL Veeva]*, dependiendo de qué [!DNL CRM] utiliza, luego el *[!UICONTROL Errores de sincronización]* pestaña.

**Paso 2:** Puede elegir entre [exportar los registros de errores como [!DNL CSV] a través del [!UICONTROL Filtrar] panel](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html#filter-sync-errors){target="_blank"}. Si solo tiene unas pocas horas, copie y pegue directamente desde el *[!UICONTROL Errores de sincronización]* tab sería el camino a seguir.

**Paso 3:** Tenga en cuenta la fecha en la que se produjo el error.

**Paso 4:** Introduzca el número de registros de personas afectadas por ese error. (A veces, su CRM solo generará un error para una persona. A veces habrá muchas personas con el mismo error a la vez).

**Paso 5:** Tenga en cuenta la dirección de correo electrónico de una persona afectada por el error. Esto facilita la referencia y la conversación de los errores con el administrador de CRM.

**Paso 6:** Pegar vínculos al registro de persona en [!DNL [!DNL Marketo Engage]] y [!UICONTROL Cliente potencial/contacto de CRM] registro de esa persona.

**Paso 7:** En la última columna, pegue el texto real del error.

## Novedades 

**Identificar códigos de error:** Para comprender los códigos de error, consulte las descripciones en la documentación para desarrolladores [Tabla de códigos de error de nivel de respuesta](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} y busque los pasos siguientes típicos para resolver los errores.

## Autores

**Amy Goldfine**\
[!DNL Adobe] Campeón de Marketo (2019-2022)
*Fundador, MarketingOpsAdvice.com*

![Amy Goldfine](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Administrador de marketing de adopción y retención en[!DNL Adobe]*

![Amy Chiu](/help/marketo-tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
