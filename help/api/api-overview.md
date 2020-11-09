---
keywords: api;apis;admin api;delivery api;reporting api;profile api
description: Informatie over Adobe Target API's, waaronder de API's Admin, Delivery, Reporting en Profile.
title: Overzicht Adobe Target API
feature: api
topic: APIs
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Overzicht Adobe Target API

[!DNL Adobe Target] API&#39;s kunnen worden gegroepeerd op basis van het type.

| API-type | Wat het u toelaat doen | Koppeling downloaden | Andere nuttige koppelingen |
| --- | --- | --- |--- |
| Beheer | Maak, wijzig en verwijder activiteiten, publiek, aanbiedingen en andere objecten (zoals [!DNL Recommendations] entiteiten, criteria, ontwerpen, enz.). De API&#39; [!DNL Recommendations] s zijn een type API voor beheerders.) | <UL><li>[Postmanverzameling voor Admin API](https://developers.adobetarget.com/api/#admin-postman-collection)</li><li>[Recommendations API Postman Collection](https://developers.adobetarget.com/api/recommendations/#section/Postman)</li></ul> | [Recommendations API&#39;s](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html) gebruiken in *Adobe Target-Tutorials* |
| Aflevering | Haal geoptimaliseerde en gepersonaliseerde inhoud op van [!DNL Target] voor levering aan een eindgebruiker. | [Doellevering-API Postman-verzameling](https://developers.adobetarget.com/api/delivery-api/#section/Getting-Started/Postman-Collection) |  |
| Rapportage | Resultaten van exportactiviteiten en andere rapportresultaten. | Rapportage-API&#39;s worden opgenomen in de Postman-verzameling [van](https://developers.adobetarget.com/api/#admin-postman-collection)Target Admin API. |  |
| Profiel | Ophalen en wijzigen van gebruikersprofielen die zijn opgeslagen in Adobe Target. | [Postmanverzameling van API-doelprofiel](https://developers.adobetarget.com/api/#profiles) |  |

>[!NOTE]
>
>Er zijn belangrijke verschillen tussen de API&#39; [!DNL Target] s voor beheer (inclusief de API&#39; [!DNL Recommendations] s) en de API&#39;s voor [!DNL Target] levering:
>
>* Admin APIs laat u diverse aspecten van vormen [!DNL Target] die u in [!DNL Target] UI kon ook vormen. Admin API&#39;s vereisen verificatie.
   >
   >
* Met levering-API&#39;s kunt u inhoud ophalen. Voor levering-API&#39;s is geen verificatie vereist.
>
>
Om Admin APIs te gebruiken, moet u eerst authentificatie vormen gebruikend Adobe I/O. [!DNL Target] Zie Verificatie [](https://experienceleague.adobe.com/docs/target-learn/tutorials/apis/configure-io-target-integration.html) configureren in *Adobe Target-Tutorials* voor meer informatie.
