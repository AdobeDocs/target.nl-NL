---
keywords: server side;server-side;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Informatie over Adobe Target API's voor levering aan de server, SDK's en doel-Recommendations API's.
title: Informatie over Adobe Target API's voor levering aan de server, Node.js SDK en Target Recommendations API's.
feature: Implement Server-side
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Serverzijde: Doel implementeren

Informatie over [!DNL Adobe Target] API&#39;s voor levering aan de serverzijde, SDK&#39;s en [!DNL Target Recommendations] API&#39;s.

Het volgende proces vindt plaats in een server-side implementatie van [!DNL Target]:

1. Een clientapparaat vraagt om een ervaring via de server.
1. Uw server verzendt dat verzoek naar [!DNL Target].
1. [!DNL Target] verzendt de reactie terug naar uw server.
1. Uw server bepaalt welke ervaring om aan het cliëntapparaat te leveren voor het terug te geven.

De ervaring hoeft niet in een browser te worden weergegeven. De ervaring kan in een e-mail of kiosk, via een stemmedewerker, of door één of andere andere niet-visuele ervaring of niet op browser-gebaseerd apparaat tonen. Aangezien uw server zich tussen de client en [!DNL Target] bevindt, is dit type implementatie ook ideaal als u meer controle en beveiliging nodig hebt of complexe back-endprocessen hebt die u op uw server wilt uitvoeren.

>[!NOTE]
>
>Een nieuwe bezoeker kan alleen op de client worden geïnitialiseerd. Een eerste bezoeker *kan niet* op de server-kant worden geïnitialiseerd.

De volgende secties verstrekken meer informatie over diverse APIs en NodeJS SDK:

## Server Side Delivery-API&#39;s

Koppeling: [Server Side Delivery API&#39;s](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Met de [!DNL Target] Delivery-API kunt u:

* Lever ervaringen over het web, met inbegrip van SPA, en mobiele kanalen evenals niet-browser gebaseerde IoT apparaten, zoals aangesloten TVs, kiosken, of in-store digitale schermen.
* Lever ervaringen van om het even welke server-zijplatform of toepassing die HTTP/s vraag kan maken.
* Lever consistente en gepersonaliseerde ervaringen aan een bezoeker ongeacht welk kanaal of welke apparaten de bezoeker gebruikte om met uw zaken in gesprek te gaan.
* De ervaringen van het geheime voorgeheugen voor een bezoeker binnen een zitting op uw server zodat de veelvoudige API vraag kan worden vermeden, die betere prestaties bereikt.
* Naadloos integreren met [!DNL Adobe Experience Cloud] producten, zoals [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM), en [!DNL Experience Cloud ID Service] van de serverzijde.

## Server Side SDK&#39;s

Koppeling: [Adobe Target SDK&#39;s](https://adobetarget-sdks.gitbook.io/docs/)

Met de [!DNL Adobe Target] SDK-documentatieportal voor server-side kunt u [!DNL Target] op uw servers implementeren in de gewenste taal.

## Doel Recommendations API&#39;s

Koppeling: [Doel Recommendations API&#39;s](https://developers.adobetarget.com/api/recommendations) en [Adobe Recommendations API-overzicht](https://experienceleague.adobe.com/docs/target-learn/recommendations-api-tutorial/recs-api-overview.html).

Met de Recommendations API&#39;s kunt u programmatisch communiceren met [!DNL Target]-adviesservers. Deze API&#39;s kunnen worden geïntegreerd met een reeks toepassingsstapels om functies uit te voeren die u doorgaans uitvoert via de [!DNL Target]-gebruikersinterface.
