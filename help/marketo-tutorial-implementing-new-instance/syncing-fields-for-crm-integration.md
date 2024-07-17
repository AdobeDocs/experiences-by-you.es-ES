---
title: Sincronización de campos para los conectores nativos de CRM
description: Aprenda a optimizar la integración inicial de CRM seleccionando estratégicamente los campos de CRM esenciales que debe utilizar el Marketo Engage. Realice el ejercicio del diccionario de datos para identificar los campos que necesita para una sincronización CRM sin problemas que ayude a los equipos de ventas y marketing a mantenerse alineados.
role: Admin
level: Beginner
doc-type: Article
solution: Marketo Engage
duration: 0
last-substantial-update: 2024-05-04T00:00:00Z
jira: KT-14811
thumbnail: KT-14811.jpeg
exl-id: 42b7ca3d-e445-4c11-ad3d-d4e70c101c8e
source-git-commit: bed599454a75159492f13aab1f802c09d92bf7ed
workflow-type: tm+mt
source-wordcount: '1569'
ht-degree: 0%

---

# Sincronización de campos para los conectores nativos de CRM

¿Utiliza Salesforce o Microsoft Dynamics dentro de su organización? Si es así, con los conectores nativos de CRM de Marketo Engage (es decir, Salesforce, Microsoft Dynamics y Veeva), puede coordinar las actividades de marketing y ventas compartiendo sin problemas información relevante entre Marketo Engage y CRM. Antes de configurar la sincronización inicial de CRM, asegúrese de identificar los campos que desea sincronizar entre los dos sistemas para mantener limpia la base de datos de Marketo Engage.

Obtenga más información sobre cómo llevar a cabo este ejercicio con las prácticas recomendadas sugeridas por Adobe Professional Services. Continúe para comprender los campos estándar y los campos personalizados y documente sus relaciones entre Marketo Engage y su CRM.

## Identifique los campos que desea sincronizar antes de integrar su CRM con el Marketo Engage

Al integrar su CRM con Marketo Engage, probablemente no necesite sincronizar todos los campos de CRM con Marketo Engage. Ser estratégico en los campos que necesita puede ayudar a su instancia de Marketo Engage a procesar el flujo de datos de forma más eficaz.

