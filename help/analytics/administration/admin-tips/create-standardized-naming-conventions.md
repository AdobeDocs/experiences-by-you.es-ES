---
title: Cree convenciones de nomenclatura estandarizada
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
source-git-commit: 058d26bd99ab060df3633fb32f1232f534881ca4
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 80%

---

# Cree convenciones de nomenclatura estandarizada

**QUÉ:** Las convenciones de nomenclatura estandarizada se aplican al propio nombre de la variable cuando se habilita en [!DNL Adobe Analytics] (A) IU de administración y los valores pasados a la dimensión. (es decir, los nombres de página serían “nombre de página (v1)” como nombre de variable y los valores de nombre de página pasados deberían ser uniformes y seguir una estructura o jerarquía específica como “nombre de sitio|página principal” o “nombre de sitio|búsqueda|resultados de búsqueda”).

**POR QUÉ:** Las convenciones de nomenclatura son una buena manera de mantener todo uniforme y que la interfaz sea fácil de entender para los usuarios. Si las crea desde el principio y las aplica en la plataforma y el código, será más fácil escalarlas.

**CÓMO:** La interfaz y el documento de etiquetado deben coincidir tanto en “Nombre” como en “Descripción”. Esto evitará que los usuarios tengan que ir a un documento de Excel y les permitirá comprender los datos directamente en la interfaz. También se recomienda escribir todo en minúsculas para mantener la coherencia.

Siempre es mejor que los nombres de las páginas sean coherentes en toda la plataforma (o los nombres de las pantallas para las aplicaciones). Por ejemplo, puede establecer “propiedad:section:subsección:subsubsección:nombre de página único” en una variable o dimensión. Si todos estos son campos independientes en la capa de datos, incluso puede crear el nombre de página directamente en el archivo JS/Launch. Tener todos estos elementos configurados también en sus propias dimensiones puede ayudarle a desglosar las propiedades o áreas específicas del sitio o aplicación con mayor facilidad y a comprender mejor el tráfico y los flujos.

Cualquier cosa que facilite a los usuarios encontrar y comprender los datos, incluidas convenciones de nomenclatura tan sencillas, aumentará el uso de [!DNL Adobe Analytics] y ofrecer mejores perspectivas para el negocio.

## Autores

Este documento lo han escrito:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, Digital [!DNL Analytics] Administrador de plataformas en NortonLifeLock
[!DNL Adobe Analytics] Campeona

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sénior en [!DNL Adobe]
