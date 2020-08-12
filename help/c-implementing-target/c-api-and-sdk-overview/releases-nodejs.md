---
keywords: at.js;sdk;node.js;release;updates;sdks;server side;serverside;server-side;nodejs
description: Opmerkingen bij de release met betrekking tot API's van de Adobe Target-server.
title: Release-aantekeningen met betrekking tot Adobe Target Node.js SDK.
feature: null
topic: Standard
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---


# Opmerkingen bij de release - Doel Node.js SDK

Opmerkingen bij de release met betrekking tot de [Adobe Target Node.js SDK](https://github.com/adobe/target-nodejs-sdk).

Met de SDK van Target Node.js kunt u [!DNL Target] server-side implementeren.

Deze Node.js SDK helpt u gemakkelijk [!DNL Target] met andere [!DNL Adobe Experience Cloud] oplossingen, zoals [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics], en [!DNL Adobe Audience Manager]te integreren.

De SDK van Node.js introduceert beste praktijken en verwijdert ingewikkeldheid wanneer het integreren met [!DNL Target] via onze levering API zodat uw techniekteams zich op bedrijfslogica kunnen concentreren.

Meer informatie over de SDK van Target Node.js vindt u op de Tech Blog van Adobe - [Open Sourcing the New Adobe Target Node.js SDK](https://medium.com/adobetech/open-sourcing-the-new-adobe-target-node-js-sdk-b6feafd828bc).

## Versie 1.0.0 (9 oktober 2019)

De volgende secties verstrekken meer informatie over versie 1.0.0 van het Doel Node.js SDK:

### Toegevoegd

* Ondersteuning voor versie 1-API van de doelweergave, inclusief de voorkeuren voor het laden van pagina&#39;s en de weergave.
* Volledige steun voor het leveren van alle soorten aanbiedingen die in Visual Experience Composer (VEC) worden authored.
* Ondersteuning voor prefetching en meldingen voor prestatieoptimalisatie door het in cache plaatsen van vooraf ingestelde inhoud.
* Ondersteuning voor het optimaliseren van prestaties bij hybride [!DNL Target] integratie `serverState` wanneer [!DNL Target] deze zowel op de server als op de client wordt geïmplementeerd.

   Wij introduceren het plaatsen genoemd `serverState` die ervaringen bevat die via server-kant worden teruggewonnen, zodat at.js v2.2+ geen extra servervraag zal maken om de ervaringen terug te winnen. Deze aanpak optimaliseert de prestaties bij het laden van pagina&#39;s.

* Open die op GitHub als [Doel Node.js SDK](https://github.com/adobe/target-nodejs-sdk)wordt ingekocht.
* Nieuwe [sendNotifications() API-methode](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientsendnotifications) voor het verzenden van weergegeven/geklikte meldingen naar [!DNL Target] voor inhoud die vooraf is ingesteld via [getOffers()](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers).
* Vereenvoudigde weergave van API-aanvraagopbouw voor levering, met automatisch invullen van interne velden met standaardwaarden (bijvoorbeeld `request.id`, `request.context`enz.).
* Validatie van API-methodeargumenten voor SDK.
* Bijgewerkte README, steekproeven, en eenheidstests.
* De nieuwe CI stroomopstelling die Acties GitHub gebruikt.
* Toegevoegde CvC, de richtlijnen van de Bijdrage, PR, en uitgiftesjablonen

### Gewijzigd

* Naam van project gewijzigd in `target-nodejs-sdk`.
* Belangrijke refactoring, die BatchMbox v2 API van het Doel vervangt met Levering v1 API van de Mening van het Doel.
* [create() API-methodeargumenten](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientcreate) zijn gewijzigd en overbodige nesting is verwijderd (zie [hier](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientcreate)de oude methodedeclaratie).
* [getOffers() API methode](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) argumenten zijn gewijzigd (zie [hier](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffers)oude methodedeclaratie).
* De `getTargetCookieName()` API-methode is vervangen door `TargetCookieName` accessor. Zie [Hulpprogrammaaccessors](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors)TargetClient.
* De `getTargetLocationHintCookieName()` API-methode is vervangen door `TargetLocationHintCookieName` accessor.  Zie [Hulpprogrammaaccessors](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclient-utility-accessors)TargetClient.

### Verwijderd

* Ondersteuning voor BatchMbox v2 API.
* De [getOffer() API-methode](https://www.npmjs.com/package/@adobe/target-node-client#targetnodeclientgetoffer) is verwijderd. Gebruik in plaats daarvan de [getOffers() API-methode](https://git.corp.adobe.com/anischev/target-nodejs-sdk/blob/TNT-33695/README.md#targetclientgetoffers) .