La sincronización inicial entre el Marketo Engage y el sistema CRM asociará automáticamente la mayoría de los campos estándar existentes (es decir, correo electrónico, nombre/apellido, empresa, etc.). Además, el conector también sincroniza [campos personalizados](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"} para los posibles clientes, contactos, cuentas y oportunidades creando nuevos campos en Marketo Engage que se asignan automáticamente a esos campos desde su CRM.

Identificar y organizar los campos que desea sincronizar desde su CRM antes de realizar la sincronización inicial es un paso fundamental en el proceso de configuración del conector nativo. Nos referimos a esto como un ejercicio de diccionario de datos, que le ayuda a minimizar el número de campos duplicados que se crean y a hacer que los pasos de reasignación subsiguientes vayan lo más suavemente posible. Este ejercicio suele incluir datos de los equipos de marketing y ventas y del administrador de CRM para garantizar que solo se sincronizan los campos relevantes con la instancia de Marketo Engage.

## Cómo crear el diccionario de datos

Por lo general, la práctica recomendada es sincronizar únicamente los campos CRM que se necesitarán con fines de marketing. Comience con este ejercicio para organizar los campos de su CRM que deberán asignarse al Marketo Engage y ejecutar correctamente la sincronización inicial de CRM la primera vez.

>[!NOTE]
>Si tiene campos personalizados en CRM que ya tienen un campo personalizado equivalente en Marketo Engage antes de comenzar la sincronización inicial, se creará un nuevo campo &quot;duplicado&quot; en Marketo Engage para el campo CRM. Puede volver a asignar el campo CRM al campo de Marketo Engage original y ocultar el campo duplicado una vez completada la sincronización inicial, pero tendrá que ponerse en contacto con el servicio de atención al cliente de [Adobe](https://experienceleague.adobe.com/en/docs/customer-one/using/home#create-a-support-ticket-with-admin-console){target="_blank"} para hacerlo. Consulte el paso 7 para obtener más información.

**Paso 1:** Cree una lista aproximada de los campos disponibles actualmente en su CRM y marque si desea que aparezcan en el Marketo Engage.

* Incluya comentarios de sus equipos de administración, marketing y ventas de CRM en el proceso de toma de decisiones.
* Documente los nombres de API y los tipos de campo para cada campo
* Determine qué nivel de acceso debe tener el Marketo Engage para estos campos (es decir, solo lectura o lectura-escritura)


**Paso 2:** Revise la sección [Administración > Administración de campos](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/view-field-mappings-between-marketo-and-salesforce){target="_blank"} de su instancia de Marketo Engage para identificar cualquier campo personalizado creado anteriormente directamente en el sistema que desee incluir en la sincronización.

* Documente los nombres de API y los tipos de campo para cada campo.
* Indique los campos que ya tienen un campo equivalente en su CRM.
* Indique campos que aún no tengan un campo equivalente en su CRM.


**Paso 3:** Comience a crear el diccionario de datos con los campos de asignación predeterminados

* Dado que Marketo Engage utiliza una base de datos plana, se recomienda dar formato al diccionario de datos de la siguiente manera:

   * Primera Columna: Nombres De Campos De Marketo Engage
   * Segunda columna: Nombres de API de Marketo Engage
   * Tercera columna: [Tipo de campo de Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"} (booleano, monetario, fecha, etc.)
   * En las columnas siguientes, repita para los tipos de objeto de CRM (posible cliente, contacto, cuenta, oportunidad) con una columna adicional para el nivel de acceso que desee que tenga el Marketo Engage (es decir, Leer, Escribir, Editar)
  <br>

  Este es un ejemplo de cómo sería:
  ![Tabla del diccionario de datos](/help/marketo-tutorial-implementing-new-instance/assets/data_dictionary.png){width="100%" zoomable="yes"}


* Comience agregando los campos predeterminados que se asignarán automáticamente a su CRM:

   * [Salesforce](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/default-salesforce-field-mapping){target="_blank"}
   * [Microsoft Dynamics](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/default-dynamics-field-mapping){target="_blank"}
   * [Veeva](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/veeva-crm-sync/sync-details/default-veeva-field-mapping){target="_blank"}

* Confirme que cada campo predeterminado en el Marketo Engage coincide con el campo del CRM con el que desea sincronizar. Por ejemplo, el campo &quot;Cancelación de suscripción&quot; en Marketo Engage podría ser el campo &quot;Exclusión de correo electrónico&quot; en su CRM.
* Ajuste el nombre de la API de CRM, los privilegios y [tipo de datos](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/field-management/custom-field-type-glossary){target="_blank"} donde sea necesario.

**Paso 4:** Agregar campos adicionales al diccionario de datos

* Incluya el Nombre para mostrar, los privilegios CRM deseados y el tipo de datos para cada campo.
* Si un campo existe en CRM pero no en el Marketo Engage, rellene la visualización del Marketo Engage y los nombres de la API con los mismos valores del campo CRM.
* Si existe un campo en Marketo Engage pero no en CRM, rellene el nombre para mostrar de CRM con el valor deseado, pero deje el nombre de la API de CRM en blanco hasta que se cree el campo.
* Si existen campos equivalentes en ambos sistemas, inclúyalos en la misma línea e indique que deberán reasignarse en la sección &quot;Notas&quot;, en el extremo derecho de la hoja del diccionario de datos.

>[!NOTE]
>Si planea crear un campo de filtro de sincronización ([Salesforce](https://nation.marketo.com/t5/product-blogs/instructions-for-creating-a-custom-sync-rule/ba-p/242758){target="_blank"} | [Microsoft Dynamics](https://community.dynamics.com/blogs/post/?postid=8a91d93e-2181-45dd-a8fb-1092010bc8f1){target="_blank"}), asegúrese de incluirlo en este paso, pero deje los nombres de API en blanco hasta que se cree el campo en su CRM.

**Paso 5:** Revise el diccionario de datos con su administrador de CRM

* Cree campos en CRM para los que ya existen en el Marketo Engage y actualice el diccionario de datos con los nombres para mostrar y API para el nuevo campo CRM.
* Realizar asignación de campos entre los objetos de contacto y posible cliente de su CRM ([Salesforce](https://nation.marketo.com/t5/product-blogs/instructions-for-creating-a-custom-sync-rule/ba-p/242758){target="_blank"}) | [Microsoft Dynamics](https://community.dynamics.com/blogs/post/?postid=8a91d93e-2181-45dd-a8fb-1092010bc8f1){target="_blank"}). Cuando un posible cliente se convierte en un contacto, esto garantiza que los campos se puedan consolidar en un único campo de Marketo Engage.
* Asegúrese de que el perfil de sincronización de Marketo tenga los privilegios adecuados para cada campo, tal como se indica en el diccionario de datos:
   * [Establecer permisos de perfil en Salesforce](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-2-of-3-create-a-salesforce-user-for-marketo-enterprise-unlimited#set-profile-permissions){target="_blank"}
   * [Establecer permisos de perfil en Microsoft Dynamics](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/microsoft-dynamics-365-with-s2s-connection/step-2-of-3-set-up#create-application-user-in-microsoft){target="_blank"}
   * [Establecer permisos de perfil en Veeva](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/microsoft-dynamics-365-with-s2s-connection/step-2-of-3-set-up#create-application-user-in-microsoft){target="_blank"}

**Paso 6:** Realizar la sincronización inicial

* Asegúrese de que todos los campos que desee sincronizar con Marketo Engage tengan los privilegios adecuados en su CRM, tal como se define en el diccionario de datos.
* Asegúrese de que todos los campos que ***no*** desea sincronizar con el Marketo Engage estén [ocultos del perfil de sincronización de Marketo](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/crm-sync/salesforce-sync/sfdc-sync-details/hide-a-salesforce-field-from-the-marketo-sync){target="_blank"}. Es mucho más fácil agregar nuevos campos a la sincronización más tarde que quitar campos que se sincronizaron involuntariamente.
* ¿Está conectando su CRM con el campo Filtro de sincronización? Si realiza la sincronización con Salesforce, póngase en contacto con Asistencia al cliente de Adobe para asegurarse de que la funcionalidad de filtrado esté activada antes de iniciar la sincronización inicial.


**Paso 7:** Revise la sección Administración de campos en Marketo Engage

* Confirme o actualice los nombres de visualización y API para los nuevos campos sincronizados.
* Identifique cualquier campo duplicado que pueda requerir una reasignación. Los campos duplicados se producen en unos pocos casos:
   * Los campos personalizados en CRM crearían un nuevo campo (potencialmente duplicado) en Marketo Engage la primera vez que se sincronizan si ya existe un campo equivalente en Marketo Engage.
   * Campos personalizados solo de participación de Marketo (es decir, un campo creado directamente en Marketo Engage) y es posible que tenga un campo equivalente sincronizado desde CRM.



**Paso 8:** Póngase en contacto con Atención al cliente de Adobe para realizar la reasignación si aparecen campos duplicados

* Póngase en contacto con el soporte técnico con la siguiente información para los campos que deben reasignarse:
   * Mostrar los nombres de las API y para los nuevos campos duplicados creados por CRM.
   * Nombre para mostrar del campo de Marketo Engage al que desea asignar el campo CRM.
   * Consulte este ejemplo [AQUÍ](https://nation.marketo.com/t5/knowledgebase/re-mapping-sfdc-marketo-fields/ta-p/299284){target="_blank"}.
* Una vez finalizada la reasignación, revise los nombres de API para los campos reasignados en Marketo Engage y actualice los valores en la columna &quot;Nombre de API&quot; del diccionario de datos para asegurarse de que contiene la información más precisa.

## ¿Qué sigue?

* Cree su diccionario de datos para organizar sus campos para la integración de CRM.
* Familiarícese con el proceso de sincronización inicial para su CRM

>[!BEGINTABS]

>[!TAB Salesforce]

Descubra cómo Marketo Engage y Salesforce trabajan juntos para mantener sus datos de ventas y marketing sincronizados.

>[!VIDEO](https://video.tv.adobe.com/v/3424719/?learn=on)

+++**Vínculos utilizados en el vídeo:**

* [Explicación de la sincronización de Salesforce](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/understanding-the-salesforce-sync.html){target="_blank"}

* [Agregar campos de Marketo a Salesforce (Enterprise/Unlimited)](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-1-of-3-add-marketo-fields-to-salesforce-enterprise-unlimited.html){target="_blank"}

* [Crear un usuario de Marketo en Salesforce (Enterprise/Unlimited)](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-2-of-3-create-a-salesforce-user-for-marketo-enterprise-unlimited.html){target="_blank"}

* [Conectar Marketo y Salesforce(Enterprise/Unlimited)](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/setup/enterprise-unlimited-edition/step-3-of-3-connect-marketo-and-salesforce-enterprise-unlimited.html){target="_blank"}

* [Los usuarios deberán configurar la aplicación conectada en el lado de Salesforce antes de continuar con la sincronización de Marketo y Salesforce.](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/log-in-using-oauth-2-0.html){target="_blank"}

* [Estado de sincronización de Salesforce](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-status.html){target="_blank"}

* [Ocultar y mostrar un campo](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/field-management/hide-and-unhide-a-field.html){target="_blank"}

* [Tutorial: Obtenga información sobre cómo sincronizar Marketo con su CRM](https://experienceleague.adobe.com/docs/marketo-learn/tutorials/lead-and-data-management/crm-sync-learn.html){target="_blank"}

+++

>[!TAB Microsoft Dynamics]

Descubra cómo funciona la sincronización de Microsoft Dynamics 365 y configure la configuración correctamente para permitir que los dos sistemas hablen entre sí.

>[!VIDEO](https://video.tv.adobe.com/v/3424737/?learn=on)

+++**Vínculos utilizados en el vídeo:**

* [Explicación de la sincronización de Microsoft Dynamics](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/understanding-the-microsoft-dynamics-sync.html){target="_blank"}

* [Descargar la solución Marketo Lead Management](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/download-the-marketo-lead-management-solution.html){target="_blank"}

* [Actualizar la solución de Marketo para Microsoft Dynamics](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/update-the-marketo-solution-for-microsoft-dynamics.html){target="_blank"}

* [Conceder consentimiento para el ID de cliente y el registro de la aplicación](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/grant-consent-for-client-id-and-app-registration.html)

* [Validar sincronización de Microsoft Dynamics](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/validate-microsoft-dynamics-sync.html){target="_blank"}

* [Estado de sincronización](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/sync-status.html){target="_blank"}

* [Corregir problemas de sincronización de validación de Dynamics](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/fix-dynamics-validation-sync-issues.html){target="_blank"}

* [Crear un filtro personalizado de sincronización de Dynamics](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/custom-dynmaics-sync-filter-details/create-a-custom-dynamics-sync-filter.html){target="_blank"}

* [Ver la URL del servicio de organización](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/sync-setup/view-the-organization-service-url.html){target="_blank"}

* [Edición de campos para sincronizar antes de eliminarlos en Dynamics](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/microsoft-dynamics/microsoft-dynamics-sync-details/editing-fields-to-sync-before-deleting-them-in-dynamics.html){target="_blank"}

* [Tutorial: Obtenga información sobre cómo sincronizar Marketo con su CRM](https://experienceleague.adobe.com/docs/marketo-learn/tutorials/lead-and-data-management/crm-sync-learn.html){target="_blank"}

+++

>[!ENDTABS]

### Autores

{{peter-livadas}}

{{amy-chiu}}

