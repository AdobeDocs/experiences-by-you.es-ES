---
title: Cree un diagrama de flujo de datos visual para comprender la pila de tecnología de marketing
description: Aprenda a crear un diagrama de "Posibles clientes y fuentes de datos" para comprender el entorno de datos, auditar y ordenar la instancia de forma eficaz.
feature-set: Marketo Engage
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13877
thumbnail: KT-13877.jpeg
hide: false
exl-id: 088bdcf1-4e49-44a7-ac78-a03742ff680b
source-git-commit: 7bbe86435c683f41509a8cbe6b117b354309644a
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 2%

---

# Cree un diagrama de flujo de datos visual para comprender la pila de tecnología de marketing

Como administrador que asume el control de [!DNL [!DNL Marketo Engage]] instancia que ha estado activa durante años, es como una misión imposible de auditar y ordenar la instancia de manera eficiente. Cuándo [!DNL Adobe] [!DNL Marketo Champion] (2019), Kelly Jo Horton, entró en una instancia de larga data, abordó este desafío mediante [creación de un diagrama de &quot;Posibles clientes y fuentes de datos&quot;](https://nation.marketo.com/t5/employee-blogs/understand-your-marketing-technology-and-data-create-this/ba-p/296774){target="_blank"} para familiarizarse con el universo de los datos. En este tutorial, aprenderá a crear su propio diagrama de flujo de datos basándose en los ejemplos compartidos por Kelly Jo Horton. ¡Conozcamos el ecosistema de MarTech!

## ¿Por qué crear un diagrama de arquitectura para la instancia heredada?

1. **Familiarícese con la pila de tecnología de marketing que heredó de una instancia activa.** Se recomienda a todos los responsables de operaciones de marketing/administradores de operaciones de plataforma que realicen este ejercicio al empezar en una empresa nueva. Este proceso de creación permite a los usuarios administradores ver una imagen completa de los datos y las actividades enviados desde integraciones externas a [!DNL [!DNL Marketo Engage]] y para solucionar fácilmente los errores de la API.
2. **Familiarícese con las partes interesadas clave que administran las integraciones externas.** Una sugerencia que Kelly Jo Horton utiliza para identificar rápidamente a las partes interesadas es hacer referencia a la lista de usuarios de API.
   1. **Vaya a la pestaña &quot;Integración>LaunchPoint&quot; en la sección &quot;Administración&quot;.** Obtenga más información sobre cómo desplazarse a la pestaña &quot;LaunchPoint&quot;: [Crear un servicio personalizado para utilizarlo con la API de REST](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api.html){target="_blank"}.
   2. Busque estadísticas de uso de API por usuario de API en la pestaña Integración > Servicios web de la sección Información de llamada de API. Al hacer clic en el número de llamada de la API, puede ver las llamadas individuales específicas realizadas por cada usuario.

## Cómo realizar este ejercicio de diagrama de flujo de datos visuales

### Paso 1: Diagrama del estado actual

Cree un diagrama &quot;Estado actual&quot;. Vea el siguiente ejemplo:

![Diagrama del estado actual](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Current_State_Lead_Data_Sources_KellyJo_Horton.png){align="center"}


### Paso 2: Diagrama de estado futuro

Cree un diagrama de &quot;estado futuro&quot; que se pueda utilizar al presentar la hoja de ruta de tecnología y sistemas a las partes interesadas no técnicas. Vea el siguiente ejemplo:

![Diagrama de estado futuro](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Future-State-Lead-Data-Sources-KellyJo-Horton.png){align="center"}

### Paso 3: Versión técnica

Cree una versión técnica que muestre detalles como el nombre de usuario de la API para cada integración, una breve descripción del tipo de datos que se insertan en [!DNL [!DNL Marketo Engage]] o extraído de [!DNL [!DNL Marketo Engage]] y un diagrama detallado de cualquier flujo y déclencheur de middleware.  Vea el siguiente ejemplo:

![Versión técnica](/help/marketo-tutorial-inherited-instance/_assets/data-flow-diagram/Lead-Data-Source-Diagram-KellyJo-Horton.png){align="center"}


## Novedades 

**Introducción a los ejemplos:**
Descargue uno de los diagramas de flujo de datos de ejemplo para asignar el estado actual de su pila de tecnología de marketing, persona y flujo de datos, o cree un diagrama para su entorno de datos desde cero mientras audita la instancia:


<table style="table-layout:fixed">
   <tr>  
      <td style="border: 0;">
      <div style="text-align: center;">
          <a href="./_assets/downloads/Current_Future_State_Lead_Data_Sources.zip">
            <strong>Estado actual y estado futuro</strong>
         </a>
      </div>
      </td>
      <td style="border: 0;">
      <div style="text-align: center;">
         <a href="./_assets/downloads/Detailed_Layers_by_Functional_Category_Stacked_Technologies.zip">
         <strong>Capas detalladas por categoría funcional </strong>   
         </a>
      </div>
      </td>
      <td style="border: 0;">
         <div style="text-align: center;">
         <a href="./_assets/downloads/Lead_Data_Source.zip">
           <strong>Flujo de posible cliente y fuente de datos </strong>  
         </a>
         </div>
       </td> 
       <td style="border: 0;">
         <div style="text-align: center;">
         <a href="./_assets/downloads/Simple_World_Class_Stage_Stack.zip">
          <strong>Diagrama simplificado</strong>  
         </a>
         </div>
        </td>  
   </tr>
   <tr>
    <td style="border: 0;">
         <div>
          <img alt="Diagrama de estado actual y estado futuro" src="./_assets/Thumbnail_Current-Future State Lead_Data Sources_KellyJo_Horton.png"/>
         </a>
      </div>
      </td>
      <td style="border: 0;">
         <div>
         <a href="./_assets/downloads/Detailed_Layers_by_Functional_Category_Stacked_Technologies.zip">
         <img alt="Capas detalladas por diagrama de categoría funcional" src="./_assets/Thumbnail_Detailed_Layers_by_Functional_Category_Stacked_Technologies_KellyJo_Horton.png" />
       </a>
         </div>
      </td>
       <td style="border: 0;">
         <div>
            <a href="./_assets/downloads/Lead_Data_Source.zip">
         <img alt="Diagrama de flujo de posibles clientes y fuentes de datos" src="./_assets/Thumbnail_Lead-Data Source Diagram_KellyJo_Horton.png" />
         </a>
         </div>
      </td>
     <td style="border: 0;">
         <div>
            <a href="./_assets/downloads/Simple_World_Class_Stage_Stack.zip">
             <img alt="Diagrama simplificado" src="./_assets/Thumbnail_Simple_World_Class_Stage_Stack.png" />
         </a>
         </div>
      </td>
</table>

Estas son algunas herramientas que puede utilizar: draw.io (Google Docs), [!DNL Adobe] XD, Figma, Gliffy (en Confluencia)

**¿Y si ya hay diagramas de arquitectura?** Los nuevos integrantes del equipo podrían tener diferentes perspectivas. No tiene valor tener [!DNL nuevo [!DNL Marketo Engage]] los administradores realizan este ejercicio como parte de su proceso de incorporación y lo comparten con otros.

## Autores

**Kelly Jo Horton**\
[!DNL Adobe] Campeón de Marketo (2019)
*Socio Cliente Senior en Etumos*

![Kelly Jo Horton](/help/marketo-tutorial-inherited-instance/_assets/authors/Customer_Author_Kelly_Jo_Horton.png){width="30%"}

**Amy Chiu**
*Administrador de marketing de adopción y retención,[!DNL Adobe]*

(/help/marketo-tutorial-inheritance-instance/_assets/authors/[!DNL Adobe]_Author_Amy_Chiu.png){width=30%}
