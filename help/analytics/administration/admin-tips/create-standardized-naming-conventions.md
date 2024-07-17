---
title: Crear convenciones de nomenclatura estandarizada
description: Las convenciones de nomenclatura estandarizada se aplican al propio nombre de la variable cuando se habilita en la IU de administración de AA y a los valores pasados a la dimensión.
solution: Analytics
feature-set: Analytics
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
exl-id: 79cec21e-2b52-4e7b-88ad-db137a8cef4e
source-git-commit: c568ed0a06551d910b6f533698ec47c15adecf6c
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Crear convenciones de nomenclatura estandarizada

**QUÉ:** Las convenciones de nomenclatura estandarizada se aplican al propio nombre de la variable cuando se habilita en la interfaz de usuario de administración de [!DNL Adobe Analytics] (AA) y a los valores pasados a la dimensión. (es decir, los nombres de página serían &quot;nombre de página (v1)&quot; como nombre de variable y los valores de nombre de página pasados deberían ser uniformes y seguir una estructura o jerarquía específica como &quot;nombre de sitio|página principal&quot; o &quot;nombre de sitio|búsqueda|resultados de búsqueda&quot;).

**POR QUÉ:** Las convenciones de nomenclatura son una excelente manera de mantener todo uniforme y que la interfaz sea fácil de entender para los usuarios. Si los crea desde el principio y los aplica en la plataforma y el código, será más fácil escalarlos.

**CÓMO:** La interfaz y el documento de etiquetado deben coincidir tanto en &quot;Nombre&quot; como en &quot;Descripción&quot;. Esto evitará que los usuarios tengan que ir a un documento de Excel y les permitirá comprender los datos directamente en la interfaz. También se recomienda escribir todo en minúsculas para mantener la coherencia.

Siempre es mejor que los nombres de las páginas sean coherentes en toda la plataforma (o los nombres de las pantallas para las aplicaciones). Por ejemplo, puede establecer &quot;`property:section:sub section:sub sub section:unique page name`&quot; en una variable o dimensión. Si todos estos son campos independientes en la capa de datos, incluso puede crear el nombre de página directamente en el archivo JS/Launch. Tener todos estos elementos configurados también en sus propias dimensiones puede ayudarle a desglosar las propiedades o áreas específicas del sitio o aplicación con mayor facilidad y a comprender mejor el tráfico y los flujos.

Cualquier cosa que facilite a los usuarios encontrar y comprender los datos, incluidas convenciones de nomenclatura tan sencillas, aumentará el uso de [!DNL Adobe Analytics] y proporcionará mejores perspectivas para la empresa.

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, directora de plataforma digital [!DNL Analytics] en NortonLifeLock
[!DNL Adobe Analytics] campeón

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en [!DNL Adobe]
