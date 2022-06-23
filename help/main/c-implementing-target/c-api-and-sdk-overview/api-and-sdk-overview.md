---
keywords: serverzijde;server-kant;api;sdk;node.js;nodejs;node js;recommendations api;api:apis
description: Meer informatie over de Adobe [!DNL Target] server-side levering APIs, SDKs, en [!DNL Target] Recommendations API's.
title: Waar kan ik informatie over krijgen? [!DNL Target] Server-Side Delivery APIs en SDKs?
feature: Implement Server-side
role: Developer
exl-id: cdee007f-f54d-4cf3-9575-6319da3434a5
source-git-commit: 3c64945eb1898457a9d6a3e7bbfa64420bf1250a
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Serverzijde: Doel implementeren

Informatie over [!DNL Adobe Target] server-side levering APIs, SDKs, en [!DNL Target Recommendations] API&#39;s.

Het volgende proces vindt plaats in een serverimplementatie van [!DNL Target]:

1. Een clientapparaat vraagt om een ervaring via de server.
1. Uw server verzendt die aanvraag naar [!DNL Target].
1. [!DNL Target] verzendt de reactie terug naar uw server.
1. Uw server bepaalt welke ervaring om aan het cliëntapparaat te leveren voor het terug te geven.

De ervaring hoeft niet in een browser te worden weergegeven. De ervaring kan in een e-mail of kiosk, via een stemmedewerker, of door één of andere andere niet-visuele ervaring of niet op browser-gebaseerd apparaat tonen. Omdat uw server tussen de client en [!DNL Target]Dit type implementatie is ook ideaal als u meer controle en beveiliging nodig hebt of complexe back-endprocessen hebt die u op uw server wilt uitvoeren.

>[!NOTE]
>
>Een nieuwe bezoeker kan alleen op de client worden geïnitialiseerd. Een nieuwe bezoeker *kan* worden geïnitialiseerd op de server.

De volgende secties verstrekken meer informatie over diverse APIs en NodeJS SDK:

## Server Side Delivery-API&#39;s

Koppeling: [Server Side Delivery-API&#39;s](https://developers.adobetarget.com/api/delivery-api/)

`/rest/v1/delivery`

Met de [!DNL Target] Leverings-API, kunt u:

* Lever ervaringen over het web, met inbegrip van SPA, en mobiele kanalen evenals niet-browser gebaseerde IoT apparaten, zoals aangesloten TVs, kiosken, of in-store digitale schermen.
* Lever ervaringen van om het even welke server-zijplatform of toepassing die HTTP/s vraag kan maken.
* Lever consistente en gepersonaliseerde ervaringen aan een bezoeker ongeacht welk kanaal of welke apparaten de bezoeker gebruikte om met uw zaken in gesprek te gaan.
* De ervaringen van het geheime voorgeheugen voor een bezoeker binnen een zitting op uw server zodat de veelvoudige API vraag kan worden vermeden, die betere prestaties bereikt.
* Naadloos integreren met [!DNL Adobe Experience Cloud] producten, zoals [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] (AAM) en de [!DNL Experience Cloud ID Service] aan de serverzijde.

## Server Side SDK&#39;s

Koppeling: [Adobe Target SDK&#39;s](https://developer.adobe.com/target/)

De [!DNL Adobe Target] SDK-documentatieportal voor server-side helpt u bij de implementatie [!DNL Target] op uw servers in uw taal van keuze.

## Doel Recommendations API&#39;s

Koppeling: [Doel Recommendations API&#39;s](https://developer.adobe.com/target/).

Met de Recommendations API&#39;s kunt u programmatisch communiceren met [!DNL Target] aanbevelingen servers. Deze API&#39;s kunnen worden geïntegreerd met een reeks toepassingsstapels om functies uit te voeren die u doorgaans via de [!DNL Target] gebruikersinterface.
