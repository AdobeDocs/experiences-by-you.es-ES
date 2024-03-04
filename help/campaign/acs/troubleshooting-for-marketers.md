---
title: Solución de problemas para especialistas en marketing
description: Conocer los errores más comunes puede ayudar a resolver problemas más rápido y aumentar su productividad. Estas sugerencias para la resolución de problemas le ayudarán a resolver de forma eficaz errores similares a medida que se producen.
solution: Campaign Standard
feature-set: Campaign
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
source-git-commit: a27a5538a7009d00d01227865ced4c5039147496
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---

# Solución de problemas para los especialistas en marketing: 5 errores comunes de flujo de trabajo y envío

Por: [Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}, Consultor Senior, Meijer

Como ingeniero sénior y experto en clientes de [!DNL Adobe] Experience Cloud durante los últimos cinco años, habilito a los usuarios empresariales en [Meijer](https://www.meijer.com/){target="_blank"}, una cadena de supercentros estadounidense fundada en 1934, para llevar a cabo complejas campañas transaccionales y de marketing con ACS. Algunos proyectos en los que he trabajado incluyen campañas personalizadas para almacenar ofertas y detalles de pedidos para personalización, integradas con [!DNL Adobe] Audience Manager y conocimiento del cliente para la ingesta de segmentos.


En mi tiempo usando ACS, me he encontrado con errores que pueden consumir tiempo y ser frustrantes de resolver. Conocer los errores más comunes puede ayudar a resolver problemas más rápido y aumentar su productividad. A continuación se muestran mis sugerencias de solución de problemas para ayudarle a resolver de forma eficaz errores similares a medida que se producen.

## Error de tipo de datos no coincidente

**Código de error:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**Causa:**
Estos tipos de errores aparecen en un flujo de trabajo cuando se intenta conciliar mediante campos de diferentes tipos de datos. Por ejemplo, cuando se carga un archivo mediante un archivo de carga que tiene un campo de cadena e intenta reconciliar el campo de cadena con un campo de perfil que tiene un tipo de datos de int.

![data-type-mismatch-error](/help/_assets/kt-13256/data-type-mismatch.png)

**Solución:**
Cambie el tipo de datos del campo en la actividad &quot;Cargar archivo&quot; por el que esté coincidiendo. Abra la actividad &quot;Cargar archivo&quot;. Vaya a la pestaña &quot;DEFINICIÓN DE COLUMNA&quot; y cambie el tipo de datos del campo deseado.


![data-type-mismatch-solution](/help/_assets/kt-13256/data-type-mismatch-solution.png)

## Error de personalización de envío

**Código de error:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**Causa:**
Este error aparece cuando se envía un correo electrónico a una dirección, pero el correo electrónico o cualquier otro identificador no se concilia con un perfil. Para enviar una comunicación por correo electrónico, el correo electrónico o el identificador siempre deben estar vinculados a un perfil.

![flujo de trabajo con actividad de reconciliación](/help/_assets/kt-13256/del-persn-error-wf.png)

**Solución:**
Debe existir un ID común del archivo cargado con la tabla de destinatarios. Esta clave común une el archivo de carga a la tabla de destinatarios dentro de la actividad de reconciliación. Es posible que no se envíen correos electrónicos a registros que no existen en la tabla de destinatarios que requiere este paso de reconciliación dentro del flujo de trabajo. Al hacerlo, reconciliaría la actividad del archivo de carga entrante con un identificador como el ID de correo electrónico del perfil. El `nms:recipient` schema hace referencia a la tabla de perfil y la reconciliación de los registros entrantes con el perfil hace que esté disponible durante la preparación del correo electrónico.

Consulte la captura de pantalla de la actividad de reconciliación como se muestra a continuación.

![flujo de trabajo con detalles de reconciliación](/help/_assets/kt-13256/del-persn-error-wf-solution.png)

Más información sobre [reconciliación](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## Error de conjunto de datos de campo común

**Código de error:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**Causa:**
Este problema se produce al utilizar **actividad de exclusión** en flujos de trabajo de ACS, al realizar una exclusión basada en el ID, cuando el conjunto Principal y el conjunto excluido no tienen los mismos nombres de campo.


![Error de conjunto de datos de campo común](/help/_assets/kt-13256/dataset-error.png)

**Solución:**

Existen dos formas de resolver este error:

1. Utilice el mismo nombre de campo tanto en el campo principal como en el excluido y utilice ese campo como ID

   O BIEN

2. Utilice el método de exclusión JOINS para seleccionar el campo en función del cual desea excluir los registros.

![Error de conjunto de datos de campo común: solución ](/help/_assets/kt-13256/dataset-error-solution.png)

## Error al soltar nombre de campo

**Código de error:**
`XTK-170036 Unable to parse expression 'i__name'`

**Causa:**

Los puntos de error pueden producirse en un **actividad de enriquecimiento**. A continuación se muestra uno de los más comunes.

![Error al soltar nombre de campo](/help/_assets/kt-13256/field-name-dropped-error.png)

Esto sucede cuando se edita manualmente un nombre de expresión en la actividad. La imagen muestra que la expresión se modificó a partir de `name `hasta `i__name`.

**Solución:**

Este error se puede resolver de tres formas:

1. Vuelva a cambiar el nombre a la expresión que estaba presente originalmente.

2. Si desea utilizar un nombre nuevo, cambie los valores en la variable **actividad de enriquecimiento**.

3. Si no recuerda qué ha cambiado, lo mejor que puede hacer es recrear la actividad.

## Error temporal descartado de tabla 

**Código de error:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**Causa:**
Este es un error común en flujos de trabajo complicados que implican enriquecimiento u otra actividad. Probablemente signifique que algunos de los flujos de trabajo de actividad no se guardan correctamente durante varios cambios en el flujo de trabajo.

![Error temporal descartado de tabla ](/help/_assets/kt-13256/temp-table-dropped-error.png)

**Solución:**
Existen muchas maneras de que se produzca este error, por lo que no hay una solución simple. Si se trata de un flujo de trabajo simple, sería mejor reconfigurar la actividad. En un flujo de trabajo complicado, es mejor copiar las actividades de flujo de trabajo en un nuevo flujo de trabajo, guardarlo y volver a ejecutarlo.
